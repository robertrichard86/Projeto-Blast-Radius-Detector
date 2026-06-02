# Blast Radius Detector

[![Open In Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1qNFw_PBNsROolWYKxygzobnVso-jZGn5?usp=sharing)

## Descrição

O **Projeto Blast Radius Detector** é uma ferramenta para analisar e estimar o impacto ("raio de explosão") de mudanças ou incidentes em sistemas e estruturas de dados. Ele auxilia na identificação de dependências e potenciais riscos.

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
