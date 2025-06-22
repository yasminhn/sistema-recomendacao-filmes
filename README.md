# 🎬 Sistema de Recomendação de Filmes com FastAPI

Este projeto implementa um sistema de recomendação baseado em conteúdo, utilizando dados do IMDb e tecnologias modernas como **FastAPI**, **Pandas**, **Scikit-Learn** e **Docker**. Ele é capaz de sugerir filmes semelhantes com base em gêneros e sinopses.

---

## 📌 Funcionalidades

- ✅ Recomendação de filmes com base em similaridade de conteúdo (gênero + sinopse)  
- ✅ API REST desenvolvida com FastAPI  
- ✅ Interface automática de documentação com Swagger (em `/docs`)  
- ✅ Containerização com Docker  
- ✅ Utilização de um dataset real com os 1000 melhores filmes do IMDb  

---

## 🧠 Modelo de Recomendação

O sistema utiliza **filtragem baseada em conteúdo**, combinando os campos **Genre** e **Overview**. Os principais passos são:

1. Pré-processamento textual com **TF-IDF**, ignorando *stopwords*  
2. Cálculo da similaridade usando **cosine similarity**  
3. Retorno dos filmes mais semelhantes ao título consultado  

---

## 🗂 Dataset

O projeto utiliza o arquivo `imdb_top_1000.csv`, contendo informações como:

- 🎞 Título do filme  
- 🎭 Gêneros  
- 📄 Sinopse (Overview)  
- ⭐ Avaliações (não utilizadas no modelo atual)

> ⚠️ O arquivo CSV deve estar no diretório raiz do projeto com o nome exato: `imdb_top_1000.csv`

---

## ⚙️ Como executar localmente (usando Docker)

1. Clone o repositório:
```bash
git clone https://github.com/yasminhn/sistema-recomendacao-filmes.git
cd sistema-recomendacao-filmes


