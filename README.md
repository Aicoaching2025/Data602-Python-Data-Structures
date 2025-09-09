# Data602-Python-Data-Structures
Understanding Python Native Data Structures

# 🌟 Staff Email Management Program 🌟

Welcome to the **Staff Email Management Program**! This program allows you to manage a dictionary of staff members' names and their associated email addresses. You can perform various actions such as:

- 🔍 **Look up a person's email address**
- ➕ **Add a new name and email address**
- ✏️ **Change an existing email address**
- ❌ **Delete a name and email address**

## 🚀 Features

- **User-Friendly Interface**: The program provides a simple and intuitive text-based interface to manage your staff data.
- **Persistence**: Staff data is saved between program sessions.
- **Real-Time Updates**: Changes to the dictionary (adding, modifying, deleting) are immediately reflected.

---

## 🛠️ How to Use the Program

1. **Start the Program**:
   - The program begins by loading an initial staff dictionary with predefined names and email addresses.
   
2. **Choose an Option**:
   - The program will present a menu with 5 options:
     1. **Look up a person's email address**
     2. **Add a new name and email address**
     3. **Change an existing email address**
     4. **Delete a name and email address**
     5. **Exit the program**

3. **Input Data**:
   - When adding or changing data, simply type the name and the corresponding email address.

4. **The Program Responds**:
   - If the name exists, you can update or delete the email address.
   - If the name does not exist, you can add a new entry.

---

## 🖥️ Code Overview

```python
# Predefined staff data (with a fixed error)
Staff_data = {
    "Candace": "candace@academicswest.com",
    "Leo": "leo@academicswest.com",
    "Stephanie": "stephanie@academicswest.com",
    "Alex": "alex@academicswest.com",
    "Kunal": "kunal@academicswest.com"
}

# Initialize the email_dict with the Staff_data
email_dict = Staff_data.copy()

# Main menu loop
def menu():
    while True:
        print("\n--- Email Management Menu ---")
        print("1. Look up a person's email address")
        print("2. Add a new name and email address")
        print("3. Change an existing email address")
        print("4. Delete an existing name and email address")
        print("5. Exit")
        
        choice = input("Enter your choice (1-5): ")
        
        if choice == "1":
            lookup_email()
        elif choice == "2":
            add_email()
        elif choice == "3":
            change_email()
        elif choice == "4":
            delete_email()
        elif choice == "5":
            print("Exiting program...")
            break
        else:
            print("Invalid choice. Please enter a number between 1 and 5.")

