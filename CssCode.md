## Aqui estão 20 instruções importantes em CSS, cada uma acompanhada por um exemplo de código:

## Seletores Básicos:
    /* Selecionando elementos por tag */
    p {
      color: blue;
    }
    
    /* Selecionando elementos por classe */
    .destaque {
      font-weight: bold;
    }
    
    /* Selecionando elementos por ID */
    cabecalho {
      background-color: #ccc;
    }

## Estilo de Texto:
    body {
      font-family: "Arial", sans-serif;
    }
    
    h1 {
      text-align: center;
      text-decoration: underline;
    }
    
    .destaque {
      color: red;
      font-size: 18px;
    }

## Modelo de Caixa:
    div {
      width: 200px;
      height: 100px;
      border: 2px solid #333;
      padding: 10px;
      margin: 20px;
    }

## Cores e Fundos:
    .fundo-azul {
      background-color: blue;
    }
    
    .texto-branco {
      color: #fff;
    }
    
    .gradiente {
      background: linear-gradient(to right, #ffcc00, #ff3300);
    }

## Layout Flexível (Flexbox):
    .container {
      display: flex;
      justify-content: space-between;
      align-items: center;
    }

## Layout de Grade (Grid):
    .grid-container {
      display: grid;
      grid-template-columns: repeat(3, 1fr);
      gap: 10px;
    }

## Posicionamento:
    .absoluto {
      position: absolute;
      top: 50px;
      left: 20px;
    }
    
    .fixo {
      position: fixed;
      bottom: 0;
      right: 0;
    }

## Transformações e Transições:
    .rotate {
      transform: rotate(45deg);
    }
    
    .transicao {
      transition: all 0.3s ease-in-out;
    }

## Animações CSS:
    @keyframes mover {
      0% { transform: translateX(0); }
      50% { transform: translateX(100px); }
      100% { transform: translateX(0); }
    }
    
    .animacao {
      animation: mover 3s infinite;
    }

## Estilos Responsivos:
    @media screen and (max-width: 600px) {
      body {
        font-size: 14px;
      }
    }

## Sombra e Borda:
    .elemento-sombra {
      box-shadow: 3px 3px 5px #888888;
    }
    
    .borda-arredondada {
      border-radius: 10px;
      border: 2px solid #333;
    }

## Opacidade:
    .transparencia {
      opacity: 0.7;
    }

## Fontes e Ícones:
    body {
      font-family: 'Roboto', sans-serif;
    }
    
    .icone {
      background-image: url('icone.png');
    }

## Pseudo-classes e Pseudo-elementos:
    a:hover {
      color: purple;
    }
    
    p::first-line {
      font-weight: bold;
    }

## Unidades Relativas e Absolutas:
    .largura-relativa {
      width: 50%;
    }
    
    .altura-absoluta {
      height: 100px;
    }

## Variáveis CSS:
    :root {
      --cor-destaque: #ff9900;
    }
    
    .elemento-destaque {
      color: var(--cor-destaque);
    }

## Filtros CSS:
    .imagem-filtrada {
      filter: grayscale(50%);
    }

## Estilos de Listas:
    ul {
      list-style-type: square;
    }
    
    ol {
      list-style-type: upper-roman;
    }

## Formatação de Tabelas:
    table {
      width: 100%;
      border-collapse: collapse;
    }
    
    th, td {
      border: 1px solid #ddd;
      padding: 8px;
      text-align: left;
    }

## Estilização de Formulários:
        input[type="text"] {
          width: 200px;
          padding: 5px;
        }
    
        button {
          background-color: #4caf50;
          color: white;
          padding: 10px 15px;
          border: none;
          border-radius: 5px;
        }

Essas são apenas algumas das muitas instruções CSS que você pode utilizar para estilizar páginas web. A combinação destas instruções permite a criação de layouts atraentes e responsivos.## 