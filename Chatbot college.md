# College Inquiry Chatbot in Python

def show_menu():
    print("\n--- College Inquiry Chatbot ---")
    print("Type your question or choose a topic below:")
    print("1. Courses Offered")
    print("2. Admission Process")
    print("3. Fees Structure")
    print("4. Contact Details")
    print("5. Hostel Facilities")
    print("6. Exit")

def chatbot_response(user_input):
    user_input = user_input.lower()

    if "course" in user_input or user_input == "1":
        return " We offer B.Tech, B.Sc, BBA, MBA, M.Tech, and MCA programs."
    
    elif "admission" in user_input or user_input == "2":
        return (" The admission process includes:\n"
                "- Online application\n"
                "- Entrance test (if applicable)\n"
                "- Document verification\n"
                "- Fee payment")
    
    elif "fee" in user_input or user_input == "3":
        return (" Fee Structure:\n"
                "- B.Tech: ₹1,00,000/year\n"
                "- MBA: ₹1,20,000/year\n"
                "- BBA/B.Sc: ₹60,000/year")
    
    elif "contact" in user_input or user_input == "4":
        return (" Contact Details:\n"
                "Phone: +91-9876543210\n"
                "Email: info@college.edu\n"
                "Website: www.college.edu")
    
    elif "hostel" in user_input or user_input == "5":
        return (" Hostel Facilities:\n"
                "- Separate hostels for boys and girls\n"
                "- 24/7 security\n"
                "- Wi-Fi, mess, and laundry available")
    
    elif "exit" in user_input or user_input == "6":
        return "Thank you for contacting us! Have a great day!"

    else:
        return " Sorry, I didn’t understand that. Please ask another question or choose an option."

# Main loop
while True:
    show_menu()
    user_input = input("You: ")
    response = chatbot_response(user_input)
    print("Bot:", response)
    if "thank you" in response.lower():
        break
