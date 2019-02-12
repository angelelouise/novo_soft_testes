# Especificação de Caso de Uso: Visualizar Relatório (Testador)

## 1. Descrição do Caso de Uso

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
**Visualizar Relatório**
1. Testador aciona a funcionalidade de Visualizar relatório de erros;
1. Exibe a listagem de erros da tarefa; **[[BD01](#bd01)]**, **[[FA01](#fa01)]**, **[[FA02](#fa02)]**, **[[FA03](#fa03)]**
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#### FA01
**Alterar erro**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de alterar erro;
1. Aciona a opção de alterar erro;
1. Retorna para o passo 3 do fluxo principal.

#### FA02
**Finalizar erro**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de finalizar erro;
1. Atribui o status "Finalizado" ao erro e adiciona ao histórico;
1. Retorna para o passo 3 do fluxo principal.

#### FA03
**Reincidir erro**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de reincidir erro;
1. Atribui o status "Reincidente" ao erro e adiciona ao histórico;
1. Retorna para o passo 3 do fluxo principal.

#### FA04
**Excluir erro**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de excluir erro;
1. Remove o erro da lista;
1. Retorna para o passo 3 do fluxo principal.

#### FA05
**Visualizar histórico**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de visualizar histórico do erro;
1. Exibe o detalhamento **[[BD02](#bd02)]**;
1. Retorna para o passo 3 do fluxo principal.

#### FA06
**Visualizar cenário**
1. Após o passo 2 do fluxo principal, o testador aciona a opção de visualizar detalhamento do cenário;
1. Exibe o detalhamento **[[BD03](#bd03)]**;
1. Retorna para o passo 3 do fluxo principal.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Visualizar Erros**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida| Observações |
|----------------------------|-----------------|-------------|-------------|-------------|
| Cenário de testes          | Hiperlink   | Não         | Saida       | Exibe um pop up **[[BD03](#bd03)]**|
| Ambientes                  | Alphanumérico   | Sim         | Saida       | N/A.|
| Tipo do Erro               | Alphanumérico   | Sim         | Saida       | Opções: Visual, Negócio, Execução, Navegação |
| Logins                     | Alphanumérico   | Sim         | Saida       | N/A. |
| Caso de uso                | Alphanumérico    | Sim         | Saida       | N/A. |
| Severidade                 | Alphanumérico   | Sim         | Saida       | Opções: SEV-1, SEV-2, SEV-3, SEV-4.|
| Status                     | Alphanumérico   | Sim         | Saida       | Opções: Cadastrado, Pendente, Em correção, Corrigido, Finalizado, Reincidente, Desconsiderado. |
| Data de Cadastro                     | Data   | Sim         | Saida       | N/A. |
| Desenvolvedor                     | Alphanumérico   | Sim         | Saida       | N/A. |
| Descrição                  | Alphanumérico   | Sim         | Saida       | N/A. |
| Anexo                      | Hiperlink       | Sim         | Saida       | Faz o download dos arquivos. |
| Marcar como reincidente    | Hiperlink       | Sim         | Saida       | Visível quando o erro está no status "Corrigido". |
| Marcar como finalizado     | Hiperlink       | Sim         | Saida       | Visível quando o erro está no status "Corrigido". |
| Alterar                    | Hiperlink       | Sim         | Saida       | Faz o download doas arquivos. |
| Histórico                  | Hiperlink       | Sim         | Saida       | **[[BD02](#bd02)]** |
| Excluir                    | Hiperlink       | Sim         | Saida       | N/A. |

### BD02
**Histórico**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Data                       | Data            | Sim         |         Saida | N/A.                   |
| Status                     | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Usuário                    | Alphanumérico   | Sim         |         Saida | N/A.                   |

### BD03
**Detalhes do cenário**

| Campo                      | Tipo            | Obrigatório | Entrada/Saida | Observações |
|----------------------------|-----------------|-------------|---------------|-------------|
| Título                     | Alphanumérico   | Sim         |         Saida | N/A. |
| Como:                      | Alphanumérico   | Sim         |         Saida | N/A. |
| Eu quero:                  | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Para:                      | Alphanumérico   | Sim         |         Saida | N/A.                  |
| Prioridade                 | Alphanumérico   | Sim         |       Entrada | Ao selecionar desmarca as outras prioridades. |
| Número do cenário          | Alphanumérico   | Sim         |         Saida | N/A.                   |
| Dado                       | Alphanumérico   | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico   | Sim         |         Saida | Só deve aparecer se estiver preenchido. |
| Quando                     | Alphanumérico   | Sim         |         Saida | N/A.                     |
| Então                      | Alphanumérico         | Sim         |         Saida | N/A.                     |
| E                          | Alphanumérico          | Sim         |         Saida | Só deve aparecer se estiver preenchido. |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio

#### RN01

## 8. Documentos Relacionados
Não se aplica.
