
def encrypt(text, key):
    result = ""
    for char in text:
        result += chr(ord(char) + key)
    return result


def decrypt(text, key):
    result = ""
    for char in text:
        result += chr(ord(char) - key)
    return result


print("===== DATA ENCRYPTION & DECRYPTION TOOL =====")

while True:
    print("\n1. Encrypt")
    print("2. Decrypt")
    print("3. Exit")

    choice = input("Enter your choice: ")

    if choice == "1":
        text = input("Enter text: ")
        key = int(input("Enter key (number): "))

        encrypted = encrypt(text, key)
        print("Encrypted text:", encrypted)

    elif choice == "2":
        text = input("Enter encrypted text: ")
        key = int(input("Enter key (number): "))

        decrypted = decrypt(text, key)
        print("Decrypted text:", decrypted)

    elif choice == "3":
        print("Thank you!")
        break

    else:
        print("Invalid choice!")