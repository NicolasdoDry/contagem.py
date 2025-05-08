# contagem.py
def contar_digitos():
    numero = input("Digite um número: ").strip()

    # Remove o sinal negativo, se houver
    if numero.startswith('-'):
        numero = numero[1:]

    # Remove ponto decimal, se for um número com casas decimais
    numero_sem_ponto = numero.replace('.', '')

    # Verifica se ainda sobrou algum caractere que não seja dígito
    if not numero_sem_ponto.isdigit():
        print("Entrada inválida. Digite um número válido.")
        return

    quantidade_digitos = len(numero_sem_ponto)
    print(f"O número digitado tem {quantidade_digitos} dígito(s).")

contar_digitos()
