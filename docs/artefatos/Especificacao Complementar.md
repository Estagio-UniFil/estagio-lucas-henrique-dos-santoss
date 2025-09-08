# Sabina Decorações
## Sistema de Orçamento para Eventos
### Especificação de Caso de Uso: Solicitar Orçamento
**Versão 1.0**

| Sistema | Versão | Data |
| :--- | :--- | :--- |
| Sabina Decorações | 1.0 | 13/08/2025 |

---

## Histórico de Revisões

| Data | Versão | Descrição | Autor |
| :--- | :--- | :--- | :--- |
| 13/08/2025 | 1.0 | Primeira versão do documento | [Lucas Henrique dos Santos] |

---

## Índice
1. Breve Descrição
2. Fluxo Básico de Eventos
3. Fluxos Alternativos
4. Subfluxos
5. Cenários Chave
6. Condições Prévias
7. Condições Posteriores
8. Pontos de Extensão
9. Requisitos Especiais

---

## 1. Breve Descrição
Este caso de uso descreve a funcionalidade de solicitação de orçamento para eventos na Sabina Decorações. O cliente preenche um formulário com detalhes do evento, seleciona pacotes de decoração e serviços adicionais, e o sistema envia os dados para análise da equipe.

## 2. Fluxo Básico de Eventos
### 2.1 Solicitar Orçamento
1. O cliente acessa a página "Solicitar Orçamento".
2. O sistema exibe um formulário com seções para:
    * Dados de contato (nome, telefone, e-mail).
    * Detalhes do evento (tipo, número de convidados, local, ideias).
    * Seleção de pacotes (Básico, Premium, Luxo).
    * Serviços adicionais (fotógrafo, buffet, DJ, etc.).
3. O cliente preenche os campos obrigatórios (marcados com asterisco).
4. O cliente seleciona um pacote de decoração e serviços opcionais.
5. O cliente clica em "Enviar Solicitação de Orçamento".
6. O sistema valida os dados:
    * Campos obrigatórios preenchidos.
    * E-mail e telefone em formatos válidos.
7. Se os dados estiverem corretos, o sistema:
    * Envia um e-mail para a equipe com os detalhes do orçamento.
    * Exibe mensagem de sucesso ao cliente.
8. O fluxo é finalizado.

## 3. Fluxos Alternativos
### 3.1 Dados Inválidos
1. Se campos obrigatórios estiverem vazios ou forem inválidos:
    * O sistema exibe mensagens de erro específicas.
    * O formulário mantém os dados preenchidos (exceto os inválidos).
2. O cliente corrige os dados e reenvia o formulário.

### 3.2 Falha no Envio do E-mail
1. Se ocorrer um erro no envio do e-mail:
    * O sistema exibe mensagem de erro ao cliente.
    * Registra o erro em logs para análise técnica.
2. O cliente pode tentar novamente ou entrar em contato por outro canal.

## 4. Subfluxos
### 4.1 Seleção de Pacote
1. O cliente clica em um card de pacote (Básico, Premium, Luxo).
2. O sistema destaca visualmente o pacote selecionado.
3. O valor do pacote é armazenado em um campo oculto do formulário.

### 4.2 Validação de Campos
1. O sistema verifica:
    * **Nome:** não vazio.
    * **Telefone:** formato válido (ex: (00) 00000-0000).
    * **E-mail:** contém "@" e domínio válido.
    * **Número de convidados:** entre 10 e 500.

## 5. Cenários Chave
### 5.1 Orçamento para Casamento
* **Cliente:** Preenche dados de casamento com 100 convidados, seleciona pacote "Luxo" e serviço de fotógrafo.
* **Sistema:** Envia e-mail com detalhes para a equipe.

### 5.2 Orçamento para Evento Corporativo
* **Cliente:** Seleciona pacote "Premium" e serviços de buffet e DJ.
* **Sistema:** Valida dados e confirma o envio.

## 6. Condições Prévias
1. O cliente deve acessar a página "Solicitar Orçamento".
2. O sistema deve estar conectado ao serviço de e-mail.
3. O formulário deve carregar as opções de pacotes e serviços do banco de dados.

## 7. Condições Posteriores
1. **Sucesso:**
    * E-mail enviado para a equipe.
    * Mensagem de confirmação exibida ao cliente.
2. **Falha:**
    * Dados não são enviados.
    * Mensagem de erro é exibida.

## 8. Pontos de Extensão
* Nenhum identificado no momento.

## 9. Requisitos Especiais
* O formulário deve ser responsivo (funcionar em dispositivos móveis).
* O e-mail deve conter um template HTML com os dados formatados.

---
**Observações:**
- Campos obrigatórios são marcados com "*".
- O sistema não calcula valores automaticamente (orçamento é enviado para análise humana).
