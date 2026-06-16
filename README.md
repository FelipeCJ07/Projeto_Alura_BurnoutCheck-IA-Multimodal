# 🧠 BurnoutCheck IA — Check-in Multimodal Experimental

[![Python](https://img.shields.io/badge/Python-3.x-3776AB?logo=python&logoColor=white)](https://www.python.org/)
[![Google Colab](https://img.shields.io/badge/Google%20Colab-F9AB00?logo=googlecolab&logoColor=white)](https://colab.research.google.com/)
[![Gemini](https://img.shields.io/badge/Google%20Gemini-1.5%20Flash-8E75B2?logo=google&logoColor=white)](https://ai.google.dev/)
[![Gradio](https://img.shields.io/badge/Gradio-UI-FF7C00?logo=gradio&logoColor=white)](https://www.gradio.app/)
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](LICENSE)

> Protótipo de **check-in de bem-estar multimodal**: o usuário descreve como se sente (texto)
> e envia uma selfie; a ferramenta usa **visão computacional** (OpenCV) e **IA multimodal**
> (Google Gemini) para devolver uma análise **cautelosa e não-diagnóstica** e sugestões de autocuidado.
> Desenvolvido como desafio de imersão em IA.

## ⚠️ Aviso importante

**Projeto experimental, educacional e demonstrativo. NÃO faz diagnósticos.**
A análise da IA não constitui diagnóstico médico, psicológico ou profissional, e as sugestões são
genéricas. Em caso de preocupação real com saúde mental, estresse ou cansaço extremo, **procure um
profissional de saúde qualificado**. O uso das informações é de responsabilidade do usuário.

## ✨ Funcionalidades

- **Check-in multimodal** — combina descrição textual + selfie
- **Detecção facial** com OpenCV (marca o rosto na imagem processada)
- **Análise por IA** com o modelo `gemini-1.5-flash-latest` (texto + imagem)
- **Sugestões de autocuidado** e de onde buscar apoio profissional
- **Aviso ético dinâmico** — reforça recursos de emergência conforme a análise
- **Histórico simples** das interações em arquivo local (`.jsonl`)
- **Interface web** em Gradio, com link público temporário a partir do Colab

## 🛠️ Tecnologias

Python · Google Colab · Google Generative AI (Gemini) · Gradio · OpenCV · Pillow · NumPy

## ▶️ Como rodar (Google Colab)

Este projeto foi feito para rodar no **Google Colab**:

1. Abra [`burnout_check_ia.ipynb`](burnout_check_ia.ipynb) no Colab (botão *Open in Colab* ou upload do arquivo).
2. Configure a chave da API do Gemini:
   - Gere a chave no [Google AI Studio](https://aistudio.google.com/app/apikey).
   - No Colab, painel lateral → ícone 🔑 (*Secrets*) → novo segredo chamado **`API_KEY`** com sua chave.
   - Ative o acesso do notebook ao segredo.
3. Menu *Ambiente de execução → Executar todas as células*.
4. Ao final, clique no link público `https://...gradio.live` gerado na saída para abrir a interface.

> A última célula fica em execução para manter o servidor da interface ativo.

## 🖼️ Demo

Interface Gradio do BurnoutCheck IA em funcionamento:

![Interface do BurnoutCheck IA](Images/anexos/36_Interface_Final_Funcionando.png)

## 📊 Apresentação

Slides detalhando o projeto, funcionalidades e desafios:
[📥 Baixar apresentação (.pptx)](presentation/BurnoutCheck_IA_Apresentacao.pptx)

> 💡 As demais imagens em [`Images/anexos/`](Images/anexos/) documentam, passo a passo, a construção do notebook.

## 📂 Estrutura

```
BurnoutCheck-IA/
├─ burnout_check_ia.ipynb   # notebook principal (Colab)
├─ Images/anexos/           # capturas do processo e da interface
├─ presentation/            # apresentação (.pptx)
└─ LICENSE
```

## 📄 Licença

Distribuído sob a licença **MIT**. Veja [LICENSE](LICENSE).
