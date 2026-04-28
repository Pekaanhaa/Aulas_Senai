# def saudacao(nome):
#     return f"Olá, {nome}! Seja bem-vindo(a)!"
# def idade(idade):
#     return f"(nome)! Você tem {idade} anos."

# nome = input("Qual é seu nome? ")
# mensagem = saudacao(nome)
# print(mensagem)

def exibir_info(**dados):
    for chave, valor in dados.items():
        print(f"{chave}: {valor}")

# Criamos um dicionário vazio para armazenar as entradas

info_usuario = {}

print("Digite as informaçoes (ou 'sair' na chave para encerrar)")

while True:
    chave = input("Nome do campo (ex:Profissão): ")
    if chave.lower == 'sair':
        break
    valor = input(f"Valor para {chave}: ")
    info_usuario[chave] = valor

# Usamos ** para desempacotar o dicionário como argumentos

exibir_info(**info_usuario)
