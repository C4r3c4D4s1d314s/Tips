# Vue.js é um framework JavaScript progressivo para a construção de interfaces de usuário. Abaixo estão 20 instruções importantes em Vue.js, cada uma acompanhada de um exemplo de código simples.

1. **{{ }} (Interpolação):**
   - **Descrição:** Renderiza dados na interface.
   - **Exemplo:**
     ```html
     <span>{{ message }}</span>
     ```
     ```javascript
     data() {
       return {
         message: 'Olá, Vue.js!'
       };
     }
     ```

2. **v-bind: (ligação de atributo):**
   - **Descrição:** Vincula um atributo HTML a uma expressão Vue.
   - **Exemplo:**
     ```html
     <img v-bind:src="imageURL" alt="Imagem">
     ```
     ```javascript
     data() {
       return {
         imageURL: 'caminho/para/imagem.jpg'
       };
     }
     ```

3. **v-model:**
   - **Descrição:** Cria uma ligação bidirecional entre um input e uma variável.
   - **Exemplo:**
     ```html
     <input v-model="username" placeholder="Digite seu nome de usuário">
     ```
     ```javascript
     data() {
       return {
         username: ''
       };
     }
     ```

4. **v-for:**
   - **Descrição:** Renderiza uma lista de elementos com base em uma matriz ou objeto.
   - **Exemplo:**
     ```html
     <ul>
       <li v-for="item in items">{{ item.name }}</li>
     </ul>
     ```
     ```javascript
     data() {
       return {
         items: [
           { id: 1, name: 'Item 1' },
           { id: 2, name: 'Item 2' },
           // ...
         ]
       };
     }
     ```

5. **v-if, v-else-if, v-else:**
   - **Descrição:** Controla a exibição condicional de elementos.
   - **Exemplo:**
     ```html
     <div v-if="isLogged">Usuário Logado</div>
     <div v-else>Faça login</div>
     ```
     ```javascript
     data() {
       return {
         isLogged: true
       };
     }
     ```

6. **v-on: (ou @):**
   - **Descrição:** Adiciona manipuladores de eventos.
   - **Exemplo:**
     ```html
     <button v-on:click="onClick">Clique em mim</button>
     ```
     ```javascript
     methods: {
       onClick() {
         alert('Botão clicado!');
       }
     }
     ```

7. **v-show:**
   - **Descrição:** Alterna a visibilidade de um elemento.
   - **Exemplo:**
     ```html
     <p v-show="isVisible">Este parágrafo é visível</p>
     ```
     ```javascript
     data() {
       return {
         isVisible: true
       };
     }
     ```

8. **v-once:**
   - **Descrição:** Renderiza o elemento apenas uma vez.
   - **Exemplo:**
     ```html
     <p v-once>{{ message }}</p>
     ```
     ```javascript
     data() {
       return {
         message: 'Renderizado apenas uma vez'
       };
     }
     ```

9. **v-pre:**
   - **Descrição:** Ignora a compilação deste elemento e todos os seus descendentes.
   - **Exemplo:**
     ```html
     <span v-pre>{{ message }}</span>
     ```
     ```javascript
     data() {
       return {
         message: 'Este texto será renderizado sem compilação'
       };
     }
     ```

10. **v-cloak:**
    - **Descrição:** Mantém o elemento e seu conteúdo ocultos até que Vue.js compile com sucesso.
    - **Exemplo:**
      ```html
      <div v-cloak>{{ message }}</div>
      ```
      ```javascript
      data() {
        return {
          message: 'Este texto será visível após a compilação do Vue.js'
        };
      }
      ```

11. **v-bind:class:**
    - **Descrição:** Vincula dinamicamente classes CSS a um elemento.
    - **Exemplo:**
      ```html
      <div v-bind:class="{ active: isActive, 'text-danger': hasError }">Classe dinâmica</div>
      ```
      ```javascript
      data() {
        return {
          isActive: true,
          hasError: false
        };
      }
      ```

12. **v-bind:style:**
    - **Descrição:** Vincula dinamicamente estilos CSS a um elemento.
    - **Exemplo:**
      ```html
      <div v-bind:style="{ color: textColor, fontSize: textSize + 'px' }">Estilo dinâmico</div>
      ```
      ```javascript
      data() {
        return {
          textColor: 'red',
          textSize: 16
        };
      }
      ```

13. **computed:**
    - **Descrição:** Calcula propriedades com base em dados reativos.
    - **Exemplo:**
      ```html
      <p>{{ reversedMessage }}</p>
      ```
      ```javascript
      computed: {
        reversedMessage() {
          return this.message.split('').reverse().join('');
        }
      },
      data() {
        return {
          message: 'Vue.js é incrível!'
        };
      }
      ```

14. **watch:**
    - **Descrição:** Observa mudanças em dados e executa ações correspondentes.
    - **Exemplo:**
      ```javascript
      watch: {
        username(newVal, oldVal) {
          console.log(`Novo valor: ${newVal}, Valor antigo: ${oldVal}`);
        }
      },
      data() {
        return {
          username: ''
        };
      }
      ```

15. **methods:**
    - **Descrição:** Define métodos personalizados.
    - **Exemplo:**
      ```html
      <button v-on:click="sayHello">Dizer Olá</button>
      ```
      ```javascript
      methods: {
        sayHello() {
          alert('Olá!');
        }
      }
      ```

16. **filters:**
    - **Descrição:** Aplica formatação de texto.
    - **Exemplo:**
      ```html
      <p>{{ message | capitalize }}</p>
      ```
      ```javascript
      filters: {
        capitalize(value) {
          if (!value) return '';
          return value.charAt(0).toUpperCase() + value.slice(1);
        }
      },
      data() {
        return {
          message: 'vue.js é poderoso!'
        };
      }
      ```

17. **props:**
    - **Descrição:** Permite a passagem de dados de pai para filho (props).
    - **Exemplo:**
      ```html
      <!-- Componente filho -->
      <child-component v-bind:

        prop-name="parentData"></child-component>
      ```
      ```javascript
      // Componente filho
      props: ['propName'],
      ```

18. **emit:**
    - **Descrição:** Emite eventos personalizados do componente filho para o componente pai.
    - **Exemplo:**
      ```html
      <!-- Componente filho -->
      <button v-on:click="emitEvent">Clique em mim</button>
      ```
      ```javascript
      // Componente filho
      methods: {
        emitEvent() {
          this.$emit('custom-event', eventData);
        }
      }
      ```

19. **$refs:**
    - **Descrição:** Acesse diretamente elementos ou componentes no DOM.
    - **Exemplo:**
      ```html
      <input ref="usernameInput" />
      ```
      ```javascript
      mounted() {
        this.$refs.usernameInput.focus();
      }
      ```

20. **Lifecycle Hooks:**
    - **Descrição:** Métodos específicos do ciclo de vida do componente.
    - **Exemplo:**
      ```javascript
      created() {
        console.log('Componente criado');
      },
      mounted() {
        console.log('Componente montado');
      },
      beforeDestroy() {
        console.log('Componente prestes a ser destruído');
      }
      ```

Estes são apenas exemplos básicos para ilustrar cada conceito. Vue.js oferece muito mais funcionalidades e opções avançadas para o desenvolvimento de aplicativos web interativos.