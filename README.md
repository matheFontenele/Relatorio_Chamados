# 📊 Relatório Unificado de Chamados

Este projeto tem como objetivo consolidar, padronizar e organizar informações de chamados oriundos de diferentes sistemas (**OTRS, MCTI e UFSC**), unificando-os em um único relatório para análise e acompanhamento.  

## 🚀 Funcionalidades

- Leitura de arquivos **CSV** e **Excel** contendo os chamados.  
- Padronização de colunas e eliminação de informações irrelevantes.  
- Inclusão de informações complementares de clientes (**Estado** e **Município**).  
- Padronização da coluna **Situação** (`Fechado com êxito` → `Fechado`, `open` → `Aberto`).  
- Conversão e unificação das colunas de datas no formato brasileiro:  
  `dd/mm/yyyy HH:MM:SS` (ex.: `05/08/2025 16:40:46`).  
- Ordenação cronológica dos chamados, do mais antigo para o mais recente.  
- Geração de um **relatório final consolidado**.  

## 🗂 Estrutura dos Dados

### Arquivo `clientes.csv`
Contém informações dos clientes:  
- **ID do Cliente**  
- **Nome** (renomeado para `Cliente`)  
- **Estado**  
- **Município**  

### Arquivos de chamados
- **otrs.csv**  
- **mcti.csv**  
- **ufsc.xlsx**  

Cada arquivo possui suas colunas originais, que são padronizadas para o formato final:  

- `Chamado`  
- `Criado` (data/hora do chamado, padronizada)  
- `Fila`  
- `Situação`  
- `Cliente`  
- `ID do Cliente`  
- `Tecnico`  
- `Estado`  
- `Municipio`  

### Relatório Final
Após o processamento, todos os chamados são unificados em um **único DataFrame** e podem ser exportados para CSV/Excel.  

## ⚙️ Tecnologias Utilizadas

- [Python 3](https://www.python.org/)  
- [pandas](https://pandas.pydata.org/)  

## ▶️ Como Executar

1. Clone este repositório:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repo.git
   ```

2. Instale as dependências:
   ```bash
   git clone https://github.com/seu-usuario/nome-do-repo.git    
    ```
3. Coloque os arquivos `otrs.csv`, `mcti.csv`, `ufsc.xlsx` e `clientes.csv` na pasta do projeto.

4. Execute o script Python principal:
   ```bash
    python relatorio.py
    ```


## 👨‍💻 Autor

- [@mathFontenele](https://github.com/matheFontenele)
Projeto desenvolvido por Matheus Fontenele 💻
Estudante de Análise e Desenvolvimento de Sistemas
