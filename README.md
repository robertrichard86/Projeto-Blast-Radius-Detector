# Blast Radius Detector

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qNFw_PBNsROolWYKxygzobnVso-jZGn5?usp=sharing)

## Descrição

O **Projeto Blast Radius Detector** é um sistema de classificação de risco para comandos de infraestrutura que estima o impacto potencial de uma operação antes de sua execução — separando comandos inofensivos de ações catastróficas. O projeto foi desenvolvido como trabalho de conclusão da disciplina de Machine Learning II e evoluiu por cinco iterações consecutivas baseadas em feedback real.
O sistema utiliza uma arquitetura de três camadas com votação ponderada: uma heurística determinística de palavras-chave (50%), um Random Forest com vetorização TF-IDF (25%) e o modelo de NLP multilingual XLM-RoBERTa-Large-XNLI via zero-shot classification (25%). O resultado final é um score de risco classificado em quatro níveis — Baixo, Médio, Alto e Crítico — acompanhado de um grafo dinâmico de propagação que mapeia os alvos afetados e potenciais cascatas de dependência.
Entre os principais recursos estão: threshold de confiança no NLP (abstém-se abaixo de 50%, prevenindo falsos positivos em comandos como ls -la), feedback loop com re-treino incremental do modelo sem necessidade de re-execução completa da pipeline, dataset de 502 exemplos com verificação de consistência por assertion, cobertura de comandos cloud-native (Terraform, Kubernetes, Docker, AWS CLI, GCloud), e console interativo com semáforo visual e breakdown por camada.

## Estrutura do Repositório

- `data/`: Diretório para armazenar conjuntos de dados e dados locais (ignorado no versionamento para evitar uploads de dados sensíveis ou grandes).
- `notebooks/`: Contém os notebooks Jupyter com as análises, experimentos e o fluxo principal do projeto.
- `src/`: Código fonte em Python, scripts auxiliares e módulos do projeto.

## Como Instalar e Executar

1. **Clone o repositório:**
   ```bash
   git clone <url-do-repositorio>
   cd "Projeto Blast Radius Detector"
   ```

2. **Crie um ambiente virtual (opcional, mas recomendado):**
   ```bash
   python -m venv venv
   source venv/bin/activate  # No Linux/Mac
   venv\Scripts\activate     # No Windows
   ```

3. **Instale as dependências:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Execute o Jupyter Notebook:**
   ```bash
   jupyter notebook
   ```
   Navegue até a pasta `notebooks/` e abra o seu notebook.

---
*Este projeto está sob a licença MIT. Veja o arquivo [LICENSE](LICENSE) para mais detalhes.*
