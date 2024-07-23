### Guia Rápido de C# para Iniciantes

- **Introdução ao C#:**
  - Linguagem de programação orientada a objetos desenvolvida pela Microsoft.
  - Variante do C, usada amplamente em diversos domínios do desenvolvimento de software.
  - Facilitada a transição para quem conhece C, C++, JavaScript ou Java.

- **Conceitos Básicos de Sintaxe:**
  - **Sintaxe:** Estrutura precisa para que o computador compreenda o código.
  - **Erros de Sintaxe:** Comandos incorretos, como vírgulas ou ponto e vírgulas ausentes, geram erros.
  - **Referências:** Disponíveis online para consulta e exemplos de código.

- **Primeiro Script: HelloWorld:**
  - **Exemplo:** 
    ```csharp
    
    public class HelloWorld
    {
        void Start()
        {
            Debug.Log("Hello World");
        }
    }
    ```
  - **Saída:** Mensagem "Hello World" no console do Unity.

- **Ferramentas de Depuração:**
  - **Debug.Log:** Exibe mensagens no console.
  - **Debug.LogWarning:** Exibe avisos.
  - **Debug.LogError:** Exibe erros.

- **Exemplos de Uso de Debug.Log:**
  - Combinação de strings com variáveis:
    ```csharp
    string name = "Player";
    Debug.Log("Hello " + name);
    ```
  - Uso de métodos de matemática:
    ```csharp
    float number = 3.14f;
    Debug.Log(Mathf.Floor(number));
    ```

- **Importância da Sensibilidade a Maiúsculas:**
  - **Case-Sensitive:** Uso correto de maiúsculas e minúsculas é crucial.
  - **Exemplo:**
    ```csharp
    Debug.Log("Correct");
    debug.log("Incorrect");
    ```

- **Uso de Pontos e Vírgulas:**
  - **Semicolon:** Cada instrução termina com ponto e vírgula.
  - Pode ter múltiplas instruções por linha, mas geralmente se usa uma por linha para melhor legibilidade.

- **Comentários no Código:**
  - **Comentários de Linha Única:**
    ```csharp
    // Este é um comentário de linha única
    ```
  - **Comentários de Múltiplas Linhas:**
    ```csharp
    /* Este é um
       comentário de múltiplas linhas */
    ```
  - **Propósito:** Melhorar a legibilidade e compreensão do código para humanos.




### Guia Rápido de C# - Variáveis e Tipos de Dados

#### O que é uma Variável?
- **Definição:** Uma variável é uma "caixa" que guarda informações na memória do computador.
- **Exemplo:** 
  ```csharp
  int playerHealth = 25;
  ```

#### Regras para Nomeação de Variáveis e Classes
- **Sem espaços:** Nomes não podem conter espaços.
- **Iniciar com letra:** Devem começar com uma letra.
- **Caracteres permitidos:** Podem conter letras, números e underscore (_).
- **Case-sensitive:** Diferenciam maiúsculas de minúsculas.
- **Nome descritivo:** Nomes devem ser descritivos para facilitar a leitura.

#### Convenção de Nomeação
- **Lower Camel Case:** Primeira letra minúscula e cada nova palavra começa com maiúscula.
  - Exemplo: `playerHealth`

#### Tipos de Dados Comuns
- **Inteiros:** Números inteiros (ex: `int` para -10, 0, 12, 3).
- **Ponto Flutuante:** Números com casas decimais (ex: `float` para -1.45f, 0.0f, 45.3f).
- **Booleanos:** Verdadeiro ou falso (ex: `bool` para `true` ou `false`).
- **Strings:** Sequência de caracteres (ex: `string` para "Hello World").

#### Tipos de Dados Comuns no Unity
- **Vector2:** Armazena uma posição X e Y.
- **Vector3:** Armazena uma posição X, Y, e Z.
- **GameObject:** Referência a um objeto do jogo ou prefab.
- **Componentes:** Referência a componentes específicos, como `AudioSource`.

#### Modificadores de Acesso
- **Public:** Acessível fora do escopo atual.
- **Private:** Acessível apenas dentro do escopo atual.
- **Padrão:** Se não especificado, geralmente é privado.

#### Exemplo de Definição de Variáveis
```csharp
public int playerHealth = 25;
private float playerSpeed = 5.5f;
bool isJumping = false;
string playerName = "John Doe";
```

#### Arrays e Listas
- **Arrays:** Armazenam listas pré-definidas de informações relacionadas.
  - Exemplo de criação de array:
    ```csharp
    string[] family = new string[5];
    family[0] = "Homer";
    family[1] = "Marge";
    family[2] = "Bart";
    family[3] = "Lisa";
    family[4] = "Maggie";
    ```
  - Forma abreviada:
    ```csharp
    string[] family = { "Homer", "Marge", "Bart", "Lisa", "Maggie" };
    ```

- **Listas:** Semelhantes a arrays, mas podem crescer e diminuir dinamicamente.
  - Exemplo de criação de lista:
    ```csharp
    List<string> family = new List<string>();
    family.Add("Homer");
    family.Add("Marge");
    family.Add("Bart");
    family.Add("Lisa");
    family.Add("Maggie");
    ```

#### Conversão de Tipos de Dados
- **Exemplo de conversão de string para int:**
  ```csharp
  string strNumber = "42";
  int number = int.Parse(strNumber);
  ```
- **Exemplo de conversão de string para float:**
  ```csharp
  string strFloat = "3.14";
  float number = float.Parse(strFloat);
  ```
- **Exemplo de conversão de int para string:**
  ```csharp
  int score = 100;
  string strScore = score.ToString();
  ```

#### Operações Matemáticas
- **Exemplo de operações com inteiros:**
  ```csharp
  int x = 5;
  int y = 3;
  int result = (x - y) * 12 / 2 + 4; // Result = 16
  ```
- **Exemplo de operações com ponto flutuante:**
  ```csharp
  float a = 10.5f;
  float b = 3.3f;
  float result = a - b; // Result = 7.2
  ```

#### Manipulação de Strings
- **Concatenação de Strings:**
  ```csharp
  string firstName = "John";
  string lastName = "Doe";
  string fullName = firstName + " " + lastName; // Result = "John Doe"
  ```
- **Propriedade de Comprimento:**
  ```csharp
  string name = "Brian";
  int length = name.Length; // Result = 5
  ```
- **Métodos de Manipulação de Strings:**
  - **ToUpper:** Converte para maiúsculas.
    ```csharp
    string upperName = name.ToUpper(); // Result = "BRIAN"
    ```
  - **ToLower:** Converte para minúsculas.
    ```csharp
    string lowerName = name.ToLower(); // Result = "brian"
    ```
  - **Trim:** Remove espaços em branco.
    ```csharp
    string trimmedName = "  Brian  ".Trim(); // Result = "Brian"
    ```
  - **Replace:** Substitui partes da string.
    ```csharp
    string newName = name.Replace("Br", "Jill"); // Result = "Jillian"
    ```


### Guia Rápido de C# - Controle de Fluxo com Condicionais e Laços

#### Ordem de Execução Padrão
- **Sequencial:** Código é executado linha por linha, de cima para baixo.

#### Modificação da Ordem de Execução
- **Ramificação:** Permite alterar a ordem de execução com base em condições.
- **Laços:** Permitem repetir a execução de blocos de código enquanto uma condição é satisfeita.

#### Operadores de Comparação
- **Igual a:** `==`
- **Diferente de:** `!=`
- **Maior que:** `>`
- **Maior ou igual a:** `>=`
- **Menor que:** `<`
- **Menor ou igual a:** `<=`

#### Condicionais: `if`, `else if`, e `else`
- **Estrutura Básica:**
  ```csharp
  if (condição) {
      // Código a ser executado se a condição for verdadeira
  } else if (outraCondição) {
      // Código a ser executado se outraCondição for verdadeira
  } else {
      // Código a ser executado se todas as condições anteriores forem falsas
  }
  ```

- **Exemplo:**
  ```csharp
  int temp = 40;

  if (temp <= 32) {
      Console.WriteLine("Está congelando");
  } else if (temp <= 60) {
      Console.WriteLine("Vista um casaco");
  } else if (temp <= 90) {
      Console.WriteLine("Está quente");
  } else {
      Console.WriteLine("Vista roupa de banho");
  }
  ```

#### Operadores Lógicos: `&&` e `||`
- **E lógico (`&&`):** Avalia como verdadeiro se ambas as condições forem verdadeiras.
- **Ou lógico (`||`):** Avalia como verdadeiro se pelo menos uma das condições for verdadeira.

- **Exemplo:**
  ```csharp
  int temp = 55;
  string weather = "sunny";

  if (temp >= 50 && temp < 65) {
      Console.WriteLine("Vista um suéter");
  }

  if (temp > 90 || weather == "sunny") {
      Console.WriteLine("Vista protetor solar");
  }
  ```

#### `switch` Statement
- **Estrutura Básica:**
  ```csharp
  switch (variável) {
      case valor1:
          // Código a ser executado se variável == valor1
          break;
      case valor2:
          // Código a ser executado se variável == valor2
          break;
      default:
          // Código a ser executado se nenhuma das condições anteriores for verdadeira
          break;
  }
  ```

- **Exemplo:**
  ```csharp
  string weather = "cloudy";

  switch (weather) {
      case "sunny":
          Console.WriteLine("Vista protetor solar");
          break;
      case "rainy":
          Console.WriteLine("Leve um guarda-chuva");
          break;
      default:
          Console.WriteLine("Vista-se adequadamente");
          break;
  }
  ```

#### Laços: `while`, `for`, e `foreach`
- **While Loop:**
  ```csharp
  int lives = 3;

  while (lives > 0) {
      Console.WriteLine("Vidas: " + lives);
      lives--;
  }
  Console.WriteLine("Você está morto");
  ```

- **For Loop:**
  ```csharp
  for (int power = 1; power < 3; power++) {
      Console.WriteLine("Power: " + power);
  }
  Console.WriteLine("Potência completa");
  ```

  - **Com Arrays:**
    ```csharp
    string[] family = { "Homer", "Marge", "Bart", "Lisa", "Maggie" };

    for (int i = 0; i < family.Length; i++) {
        Console.WriteLine(family[i]);
    }
    ```

- **For Each Loop:**
  ```csharp
  List<string> family = new List<string> { "Homer", "Marge", "Bart", "Lisa", "Maggie" };

  foreach (string familyName in family) {
      Console.WriteLine(familyName);
  }
  ```

#### Resumo
- **Condicionais (`if`, `else if`, `else`, `switch`)** permitem executar código baseado em condições lógicas.
- **Laços (`while`, `for`, `foreach`)** permitem repetir a execução de código enquanto uma condição é satisfeita.
- Esses mecanismos são fundamentais para controlar a lógica e o fluxo do programa em C#.



### Guia Rápido de C# - Funções e Classes

#### Funções
- **Definição:** Funções são blocos de código que executam uma tarefa específica e podem receber informações (argumentos) e retornar um resultado.
- **Nomenclatura:** Usamos o estilo Upper Camel Case (Pascal Case) para nomear funções (e.g., `AddTwoNumbers`).

#### Estrutura de uma Função
- **Sintaxe Básica:**
  ```csharp
  [acesso] [tipo de retorno] NomeDaFuncao([tipo argumento1, nome argumento1, tipo argumento2, nome argumento2]) {
      // Corpo da função
  }
  ```

- **Componentes:**
  - **Acesso:** Modificadores como `public`, `private`, `protected`.
  - **Tipo de Retorno:** O tipo de dado que a função retorna (e.g., `int`, `string`, `void`).
  - **Nome da Função:** Nome único da função.
  - **Argumentos:** Lista de parâmetros que a função aceita.

- **Exemplo:**
  ```csharp
  public int AddTwo(int x, int y) {
      int z = x + y;
      return z;
  }
  ```

#### Chamando uma Função
- **Sintaxe:**
  ```csharp
  TipoVariável resultado = NomeDaFuncao(argumento1, argumento2);
  ```

- **Exemplo:**
  ```csharp
  int playerHealth = AddTwo(5, 6);
  Console.WriteLine(playerHealth); // Saída: 11
  ```

#### Benefícios das Funções
- **Modularização:** Dividem problemas em partes menores e gerenciáveis.
- **Reutilização:** Evitam duplicação de código, permitindo reutilizar funções.
- **Abstração:** Escondem detalhes de implementação, permitindo que se concentre no uso da função.

#### Classes
- **Definição:** Classes são contêineres que agrupam variáveis (propriedades) e funções (métodos) relacionadas.
- **Nomenclatura:** Usamos o estilo Upper Camel Case para nomear classes (e.g., `Player`).

#### Estrutura de uma Classe
- **Sintaxe Básica:**
  ```csharp
  [acesso] class NomeDaClasse {
      // Propriedades
      [acesso] tipo NomePropriedade;

      // Métodos
      [acesso] tipoDeRetorno NomeMetodo([tipo argumento]) {
          // Corpo do método
      }
  }
  ```

- **Componentes:**
  - **Acesso:** Modificadores como `public`, `private`, `protected`.
  - **Propriedades:** Variáveis dentro da classe.
  - **Métodos:** Funções dentro da classe.

- **Exemplo de Classe:**
  ```csharp
  public class Player {
      public string Name;
      private int health;

      public void SetHealth(int value) {
          health = value;
      }

      public int GetHealth() {
          return health;
      }
  }
  ```

#### Instanciando e Usando uma Classe
- **Criação de Instância:**
  ```csharp
  Player player1 = new Player();
  ```

- **Uso de Propriedades e Métodos:**
  ```csharp
  player1.Name = "Homer";
  player1.SetHealth(100);
  int currentHealth = player1.GetHealth();
  Console.WriteLine($"{player1.Name} has {currentHealth} health.");
  ```

#### Benefícios das Classes
- **Organização:** Agrupam código relacionado.
- **Reutilização:** Permitem reutilizar código através de instâncias.
- **Abstração e Encapsulamento:** Escondem detalhes de implementação e protegem dados internos.

### Exemplo Completo
Aqui está um exemplo que combina funções e classes:

```csharp
using System;

public class Game {
    public class Player {
        public string Name;
        private int health;

        public void SetHealth(int value) {
            health = value;
        }

        public int GetHealth() {
            return health;
        }

        public void PrintStatus() {
            Console.WriteLine($"{Name} has {health} health.");
        }
    }

    public int AddTwo(int x, int y) {
        return x + y;
    }

    public void Start() {
        Player player1 = new Player();
        player1.Name = "Homer";
        player1.SetHealth(AddTwo(50, 50));
        player1.PrintStatus();
    }
}

class Program {
    static void Main(string[] args) {
        Game game = new Game();
        game.Start();
    }
}
```

### Guia Rápido de Programação em Unity

Unity é um ambiente orientado a eventos, onde frequentemente adicionamos funções às nossas classes para responder a eventos que ocorrem enquanto o jogo está sendo executado. Vamos explorar alguns conceitos específicos do Unity:

#### Ciclo de Vida dos Componentes

1. **Eventos de Inicialização:**
   - **Awake:** Chamado quando o script é carregado, ideal para inicializações que não dependem de outros scripts.
   - **OnEnable:** Chamado quando o GameObject é ativado.
   - **Start:** Chamado na primeira atualização em que o script está ativo, usado para inicializações que dependem de outros scripts.

2. **Eventos de Loop de Jogo:**
   - **Update:** Chamado uma vez por frame, usado para lógica que precisa ser verificada ou atualizada continuamente.
   - **LateUpdate:** Chamado após todos os `Update` terem sido processados, útil para ajustes finais após todas as atualizações.

3. **Eventos de Física:**
   - **FixedUpdate:** Chamado em intervalos fixos, sincronizado com o motor de física, ideal para cálculos físicos.

4. **Eventos de Interação:**
   - **OnCollisionEnter, OnTriggerEnter:** Chamados quando o GameObject colide com outro ou entra em um gatilho, respectivamente.
   - **OnMouseDown, OnMouseUp:** Chamados quando o mouse interage com o GameObject.

#### Manipulação de GameObjects

- **Referência ao GameObject Atual:**
  ```csharp
  gameObject.SetActive(false); // Desativa o GameObject
  Debug.Log(gameObject.name);   // Imprime o nome do GameObject no console
  ```

- **Referência a Outros GameObjects:**
  - **Via Variável Pública:**
    ```csharp
    public GameObject otherObject;
    ```

  - **Via Busca no Cena:**
    ```csharp
    GameObject otherObject = GameObject.Find("ObjectName");
    GameObject taggedObject = GameObject.FindWithTag("ObjectTag");
    ```

#### Manipulação de Componentes

- **Acessar e Modificar Transform:**
  ```csharp
  gameObject.transform.position = new Vector3(1, 2, 3);
  ```

- **Usar `GetComponent`:**
  ```csharp
  Rigidbody rb = gameObject.GetComponent<Rigidbody>();
  rb.useGravity = false;
  ```

- **Variável Pública para Componentes:**
  ```csharp
  public Rigidbody rb;
  ```

#### Instanciação de GameObjects

- **Instanciar Prefabs:**
  ```csharp
  public GameObject prefab;

  void Update() {
      if (Input.GetButtonDown("Fire1")) {
          Vector3 position = transform.position;
          Quaternion rotation = transform.rotation;
          Instantiate(prefab, position, rotation);
      }
  }
  ```

#### Referências e Recursos

- **Documentação do Unity:** [Unity Scripting API](https://docs.unity3d.com/ScriptReference/)
- **Documentação do C#:** [Microsoft C# Documentation](https://docs.microsoft.com/en-us/dotnet/csharp/)
- **Comunidade:** [Fórum do Unity](https://forum.unity.com/), [Stack Overflow](https://stackoverflow.com/)

### Exemplo de Código Completo em Unity

```csharp
using UnityEngine;

public class PlayerController : MonoBehaviour {
    public float moveSpeed = 5f;
    public GameObject projectilePrefab;

    void Start() {
        Debug.Log("Game Started");
    }

    void Update() {
        // Movimento do Jogador
        float moveHorizontal = Input.GetAxis("Horizontal");
        float moveVertical = Input.GetAxis("Vertical");
        Vector3 movement = new Vector3(moveHorizontal, 0, moveVertical);
        transform.Translate(movement * moveSpeed * Time.deltaTime);

        // Disparo de Projetil
        if (Input.GetButtonDown("Fire1")) {
            Vector3 position = transform.position + transform.forward;
            Quaternion rotation = transform.rotation;
            Instantiate(projectilePrefab, position, rotation);
        }
    }

    void OnCollisionEnter(Collision collision) {
        if (collision.gameObject.CompareTag("Enemy")) {
            Debug.Log("Collided with Enemy");
        }
    }
}
```
