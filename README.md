# Prova-algoritimo--26-05-2026


## dados do aluno 
**Aluno**:Mateus Bohn dos Santos 
curso;informatica para internet
turma : 2608

## Descrição do codigo 


Eu utilizei a matriz para ter um espaço na memória .Iniciei o **equanto** para continuar um loop infinito onde o sistema só vai para quando digitar 6.Fiz  os escreval para determinar a decisão da pessoa contendo o **leia** e a variável **opção** para armazenar a opção e ser usado nos comandos **se** onde se ele digitar os números sugeridos irá para uma decisão diferente.


Decisão 1


Aqui temos um uso do se a opção  for igual a 1 ele tomará a decisão abaixo .Dentro do código temos **se** quantidade maior que 10 ou seja ele irá limitar o número de reservas a 10 se caso passar disso ele cairá nessa condição.


O senao sera a opção de cadastro onde inicializará  a quantidade recebendo quantidade + 1 para iniciar


com isso eu aplicarei a opção no escreval com o resultado a  variável leitura recupera o valor e implementar na linha ou coluna na matriz como abaixo


 se opcao  = 1 entao

      se quantidade > 10 entao
        escreval(" Se esgotaram as reservas ")

      senao
        quantidade<-quantidade+1

        escreval("#################### Cadastrar reservas ############################################")

        escreval("################ Digite o nome do cliente  #########################################")
        leia(leitura)
        reservas[quantidade , 1 ]<-leitura
        escreval("####################################################################################")
        limpatela
        escreval("################ Digite a quantidade de pessoas  ###########################################")
        leia(leitura)
        reservas[quantidade , 2 ]<-leitura

        escreval("####################################################################################")
        limpatela
        escreval("################ Digite a Data da consulta #########################################")
        leia(leitura)
        reservas[quantidade , 3 ]<-leitura

        escreval("####################################################################################")
        limpatela
        escreval("################ Digite o status da reserva (ativa/cancelada)######################################")
        leia(leitura)
        reservas[quantidade , 4]<-leitura

        escreval("####################################################################################")
        limpatela
      fimse
    fimse

decisão 2 

Aqui usei o **achou** como lógico para ver se a variável é verdadeira ou falsa onde o usuário vai digitar a o nome da reserva  e o comando leia vai armazenar o resultado na variável **busca** tendo esse resultado ele verificará  usando o **para** a a linha indicando a linha da matriz onde ele passará linha por linha então usará o se se caso a matriz for verdadeira  o achou receberá verdadeiro  e executa fazendo com que a reserva seja cancelada  caso contrário ele continuará falso e cairá na outra decisão onde identificaram como não havendo nenhum resultado de busca.




 se opcao = 2 entao
      achou<-falso

      escreva("Digite o Nome para cancelar a reserva  ")
      leia(busca)

      para linha de 1 ate quantidade passo 1 faca
        se reservas[linha,1] = busca entao

          achou<-verdadeiro

          reservas[linha , 4 ]<-"Cancelada"

          escreval("Sua reserva foi cancelada")
        fimse
      fimpara

      se achou = falso entao
        escreval("Esse nome não possui reserva ")
      fimse
      limpatela
    fimse




Decisão 3 

Usei o se com a variavel opcao como na anterior para tomar uma decisão 

aqui usei o **achou** como lógico para ver se a variável é verdadeira ou falsa onde o usuário vai digitar a o nome da reserva  e o comando leia vai armazenar o resultado na variável **busca** tendo esse resultado ele verificará  usando o **para** a a linha indicando a linha da matriz onde ele passará linha por linha então usará o se se caso a matriz for verdadeira  o achou receberá verdadeiro  e executar o código e mostrar a reserva pesquisada caso contrário ele continuará falso e cairá na outra decisão onde identificaram como não havendo nenhum resultado de busca.



  se opcao = 3 entao
      achou<-falso

      escreva("Digite nome da reserva")
      leia(busca)

      para linha de 1 ate quantidade passo 1 faca
        se reservas[linha,1] = busca entao

          achou<-verdadeiro
          escreval("Nome: " ,reservas[linha ,1  ] ," Quantidade de pessoas: ",reservas[linha ,2 ] ,"Data da reserva" ,reservas[linha ,3 ] ,"Status da reserva " ,reservas[linha ,4 ])
        fimse
      fimpara

      se achou = falso entao
        escreval("Nenhum resultado encontrado nas reservas listadas")
      fimse
      limpatela
    fimse


Decisão 4 


Aqui é usado uma estrutura de repetição onde ele passará coluna por coluna e linha por linha mostrando todos os dados recebidos no sistema desenvolvidos caso não há nenhuma reserva cadastrada ele irá cair na primeira condição onde mostrará a opção nenhuma reserva cadastrada



 se opcao = 4 entao
      se quantidade = 0 entao
        escreval("---------------    Nenhma reserva cadastrada    -----------------")
      senao
        escreval("|  Nome  | quantidade pessoas | Data | Status da reserva |")
        para linha de 1 ate quantidade passo 1 faca
          para coluna de 1 ate 4 passo 1 faca
            escreva ( "|  ", reservas[linha,coluna], "     ")
          fimpara
          escreva("  |")
          escreval("")
        fimpara
      fimse
    fimse

Decisão 5 

Aqui haverá uma estrutura de repetição parecida com a parte anterior só que aqui ele mostrará todas as reservas ativas caso não ele não executa e com contador para contar o total de reservas e mostrar o total



então ele lista todos os ativos e escreve o total 

     se opcao= 5 entao

      escreva(" Total reservas ativas ")


      para linha de 1 ate quantidade passo 1 faca
        para coluna de 1 ate 4 passo 1 faca
          se reservas[linha,4] ="Ativa" entao
            limpatela
            escreval("Nome: " ,reservas[linha ,1  ] ," Quantidade de pessoas: ",reservas[linha ,2 ] ," Data da reserva " ,reservas[linha ,3 ] ," Status da reserva " ,reservas[linha ,4 ])
contador<-contador+1

          fimse
        fimpara
      fimpara
escreval("Total ativos " ,contador)
    fimse



```