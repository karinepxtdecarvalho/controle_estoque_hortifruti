main.py# Sistema de Controle de Estoque - Hortifruti

estoque = {}

def cadastrar_produto():
    nome = input("Digite o nome do produto: ")
    quantidade = int(input("Digite a quantidade: "))
    estoque[nome] = quantidade
    print(f"Produto {nome} cadastrado com sucesso!\n")

def listar_produtos():
    if not estoque:
        print("Estoque vazio.\n")
    else:
        print("=== Produtos em Estoque ===")
        for produto, quantidade in estoque.items():
            print(f"{produto} - Quantidade: {quantidade}")
        print()

def atualizar_estoque():
    nome = input("Digite o nome do produto para atualizar: ")
    if nome in estoque:
        nova_quantidade = int(input("Digite a nova quantidade: "))
        estoque[nome] = nova_quantidade
        print("Estoque atualizado com sucesso!\n")
    else:
        print("Produto não encontrado.\n")

def menu():
    while True:
        print("=== Sistema de Controle de Estoque ===")
        print("1 - Cadastrar produto")
        print("2 - Listar produtos")
        print("3 - Atualizar estoque")
        print("4 - Sair")
        
        opcao = input("Escolha uma opção: ")
        
        if opcao == "1":
            cadastrar_produto()
        elif opcao == "2":
            listar_produtos()
        elif opcao == "3":
            atualizar_estoque()
        elif opcao == "4":
            print("Saindo do sistema...")# Atualização pela equipe de operaçôes
            break
        else:
            print("Opção inválida.\n")

menu()
05:18
