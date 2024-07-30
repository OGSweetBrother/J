import random

def jogar_jogo():
    print("Bem-vindo ao jogo Pedra, Papel e Tesoura!")
    opcoes = ["Pedra", "Papel", "Tesoura"]

    while True:
        jogador = input("Escolha Pedra, Papel ou Tesoura (ou 'sair' para sair do jogo): ").capitalize()
        if jogador == 'Sair':
            print("Obrigado por jogar!")
            break

        if jogador not in opcoes:
            print("Escolha inválida. Por favor, escolha Pedra, Papel ou Tesoura.")
            continue

        computador = random.choice(opcoes)
        print(f"Você escolheu: {jogador}")
        print(f"O computador escolheu: {computador}")

        if jogador == computador:
            print("Empate!")
        elif (jogador == "Pedra" and computador == "Tesoura") or \
             (jogador == "Papel" and computador == "Pedra") or \
             (jogador == "Tesoura" and computador == "Papel"):
            print("Você ganhou!")
        else:
            print("Você perdeu!")

if __name__ == "__main__":
    jogar_jogo()
