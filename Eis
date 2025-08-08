import random
import string

class User:
    def __init__(self, name):
        self.name = name
        self.username = self.generate_username()
        self.password = self.generate_password()

    def generate_username(self):
        return self.name.lower().replace(" ", "") + str(random.randint(100, 999))

    def generate_password(self, length=8):
        characters = string.ascii_letters + string.digits
        return ''.join(random.choice(characters) for _ in range(length))

    def update_name(self, new_name):
        self.name = new_name
        self.username = self.generate_username()  # update username

    def update_password(self, new_password):
        self.password = new_password

    def display(self):
        print(f"Name: {self.name}")
        print(f"Username: {self.username}")
        print(f"Password: {self.password}")


# Example usage
if __name__ == "__main__":
    name = input("Enter your name: ")
    user = User(name)
    user.display()

    # Update
    choice = input("Do you want to update your name? (y/n): ")
    if choice.lower() == 'y':
        new_name = input("Enter new name: ")
        user.update_name(new_name)
        user.display()

    choice = input("Do you want to update your password? (y/n): ")
    if choice.lower() == 'y':
        new_pass = input("Enter new password: ")
        user.update_password(new_pass)
        user.display()

