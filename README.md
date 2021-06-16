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

###Relembrando IF
   resposta = input('Você costuma viajar de avião?: ')
   if resposta == "sim":
     print('Que bom')
     resposta2 = input('Gostaria de ver nossas ofertas?: ')
   if resposta2 == 'sim':
     input('Insira seu e-mail: ')
     print('Você receberá um e-mail em sua caixa de mensagens, obrigado!')
   elif resposta2 == 'não':
     print('Obrigado pela atenção.')
   else:
     print('Não entendi sua resposta')
     
### Relembrando INT

idade = int(input('Qual sua idade meu caro amigo?: '))
if idade < 18:
  print('Poxa amigão, ao fazer 18 anos, irei pagar sua CNH!')
else:
  print ('Coisa boa amigo, irei pagar sua CNH!')     

### FUNÇÃO WHILE


num1 = int(input('Digite um Número: '))
num2 = int(input('Digite outro Número: '))

while num1 > num2:
  print('O primeiro número digitado, é maior!')
  num1 = int(input('Digite um Número: '))
  num2 = int(input('Digite outro Número: '))
  
############## ATIVIDADE WHILE ########################################################################################################################################## 

###1 - Faça um programa que leia o sexo biológico de uma pessoa, mas só aceite os valores ‘M’ ou ‘F’.
###Caso esteja errado, peça a digitação novamente até ter um valor correto.

sexo = input('Digite seu sexo: [F / M]\n').upper()
while sexo != 'F' and sexo != 'M':
  sexo = input('Entrada Inválida! Digite seu sexo: [F / M]\n').upper()
print('Obrigado')

### 2 - Escreva um programa que pede a senha uma senha ao usuário, e só sai do loop quando digitarem
### corretamente a senha. A senha é “Blue123”
### 2b - Exiba quantas vezes o usuário errou a digitação.

senha = 'Blue123'
acesso = str(input('Digite sua senha: '))
tentativas = 0

while acesso != senha:
  print('Senha incorreta')
  acesso = str(input('Digite sua senha: '))
  tentativas = tentativas + 1

if tentativas > 0:
  print('Seja bem vindo.')
  print('A senha foi digitada incorretamente ' + str(tentativas) + ' vezes')
else:
  print('Seja bem vindo.')


### 3 Crie um jogo onde o computador vai “pensar” em um número entre 0 e 10. O jogador vai tentar
adivinhar qual número foi escolhido até acertar, mostrando no final quantos palpites foram
necessários para vencer

### Crie um programa que leia a idade e o sexo de várias pessoas.
A cada pessoa cadastrada, o programa deverá perguntar se o usuário quer ou não continuar.
No final mostre:

A) Quantas pessoas tem mais de 18 anos
B) Quantos homens foram cadastrados.
C) Quantas mulheres tem menos de 20 anos.

##RESPOSTA:
while continuação != 'N':
  nome = str(input('Qual o seu sexo?: '))[0:1].upper()
  idade = int(input('Quantos anos você tem?: '))
  continuação = str(input('Deseja continuar?[S/N]: '))[0:1].upper()

while continuação == 'N':
  break


### Resposta Desafio

print('Seja bem vindo a Delegacia de plantão de Parnamirim')
print('Olá, sou o Detetive Lucas Marciel, tudo bem?')
print('Irei iniciar o interrogatório!')
pergunta1 = str(input('Você telefonou para a vítima? [S / N]: ')[0:1]).upper()
pergunta2 = str(input('Você esteve no local do crime? [S / N]: ')[0:1]).upper()
pergunta3 = str(input('Você mora perto da vítima? [S / N]: ')[0:1]).upper()
pergunta4 = str(input('Você devia para a vítima? [S / N]: ')[0:1]).upper()
pergunta5 = str(input('Você já trabalhou com a vítima? [S / N]: ')[0:1]).upper()
cont = 0
x = 0
sim = 0

if pergunta1 == 'S':
    cont = cont + 1
if pergunta2 == 'S':
    cont = cont + 1
if pergunta3 == 'S':
    cont = cont + 1
if pergunta4 == 'S':
    cont = cont + 1
if pergunta5 == 'S':
    cont = cont + 1
if cont == 5:
    print('Você é o assasino, você está preso!!')
if cont >= 3 and cont <= 4:
    print('Você é cumplice do assasinato, está preso!!')
if cont == 2:
    print('Você é Suspeito na investigação, poderá ser chamado novamente!')
if cont <= 1:
    print('Você está liberado, Inocente!')
    
##Lista + ##FOR + ##RANGE
lista =[10, 20, 30, 40, 50, 'macaco', 'chinelo']
print(len(lista))
print(lista)
print(type(lista))

for i in range (len(lista)):
    print(i)
    print()
for i in lista:
    print(i)


###Função FOR + RANGE
Escolhe um elemento que irá se repetir, durante uma determinada sequência
###Exemplo:

Letras_a = 0 
cont = 0
for i in range(0,10, 4):
    print(i)
    print('Olha o MACACO')
    cont += 1
    if i == "a" or i == "A":
        Letras_a += 1
        break
print(f'Contador:', cont)

###Como utilizar uma lista, e como substituir os elementos da lista, usando a função INPUT
###Observação, ao usar o FOR, o "i" assume o papel do indice 0 da lista.
Ou seja, não importa qual for o caractere escolhido.

l = [10,20,30,40,50]
print(l)
print(len(l))
for i in range(5):
    print(i)
for i in range(5):
    print(i)
    l[i] = input(f'Digite o novo valor para {i}: ')
    print(l)
