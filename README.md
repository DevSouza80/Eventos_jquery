# 📘 Documentação jQuery - Eventos e Interações

## 📌 Inicialização do jQuery

```javascript
$(function(){
```

* Garante que o código só será executado após o carregamento completo do DOM.

---

## 🖱️ Função: validarCliqueHover()

### 🎯 Objetivo:

Manipular eventos de **clique** e **hover** em elementos.

### 📌 Código:

```javascript
function validarCliqueHover(){

    $('.artigo1').click(function(){
        $('.artigo2').css('background-color', 'purple');
    });

    $('.artigo1').hover(function(){
        $('.artigo2').css('background-color', 'red');
    }, function(){
        $('.artigo2').css('background-color', 'rgb(100,100,100)');
    });

}
```

### 🧠 Explicação:

#### ✔️ `.click()`

* Executa uma função quando o elemento é clicado.
* Neste caso:

  * Ao clicar em `.artigo1`, o fundo de `.artigo2` fica **roxo**.

#### ✔️ `.hover()`

* Possui dois estados:

  1. Quando o mouse entra
  2. Quando o mouse sai

* Comportamento:

  * Mouse entra → fundo fica **vermelho**
  * Mouse sai → fundo volta para **cinza**

---

## 📝 Função: validarFormulario()

### 🎯 Objetivo:

Trabalhar com eventos de formulário.

### 📌 Código:

```javascript
function validarFormulario(){

    $('textarea').focus(function(){
        // Executa quando o campo recebe foco
    }).blur(function(){
        // Executa quando o campo perde foco
    });

    $('select').change(function(){
        console.log("Meu select foi alterado!");
    });

}
```

### 🧠 Explicação:

#### ✔️ `.focus()`

* Dispara quando o usuário clica ou entra no campo.
* Muito usado para:

  * Validação
  * Destaque de campo
  * UX

#### ✔️ `.blur()`

* Dispara quando o usuário sai do campo.
* Ideal para:

  * Validação final
  * Mensagens de erro

#### ✔️ `.change()`

* Dispara quando o valor de um `<select>` muda.
* Aqui:

  * Exibe uma mensagem no console.

---

## 🧩 Boas Práticas

* ✔️ Sempre usar `$(function(){})` para evitar erros de carregamento
* ✔️ Separar funções por responsabilidade
* ✔️ Nomear funções de forma clara (ex: `validarFormulario`)
* ✔️ Evitar repetição de código

---

## 🚀 Possíveis Melhorias

* Adicionar validação real de formulário
* Criar animações com `.fadeIn()` ou `.slideDown()`
* Usar classes ao invés de `.css()` direto
* Modularizar o código

---

## 📚 Conclusão

Esse código demonstra conceitos importantes do jQuery:

* Manipulação de eventos
* Interação com o usuário
* Alteração de estilos dinamicamente

Ideal para treinar lógica de front-end e comportamento de interface.

---
