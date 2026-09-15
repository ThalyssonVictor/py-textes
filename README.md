usuarios = []
admin = input("Digite a senha de admin:")
if admin == "12345":
    print("\n------Menu de Opções------")
    print(" 1 para cadastrar usuario:")
    print(" 2 para pesquisar/listar usuario:")
    print(" 3 para remover usuario:")

digite = input("\nDigite a opção desejada:")
if digite == "1":
    login = input("Digite o nome do usuario:")
    senha = input("Digite a senha do usuario:")
    usuarios.append({"login": login, "senha": senha})
    print("Usuario cadastrado!")
    
elif digite == "2":
    if not usuarios:
        print("Nenhum usuario cadastrado:")
    else:
        print("\nUsuarios cadastrados:")
    for i in usuarios:
        print("Login:", i["login"], "Senha:", i["senha"])

elif digite == "3":
    login = input("Digite o login do usuario para remover:")
    encontrado = False
    for i in usuarios:
        if i["login"] == login:
            usuarios.remove(i)
            print("Usuario removido!")
            encontrado = True
            break
    if not encontrado:
        print("Usuario nao encontrado.")
