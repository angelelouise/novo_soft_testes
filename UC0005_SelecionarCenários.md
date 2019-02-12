# Especificação de Caso de Uso: Selecionar Cenários

## 1. Descrição do Caso de Uso
Essa é a funcionalidade responsável por permitir a seleção de cenários de testes para anexar ao plano de testes.

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Sistema aciona a funcionalidade de Cadastrar Plano de Testes;
1. Exibe os cenários de acordo com o módulo e o(s) caso(s) de uso recebidos por parâmetro; **[[BD01](#bd01)]**, **[[BD02](#bd02)]**, **[[BD03](#bd03)]**
1. Testador seleciona os cenários desejados;
1. Testador finaliza a ação;
1. Sistema retorna os cenários selecionados para a funcionalidade que executou a chamada;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
Não se aplica.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Formulário de busca**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Módulo                     | Alphanumérico   | Sim         |         Saida | N/A. |
| Caso(s) de uso             | Alphanumérico   | Sim         |         Saida | N/A. |
| Tags                       | Alphanumérico   | Sim         |      Entrada  | N/A. |
| Buscar Cenários            | Alphanumérico   | Sim         |      Entrada  | N/A. |
| Cadastrar Novo Cenário     | Link            | Sim         |      Entrada  | N/A. |

### BD02
**Narrativa**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico   | Sim         |         Saida | N/A. |
| Como:                      | Alphanumérico   | Sim         |         Saida | N/A. |
| Eu quero:                  | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Para:                      | Alphanumérico   | Sim         |         Saida | N/A.                  |
| Selecionar Narrativa       | Seleção única   | Sim         |         Entrada | N/A.                  |

### BD03
**Cenários**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Selecionar Cenário         | Seleção única   | Sim         |       Entrada | Ao selecionar desmarca as outras prioridades. |
| Número do cenário          | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Dado                       | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | Só deve aparecer se estiver preenchido. |
| Quando                     | Alphanumérico   | Sim         |         Saida | N/A.                     |
| Então                      | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | Só deve aparecer se estiver preenchido. |
| Cadastrar Cenário na Narrativa | Link            | Sim         |      Entrada  | N/A. |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
