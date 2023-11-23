---
author: Mayk Brito
pubDatetime: 2023-11-23T11:15:00Z
title: Aprendendo Algoritmos! Conheça o BubbleSort
featured: true
draft: false
tags:
  - algoritmos
description:
  Neste post nós iremos entender o que é e para que serve um bubble sort e vamos implementar um código em javascript.
---



## Table of contents


# Entendendo o Bubble Sort com Exemplos Simples

Olá, jovem aprendiz de programação! Hoje, vamos embarcar em uma aventura pelo mundo da ordenação de elementos, que é como organizar coisas em ordem. 

Imagine que você tem uma pilha de cartas de Pokémon e quer organizá-las por ordem crescente de poder. Em programação, há várias maneiras de fazer isso e uma delas é o famoso método Bubble Sort, ou "Ordenação Bolha" em português. 

Vamos aprender juntos como ele funciona!

## Bubble Sort?

Bubble Sort é um algoritmo, que é uma série de passos que seguimos para realizar uma tarefa, criado por programadores para organizar itens em uma lista.

É chamado de "Bubble" porque os números maiores "borbulham" (ou sobem) para o topo da lista, enquanto organizamos a lista do menor para o maior número.

Usamos o Bubble Sort quando temos uma lista de números (ou outras coisas que podem ser comparadas, como letras) e queremos colocá-los em uma ordem específica.

Usamos em qualquer lugar que você precise organizar dados, como em um jogo, numa lista de compras, ou até mesmo para ordenar os resultados de uma pesquisa.

Porque às vezes é mais fácil encontrar o que você precisa se as coisas estiverem organizadas. É como encontrar seu brinquedo favorito se seu quarto estiver arrumado!

## Como Funciona?

Estaremos fazendo várias passagens pela lista, sempre comparando pares de números e trocando suas posições se estiverem na ordem errada.

**Passo 1: Compare os Números**
Imagine que temos cinco números: 3, 5, 2, 4, 1. Começamos comparando o primeiro número (3) com o segundo (5). Eles estão na ordem correta, então deixamos como está.

**Passo 2: Continue Comparando**
Agora compare 5 com 2. Estão na ordem errada, **então trocamos**. A lista fica assim: 3, 2, 5, 4, 1.
Continue fazendo isso até o fim da lista.

**Passo 3: Repita**
Depois de chegarmos ao fim da lista, voltamos ao começo e fazemos tudo de novo, até que consigamos passar por toda a lista sem precisar fazer trocas.

## Simples, né? Agora Vamos Ver Isso no Código!

```jsx
function bubbleSort(array) {
    let swapped;
    do {
        swapped = false;
        for (let i = 0; i < array.length - 1; i++) {
            if (array[i] > array[i + 1]) {
                // Troca os elementos!
                let temp = array[i];
                array[i] = array[i + 1];
                array[i + 1] = temp;
                swapped = true;
            }
        }
    } while (swapped);
    return array;
}

// Agora vamos testar a função com alguns números.
const minhaLista = [3, 5, 2, 4, 1];
console.log('Lista original:', minhaLista);

const listaOrdenada = bubbleSort(minhaLista);
console.log('Lista organizada:', listaOrdenada);

```

## E... Hora de Concluir!

Bubble Sort não é o método mais rápido para ordenar itens, mas é um dos mais simples de entender e um ótimo lugar para começar a aprender sobre algoritmos de ordenação. É como aprender a andar de bicicleta com rodinhas antes de partir para as big bikes!

Então, agora que você sabe como o Bubble Sort funciona e viu ele em ação com um código de JavaScript, que tal tentar mexer no código e ver o que acontece quando você muda os números da lista? Experiências são as melhores maneiras de aprender!

Lembre-se: a prática leva à perfeição, então continue praticando e, um dia, você se tornará um mestre da programação!

Até a próxima, jovem programador! 🚀
