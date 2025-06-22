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

## ⚙️ Como executar localmente (usando Play with Docker)

1. Acesse o site [Play with Docker](https://labs.play-with-docker.com) e inicie uma nova instância clicando em "Start".

2. No terminal da instância, clone o repositório:
```bash
git clone https://github.com/yasminhn/sistema-recomendacao-filmes.git
cd sistema-recomendacao-filmes
```
3. Suba a aplicação:
```bash
docker-compose up --build
````
4. Após o build, clique em "OPEN PORT", digite 8000 e pressione Enter. Você será direcionado para a interface do sistema de recomendação!
---

![WhatsApp Image 2025-06-22 at 20 53 13](https://github.com/user-attachments/assets/aa772e93-fba3-4776-b48d-edf233c43425)



