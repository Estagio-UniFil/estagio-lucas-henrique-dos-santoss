# **Sabina Decorações**

> **Sistema de Portfólio Online**
> **Especificação de Caso de Uso: Ver Galeria de Fotos**

**Versão 1.0**

| **Sistema** | **Versão** | **Data** |
| :--- | :--- | :--- |
| Sabina Decorações | 1.0 | 28/08/2025 |

---

## **Histórico de Revisões**
| **Data** | **Versão** | **Descrição** | **Autor** |
| :--- | :--- | :--- | :--- |
| 28/08/2025 | 1.0 | Primeira versão do documento | Gemini |

---

## **Índice**
1. [Breve Descrição](#1-breve-descrição)
2. [Fluxo Básico de Eventos](#2-fluxo-básico-de-eventos)
3. [Fluxos Alternativos](#3-fluxos-alternativos)
4. [Subfluxos](#4-subfluxos)
5. [Cenários Chave](#5-cenários-chave)
6. [Condições Prévias](#6-condições-prévias)
7. [Condições Posteriores](#7-condições-posteriores)
8. [Pontos de Extensão](#8-pontos-de-extensão)
9. [Requisitos Especiais](#9-requisitos-especiais)

---

### **1. Breve Descrição**
Este caso de uso descreve como um usuário do site da Sabina Decorações visualiza a galeria de fotos dos trabalhos realizados. O objetivo é permitir que clientes em potencial e visitantes possam explorar o portfólio da empresa, inspirar-se e filtrar as imagens por categoria de evento.

---

### **2. Fluxo Básico de Eventos**

#### **2.1 Visualizar Galeria**
1. O usuário acessa a página "Galeria" no site.
2. O sistema busca a lista de fotos cadastradas.
3. O sistema exibe a página `galeria_fotos.html`, renderizando as fotos em uma grade.
    - Cada item exibe a imagem, categoria e título.
4. O usuário pode clicar em um botão de filtro de categoria (ex: "Casamentos", "Corporativos").
5. O sistema, através de um script no navegador, atualiza a grade para exibir apenas as fotos da categoria selecionada.
6. O fluxo é finalizado quando o usuário navega para outra página.

---

### **3. Fluxos Alternativos**

#### **3.1 Galeria Vazia**
1. No passo 2 do fluxo básico, o sistema verifica que não há fotos cadastradas.
2. O sistema exibe uma mensagem informativa na página, como "Nenhuma foto disponível no momento".
3. O fluxo é finalizado.

---

### **4. Subfluxos**

#### **4.1 Filtragem de Categoria**
1. O usuário clica em um botão de filtro (ex: "Todos", "Casamentos").
2. Um script no lado do cliente (JavaScript) percorre todos os itens da galeria.
3. O script exibe os itens que correspondem à categoria selecionada e oculta os demais.
4. O botão de filtro clicado é visualmente destacado como "ativo".

---

### **5. Cenários Chave**

#### **5.1 Visualização Completa da Galeria**
- **Usuário**: Acessa a página "Galeria".
- **Sistema**: Carrega e exibe com sucesso todas as imagens disponíveis no portfólio.

#### **5.2 Filtragem de Fotos por Categoria**
- **Usuário**: Clica no botão de filtro "Corporativos".
- **Sistema**: Atualiza a visualização para mostrar apenas as fotos da categoria "Corporativos".

---

### **6. Condições Prévias**
1. O usuário deve ter acesso à internet e a um navegador web.
2. O site deve estar online e acessível.
3. A lista de fotos (estática ou vinda de um banco de dados) deve estar disponível para a aplicação.

---

### **7. Condições Posteriores**
1. **Sucesso**:
    - A galeria de fotos é exibida corretamente para o usuário.
    - O filtro de categoria funciona conforme o esperado.
2. **Falha**:
    - Se não houver fotos, uma mensagem informativa é exibida.
    - O estado do sistema não é alterado.

---

### **8. Pontos de Extensão**
- **Integração com Banco de Dados**: As fotos poderiam ser gerenciadas por um administrador através de um painel, em vez de estarem fixas no código.
- **Visualização Ampliada (Lightbox)**: Permitir que o usuário clique em uma foto para vê-la em tamanho maior.

---

### **9. Requisitos Especiais**
- O layout da galeria deve ser responsivo para se adaptar a diferentes tamanhos de tela (desktops, tablets e smartphones).
- As imagens devem ser otimizadas para carregamento rápido na web.

---

**Observações**:
- A funcionalidade não requer que o usuário esteja logado.
- A implementação atual utiliza uma lista de fotos estática no arquivo `views.py`.
