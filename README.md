# Automação de Cadastro com PyAutoGUI 🖥️

Este projeto realiza a automação do processo de cadastro de produtos em um formulário web, utilizando o site da [Hashtag Treinamentos](https://dlp.hashtagtreinamentos.com/python/intensivao/login). A automação foi desenvolvida com a biblioteca `pyautogui` para interagir com o navegador, preenchendo o formulário com dados retirados de uma planilha Excel.

## 📋 Funcionalidades

- Leitura de uma planilha Excel contendo detalhes dos produtos (codigo, marca, tipo, etc.).
- Preenchimento automático dos campos do formulário do site.
- Submissão dos dados de forma sequencial para o cadastro de múltiplos produtos.
- Ferramenta adicional para capturar a posição dos campos no formulário (arquivo pegar_posição.py).

## 🔧 Tecnologias Utilizadas

- **Python 3.x**: Linguagem principal utilizada no projeto.
- **PyAutoGUI**: Biblioteca responsável pela automação de ações como clique e digitação.
- **OpenPyXL**: Biblioteca para leitura da planilha Excel.
- **Time**: Para controle de intervalos entre as ações.

## 📂 Estrutura do Projeto

```bash
├── cadastro_automacao.py    # Script principal para automação
├── produtos.xlsx            # Planilha de produtos
└── README.md                # Este arquivo
```

## 🚀 Como Usar

1. Clone o repositório:
    ```bash
    git clone https://github.com/GbrPS1/automaçãoCadastroFormulario.git
    cd nome-do-repositorio
    ```

2. Preencha a planilha `produtos.csv` com os detalhes dos produtos que deseja cadastrar:
    - Colunas: `Produto`, `preco_unitario`, `Categoria`, etc.

3. Execute o script para iniciar a automação:
    ```bash
    python Automação_CadastroFormulario.py
    ```

4. Certifique-se de que o site da Hashtag Treinamentos está aberto no navegador e pronto para receber o cadastro.

## 📈 Passo a Passo da Automação

1. **Leitura da Planilha**: O script lê a planilha `produtos.csv` usando a biblioteca.
2. **Abertura do Navegador**: O navegador deve estar aberto e posicionado no formulário de cadastro do site da Hashtag Treinamentos.
3. **Preenchimento Automático**: Com o `pyautogui`, o script move o cursor até os campos do formulário e os preenche com os dados do produto.
4. **Submissão**: Após preencher todos os campos, o botão "Enviar" é clicado para cadastrar o produto.
5. **Repetição**: O processo é repetido para cada produto listado na planilha.

## ⚠️ Observações

- Certifique-se de que a janela do navegador está visível e o formulário do site está devidamente posicionado na tela.
- Utilize o pegar_posição.py para ajustar as coordenadas de acordo com sua tela, caso necessário.
- Ajuste os tempos de espera no código, caso necessário, para evitar problemas de sincronização.
