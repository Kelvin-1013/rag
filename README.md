# RAG (Retrieval Augmented Generation) System

## Table of Contents
1. [Project Overview](#project-overview)
2. [Features](#features)
3. [Architecture](#architecture)
4. [Installation](#installation)
5. [Usage](#usage)
6. [API Endpoints](#api-endpoints)
7. [Security Features](#security-features)
8. [Vector Database Integration](#vector-database-integration)
9. [Document Processing](#document-processing)
10. [Query System](#query-system)
11. [Configuration](#configuration)
12. [Dependencies](#dependencies)
13. [File Structure](#file-structure)
14. [Contributing](#contributing)
15. [License](#license)
16. [Contact](#contact)

## Project Overview

This project implements a sophisticated Retrieval Augmented Generation (RAG) system designed to process, store, and query various document types while maintaining a high level of data security. The system integrates multiple embedding models, supports various document formats, and implements advanced security features such as data masking and unmasking.

## Features

- Multi-format document processing (PDF, JSON, TXT)
- Secure data handling with masking of sensitive information
- Multiple embedding models for different use cases
- Namespace support for multi-tenant or categorized data storage
- Flexible querying system with masked and unmasked options
- Integration with external Language Model (LLM) API
- Modular and extensible architecture

## Architecture

The system is built on a modular architecture with the following main components:

1. **Document Ingestion**: Handles the processing of various document types.
2. **Security Layer**: Implements data masking and unmasking.
3. **Vector Database**: Stores document embeddings for efficient retrieval.
4. **Query Processing**: Manages document retrieval and interaction with LLM.
5. **API Layer**: Provides RESTful endpoints for system interaction.

```mermaid
graph TB
    A[Client] --> B[API Layer]
    B --> C[Document Ingestion]
    B --> D[Query Processing]
    C --> E[Security Layer]
    D --> E
    E --> F[Vector Database]
    D --> G[External LLM API]