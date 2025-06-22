# 🎬 Sistema de Recomendação de Filmes com FastAPI

Este projeto implementa um sistema de recomendação baseado em conteúdo, utilizando dados do IMDb e tecnologias modernas como **FastAPI**, **Pandas**, **Scikit-Learn** e **Docker**. Ele é capaz de sugerir filmes semelhantes com base em gêneros e sinopses.

---

## 📌 Funcionalidades

- ✅ Recomendação de filmes com base em similaridade de conteúdo (gênero + descrição)
- ✅ API REST criada com FastAPI
- ✅ Interface automática de documentação com Swagger
- ✅ Containerização com Docker
- ✅ Dataset real com os 1000 melhores filmes do IMDb

---

## 🧠 Modelo de Recomendação

Este sistema utiliza **filtragem baseada em conteúdo**, combinando os campos `Genre` e `Overview` do dataset. Os passos principais são:

1. Pré-processamento textual com TF-IDF (ignora stopwords)
2. Cálculo de similaridade usando cosseno (`cosine_similarity`)
3. Retorno dos filmes mais semelhantes ao título consultado

---

## 🗂 Dataset

O projeto utiliza o arquivo `imdb_top_1000.csv`, que contém informações como:

- Título do filme
- Gêneros
- Sinopse (overview)
- Avaliações (não utilizadas no modelo atual)

O CSV deve estar na pasta `app/` com o nome exato: `imdb_top_1000.csv`.

---

## ⚙️ Como executar localmente

1. Clone o repositório:

```bash
git clone https://github.com/yasminhn/sistema-recomendacao-filmes.git
cd sistema-recomendacao-filmes
