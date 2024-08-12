def encrypt(text, shift):
    ciphertext = ""
    for char in text:
        if char.isalpha():  
            if char.isupper():
                start = ord('A')
            else:
                start = ord('a')
            shifted_char = chr((ord(char) - start + shift) % 26 + start)
            ciphertext += shifted_char
        else:
            ciphertext += char  
    return ciphertext

def decrypt(text, shift):
    return encrypt(text, -shift)  

def main():
    while True:
        option = input("\nEnter 'e' for encryption or 'd' for decryption. Press 'z' to quit: ").lower()
        
        if option == 'e':
            text = input("Enter message: ")
            shift = int(input("Enter shift value: "))
            message = encrypt(text, shift)
            print("Encrypted message:", message)
        
        elif option == 'd':
            text = input("Enter message: ")
            shift = int(input("Enter shift value: "))
            message = decrypt(text, shift)
            print("Decrypted message:", message,)

        elif option == 'z':
            break
        
        else:
            print("Invalid choice!")

if __name__ == "__main__":
    main()