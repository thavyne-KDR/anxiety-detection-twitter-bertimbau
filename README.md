# 🧠 Detecção de Ansiedade em Tweets utilizando BERTimbau
[![Abrir no Colab](https://colab.research.google.com/assets/colab-badge.svg)](https://colab.research.google.com/drive/1dC9hHf_Qr4NFwP7EjWbYwcSXOxUGtcqV?usp=sharing)

Este projeto apresenta uma abordagem de **Processamento de Linguagem Natural (PLN)** para identificar **sinais de ansiedade em textos publicados no Twitter**, utilizando o modelo **BERTimbau**.

O objetivo é treinar um modelo capaz de reconhecer padrões linguísticos associados à ansiedade em textos curtos de redes sociais.

---

# 📌 Sobre o Projeto

As redes sociais se tornaram um espaço onde muitas pessoas expressam sentimentos, preocupações e experiências pessoais. A partir dessas publicações, é possível identificar sinais relacionados à saúde mental.

Neste projeto foi desenvolvido um modelo de **classificação de textos** capaz de identificar automaticamente se um tweet apresenta **sinais de ansiedade** ou **não ansiedade**.

Para isso, foi utilizado o modelo **BERTimbau**, uma versão do BERT treinada especificamente para o idioma português.

---

# 🤖 Modelo Utilizado

O modelo utilizado neste projeto foi:

**BERTimbau (neuralmind/bert-base-portuguese-cased)**

Esse modelo é uma adaptação do BERT treinada em grandes volumes de textos em português brasileiro, sendo bastante eficiente em tarefas de **Processamento de Linguagem Natural**.

O treinamento foi realizado utilizando a técnica de **fine-tuning**, adaptando o modelo pré-treinado para a tarefa de classificação de ansiedade.

Configurações principais do treinamento:

- Modelo: BERTimbau
- Tipo de tarefa: Classificação binária
- Épocas de treinamento: **6**
- Divisão treino/teste: **80% / 20%**
- Batch size: **16**
- Learning rate: **1e-5**

---

# 📊 Dataset

O dataset utilizado neste projeto foi construído a partir da combinação de dois conjuntos de dados públicos.

### SetembroBR

Dataset composto por tweets em português relacionados a **ansiedade e depressão**.

Neste projeto foram utilizados apenas os tweets rotulados como **ansiedade**.

---

### TweetSentBR

Dataset amplamente utilizado para **análise de sentimentos em tweets em português**.

Tweets desse dataset foram utilizados para representar a classe **não ansiedade**.

---

### Dataset Final

A partir da combinação dos dois datasets foi criado um **dataset balanceado**, contendo:

- Tweets com **ansiedade**
- Tweets **sem ansiedade**

Além disso, foram adicionados **alguns textos sintéticos**, com o objetivo de enriquecer o conjunto de dados e melhorar a capacidade do modelo de reconhecer diferentes formas de expressão de ansiedade.

O dataset final utilizado no treinamento encontra-se neste repositório.

---

# ⚙️ Metodologia

O fluxo geral do projeto foi o seguinte:

1️⃣ Construção do dataset combinado  
2️⃣ Balanceamento das classes (ansiedade / não ansiedade)  
3️⃣ Tokenização dos textos utilizando o tokenizer do BERTimbau  
4️⃣ Fine-tuning do modelo BERTimbau  
5️⃣ Avaliação do modelo no conjunto de teste  

Bibliotecas utilizadas:

- Transformers (HuggingFace)
- PyTorch
- Scikit-learn
- Pandas
- NumPy

---

# 📈 Resultados

O modelo apresentou os seguintes resultados no conjunto de teste:

| Métrica | Valor |
|------|------|
| Accuracy | **0.89** |
| F1-score (macro) | **0.89** |

Relatório de classificação:

| Classe | Precision | Recall | F1-score |
|------|------|------|------|
| Não ansiedade | 0.91 | 0.88 | 0.89 |
| Ansiedade | 0.88 | 0.91 | 0.90 |

Esses resultados indicam que o modelo conseguiu identificar de forma consistente padrões linguísticos associados à ansiedade em textos publicados no Twitter.

---

# 📊 Matriz de Confusão

A matriz de confusão obtida no processo de avaliação apresenta os seguintes valores:

- Verdadeiros negativos: **100**
- Verdadeiros positivos: **104**
- Falsos positivos: **14**
- Falsos negativos: **10**

Isso demonstra que o modelo mantém um bom equilíbrio entre identificar corretamente textos com ansiedade e evitar classificações incorretas.

---

# 🚀 Notebook no Google Colab

O treinamento completo do modelo pode ser acessado no notebook abaixo:

👉 **Abrir no Colab:**  
https://colab.research.google.com/drive/1dC9hHf_Qr4NFwP7EjWbYwcSXOxUGtcqV?usp=sharing

---

# 🧠 Detecção de Ansiedade em Tweets utilizando BERTimbau

Este projeto apresenta uma abordagem de **Processamento de Linguagem Natural (PLN)** para identificar **sinais de ansiedade em textos publicados no Twitter**, utilizando o modelo **BERTimbau**.

O objetivo é treinar um modelo capaz de reconhecer padrões linguísticos associados à ansiedade em textos curtos de redes sociais.

---

# 📌 Sobre o Projeto

As redes sociais se tornaram um espaço onde muitas pessoas expressam sentimentos, preocupações e experiências pessoais. A partir dessas publicações, é possível identificar sinais relacionados à saúde mental.

Neste projeto foi desenvolvido um modelo de **classificação de textos** capaz de identificar automaticamente se um tweet apresenta **sinais de ansiedade** ou **não ansiedade**.

Para isso, foi utilizado o modelo **BERTimbau**, uma versão do BERT treinada especificamente para o idioma português.

---

# 🤖 Modelo Utilizado

O modelo utilizado neste projeto foi:

**BERTimbau (neuralmind/bert-base-portuguese-cased)**

Esse modelo é uma adaptação do BERT treinada em grandes volumes de textos em português brasileiro, sendo bastante eficiente em tarefas de **Processamento de Linguagem Natural**.

O treinamento foi realizado utilizando a técnica de **fine-tuning**, adaptando o modelo pré-treinado para a tarefa de classificação de ansiedade.

Configurações principais do treinamento:

- Modelo: BERTimbau
- Tipo de tarefa: Classificação binária
- Épocas de treinamento: **6**
- Divisão treino/teste: **80% / 20%**
- Batch size: **16**
- Learning rate: **1e-5**

---

# 📊 Dataset

O dataset utilizado neste projeto foi construído a partir da combinação de dois conjuntos de dados públicos.

### SetembroBR

Dataset composto por tweets em português relacionados a **ansiedade e depressão**.

Neste projeto foram utilizados apenas os tweets rotulados como **ansiedade**.

---

### TweetSentBR

Dataset amplamente utilizado para **análise de sentimentos em tweets em português**.

Tweets desse dataset foram utilizados para representar a classe **não ansiedade**.

---

### Dataset Final

A partir da combinação dos dois datasets foi criado um **dataset balanceado**, contendo:

- Tweets com **ansiedade**
- Tweets **sem ansiedade**

Além disso, foram adicionados **alguns textos sintéticos**, com o objetivo de enriquecer o conjunto de dados e melhorar a capacidade do modelo de reconhecer diferentes formas de expressão de ansiedade.

O dataset final utilizado no treinamento encontra-se neste repositório.

---

# ⚙️ Metodologia

O fluxo geral do projeto foi o seguinte:

1️⃣ Construção do dataset combinado  
2️⃣ Balanceamento das classes (ansiedade / não ansiedade)  
3️⃣ Tokenização dos textos utilizando o tokenizer do BERTimbau  
4️⃣ Fine-tuning do modelo BERTimbau  
5️⃣ Avaliação do modelo no conjunto de teste  

Bibliotecas utilizadas:

- Transformers (HuggingFace)
- PyTorch
- Scikit-learn
- Pandas
- NumPy

---

# 📈 Resultados

O modelo apresentou os seguintes resultados no conjunto de teste:

| Métrica | Valor |
|------|------|
| Accuracy | **0.89** |
| F1-score (macro) | **0.89** |

Relatório de classificação:

| Classe | Precision | Recall | F1-score |
|------|------|------|------|
| Não ansiedade | 0.91 | 0.88 | 0.89 |
| Ansiedade | 0.88 | 0.91 | 0.90 |

Esses resultados indicam que o modelo conseguiu identificar de forma consistente padrões linguísticos associados à ansiedade em textos publicados no Twitter.

---

# 📊 Matriz de Confusão

A matriz de confusão obtida no processo de avaliação apresenta os seguintes valores:

- Verdadeiros negativos: **100**
- Verdadeiros positivos: **104**
- Falsos positivos: **14**
- Falsos negativos: **10**

Isso demonstra que o modelo mantém um bom equilíbrio entre identificar corretamente textos com ansiedade e evitar classificações incorretas.

---

# 🚀 Notebook no Google Colab

O treinamento completo do modelo pode ser acessado no notebook abaixo:

👉 **Abrir no Colab:**  
https://colab.research.google.com/drive/1dC9hHf_Qr4NFwP7EjWbYwcSXOxUGtcqV?usp=sharing

---

# 📁 Estrutura do Repositório
anxiety-detection-twitter-bertimbau
│
├── notebook
│ └── treinamento_modelo.ipynb
│
├── dataset
│ └── dataset_ansiedade_vs_nao_balanceado.csv
│
├── imagens
│ └── matriz_confusao.png
│
└── README.md


---

# 🧑‍💻 Autores

**Alex da Conceição Lima, Ana Lívia Farias Silva, Thávyne Kerolly Dias Ribeiro**

Curso: Análise e Desenvolvimento de Sistemas  
Instituto Federal do Piauí – Campus Picos

---

# 📚 Referências

DEVLIN, J. et al.  
BERT: Pre-training of Deep Bidirectional Transformers for Language Understanding. 2019.

SOUZA, F.; NOGUEIRA, R.; LOTUFO, R.  
BERTimbau: Pretrained BERT Models for Brazilian Portuguese. 2020.

VASWANI, A. et al.  
Attention Is All You Need. 2017.
