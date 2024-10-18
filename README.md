# Ícones Neon Página Web

Este projeto é uma página web simples que apresenta cinco ícones neon animados usando apenas HTML e CSS. Cada ícone representa uma funcionalidade diferente e possui um efeito neon colorido.

## Ícones e suas cores

1. **Casa (Home)** - Azul Neon (#2483ff)
2. **Perfil (Perfil)** - Amarelo Neon (#fff200)
3. **Curtidas (Curtidas)** - Vermelho Neon (#ff253f)
4. **Configurações (Config)** - Verde Neon (#25d366)
5. **Procurar (Procurar)** - Rosa Neon (#f32ec8)

## Estrutura do Projeto

O projeto é composto por dois arquivos principais:

1. **HTML** (`index.html`):
    ```html
    <!DOCTYPE html>
    <html lang="pt-br">
    <head>
      <meta charset="UTF-8" />
      <title>Ícone Efeito Neon</title>
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/meyer-reset/2.0/reset.min.css" />
      <link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.5.1/css/all.min.css" />
      <link rel="stylesheet" href="./style.css" />
      <style>
        .neon-text {
          font-family: 'Arial', sans-serif;
          color: #fff;
          text-shadow:
            0 0 5px #fff,
            0 0 10px #fff,
            0 0 20px #fff,
            0 0 30px var(--clr),
            0 0 40px var(--clr),
            0 0 50px var(--clr),
            0 0 60px var(--clr);
          margin-top: 50px;
          text-align: center;
        }

        .footer-container {
          position: relative;
          padding-bottom: 100px; /* Para evitar sobrepor o texto */
        }
      </style>
    </head>
    <body>
      <ul>
        <li style="--clr: #2483ff">
          <a href="#">
            <i class="fa-solid fa-house"></i>
            <span>Home</span>
          </a>
        </li>
        <li style="--clr: #fff200">
          <a href="#">
            <i class="fa-solid fa-user"></i>
            <span>Perfil</span>
          </a>
        </li>
        <li style="--clr: #ff253f">
          <a href="#">
            <i class="fa-solid fa-heart"></i>
            <span>Curtidas</span>
          </a>
        </li>
        <li style="--clr: #25d366; display: flex; align-items: center; justify-content: center;">
          <a href="#" style="text-align: center;">
            <i class="fa-solid fa-gear"></i>
            <span style="display: block; margin-top: 5px; font-size: 18px;">Config</span>
          </a>
        </li>
        <li style="--clr: #f32ec8">
          <a href="#">
            <i class="fa-solid fa-magnifying-glass"></i>
            <span>Procurar</span>
          </a>
        </li>
      </ul>
      <div class="footer-container">
        <div class="neon-text" style="--clr: #00ff00;">Desenvolvido por Deu um Batista</div>
      </div>
    </body>
    </html>
    ```

2. **CSS** (`style.css`):
    ```css
    * {
      margin: 0;
      padding: 0;
      box-sizing: border-box;
    }

    :root {
      --bg: #222;
      --clr: #fff;
    }

    body {
      display: flex;
      justify-content: center;
      align-items: center;
      min-height: 100vh;
      background: var(--bg);
    }

    ul {
      position: relative;
      display: flex;
      gap: 50px;
    }

    ul li {
      position: relative;
      list-style: none;
      width: 80px;
      height: 80px;
      display: flex;
      justify-content: center;
      align-items: center;
      cursor: pointer;
      transition: 0.5s;
    }

    ul li::before {
      content: "";
      position: absolute;
      inset: 30px;
      box-shadow: 0 0 0 10px var(--clr), 0 0 0 20px var(--bg), 0 0 0 22px var(--clr);
      transition: 0.5s;
    }

    ul li:hover::before {
      inset: 15px;
    }

    ul li::after {
      content: "";
      position: absolute;
      inset: 0;
      background: var(--bg);
      transform: rotate(45deg);
      transition: 0.5s;
    }

    ul li:hover::after {
      inset: 0px;
      transform: rotate(0deg);
    }

    ul li a {
      position: relative;
      text-decoration: none;
      z-index: 10;
      display: flex;
      justify-content: center;
      align-items: center;
    }

    ul li a i {
      font-size: 2em;
      transition: 0.5s;
      color: var(--clr);
      opacity: 1;
    }

    ul li:hover a i {
      color: var(--clr);
      transform: translateY(-40%);
    }

    ul li a span {
      position: absolute;
      font-family: sans-serif;
      color: var(--clr);
      opacity: 0;
      transition: 0.5s;
      transform: scale(0) translateY(200%);
    }

    ul li:hover a span {
      opacity: 1;
      transform: scale(1) translateY(100%);
    }

    ul li:hover a i,
    ul li a span {
      filter: drop-shadow(0 0 20px var(--clr)) drop-shadow(0 0 40px var(--clr)) drop-shadow(0 0 60px var(--clr));
    }
    ```

## Como Usar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` no seu navegador.

## Descrição

A página apresenta cinco ícones com efeitos de neon e animações de hover. Cada ícone tem uma cor neon distinta e está associado a diferentes funcionalidades (Home, Perfil, Curtidas, Configurações, e Procurar).

