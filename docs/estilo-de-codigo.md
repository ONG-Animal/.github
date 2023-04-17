# Guia de Estilo de Código

Este guia de estilo de código é destinado a desenvolvedores que utilizam as tecnologias Node, Express, Prisma, React e TypeScript para criar aplicativos web full-stack. O objetivo é estabelecer convenções e padrões para tornar o código mais legível, consistente e fácil de manter. Essas diretrizes seguem os princípios de código limpo, que visam escrever código legível, consistente e fácil de manter. Algumas dessas diretrizes incluem:

- Usar nomes significativos e descritivos para variáveis, funções e classes.
- Limitar o tamanho das funções e dos arquivos.
- Usar espaçamento consistente para melhorar a legibilidade do código.
- Manter a consistência na organização do código, como a ordem das declarações e a indentação.
- Lidar com erros de forma apropriada, como tratar exceções e retornar códigos de erro adequados.

Além disso, essas diretrizes também se baseiam nos princípios DRY (*Don't Repeat Yourself*) e YAGNI (*You Aren't Gonna Need It*).

O princípio DRY incentiva a evitar a duplicação de código, mantendo apenas uma única fonte de verdade para cada parte do código. Isso é abordado em várias diretrizes, como:

- Usar funções e módulos para compartilhar código entre diferentes partes do aplicativo.
- Usar configurações centralizadas para evitar a duplicação de informações, como a conexão com o banco de dados.
- Usar variáveis para armazenar valores que são usados mais de uma vez no código.

O princípio YAGNI incentiva a evitar a adição de funcionalidades ou código desnecessários. Isso é abordado em várias diretrizes, como:

- Escrever apenas o código necessário para atender aos requisitos do projeto.
- Evitar a criação de código especulativo ou de recursos que ainda não são necessários.
- Priorizar a simplicidade do código em vez de funcionalidades excessivamente complexas ou detalhadas.
- Seguir esses princípios ajuda a manter o código limpo, conciso e eficiente, além de reduzir a complexidade e os possíveis erros do código.

<details>
  <summary>Convenções de Nomenclatura</summary> 
  
  ## Nomes de variáveis, funções e classes devem ser escritos em camelCase, começando com letra minúscula.
  
  Exemplo: 
  
  ```typescript
  const minhaVariavel = 42

  function minhaFuncao() {
    // ...
   }

  class minhaClasse {
    // ...
  }     
  ```
  
  ## Nomes de constantes devem ser escritos em UPPERCASE, separando as palavras com underline.
  
  Exemplo: 
  
  ```typescript
    const MINHA_CONSTANTE = 3.1415
  ```
  
  ## Nomes de tipos devem ser escritos em PascalCase.
  
  Exemplo: 
  
  ```typescript
    type MeuTipo = {
      // ...
  }
 ```
  
  ## Nomes de arquivos devem ser escritos em kebab-case.
  
  Exemplo: 
  
  ```css
    meu-arquivo.ts
 ```
  
</details>

<details>
  <summary>Padrões de código</summary>  
  
  
  ## Use declarações de importação e exportação padrão.
  
  Exemplo: 
  
  ```typescript
    // meu-arquivo.ts
      export function minhaFuncao() {
        // ...
      }
    }
 ```
  
  ```typescript
    // outro-arquivo.ts
    import { minhaFuncao } from "./meu-arquivo"
   ```
  
  
  ## Use a sintaxe de objeto literal para criar objetos.
  
  Exemplo: 
  
  ```typescript
      const meuObjeto = {
          propriedade1: "valor1",
          propriedade2: "valor2",
      }
 ```
  
  
  ## Use a sintaxe de array literal para criar arrays.
  
  Exemplo: 
  
  ```typescript
     const meuArray = ["valor1", "valor2"]
 ```
  
  ## Use a sintaxe de template string para interpolar strings.
  
  Exemplo: 
  
  ```typescript
      const meuNumero = 22
      console.log(`O número é ${meuNumero}.`)
 ```
  
  ## Use o operador spread (...) para mesclar objetos e arrays.
  
  Exemplo: 
  
  ```typescript
      const objeto1 = { propriedade1: "valor1" }
      const objeto2 = { propriedade2: "valor2" }
      const meuObjeto = { ...objeto1, ...objeto2 }
      console.log(meuObjeto) // { propriedade1: "valor1", propriedade2: "valor2" }

      const array1 = ["valor1"]
      const array2 = ["valor2"]
      const meuArray = [...array1, ...array2]
      console.log(meuArray) // ["valor1", "valor2"]
 ```
  
  ## Use o padrão de projeto de módulo para estruturar o código.
  
  Exemplo: 
  
  ```css
        src/
          components/
            meu-componente/
              index.tsx
              meu-componente.tsx
          models/
            meu-modelo.ts
          services/
            meu-servico.ts
          utils/
            minha-util.ts
          app.tsx
 ```
  
  ## Use o padrão de código assíncrono para trabalhar com chamadas assíncronas.
  
  ### Use a palavra-chave "async" para definir funções assíncronas.
  
  Exemplo: 
  
  ```typescript
      async function minhaFuncaoAssincrona() {
        // ...
      }
 ```
  
  ### Use a palavra-chave "await" para esperar que uma chamada assíncrona seja concluída.
  
  Exemplo: 
  
  ```typescript
      async function minhaFuncaoAssincrona() {
        const resultado = await fetch("https://exemplo.com/api/dados")
        const json = await resultado.json()
        console.log(json)
      }
 ```
  
  ### Use o tratamento de erro para lidar com exceções em chamadas assíncronas.
  
  Exemplo: 
  
  ```typescript
      async function minhaFuncaoAssincrona() {
        try {
          const resultado = await fetch("https://exemplo.com/api/dados")
          const json = await resultado.json()
          console.log(json)
        } catch (erro) {
          console.error(erro)
        } finally {
          console.log("a promessa acabou!")
          }
      }
 ```
  
  ### Use a biblioteca "promisify" do Node para transformar funções que usam callbacks em funções que retornam promessas.
  
  Exemplo: 
  
  ```typescript
        import { promisify } from "util"
        import { readFile } from "fs"

        const leituraDoArquivo = promisify(readFile)

        async function meuPrograma() {
          try {
            const conteudo = await leituraDoArquivo("meu-arquivo.txt", "utf8")
            console.log(conteudo)
          } catch (erro) {
            console.error(erro)
          }
        }
 ```
  
  ### Use a biblioteca "async" do Node para executar tarefas assíncronas em paralelo.
  
  Exemplo: 
  
  ```typescript
      import { parallel } from "async"

      function tarefa1(callback) {
        // ...
      }

      function tarefa2(callback) {
        // ...
      }

      function tarefa3(callback) {
        // ...
      }

      parallel([tarefa1, tarefa2, tarefa3], (erro, resultados) => {
        if (erro) {
          console.error(erro)
        } else {
          console.log(resultados)
        }
      })
 ```
  
</details>
