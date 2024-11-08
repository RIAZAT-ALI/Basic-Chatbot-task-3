# Basic-Chatbot-task-3
This is 2nd task of CODE ALPHA internship

import random

# Define responses in a dictionary
responses = {
    "hi": ["Hey"],
    "how are you?": ["I'm good"],
    "your good name?": ["I'm chatbot"],
    "your current degree?": ["I have no degree ."],
    "quit": ["Goodbye"]
}


def get_response(user_input):
    user_input = user_input.lower().strip()


    if user_input in responses:
        return random.choice(responses[user_input])
    else:
        return "I don't understand."



print("Hi! talk to me and type 'quit' to exit.")

while True:
    user_input = input("user: ")


    if "quit" in user_input.lower():
        print("Chatbot:", get_response("quit"))
        break


    print("Chatbot:", get_response(user_input))
