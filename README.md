# Blue_TC3C5_MOD1
"Repositório criado para guardar projetos da turma TC3C5"
###Tabela de conversão R$ para Moedas.

print("Tabela de Conversão do Real")

num1 = int(input("Digite o Valor em Real R$: "))
print("Conversão para Dolar é R$:", num1 * 0.20)
print("Conversão para Euro é R$:", num1 * 0.1631)
print("Conversão para Libra Esterlina é R$:", num1 * 0.1402)
print("Conversão para Dolar Canadense é R$:", num1 * 0.0240)
print("Conversão para Peso Argentino é R$:", num1 * 18.85)
print("Conversão para Peso Chileno é R$:", num1 * 142.51)

###Tabela de cálculo reajuste de Aluguel.

print("Reajuste Aluguel IGPM 31%")
num1 = int(input("Digite o Valor do Aluguel: "))
print("O novo valor do aluguel é R$: ", num1 * 0.31 + num1)

### 01 - Escreva um programa que deve receber o nome completo do usuário e retornar uma saudação com o nome no formato adequado (todas as primeiras letras em maiúsculas).

#Primeira opção
comando1 = input("Olá amigo, qual o seu nome?").title()
print(f"Bem-vindo(a) {comando1}! ")

#Segunda opção
comando1 = input("Olá amigo, qual o seu nome?").title()
print("Bem vindo (a)", comando1.title() + "!")

### 02 - Escreva um programa que solicite uma frase ao usuário e escreva a frase toda em 
maiúscula e sem espaços em branco.

ex1 = input('Digite uma Frase: \n"')
print(ex1.upper().replace(" ",""))

### 03 – Faça um programa que solicite a altura e o peso do usuário, e calcule o seu IMC. Os 
dados entrados precisam ser corrigidos pelo programa (trocando “,” por “.” e eliminando 
espaços e letras extras)

altura = float(input('Qual a sua Altura?\nM:').lower().replace(',' , '.').replace(" ","").replace("m",""))
peso = float(input('Qual o seu Peso?\nKg:').lower().replace(',' , '.').replace(" ","").replace("k","").replace("g",""))
imc = peso / (altura**2)

print(f"O seu IMC é: {imc:.1f}")


### Exemplo Aula 03 - Fatiamento de Strings

string1 = "Os limites só existem se você os deixar existir.(goku)"
print(string1[48:54])

### Exemplo Aula 03 - Aluno aprovado ou reprovado.

nota1 = float(input('Digite a Primeira Nota '))
nota2 = float(input('Digite a Segunda Nota '))

media = (nota1 + nota2) / 2

if media >=6:
    print("Parabéns, você foi aprovado!!")
else:
    print("Aluno reprovado, estude mais!!")
    
### Faça um script que peça um valor e mostre na tela se o valor é positivo ou negativo e implemente a funcionalidade de não aceitar o número 0, no input.

numero = float(input('Informe um número ' ).replace(",","."))
if numero >0:
    print('Esse número é positivo')
elif numero ==0:
    print('Digito 0 não é permitido.')
else:
    print('Esse número é negativo.')


### Faça um programa que peça dois números, imprima o maior deles ou imprima "Numeros iguais" se os números forem iguais.

numero1 = input('Digite o primeiro número: ')
numero2 = input('Digite o segundo número: ')

if numero1 > numero2:
    print(f'O número maior é {numero1}')
else:
  if numero1 == numero:
    print('Os números possuem o mesmo valor.')
  else: 
    print(f'O maior é {numero2}')

### Adicione ao Exercício do Aluno aprovado ou reprovado, com a condição "Em recuperação" através do Else.

nota1 = float(input('Digite a Primeira Nota '))
nota2 = float(input('Digite a Segunda Nota '))

media = (nota1 + nota2) / 2

if media >=6:
    print("Parabéns, você foi aprovado!!")
elif media >= 4 and media < 6:
    print('Aluno em Recuperação':)

else:
    print("Aluno reprovado, estude mais!!")
   
### Crie um programa em Python que peça a nota do aluno, que deve ser um float entre 0.00 e 10.0

#Se a nota for menor que 6.0, deve exibir a nota F.
#Se a nota for de 6.0 até 7.0, deve exibir a nota D.
#Se a nota for entre 7.0 e 8.0, deve exibir a nota C.
#Se a nota for entre 8.0 e 9.0, deve exibir a nota B.
#Por fim, se for entre 9.0 e 10.0, deve exibir um belo de um A.

nota = float()input('Insira sua nota': )



