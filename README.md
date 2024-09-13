def add(x, y):
    return x + y

def subtract(x, y): 
    return x - y

def multiply(x, y):
    return x * y

def divide(x, y):
    if y != 0:
        return x / y
    else:
        return "Erreur : Division par 0"

def main():
    print("Choisissez une opération :")  
    print("1. Addition")
    print("2. Soustraction")
    print("3. Multiplication")
    print("4. Division")

    choice = input("Entrez le numéro de l'opération (1/2/3/4) : ")

    try:
        num1 = float(input("Entrez le premier nombre : "))
        num2 = float(input("Entrez le deuxième nombre : "))
    except ValueError:
        print("Erreur : Entrez un nombre valide.")
        return

    if choice == '1':
        print(f"Résultat : {add(num1, num2)}")
    elif choice == '2':
        print(f"Résultat : {subtract(num1, num2)}")  
    elif choice == '3':
        print(f"Résultat : {multiply(num1, num2)}")
    elif choice == '4':
        print(f"Résultat : {divide(num1, num2)}")
    else:
        print("Choix invalide")

if __name__ == "__main__":
    main()

