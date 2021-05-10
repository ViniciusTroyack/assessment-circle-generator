# Atividade: Circle generator

Para começar, acesse [este link](https://gitlab.com/kenzie-academy-brasil/se/fe/getting-started-with-javascript/assessment-circle-generator), faça o fork e clone o repositório.

## Introdução

No repositório clonado, foi fornecido o código HTML e CSS. Portanto, precisamos nos preocupar somente em entender o que esses códigos estão fazendo.

Nesta entrega você irá criar um gerador de círculos, veja o exemplo:

![](https://files-kenzie-academy-brasil.s3.amazonaws.com/q1/sprint3/click_generator.gif)

## Seu objetivo:

Organizar os códigos abaixo, de modo que seu projeto tenha o mesmo comportamento que o exemplo fornecido anteriormente.

## Início

Como os códigos HTML e CSS já estão prontos, agora é hora de partir para o JavaScript.

No exemplo acima, vimos que **ao clicar no botão GENERATE**, novos círculos de cores diferentes são criados.

- Passo 1: Adicionar o evento de click no botão GENERATE.

```js
const buttonGenerate = document.getElementById("buttonGenerate");
buttonGenerate.addEventListener("click", () => {
  // teu código vai aqui ...
});
```

- Passo 2: Criar uma função que gere novos círculos.

```js
const createCircle = (color) => {
  const newCircle = document.createElement("div");
  newCircle.style.border = `solid 4px ${color}`;

  // ADICIONA A CLASSE QUE POSSUI OS ESTILOS PADRÃO DOS CÍRCULOS
  newCircle.classList.add('circle');

  return newCircle;
};
```

- Passo 3: Criar uma função que defina as cores de forma aleatória.

```js
const randomColor = () => {
  const colors = ["#1F271B", "#003F91", "#6D326D", "#157A6E", "#916953"];

  return colors[Math.floor(Math.random() * 5)];
};
```

## Resetando o HTML

No código HTML fornecido, vimos que o local de armazenamento dos círculos é a div com o id **boxStorage**. Com essa informação, fica muito simples resetar o conteúdo dessa div.

No exemplo acima, **ao clicar no botão RESET** todos os círculos somem.

- Passo 1: Adicionar o evento de click no botão RESET.

```js
const buttonReset = document.getElementById("buttonReset");
buttonReset.addEventListener("click", () => {
  // teu código vai aqui ...
});
```

- Passo 2: Resetar o conteúdo HTML dentro da div boxStorage.

```js
const boxStorage = document.getElementById("boxStorage");
boxStorage.innerHTML = "";
```
