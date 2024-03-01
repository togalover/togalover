```python
from flask import Flask, request

app = Flask(__name__)

@app.route('/', methods=['POST'])
def bot():
    # Get user's message
    message = request.form['message']

    # Define bot's response
    if 'hi' in message.lower() or 'hello' in message.lower():
        response = "Hi there! How can I help you today?"
    elif 'thanks' in message.lower() or 'thank you' in message.lower():
        response = "You're welcome! Anything else you need help with?"
    else:
        response = "I'm sorry, I didn't understand what you said. Could you please rephrase that?"

    # Return bot's response
    return response

if __name__ == '__main__':
    app.run(debug=True)
```
