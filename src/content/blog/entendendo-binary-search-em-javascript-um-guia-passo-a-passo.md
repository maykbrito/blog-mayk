---
author: Mayk Brito
pubDatetime: 2023-11-23T12:19:00Z
title: Entendendo Binary Search em JavaScript - Um Guia Passo-a-Passo
featured: true
draft: false
tags:
  - algoritmos
description:
  Busca binária é um dos métodos mais eficientes para localizar um elemento em uma lista ordenada.
---

Se você tem interesse no universo de algoritmos e programação, sem dúvida se deparará com o termo 'Binary Search' ou 'Busca Binária'. Este método é um dos mais eficientes para localizar um elemento em uma lista ordenada. Hoje, nós vamos aprender como implementar o Binary Search em JavaScript.

## Table of contents

## **O que é Binary Search?**

A busca binária é um algoritmo de busca que divide uma lista ordenada de elementos pela metade, e verifica se o elemento do meio é igual, menor ou maior que o valor que estamos procurando. Se igual, ele o retorna; se não, ele reduz o problema pela metade e repete o processo. 

Imagine que você está buscando uma página em um livro ….

## **Por que usar Binary Search?**

O Binary Search é muito mais eficiente do que a busca linear (percorrer cada elemento da lista), principalmente quando a quantidade de elementos é grande. Ele tem uma complexidade de tempo de O(log n), o que o torna rápida para listas grandes.

## **Como funciona a Binary Search?**

Vamos tomar como exemplo uma lista ordenada de inteiros. O Binary Search começará no meio. Se o número do meio é o que estamos procurando, estamos prontos. Se não, e o número que procuramos é menor que o número do meio, repetimos o processo, mas agora com a metade esquerda da lista. Se o número que procuramos é maior que o número do meio, repetimos com a metade direita da lista.

## **Onde utilizar Binary Search?**

O Binary Search é ideal para qualquer situação onde temos uma lista ordenada e precisamos encontrar um valor específico. Isso aplica-se em muitos campos, de jogos de computador a bancos de dados.

## **Quem pode utilizar Binary Search?**

Qualquer um com uma compreensão básica de JavaScript e algoritmos pode implementar o Binary Search.

## **Quando usar Binary Search?**

Você deve usar a busca binária quando sua lista está ordenada e você precisa de uma maneira eficiente de encontrar um determinado elemento.

## **Como implementar Binary Search em JavaScript?**

Considere um array ordenado chamado `myArray` e um valor `x` que queremos encontrar. Aqui está um exemplo simples de implementação:

```jsx
    function binarySearch(myArray, x) {
       let start = 0, end = myArray.length-1;

       // iteração até que start seja menor ou igual ao fim
       while (start <= end) {
           let mid=Math.floor((start + end)/2);

           // se x for encontrado, retorna o índice
           if (myArray[mid]===x) return myArray.indexOf(x);

           // se x for maior, ignora a esquerda metade
           else if (myArray[mid] < x)
                start = mid + 1;
           // se x é menor, ignora a direita metade
           else
                end = mid - 1;
       }

       return false;
    }

```

## **Qual é o próximo passo a seguir?**

Agora que você entende o que é a Binary Search e viu como implementá-la em JavaScript, é hora de colocar esse conhecimento em prática! Comece criando listas ordenadas e usando a busca binária para encontrar diferentes valores.

Espero que este artigo lhe tenha dado uma compreensão clara de Binary Search em JavaScript. Feliz Codificação!