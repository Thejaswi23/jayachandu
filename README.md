inp = input("Enter the message: ")
a = "abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ"
b = "zyxwvutsrqponmlkjihgfedcbaZYXWVUTSRQPONMLKJIHGFEDCBA"

var = ''.join([b[a.index(i)] if i in a else i for i in inp])
print("Encrypted message:", var)

inp2 = input("Do you want to decrypt? (Y/N): ")
if inp2.upper() == "Y":
    decrypted_var = ''.join([a[b.index(i)] if i in b else i for i in var])
    print("Decrypted message:", decrypted_var)
else:
    print("Not decrypted")
