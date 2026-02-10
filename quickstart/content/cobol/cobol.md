+++
title = 'Codigo em cobol para interessados!'
date = '2026-02-09'
+++

```COBOL
      *É BEM IMPORTANTE RESPEITAR AS LINHAS NO COBOL JÁ QUE SERVE COMO
      * CODAR EM CARTÃO PERFURADO
      *Meu Hello Wolrd em Cobol
       
      *Uma divisião para incluir informações documentais. como o nome do
      *programa nome do autor
      * a posição 7 indica como o compilador deve intepretar aquela 
      * linha por isso os asteristicos ficam aqui..
      * já a 8 já indica o codigo em si
       IDENTIFICATION DIVISION.            
       PROGRAM-ID. hello.
       ENVIRONMENT DIVISION.
      * INDICA O COMPPUTADOR ONDE O PROGRAMA ESTÁ SENDO ESCRITO
       DATA DIVISION.
      * ARQUIVOS DE ENTRADA E SAIDA,VARIAVEIS E CONSTANTES
       PROCEDURE DIVISION.
           
           display "HELLO WOLRD!".
           stop run.
       

```