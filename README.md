# 📊 Ollama Benchmark RAM/VRAM

Este projeto permite medir **tempo de execução**, **uso de RAM** e **uso de VRAM (GPU)** de diferentes modelos rodando no [Ollama](https://ollama.com).  
Ele roda benchmarks em **melhor de N rodadas** (default: 3), salvando os resultados em CSVs e exibindo tabelas no Jupyter/VSCode.

---

## 🚀 Funcionalidades

- Mede **tempo total de execução** (`elapsed_wall_sec`) de cada modelo.  
- Mede **pico de RAM** (MB) usado pelo processo do Ollama.  
- Mede **pico de VRAM (Δ MB)** alocado na GPU durante a geração.  
- Executa cada teste em **N rodadas** (configurável).  
- Suporte a **Cold Start** opcional: descarrega o modelo da memória entre rodadas, para medir custo de carregamento.  
- Exporta resultados em arquivos CSV para análise posterior.  
- Mostra uma prévia da saída do modelo (`output_preview`) para cada rodada.

---

## 📦 Dependências

Você precisa ter instalado:

- **Python 3.9+**
- **Bibliotecas Python**:
  ```bash
  pip install ollama pandas psutil pynvml
