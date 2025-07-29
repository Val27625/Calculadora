# *Calculadora*
Este repositório apresenta uma calculadora Python simples que executa operações básicas (adição, subtração, multiplicação e divisão), acompanhada de um shell script (calculadora.sh) para facilitar sua execução.
---

Como Executar o Script

Para executar esta calculadora, você precisará ter o **Python 3** instalado em seu sistema.

1.  **Clone o repositório:**
 ```bash
git clone https://github.com/Val27625/Calculadora.git
cd Calculadora
```
    

2.  **Execute o script Python diretamente:**
   ```bash
   python calculadora.py
   ```

3.  **Executar via script Shell (Opcional):**
    Para maior conveniência, um script shell (`.sh`) foi fornecido.
    * **Dê permissão de execução ao script:**
        ```bash
        chmod +x executar_calculadora.sh
        ```
    * **Execute o script:**
        ```bash
        ./executar_calculadora.sh
        ```
    Este script irá iniciar a calculadora e pausar o terminal após a execução.

---

## Explicação do Código Python (`calculadora.py`)

O script `calculadora.py` é uma calculadora de linha de comando que realiza operações básicas (soma, subtração, multiplicação, divisão).

### Estrutura do Código:

* **Cores ANSI (`c`):** Uma tupla de strings que contém códigos de escape ANSI para colorir o texto no terminal, melhorando a experiência do usuário.
    * `c[0]`: Sem cor (reset).
    * `c[1]`: Vermelho (para mensagens de erro).
    * `c[2]`: Verde.
    * `c[3]`: Amarelo (para resultados).
    * `c[4]`: Azul.
    * `c[5]`: Roxo (para prompts de entrada).

* **`isFloat(msg)` função:**
    * **Propósito:** Garante que a entrada do usuário seja um número decimal (float) válido.
    * **Funcionamento:** Solicita uma entrada (`msg`) repetidamente até que um `float` válido seja fornecido. Utiliza um bloco `try-except` para capturar `ValueError` ou `TypeError` caso a entrada não possa ser convertida para um número. Em caso de erro, exibe uma mensagem em vermelho.

* **`verif_op(msg)` função:**
    * **Propósito:** Valida o operador matemático inserido pelo usuário.
    * **Funcionamento:** Apresenta um menu de opções de operadores (`+`, `-`, `*`, `/`) e solicita a escolha. Repete a solicitação até que um operador válido seja digitado. Em caso de entrada inválida, exibe uma mensagem de erro em vermelho.

* **`operacao(operador, x, y)` função:**
    * **Propósito:** Realiza a operação matemática selecionada e formata o resultado.
    * **Funcionamento:** Recebe o `operador` e os dois números (`x` e `y`). Compara o `operador` e executa a operação correspondente.
    * **Tratamento de Erro:** Inclui uma verificação para **divisão por zero**, exibindo uma mensagem de erro em vermelho se `y` for `0` na operação de divisão.
    * **Saída:** Retorna uma string formatada com o cálculo e o resultado em amarelo.

* **Fluxo Principal do Programa:**
    * O programa executa em um loop `while` que continua enquanto o usuário não digitar 'N' (ou 'n') para sair.
    * Dentro do loop, ele primeiro solicita ao usuário para escolher uma operação usando `verif_op`.
    * Em seguida, pede os dois números (`x` e `y`) para a operação, utilizando `isFloat` para validar as entradas.
    * Chama a função `operacao` para calcular e exibir o resultado.
    * Após cada cálculo, pergunta ao usuário se deseja continuar (`S/N`).
    * Ao sair do loop, exibe uma mensagem de despedida.

### Melhorias Implementadas:
* Passagem de `x` e `y` como argumentos para a função `operacao` para melhor encapsulamento.
* Tratamento de `ZeroDivisionError` dentro da função `operacao`.
* Correção do símbolo da multiplicação no menu de opções.
* Normalização da entrada `finalizar` para maiúscula.
* Remoção do espaço extra no final dos prompts de `isFloat`.
* Remoção do operador '0' de `verif_op` por não ter função definida.



 
