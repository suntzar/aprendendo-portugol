# **Aula Completa de Portugol: Do Básico ao Avançado**

#### **Introdução: O que é e por que usar o Portugol?**

O **Portugol** não é uma linguagem de programação usada para criar aplicativos que você usa no dia a dia (como Instagram ou jogos). Ele é uma **pseudolinguagem**, o que significa que é uma forma de escrever algoritmos (uma sequência de passos para resolver um problema) em português estruturado.

**Analogia:** Pense no Portugol como a "rodinha de apoio" da bicicleta da programação. Antes de sair pedalando em uma bicicleta profissional (como Python, Java, ou C++), você aprende o equilíbrio, a direção e a pedalar com a segurança das rodinhas. O Portugol te ensina a **lógica de programação**, que é o conceito mais importante e universal, sem que você se preocupe com regras complexas e detalhes técnicos de uma linguagem "de verdade".

**Ferramenta que usaremos:** **Portugol Studio**. É um ambiente de desenvolvimento gratuito, excelente para iniciantes, que te ajuda a escrever, testar e visualizar o que seu código está fazendo. Recomendo fortemente que você o baixe e vá testando os exemplos.

---

### **Capítulo 1: A Estrutura Básica e o Primeiro Programa ("Alô, Mundo!")**

Todo programa em Portugol tem uma estrutura mínima. É como o esqueleto do nosso robô.

```portugol
programa {
    funcao inicio() {
        // O código que será executado começa aqui

    }
}
```

*   `programa { ... }`: Delimita o início e o fim do seu programa inteiro.
*   `funcao inicio() { ... }`: É a função principal. A execução do seu código sempre começa aqui. Pense nela como o botão "Ligar" do nosso robô.

**Nosso primeiro comando: `escreva()`**
O comando `escreva()` serve para mostrar uma mensagem na tela (no console).

**Exemplo: O "Alô, Mundo!"**

```portugol
programa {
    funcao inicio() {
        // A linha abaixo vai exibir a mensagem "Alô, Mundo!" na tela.
        escreva("Alô, Mundo!") 
    }
}
```

**Análise Detalhada:**
1.  O programa começa.
2.  Ele entra na `funcao inicio()`.
3.  Ele lê a linha `escreva("Alô, Mundo!")`.
4.  A função `escreva()` pega o texto que está entre aspas duplas (`"`) e o exibe na tela de saída do programa.

---

### **Capítulo 2: Guardando Informações - Variáveis e Tipos de Dados**

Para um programa ser útil, ele precisa guardar informações (números, textos, etc.). Para isso, usamos **variáveis**.

**Analogia:** Uma variável é como uma **caixa etiquetada** na memória do computador. Você dá um nome à etiqueta (o nome da variável) e guarda algo dentro dela. O tipo de coisa que você pode guardar depende do "tipo" da caixa.

**Como declarar uma variável:**
`tipo_da_variavel nome_da_variavel`

**Os Principais Tipos de Dados (Tipos de Caixas):**

1.  **`inteiro`**: Para números inteiros, sem casas decimais. (Ex: 10, -5, 0, 999)
2.  **`real`**: Para números com casas decimais. (Ex: 2.5, -0.75, 3.14159)
3.  **`caractere`**: Para um único símbolo, letra ou número, entre aspas simples. (Ex: 'A', 'b', '7', '$')
4.  **`cadeia`**: Para textos, uma sequência de caracteres, entre aspas duplas. (Ex: "João da Silva", "Meu primeiro programa")
5.  **`logico`**: Para guardar apenas dois valores possíveis: `verdadeiro` ou `falso`.

**Exemplo Prático com Variáveis:**

```portugol
programa {
    funcao inicio() {
        // 1. Declarando as variáveis (criando as caixas)
        cadeia nome_aluno
        inteiro idade
        real nota_final
        logico esta_aprovado

        // 2. Atribuindo valores às variáveis (guardando coisas nas caixas)
        nome_aluno = "Maria"
        idade = 17
        nota_final = 8.5
        esta_aprovado = verdadeiro

        // 3. Usando as variáveis para exibir informações
        escreva("Nome do Aluno: ", nome_aluno, "\n") // "\n" serve para pular uma linha
        escreva("Idade: ", idade, " anos\n")
        escreva("Nota Final: ", nota_final, "\n")
        escreva("Está Aprovado? ", esta_aprovado, "\n")
    }
}
```

**Constantes:** Se você tem um valor que NUNCA vai mudar (como o valor de PI), você pode declará-lo como uma constante.
`constante real PI = 3.14159`

---

### **Capítulo 3: Interagindo com o Usuário - Entrada de Dados**

Um programa fica muito mais interessante quando ele pode receber informações do usuário. Para isso, usamos o comando `leia()`.

**Como funciona o `leia()`:**
Ele pausa o programa e fica esperando o usuário digitar algo e apertar "Enter". O que o usuário digitar será guardado na variável que você indicar.

**Exemplo: Um programa de cadastro simples**

```portugol
programa {
    funcao inicio() {
        // Declara as variáveis que vão guardar as respostas do usuário
        cadeia nome_usuario
        inteiro idade_usuario

        // Pede o nome para o usuário
        escreva("Olá! Por favor, digite o seu nome: ")
        leia(nome_usuario) // O programa para aqui e espera o usuário digitar o nome

        // Pede a idade para o usuário
        escreva("Agora, digite a sua idade: ")
        leia(idade_usuario) // O programa para aqui e espera o usuário digitar a idade

        // Exibe uma mensagem personalizada de volta
        escreva("\n--- Ficha de Cadastro ---\n")
        escreva("Nome digitado: ", nome_usuario, "\n")
        escreva("Idade digitada: ", idade_usuario, " anos.\n")
        escreva("Seja bem-vindo(a), ", nome_usuario, "!")
    }
}
```

**Análise Detalhada:**
1.  O programa exibe a mensagem "Olá! ...".
2.  O `leia(nome_usuario)` é executado. O cursor fica piscando, esperando.
3.  Você digita "Carlos" e aperta Enter. A palavra "Carlos" é armazenada na variável `nome_usuario`.
4.  O mesmo processo se repete para a idade.
5.  No final, o programa usa os valores que você digitou (e que estão guardados nas variáveis) para montar uma frase de resposta.

---

### **Capítulo 4: Fazendo Contas e Comparações - Operadores**

Os operadores são os símbolos que usamos para realizar operações matemáticas, comparações e lógicas.

#### **4.1. Operadores Aritméticos**

São os símbolos matemáticos que você já conhece.

| Operador | Descrição          | Exemplo (`a=10`, `b=3`) | Resultado |
| :------- | :----------------- | :---------------------- | :-------- |
| `+`      | Soma               | `a + b`                 | 13        |
| `-`      | Subtração          | `a - b`                 | 7         |
| `*`      | Multiplicação      | `a * b`                 | 30        |
| `/`      | Divisão            | `a / b`                 | 3.333...  |
| `%`      | Módulo (Resto)     | `a % b`                 | 1         |

**Exemplo: Calculadora de Média**

```portugol
programa {
    funcao inicio() {
        real nota1, nota2, nota3, media

        escreva("Digite a primeira nota: ")
        leia(nota1)

        escreva("Digite a segunda nota: ")
        leia(nota2)

        escreva("Digite a terceira nota: ")
        leia(nota3)

        media = (nota1 + nota2 + nota3) / 3.0 // Usamos parênteses para garantir a ordem da operação

        escreva("\nA média final do aluno é: ", media)
    }
}
```

#### **4.2. Operadores Relacionais**

São usados para comparar dois valores. O resultado de uma comparação é sempre um valor **lógico** (`verdadeiro` ou `falso`).

| Operador | Descrição            | Exemplo (`a=10`, `b=5`) | Resultado   |
| :------- | :------------------- | :---------------------- | :---------- |
| `==`     | Igual a              | `a == 10`               | `verdadeiro`|
| `!=`     | Diferente de         | `a != b`                | `verdadeiro`|
| `>`      | Maior que            | `a > b`                 | `verdadeiro`|
| `<`      | Menor que            | `a < b`                 | `falso`     |
| `>=`     | Maior ou igual a     | `b >= 5`                | `verdadeiro`|
| `<=`     | Menor ou igual a     | `a <= b`                | `falso`     |

#### **4.3. Operadores Lógicos**

São usados para combinar múltiplas condições (múltiplas expressões lógicas).

| Operador | Nome Lógico | Descrição                                        | Exemplo (`a=V`, `b=F`) | Resultado |
| :------- | :---------- | :----------------------------------------------- | :---------------------- | :-------- |
| `e`      | E (AND)     | Retorna `verdadeiro` somente se AMBAS as condições forem verdadeiras. | `a e b`                 | `falso`   |
| `ou`     | OU (OR)     | Retorna `verdadeiro` se PELO MENOS UMA das condições for verdadeira. | `a ou b`                | `verdadeiro`|
| `nao`    | NÃO (NOT)   | Inverte o valor lógico. O que é `verdadeiro` vira `falso`, e vice-versa. | `nao b`                 | `verdadeiro`|

---

### **Capítulo 5: Tomando Decisões - Estruturas Condicionais**

É aqui que nossos programas começam a ficar "inteligentes". Eles podem tomar caminhos diferentes dependendo de certas condições.

#### **5.1. `se` / `senao` (if / else)**

É a estrutura de decisão mais fundamental. "SE (if) uma condição for verdadeira, faça isso. SENÃO (else), faça aquilo."

**Estrutura:**

```portugol
se (condicao) {
    // Bloco de código a ser executado se a condição for VERDADEIRA
} senao {
    // Bloco de código a ser executado se a condição for FALSA
}
```

**Exemplo: Verificador de Média**

```portugol
programa {
    funcao inicio() {
        real media
        escreva("Digite a média do aluno: ")
        leia(media)

        se (media >= 7.0) {
            escreva("Parabéns! Aluno APROVADO!")
        } senao {
            escreva("Que pena! Aluno REPROVADO.")
        }
    }
}
```

**Condicionais Aninhadas (`senao se`)**

E se tivermos mais de duas possibilidades (Aprovado, Recuperação, Reprovado)?

```portugol
se (media >= 7.0) {
    escreva("APROVADO")
} senao se (media >= 5.0 e media < 7.0) { // Duas condições combinadas com 'e'
    escreva("RECUPERAÇÃO")
} senao {
    escreva("REPROVADO")
}
```

#### **5.2. `caso` / `pare` (switch / case)**

Útil quando você precisa testar uma ÚNICA variável contra vários valores possíveis. É mais limpo que usar vários `senao se`.

**Estrutura:**

```portugol
escolha (variavel) {
    caso valor1:
        // Código para o valor1
        pare // O 'pare' é ESSENCIAL para sair do 'escolha'
    caso valor2:
        // Código para o valor2
        pare
    caso contrario:
        // Código se nenhum dos casos acima for atendido
        pare
}
```

**Exemplo: Menu de Opções**

```portugol
programa {
    funcao inicio() {
        inteiro opcao
        escreva("--- MENU ---\n")
        escreva("1 - Ver Saldo\n")
        escreva("2 - Fazer Depósito\n")
        escreva("3 - Fazer Saque\n")
        escreva("Digite sua opção: ")
        leia(opcao)

        escolha (opcao) {
            caso 1:
                escreva("Seu saldo é R$ 1000,00")
                pare
            caso 2:
                escreva("Depósito realizado com sucesso.")
                pare
            caso 3:
                escreva("Saque realizado com sucesso.")
                pare
            caso contrario:
                escreva("Opção inválida!")
                pare
        }
    }
}
```

---

### **Capítulo 6: Repetindo Tarefas - Estruturas de Repetição (Laços)**

Laços (ou loops) servem para executar o mesmo bloco de código várias vezes, sem precisar escrevê-lo repetidamente.

#### **6.1. `para` (for)**

Use o `para` quando você **sabe exatamente quantas vezes** quer repetir uma tarefa.

**Estrutura:**
`para (inicialização; condição; incremento)`

```portugol
// Este laço vai contar de 1 até 10
para (inteiro i = 1; i <= 10; i++) { // i++ é o mesmo que i = i + 1
    escreva("Número: ", i, "\n")
}
```
**Análise Detalhada:**
1.  `inteiro i = 1`: Uma variável `i` é criada e começa com o valor 1.
2.  `i <= 10`: A condição é checada. 1 é menor ou igual a 10? Sim. Então o código dentro do laço executa.
3.  `escreva(...)` é executado.
4.  `i++`: A variável `i` é incrementada. Agora `i` vale 2.
5.  O ciclo recomeça do passo 2, até que a condição `i <= 10` se torne falsa.

#### **6.2. `enquanto` (while)**

Use o `enquanto` quando você quer que o laço continue **enquanto uma condição for verdadeira**, mas você não sabe de antemão quantas vezes isso vai acontecer. A condição é testada **antes** de cada execução.

**Exemplo: Senha secreta**

```portugol
programa {
    funcao inicio() {
        cadeia senha_digitada = ""
        constante cadeia SENHA_SECRETA = "1234"

        enquanto (senha_digitada != SENHA_SECRETA) {
            escreva("Digite a senha: ")
            leia(senha_digitada)

            se (senha_digitada != SENHA_SECRETA) {
                escreva("Senha incorreta. Tente novamente.\n")
            }
        }

        escreva("Acesso permitido!")
    }
}
```

#### **6.3. `faca...enquanto` (do...while)**

É muito parecido com o `enquanto`, mas com uma diferença crucial: o bloco de código é executado **pelo menos uma vez**, e a condição só é testada no **final**.

**Exemplo: Menu que sempre aparece uma vez**

```portugol
programa {
    funcao inicio() {
        inteiro opcao

        faca {
            escreva("\n--- MENU ---\n")
            escreva("1 - Jogar de novo\n")
            escreva("2 - Sair\n")
            escreva("Sua escolha: ")
            leia(opcao)
        } enquanto (opcao != 2) // O laço continua enquanto a pessoa não digitar 2

        escreva("Obrigado por jogar!")
    }
}
```

---

### **Capítulo 7: Organizando Dados em Coleções - Vetores e Matrizes**

E se você precisar guardar 50 notas de alunos? Criar `nota1`, `nota2`, ..., `nota50` não é prático. Para isso, usamos coleções.

#### **7.1. Vetores (Arrays de 1 Dimensão)**

Um vetor é uma coleção de variáveis do **mesmo tipo**, acessadas por um índice numérico.

**Analogia:** Pense em um armário com várias gavetas numeradas. O armário é o vetor, e cada gaveta guarda um item.

**Declaração:**
`tipo nome_do_vetor[tamanho]`

**Exemplo: Guardando e calculando a média de 5 notas**

```portugol
programa {
    funcao inicio() {
        real notas[5] // Cria um "armário" com 5 gavetas (índices de 0 a 4)
        real soma = 0.0
        real media

        // Usamos um laço 'para' para preencher o vetor
        para (inteiro i = 0; i < 5; i++) {
            escreva("Digite a nota ", i + 1, ": ")
            leia(notas[i]) // Guarda a nota na "gaveta" de índice 'i'
        }

        escreva("\n--- Calculando a Média ---\n")

        // Usamos outro laço 'para' para somar as notas guardadas
        para (inteiro i = 0; i < 5; i++) {
            soma = soma + notas[i]
        }

        media = soma / 5.0
        escreva("A média da turma é: ", media)
    }
}
```
**Importante:** Na maioria das linguagens, incluindo o Portugol Studio, o primeiro índice de um vetor é **0**. Um vetor de tamanho 5 tem os índices 0, 1, 2, 3 e 4.

#### **7.2. Matrizes (Arrays de 2 Dimensões)**

Uma matriz é como um vetor de vetores. É uma tabela com linhas e colunas.

**Analogia:** Um tabuleiro de xadrez ou uma planilha do Excel.

**Declaração:**
`tipo nome_da_matriz[numero_de_linhas][numero_de_colunas]`

**Exemplo: Preenchendo um tabuleiro 3x3**

```portugol
programa {
    funcao inicio() {
        inteiro tabuleiro[3][3]

        // Para percorrer uma matriz, precisamos de dois laços 'para', um dentro do outro
        para (inteiro linha = 0; linha < 3; linha++) {
            para (inteiro coluna = 0; coluna < 3; coluna++) {
                escreva("Digite o valor para a posição [", linha, "][", coluna, "]: ")
                leia(tabuleiro[linha][coluna])
            }
        }
        
        escreva("\n--- Tabuleiro Preenchido ---\n")

        // Para exibir a matriz, também usamos dois laços
        para (inteiro linha = 0; linha < 3; linha++) {
            para (inteiro coluna = 0; coluna < 3; coluna++) {
                escreva(tabuleiro[linha][coluna], "\t") // "\t" dá um espaço de tabulação
            }
            escreva("\n") // Pula para a próxima linha ao final de cada linha da matriz
        }
    }
}
```

---

### **Capítulo 8: Quebrando o Problema em Partes - Funções e Procedimentos**

À medida que os programas crescem, colocar todo o código dentro da `funcao inicio()` se torna confuso. A solução é quebrar o problema em pedaços menores e reutilizáveis, usando **funções** e **procedimentos**.

*   **Procedimento**: Um bloco de código que realiza uma tarefa, mas **não retorna um valor**.
*   **Função**: Um bloco de código que realiza uma tarefa e **retorna um valor** ao final.

**Exemplo: Uma Calculadora Modular**

```portugol
programa {

    // PROCEDIMENTO para mostrar o menu (não retorna nada, só exibe)
    procedimento mostrar_menu() {
        escreva("\n--- CALCULADORA ---\n")
        escreva("1 - Somar\n")
        escreva("2 - Subtrair\n")
        escreva("0 - Sair\n")
        escreva("Escolha uma opção: ")
    }

    // FUNÇÃO para somar (recebe dois números e RETORNA o resultado)
    funcao real somar(real n1, real n2) {
        real resultado = n1 + n2
        retorne resultado
    }
    
    // FUNÇÃO para subtrair
    funcao real subtrair(real n1, real n2) {
        retorne n1 - n2 // Forma mais curta de retornar
    }

    // A execução principal agora é mais limpa e organizada
    funcao inicio() {
        inteiro opcao = -1
        real num1, num2, resultado_operacao

        enquanto (opcao != 0) {
            mostrar_menu() // Chama o procedimento para exibir o menu
            leia(opcao)

            se (opcao == 1 ou opcao == 2) {
                escreva("Digite o primeiro número: ")
                leia(num1)
                escreva("Digite o segundo número: ")
                leia(num2)

                se (opcao == 1) {
                    resultado_operacao = somar(num1, num2) // Chama a função e guarda o retorno
                    escreva("O resultado da soma é: ", resultado_operacao, "\n")
                } senao se (opcao == 2) {
                    resultado_operacao = subtrair(num1, num2)
                    escreva("O resultado da subtração é: ", resultado_operacao, "\n")
                }
            } senao se (opcao != 0) {
                 escreva("Opção inválida!\n")
            }
        }
        escreva("Fim do programa.")
    }
}
```

---

### **Conclusão e Próximos Passos**

Parabéns! Você percorreu uma jornada completa pela lógica de programação usando Portugol. Você aprendeu a:

*   Escrever e ler dados (`escreva`, `leia`).
*   Armazenar informações (`variáveis`, `tipos de dados`).
*   Realizar cálculos e comparações (`operadores`).
*   Fazer seu programa tomar decisões (`se`, `caso`).
*   Repetir tarefas de forma eficiente (`para`, `enquanto`, `faca...enquanto`).
*   Organizar grandes volumes de dados (`vetores`, `matrizes`).
*   Estruturar seu código de forma limpa e reutilizável (`funções`, `procedimentos`).

Estes são os **pilares fundamentais de 99% das linguagens de programação**. O que muda de uma para outra é a sintaxe (a forma de escrever), mas a lógica que você aprendeu aqui é universal.

**Seu próximo passo?**
1.  **Pratique!** Tente criar pequenos programas: uma tabuada, um jogo de adivinhação, um sistema de cadastro de livros.
2.  **Migre para uma linguagem de programação "real".** Minha sugestão seria **Python**, pois sua sintaxe é muito limpa e próxima da leitura humana, tornando a transição do Portugol muito suave. Você vai ver que um `se` em Portugol é um `if` em Python, um `para` é um `for`, e assim por diante. A lógica é a mesma!

Lembre-se: programar é resolver problemas. A linguagem é apenas a ferramenta. Você acabou de aprender a manusear seu primeiro e mais importante conjunto de ferramentas: a lógica.
