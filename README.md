# 🏢 Data Warehouse Central - Pipeline ETL em Python

Um sistema centralizado de Extração, Transformação e Carga (ETL) desenvolvido em Python para consolidar e analisar dados de três domínios de negócio distintos: **Hospedagem**, **Locação de Imóveis** e **Vendas de Clientes**.

Este projeto foi desenhado com foco em resiliência estrutural, otimização extrema de memória RAM e geração de relatórios de Inteligência de Negócios (BI) diretamente no terminal em formato interativo (CLI).

## 🚀 Funcionalidades e Engenharia de Dados

- **📥 Extração Segura e Bypass HTTP:** Consumo de APIs JSON contornando bloqueios de firewall (Erro 403) utilizando mascaramento dinâmico de `User-Agent` com bibliotecas nativas.
- **🧠 Prevenção de Explosão Cartesiana:** Achatamento (*flattening*) seguro de arquivos JSON altamente aninhados. O algoritmo extrai automaticamente o primeiro elemento de listas internas, evitando o temido `ArrayMemoryError` e preservando gigabytes de RAM.
- **⚡ Otimização de Memória (Downcast):** Redução drástica do peso dos DataFrames através da conversão inteligente e segura de tipos nativos (ex: `float64` para `float32`), otimizando a performance de processamento.
- **🔄 Sistema de I/O e Backups:** Criação automática de um ambiente de trabalho local (`Python_df`) com sistema autônomo de rotação de backups (mantendo as 2 versões mais recentes de cada banco de dados).
- **📊 Relatórios e BI:** Geração de análises financeiras rigorosas (pagamentos em dia vs. atrasados), ranking estatístico de clientes e plotagem de gráficos de tendências financeiras utilizando `Seaborn` e `Matplotlib`.
- **🌐 Renderização HTML:** Conversão sob demanda de amostras dos DataFrames limpos para visualização estilizada e responsiva diretamente no navegador web.

## 🛠️ Tecnologias Utilizadas

- **Python 3.12+**
- **Pandas 2.0+** (Motor principal de ETL e manipulação colunar)
- **NumPy** (Tipagem matemática e tratamento de dados ausentes)
- **Matplotlib & Seaborn** (Criação de gráficos analíticos)
- **urllib & json** (Requisições seguras e parseamento de estruturas aninhadas)

## ⚙️ Como Instalar e Executar

1. **Clone este repositório:**
   ```bash
   git clone [https://github.com/MARINALDOSOUZA/data_warehouse_etl.git](https://github.com/MARINALDOSOUZA/data_warehouse_etl.git)
   cd data_warehouse_etl
