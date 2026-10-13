# Contact-book
For contact 

contacts = {}

def add_contact():
    name = input("Enter name: ")
    phone = input("Enter phone number: ")
    contacts[name] = phone
    print("Contact saved successfully!")

def search_contact():
    name = input("Enter name to search: ")

    if name in contacts:
        print("Phone Number:", contacts[name])
    else:
        print("Contact not found!")

def show_contacts():
    for name, phone in contacts.items():
        print(name, ":", phone)

while True:
    print("\n1. Add Contact")
    print("2. Search Contact")
    print("3. Show All Contacts")
    print("4. Exit")

    choice = input("Enter choice: ")

    if choice == "1":
        add_contact()
    elif choice == "2":
        search_contact()
    elif choice == "3":
        show_contacts()
    elif choice == "4":
        break
    else:
        print("Invalid choice!")
        
