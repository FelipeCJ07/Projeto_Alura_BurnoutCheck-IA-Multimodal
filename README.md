# 🧠 BurnoutCheck IA - Check-in Multimodal Experimental

## 📊 Apresentação do Projeto

Você pode visualizar ou baixar os slides desta apresentação que detalha o projeto, suas funcionalidades e desafios:

[Download/Visualizar Slides da Apresentação (.pptx)](presentation/BurnoutCheck_IA_Apresentacao.pptx)

## ✨ Projeto Extraordinário de Imersão em IA ✨

Este projeto implementa uma ferramenta experimental de check-in de bem-estar que explora o poder da **Inteligência Artificial Multimodal** e técnicas de **Visão Computacional**. Desenvolvido como parte de um desafio de imersão em IA, o objetivo é criar um protótipo funcional que permite ao usuário realizar um "check-in" sobre seu estado emocional e físico, utilizando descrição textual e uma selfie, para receber uma análise **cautelosa e não-diagnóstica** gerada por IA.



---

## ⚠️ AVISO IMPORTANTE E ÉTICA ⚠️

**Este é um projeto EXPERIMENTAL, protótipo e educacional, criado exclusivamente para fins de demonstração de capacidades de IA multimodal e visão computacional.**

* A análise fornecida pela Inteligência Artificial (IA) é baseada em padrões identificados nos dados em que o modelo foi treinado e **não constitui, em hipótese alguma, um diagnóstico médico, psicológico ou profissional.**
* As sugestões de autocuidado e recursos são **genéricas** e informativas, não substituem o aconselhamento personalizado de um especialista qualificado.
* A detecção facial é uma funcionalidade técnica para processamento da imagem e não implica qualquer julgamento ou análise profissional sobre a aparência.
* A precisão da análise multimodal da IA pode variar e é limitada pela qualidade dos inputs (texto e imagem) e pelas capacidades inerentes ao modelo.

**🚫🚫🚫 ESTA FERRAMENTA NÃO FAZ DIAGNÓSTICOS! 🚫🚫🚫**

**SEMPRE**, em caso de preocupações reais com saúde mental, cansaço extremo, estresse crônico ou qualquer outro problema de saúde, **PROCURE IMEDIATAMENTE UM PROFISSIONAL DE SAÚDE QUALIFICADO** (médico, psicólogo, psiquiatra, etc.). A responsabilidade pelo uso das informações geradas por esta ferramenta é inteiramente do usuário, que deve estar ciente de suas limitações estritas e propósito demonstrativo.

---

## 🚀 Funcionalidades Principais

* **Check-in Multimodal:** Aceita como input uma descrição textual do seu estado emocional/físico E uma selfie.
* **Detecção Facial:** Utiliza OpenCV para detectar rostos na selfie e exibir a imagem processada com uma marcação.
* **Análise com Gemini IA:** Envia o texto, a imagem (original) e o status da detecção facial para o modelo multimodal `gemini-1.5-flash-latest` para obter uma análise integrada.
* **Sugestões de Autocuidado:** Fornece sugestões gerais e práticas baseadas na análise da IA.
* **Sugestões de Recursos/Ajuda:** Indica tipos de recursos e ações práticas para buscar apoio profissional, incluindo exemplos.
* **Aviso Ético Dinâmico:** Exibe um disclaimer padrão ou um aviso enfático com recursos de emergência, dependendo da análise da IA.
* **Histórico Simples:** Salva um log textual básico das interações em um arquivo local (`.jsonl`) no ambiente de execução e o carrega ao iniciar.
* **Interface Web Interativa:** Utiliza Gradio para criar uma interface de usuário web amigável, acessível via link público temporário a partir do Google Colab.

---

## 💻 Tecnologias Utilizadas

* **Google Colab:** Ambiente de execução.
* **Python:** Linguagem principal.
* **Google Generative AI (`google-generativeai`):** Interação com API Gemini.
* **Gradio (`gradio`):** Construção da interface web.
* **OpenCV (`opencv-python`):** Visão Computacional (detecção facial).
* **Pillow (`PIL`):** Manipulação de Imagens.
* **Outras:** `os`, `json`, `datetime`, `numpy`, etc.

---

## ▶️ Como Rodar o Projeto

A maneira mais fácil e rápida de executar o BurnoutCheck IA é utilizando o **Google Colab**:

1.  **Abra o notebook:** Clique no link do arquivo `.ipynb` no repositório GitHub. O GitHub oferece a opção "Open in Colab". Alternativamente, baixe o arquivo e faça upload no Colab.
2.  **Configure sua Chave de API do Google Gemini:**
    * Obtenha sua chave de API na Google AI Studio (https://aistudio.google.com/app/apikey).
    * No painel lateral esquerdo do Colab, clique no ícone de chave (🔑).
    * Crie um novo segredo com o nome `API_KEY`.
    * Cole sua chave de API no campo "Value".
    * Ative a chave "Notebook access to secrets" para este notebook.
3.  **Execute as Células:** Vá no menu "Ambiente de execução" e selecione "Executar todas as células". Alternativamente, execute cada célula sequencialmente, de cima para baixo (Shift + Enter).
4.  **Acesse a Interface:** Após a última célula (Célula 8) terminar de carregar, um link público (`https://...gradio.live`) aparecerá na saída. Clique neste link para abrir a interface Gradio em uma nova aba do seu navegador.

A célula 8 permanecerá em estado de execução para manter o servidor da interface ativo. Para parar a aplicação, interrompa a execução da Célula 8 no Colab.

---

## 🖼️ Screenshots da Interface

Aqui estão algumas capturas de tela da interface Gradio do projeto e do fluxo de execução:

![1 - Importação de Bibliotecas no Colab](Images/anexos/01_Importacao_Bibliotecas.png)

![2 - Configuração da API Gemini](Images/anexos/02_Configuracao_API_Gemini.png)

![3 - Funções Auxiliares (Imagem)](Images/anexos/03_Funcoes_Auxiliares_Imagens.png)

![4 - Detecção Facial com OpenCV](Images/anexos/04_Deteccao_Facial_OpenCV.png)

![5 - Pré-processamento de Imagem e Texto](Images/anexos/05_Preprocessamento_Imagens_Texto.png)

![6 - Início da Função Process_Checkin](Images/anexos/06_Inicio_Funcao_Process_Checkin.png)

![7 - Processamento de Texto](Images/anexos/07_Process_Checkin_Texto.png)

![8 - Processamento de Imagem](Images/anexos/08_Process_Checkin_Imagem.png)

![9 - Processo de Checkin Multimodal](Images/anexos/09_Process_Checkin_Multimodal.png)

![10 - Processo Checkin (Formatação)](Images/anexos/10_Process_Checkin_Formatacao.png)

![11 - Funções Auxiliares (Formatação)](Images/anexos/11_Funcoes_Auxiliares_Formatacao.png)

![12 - Início da Interface Gradio](Images/anexos/12_Inicio_Interface_Gradio.png)

![13 - Estilos CSS da Interface](Images/anexos/13_Estilos_CSS_Interface.png)

![14 - Título e Descrição da Interface](Images/anexos/14_Titulo_Descricao_Interface.png)

![15 - Componente de Entrada (Texto)](Images/anexos/15_Componente_Entrada_Texto.png)

![16 - Componente de Entrada (Imagem)](Images/anexos/16_Componente_Entrada_Imagem.png)

![17 - Botões de Ação](Images/anexos/17_Botoes_Acao.png)

![18 - Componentes de Saída](Images/anexos/18_Componentes_Saida.png)

![19 - Componente de Histórico](Images/anexos/19_Componente_Historico.png)

![20 - Layout da Interface (Início)](Images/anexos/20_Layout_Interface_Inicio.png)

![21 - Layout Componentes de Entrada](Images/anexos/21_Layout_Componentes_Entrada.png)

![22 - Layout Botões de Ação](Images/anexos/22_Layout_Botoes_Acao.png)

![23 - Layout Componentes de Saída](Images/anexos/23_Layout_Componentes_Saida.png)

![24 - Integração Processo Checkin Interface](Images/anexos/24_Integracao_Process_Checkin_Interface.png)

![25 - Process Checkin Continuação](Images/anexos/25_Process_Checkin_Continuacao.png)

![26 - Process Checkin Finalização](Images/anexos/26_Process_Checkin_Finalizacao.png)

![27 - Vinculo Botao Enviar Funcao](Images/anexos/27_Vinculo_Botao_Enviar_Funcao.png)

![28 - Vinculo Botao Sair](Images/anexos/28_Vinculo_Botao_Sair.png)

![29 - Configuração Lançamento Interface](Images/anexos/29_Configuracao_Lancamento_Interface.png)

![30 - Lançamento Interface Parte 1](Images/anexos/30_Lancamento_Interface_Parte1.png)

![31 - Lançamento Interface Parte 2](Images/anexos/31_Lancamento_Interface_Parte2.png)

![32 - Lançamento Interface Parte 3](Images/anexos/32_Lancamento_Interface_Parte3.png)

![33 - Lançamento Interface Parte 4](Images/anexos/33_Lancamento_Interface_Parte4.png)

![34 - Lançamento Interface Parte 5](Images/anexos/34_Lancamento_Interface_Parte5.png)

![35 - URL Pública Gerada](Images/anexos/35_URL_Publica_Gerada.png)

![36 - Interface Final Funcionando](Images/anexos/36_Interface_Final_Funcionando.png)
