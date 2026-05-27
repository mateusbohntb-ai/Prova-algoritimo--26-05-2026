# Codigo 

```js 

algoritmo "Primeiro Programa"

var
  reservas:matriz [1..4 , 1..10] de caracter
  quantidade,opcao,contador:inteiro
  leitura,busca,linha,coluna:caracter
  achou:logico
inicio
contador<-0
  quantidade<-0
  opcao<-0
  enquanto opcao  <>  6 faca

    escreval("####################################################################################")

    escreval("Bem vindo ao restaurante seu João ")
    escreval("####################################################################################")
    escreval("Digite 1 para regitrar uma reserva ")
    escreval("Digite 2 para cancelar uma reserva pelo nome ")
    escreval("Digite 3 buscar a reserva pelo nome")
    escreval("Digite 4 listar todas as reservas ")
    escreval("Digite 5 exibir total de reservas")
    escreval("Digite 6 sair do sistema")
    leia(opcao)
    escreval("####################################################################################")
    limpatela


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
       
      fimse
    fimse

    se opcao = 2 entao
      achou<-falso
      escreval("####################################################################################")
      escreva("Digite o Nome para cancelar a reserva  ")
      leia(busca)
      escreval("####################################################################################")
      para linha de 1 ate quantidade passo 1 faca
        se reservas[linha,1] = busca entao

          achou<-verdadeiro

          reservas[linha , 4 ]<-"Cancelada"
          escreval("####################################################################################")
          escreval("Sua reserva foi cancelada")
          escreval("####################################################################################")
        fimse
      fimpara

      se achou = falso entao
        escreval("####################################################################################")
        escreval("Esse nome não possui reserva ")
        escreval("####################################################################################")
      fimse
 
    fimse


    se opcao = 3 entao
      achou<-falso
      escreval("####################################################################################")
      escreva("Digite nome da reserva")
      escreval("####################################################################################")
      leia(busca)

      para linha de 1 ate quantidade passo 1 faca
        se reservas[linha,1] = busca entao

          achou<-verdadeiro
          escreval("####################################################################################")
          escreval("Nome: " ,reservas[linha ,1  ] ," Quantidade de pessoas: ",reservas[linha ,2 ] ,"Data da reserva" ,reservas[linha ,3 ] ,"Status da reserva " ,reservas[linha ,4 ])
          escreval("####################################################################################")
        fimse
      fimpara

      se achou = falso entao
        escreval("####################################################################################")
        escreval("Nenhum resultado encontrado nas reservas listadas")
        escreval("####################################################################################")
      fimse

    fimse


    se opcao = 4 entao
      se quantidade = 0 entao
        escreval("####################################################################################")
        escreval("---------------     Nenhum reserva cadastrada   -----------------")
        escreval("####################################################################################")
      senao
        escreval("####################################################################################")
        escreval("|  Nome  | quantidade pessoas | Data | Status da reserva |")
        para linha de 1 ate quantidade passo 1 faca
          para coluna de 1 ate 4 passo 1 faca
            escreva ( "|  ", reservas[linha,coluna], "     ")
          fimpara
          escreva("  |")
          escreval("")
          escreval("####################################################################################")
       
        fimpara
      fimse
    fimse

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




  fimenquanto
fimalgoritmo


```