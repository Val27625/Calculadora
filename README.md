# **Calculadora**
Este repositório apresenta uma calculadora Python simples que executa operações básicas (adição, subtração, multiplicação e divisão), acompanhada de um shell script (calculadora.sh) para facilitar sua execução.

# **Executar**

1- Clonar o Repositório - Clone este repositório para o seu computador:

2- Depois de clonar, navegue até o diretório, aonde o repositório foi salvo:

```bash
cd caminho/para/seu/repositório
```

3- Crie e edite o arquivo calculadora.sh - Crie o arquivo shell script com o seguinte comando:

```bash
 nano calculadora.sh
```

Abrirá o editor de texto nano. Dentro do arquivo, cole o código:

```bash
#!/bin/bash
#Script para executar a calculadora Python
Python3 calculadora.py
```

 4 - Para tornar o Script Executável, você precisará alterar as permissões. Execute o seguinte comando:

```bash
chmod +x calculadora.sh
```
Isso garante que você possa executar o arquivo como um script.


5 - Definir Permissões de Acesso Para garantir que apenas o proprietário do arquivo tenha permissão de escrita e outros usuários tenham apenas permissão de leitura, use:

```bash
chmod 744 calculadora.sh
```

6 - Agora, você pode rodar o script para executar a calculadora Python com o seguinte comando:

```bash
./calculadora.sh
```

>> Requisitos Python 3.10 ou superior
Terminal (Linux/Mac) ou Git Bash (sem Windows)



 
