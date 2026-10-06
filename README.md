# Fashion E-Commerce Chatbot

An AI-powered fashion e-commerce web application that combines product browsing with an intelligent chatbot to help users discover and interact with fashion products.

## Live Demo

**[View the Live Application](https://fashionchatbot.netlify.app/)**

---

##  Project Overview

The **Fashion E-Commerce Chatbot** is a full-stack web application designed to provide an interactive shopping experience through an integrated AI chatbot.

The application allows users to explore fashion products through a web-based interface while interacting with a chatbot for product-related assistance. The project combines a modern React frontend with a Python-based backend, relational database storage, vector-based semantic search, and AI/NLP technologies.

The main objective of the project is to make product discovery more natural and interactive by allowing users to communicate with the application instead of relying only on traditional product-search methods.

---

##  Objectives

- Build an interactive fashion e-commerce platform.
- Provide an AI-powered conversational interface for product discovery.
- Enable semantic search using vector embeddings.
- Store and manage product and user-related information efficiently.
- Integrate frontend, backend, database, and AI components into a single web application.
- Provide a responsive and user-friendly shopping experience.

---

##  Key Features

###  E-Commerce Features

- Product browsing
- Product information display
- Product search and discovery
- Product availability information
- User-oriented shopping interface

###  AI Chatbot

- Conversational interaction with users
- Product-related queries
- Intelligent product discovery
- Natural-language interaction
- AI-assisted shopping experience

###  Semantic Search

The application uses semantic search techniques to improve product discovery.

Instead of relying only on exact keyword matching, product information can be represented using vector embeddings, allowing the system to identify products based on the semantic meaning of a user's query.

###  Product Management

Product information is maintained using structured data and can be used by the chatbot and search functionality to provide relevant results.

---

##  System Architecture

```text
                    ┌──────────────────────┐
                    │       User           │
                    └──────────┬───────────┘
                               │
                               ▼
                    ┌──────────────────────┐
                    │ React + TypeScript   │
                    │      Frontend        │
                    └──────────┬───────────┘
                               │
                         API Requests
                               │
                               ▼
                    ┌──────────────────────┐
                    │    FastAPI Backend   │
                    │       (Python)        │
                    └───────┬───────┬──────┘
                            │       │
                ┌───────────┘       └────────────┐
                ▼                                ▼
       ┌─────────────────┐              ┌─────────────────┐
       │   PostgreSQL    │              │    ChromaDB     │
       │    Database     │              │  Vector Store   │
       └─────────────────┘              └────────┬────────┘
                                                  │
                                                  ▼
                                      ┌─────────────────────┐
                                      │ Sentence Transformer│
                                      │    Embeddings       │
                                      └─────────────────────┘
```

---

##  Technology Stack

### Frontend

- **React**
- **TypeScript**
- **Vite**
- HTML
- CSS

### Backend

- **Python**
- **FastAPI**
- **SQLAlchemy**

### Database

- **PostgreSQL**

### Vector Database

- **ChromaDB**

### AI / NLP

- **Sentence Transformers**
- Vector embeddings
- Semantic search
- AI-powered conversational interaction

### Deployment

- **Netlify** for the deployed frontend

---

##  AI & Semantic Search

One of the major components of this project is the integration of semantic search.

Product information is converted into numerical vector representations using a sentence-embedding model. These embeddings are stored in **ChromaDB**, allowing the system to compare the semantic similarity between a user's query and available products.

### Example

Instead of searching only for:

```text
"black dress"
```

a semantic search system can understand related descriptions such as:

```text
"dark-colored party wear suitable for women"
```

and identify products with similar meaning.

This improves product discovery compared with basic keyword-based searching.

---

##  Database Design

The backend uses PostgreSQL for structured application data.

The project includes data concepts such as:

```text
Users
Products
Orders
Order Items
User Preferences
Chat Logs
Sessions
```

PostgreSQL handles structured transactional data, while ChromaDB is used for vector-based semantic search.

---

##  Application Flow

```text
User
  │
  ▼
Frontend
  │
  ├── Browse Products
  │
  └── Ask Chatbot
          │
          ▼
      FastAPI API
          │
     ┌────┴─────┐
     ▼          ▼
PostgreSQL   ChromaDB
     │          │
     │     Semantic Search
     │          │
     └────┬─────┘
          ▼
     Relevant Data
          │
          ▼
    Chatbot Response
          │
          ▼
       Frontend
---

##  What I Learned

Through this project, I gained practical experience in:

- Building full-stack web applications
- Developing REST APIs using FastAPI
- Connecting React applications with backend APIs
- Working with PostgreSQL
- Using SQLAlchemy for database operations
- Working with vector databases
- Generating and using sentence embeddings
- Implementing semantic search
- Integrating AI-based conversational functionality
- Debugging frontend-backend communication
- Deploying web applications

---

##  Future Enhancements

Possible improvements include:

- Personalized product recommendations
- Advanced filtering and sorting
- Improved conversational context handling
- User-specific recommendation history
- Shopping cart and checkout integration
- Payment gateway integration
- Improved AI response generation
- Product image-based search
- Voice-based shopping assistant
- Enhanced recommendation algorithms

---

##  Project

**Fashion E-Commerce Chatbot**

A full-stack AI-assisted e-commerce project focused on combining conversational AI, semantic search, and modern web technologies to improve fashion product discovery.
