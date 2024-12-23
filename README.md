# README.md

Este documento foi criado para orientar o uso do script `short_genome_seq_mining_test.ipynb`. Ele descreve em detalhes as funcionalidades do pipeline, requisitos técnicos e procedimentos para personalização e execução do código.

## Visão Geral do Projeto

O notebook `short_genome_seq_mining_test.ipynb` implementa um pipeline de bioinformática para mineração de sequências genômicas curtas. O objetivo principal é identificar proteínas de interesse, como defensinas ou lectinas, com base em descrições de anotações fornecidas.

### Funcionalidades principais:

1. Montagem do Google Drive no Google Colab para acesso aos dados.
2. Instalação automatizada de pacotes Python necessários.
3. Processamento de arquivos de anotação e sequências proteicas.
4. Extração de proteínas específicas e armazenamento em arquivos FASTA enriquecidos com metadados.

---

## Estrutura do Repositório

- `short_genome_seq_mining_test.ipynb`: Notebook principal contendo o pipeline.
- `data/`: Diretório sugerido para armazenar arquivos de entrada (FASTA e anotações).
- `outputs/`: Diretório para resultados gerados durante a execução.

---

## Requisitos Técnicos

- **Python**: Versão 3.8 ou superior.
- **Pacotes Python necessários**:
  - `Biopython`
  - `tqdm`

Instale os pacotes com o seguinte comando:

```bash
pip install biopython tqdm
```

---

## Guia de Uso

### 1. Configuração do Ambiente

Caso esteja utilizando o Google Colab, o script já contém etapas para montar o Google Drive e acessar os arquivos. Se estiver rodando localmente, certifique-se de que os arquivos estão no caminho especificado e que o Python está configurado corretamente.

### 2. Dados de Entrada Necessários

- **Arquivo de Anotação**: Um arquivo tabular com informações detalhadas sobre proteínas (e.g., `annotation_info.txt`).
- **Arquivo FASTA**: Contém as sequências proteicas associadas às anotações.

#### Exemplo de formato esperado:

**Arquivo de Anotação (TSV):**

```
peptideName	Best-hit-rice-defline
protein1	Defensin-like protein
protein2	Lectin-related protein
```

**Arquivo FASTA:**

```
>protein1
MKTAYIAKQRQIS...
>protein2
GQSPTNLYFGGRK...
```

### 3. Execução do Pipeline

1. Abra o notebook no Jupyter ou Google Colab.
2. Execute as células sequencialmente, ajustando as variáveis globais, como os caminhos dos arquivos e o diretório de saída, conforme necessário.
3. Os resultados serão salvos no diretório especificado em formato FASTA.

---

## Adaptação para Outros Conjuntos de Dados

### Procedimentos:

1. **Atualização dos Caminhos**: Substitua os valores das variáveis `annotation_file`, `fasta_file` e `output_dir` para refletir os novos arquivos.
2. **Verificação do Formato**: Certifique-se de que os arquivos de entrada seguem os padrões descritos anteriormente. Use ferramentas como SeqKit para conversão, se necessário.

---

## Solução de Problemas

1. **Erro de Importação**: Confirme que os pacotes estão instalados e corretamente configurados.
2. **Problemas no Parsing de Dados**: Verifique a integridade e o formato dos arquivos de entrada.
3. **Resultados Incompletos**: Garanta que os critérios de filtragem no arquivo de anotações correspondam aos dados fornecidos.

---

## Informações de Contato

Para suporte ou dúvidas, entre em contato com:

**Madson Aragão**  
Email: [madsondeluna@gmail.com](mailto:madsondeluna@gmail.com)  
LinkedIn: [Madson Aragão](https://www.linkedin.com/in/madsonaragao)


