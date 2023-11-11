# Secure-File-Deletion-
ecure File Deletion Using shutil Documentation
This Python script demonstrates how to securely delete a file by overwriting its content before removal. It provides a class, FileDeletion, that allows users to specify a file path and securely delete the file. Below is a detailed explanation of how the code works:
Code Structure and Functionality:
The code is organized into a class, FileDeletion, which encapsulates the file deletion logic. The class includes the following methods:
    1. FileDeletion Class:
        ◦ The class represents a file deletion operation with secure content overwriting.
        ◦ Constructor (__init__): Initializes the file path to be deleted.
    2. check_file Method:
        ◦ Checks if the specified file exists at the provided file path.
        ◦ Returns True if the file exists.
        ◦ Prints a message and returns False if the file does not exist.
    3. secure_file Method:
        ◦ Checks if the file exists using the check_file method.
        ◦ If the file exists, it opens the file in binary write mode ("wb").
        ◦ Overwrites the content of the file with random bytes generated using os.urandom.
        ◦ Deletes the file using shutil.rmtree, ensuring secure deletion.
        ◦ Prints success messages after overwriting and deleting the file.
        ◦ If the file does not exist, it prints a "Try again" message.
    4. Main Section (if __name__ == "__main__":):
        ◦ Prompts the user to enter the file path of the file to be securely deleted.
        ◦ Creates a FileDeletion object with the provided file path.
        ◦ Calls the check_file method to check if the file exists.
        ◦ Calls the secure_file method to securely delete the file.
How the Code Works:
    1. The script starts by defining the FileDeletion class, which encapsulates the secure file deletion logic.
    2. In the main section:
        ◦ The user is prompted to enter the file path of the file to be securely deleted.
    3. A FileDeletion object is created with the provided file path.
    4. The script checks if the file exists using the check_file method:
        ◦ If the file exists, it proceeds to securely delete the file.
        ◦ If the file does not exist, it prints a "Try again" message.
    5. In the secure_file method:
        ◦ The script opens the file in binary write mode ("wb").
        ◦ It overwrites the content of the file with random bytes generated using os.urandom.
        ◦ After overwriting, the file is securely deleted using shutil.rmtree.
    6. Success messages are printed after overwriting and deleting the file.
This script provides a basic implementation for securely deleting files by overwriting their content. It can be further enhanced to handle various scenarios and ensure data privacy and security.
