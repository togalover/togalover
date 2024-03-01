```
# import necessary libraries
import random

# define function to generate responses
def generate_response(user_input):
    # possible responses
    bot_responses = [
        "Hello! How can I assist you today?",
        "Nice to hear from you! How may I help you?",
        "Good day! What can I do for you?",
        "Hi there! What do you need help with?",
        "Greetings! How can I be of service to you?"
    ]
    # return a random response
    return random.choice(bot_responses)

# start conversation with user
print("Hello! I am a friendly AI bot. How can I assist you today?")

# loop through conversation
while True:
    # get user input
    user_input = input().lower()

    # exit loop if user says goodbye
    if user_input == "goodbye":
        print("Goodbye! Have a nice day.")
        break
    
    # generate response
    bot_response = generate_response(user_input)
    
    # print response
    print(bot_response)
```
