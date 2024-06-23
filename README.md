# Conversor-de-.Py-para-.Exe
Conversor de arquivo .py para um executável .exe

![Captura de tela 2024-06-23 202150](https://github.com/hfa90/Conversor-de-.Py-para-.Exe/assets/163853542/600d6146-7ccc-4813-af02-48bf2eb65b14)

Este código é um conversor de arquivos Python (.py) para arquivos executáveis (.exe) usando uma interface gráfica simples (GUI) criada com a biblioteca Tkinter. Ele funciona da seguinte maneira:

**Funcionalidades:**

1. **Selecionar arquivo:**
   - Permite ao usuário navegar e escolher um arquivo Python (.py) que deseja converter.
   - Exibe o caminho do arquivo selecionado em um campo de texto.

2. **Converter para .exe:**
   - Ao clicar no botão "Converter para .exe":
     - Obtém o caminho do arquivo Python informado.
     - Verifica se um arquivo foi selecionado, caso contrário, exibe um erro.
     - Usa o **PyInstaller** (uma biblioteca para criar executáveis a partir de scripts Python) para realizar a conversão.
     - Executa o `PyInstaller` no terminal com a opção **onefile** para gerar um único arquivo executável.
     - Procura o arquivo .exe gerado na pasta **dist**.
     - Se o arquivo .exe for encontrado, exibe uma mensagem de sucesso com o caminho do executável.
     - Se ocorrer um erro durante o processo, exibe uma mensagem de erro correspondente.

**Interface Gráfica (GUI):**

- Cria uma janela principal com o título "Conversor de .py para .exe".
- Possui um rótulo ("Selecione o arquivo .py:"), um campo de texto para exibir o caminho do arquivo e um botão "Procurar" para selecionar o arquivo.
- Inclui um botão "Converter para .exe" que inicia o processo de conversão quando clicado.

**Bibliotecas Utilizadas:**

- **tkinter**: Para criar a interface gráfica.
- **filedialog** de **tkinter**: Para abrir a janela de seleção de arquivos.
- **messagebox** de **tkinter**: Para exibir mensagens de erro e sucesso.
- **subprocess**: Para executar o **PyInstaller** no terminal.
- **os**: Para manipulação de caminhos de arquivos e diretórios.

**Observações:**

- O código assume que o **PyInstaller** está instalado no sistema.
- É importante ter cuidado ao criar executáveis, pois eles podem ser usados para distribuir malware. Certifique-se de converter apenas seus próprios scripts Python.
