# Aqui estão 20 instruções importantes em TypeScript, cada uma acompanhada por um exemplo de código:

## Declaração de Variáveis:
    let nome: string = "João";

## Tipos Básicos:
    let idade: number = 25;
    let ativo: boolean = true;

## Declaração de Funções:
    function saudacao(nome: string): string {
      return "Olá, " + nome + "!";
    }
    
    let mensagem: string = saudacao("Maria");

## Tipos de Arrays:
    let numeros: number[] = [1, 2, 3];
    let palavras: Array<string> = ["maçã", "banana", "laranja"];

## Tipos de Objetos:
    let pessoa: { nome: string; idade: number } = { nome: "Carlos", idade: 30 };

## Enumerações (Enums):
    enum DiaDaSemana {
      Segunda,
      Terca,
      Quarta,
      Quinta,
      Sexta,
      Sabado,
      Domingo
    }
    
    let hoje: DiaDaSemana = DiaDaSemana.Quarta;

## Union Types:
    let nota: number | string;
    nota = 10;
    nota = "A";

## Type Assertion:
    let comprimento: any = "abc";
    let comprimentoString: number = (comprimento as string).length;

## Interfaces:
    interface Usuario {
      nome: string;
      idade: number;
    }
    
    function mostrarUsuario(usuario: Usuario): void {
      console.log(`Nome: ${usuario.nome}, Idade: ${usuario.idade}`);
    }

## Classe:
    class Carro {
      marca: string;
    
      constructor(marca: string) {
        this.marca = marca;
      }
    
      acelerar(): void {
        console.log("Vrum vrum!");
      }
    }
    
    let meuCarro = new Carro("Toyota");
    meuCarro.acelerar();

## Herança:
    class Veiculo {
      cor: string;
    
      constructor(cor: string) {
        this.cor = cor;
      }
    
      buzinar(): void {
        console.log("Beep beep!");
      }
    }
    
    class Bicicleta extends Veiculo {
      pedalar(): void {
        console.log("Pedalando...");
      }
    }
    
    let minhaBicicleta = new Bicicleta("vermelha");
    minhaBicicleta.buzinar();
    minhaBicicleta.pedalar();

## Módulos:
    // Em arquivo modulo.ts
    export function dobrar(numero: number): number {
      return numero * 2;
    }
    
    // Em outro arquivo
    import { dobrar } from "./modulo";
    let resultado: number = dobrar(5);

## Generics:
    function repetir<T>(valor: T, quantidade: number): T[] {
      return new Array(quantidade).fill(valor);
    }
    
    let numerosRepetidos: number[] = repetir(3, 5);

## Decoradores:
    function logarClasse(construtor: Function) {
      console.log(construtor);
    }
    
    @logarClasse
    class ExemploDecorador {
      // ...
    }

## Async/Await:
    function aguardar(ms: number): Promise<void> {
      return new Promise(resolve => setTimeout(resolve, ms));
    }
    
    async function exemploAsync(): Promise<void> {
      console.log("Início");
      await aguardar(2000);
      console.log("Fim");
    }
    
    exemploAsync();

## Tipagem de Parâmetros Rest e Spread:
    function juntarStrings(...partes: string[]): string {
      return partes.join("-");
    }
    
    let resultadoConcatenacao: string = juntarStrings("a", "b", "c");

## Namespace:
    namespace Geometria {
      export const PI = 3.14;
    
      export function calcularCircunferencia(raio: number): number {
        return 2 * PI * raio;
      }
    }
    
    let circunferencia: number = Geometria.calcularCircunferencia(5);

## Ambient Declarations:
    declare var $: any;
    
    $("#meuElemento").hide();

## Nunca (Never):
    function lancarErro(mensagem: string): never {
      throw new Error(mensagem);
    }

## Tipagem de Nulo e Undefined:
    let nomePossivelNulo: string | null | undefined;

Estas são apenas algumas das muitas características e instruções que TypeScript oferece para trazer tipagem estática e outros recursos avançados ao JavaScript.