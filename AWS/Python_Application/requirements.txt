from flask import Flask

app = Flask(__name__)

# Home route
@app.route('/')
def home():
    return '<h1>Welcome to My Simple Flask App</h1><p>This is the home page.</p>'

# About route
@app.route('/about')
def about():
    return '<h1>About Us</h1><p>This is the about page.</p>'

# Contact route
@app.route('/contact')
def contact():
    return '''
    <h1>Contact Us</h1>
    <p>Email: contact@example.com</p>
    <p>Phone: +123 456 7890</p>
    '''

if __name__ == '__main__':
    app.run(host='0.0.0.0', port=5000)
