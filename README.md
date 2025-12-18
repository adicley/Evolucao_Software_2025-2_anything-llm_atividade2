# Evolucao_Software_2025-2_anything-llm_atividade2

## Objetivo

A atividade 2 consiste em analisar o código-fonte das releases do projeto escolhido, no caso da equipe, o projeto [anything-llm](https://github.com/Mintplex-Labs/anything-llm), utlizando três modelos de linguagem disponibilizados no [Hugging Face](https://huggingface.co/models), onde os modelos escolhidos para realizar a atividade foram do tipo text-generation, para identificação de possíveis code smells no código-fonte do projeto.

## Requisitos de Hardware

O projeto foi executado no ambiente de nuvem do Google Colab com:
- GPU: T4 16GB (15 GB de VRAM disponível)
- RAM do sistema: 12.77GB
- Disco: 112GB

## Instruções para execução da atividade

1. Clone o repositório e instale as dependências:
   ```bash
   pip install -r requirements.txt
   ```
2. Feito isso, basta abrir o notebook `main.ipynb` disponibilizado no repositório e executar as células, em ordem, para a criação do arquivo contendo a identicações de code smells nos artefatos de código disponibilizados na pasta `source_code_artefacts`.
3. Ao final, o arquivo contendo os apontamentos de code smells ficaram salvos no arquivo `models_resp.json` na pasta `models_code_smells_resp/`.

## Modelo Utilizados

1. O primeiro modelo de geração de texto escolhido foi o [microsoft/Phi-3-mini-128k-instruct](https://huggingface.co/microsoft/Phi-3-mini-128k-instruct), um modelo com 4B de parâmetros, janela de contexto de 128K tokens, o qual foi treinado utilizando o dataset Phi-3.
2. O segundo modelo foi o [microsoft/Phi-4-mini-instruct](https://huggingface.co/microsoft/Phi-4-mini-instruct), um modelo base com 4B de parâmetros, janela de contexto de 128K tokens que foi treinado utilizando dados sintético e dados públicos filtrados.
3. O terceiro modelo foi o [deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B](https://huggingface.co/deepseek-ai/DeepSeek-R1-Distill-Qwen-1.5B), um modelo com 2B de parâmetros, janela de contexto de 128K tokens, onde, dentro todos os modelos escolhidos, foi o único que foi treinado utilizando a técnica de aprendizado por reforço (Reinforcement Learning) sem ajuste fino supervisionado.
