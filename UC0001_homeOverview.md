# Especificação de Caso de Uso: Home

## 1. Descrição do Caso de Uso
Essa é a funcionalidade responsável por exibir as tarefas que estão na fila para serem testadas.

## 2.Pré-condições
O usuário estar logado com a permissão de testador.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Testador aciona a funcionalidade de Home;
1. Sistema exibe as tarefas do GAS que estão no status "Pronta para testar" e o menu de utilização; **[[BD01](#bd01)]**, **[[BD02](#bd02)]**
1. Sistema exibe as tarefas do GAS que estão no status "Testando" atribuídas para o testador logado; **[[BD01](#bd01)]**
1. Testador seleciona a opção de cadastrar um plano para uma tarefa; **[[FA02](#fa02)]**
1. Sistema verifica se a tarefa não possui um plano de testes cadastrado; **[[FA01](#fa01)]**
1. Caso não exista plano de testes, o sistema inicia a funcionalidade UC0002_CadastrarPlanodeTestes;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo
#### FA01
**Executar Plano de Testes**

1. Após o passo 5, caso exista um plano de testes cadastrado, inicia a funcionalidade UC0003_ExecutarPlanodeTestes;
1. Retorna para o passo 7 do fluxo principal.

#### FA02
**Visualizar Relatório de Erros**

1. No passo 4, o testador seleciona a opção de visualizar relatório de erros;
1. Inicia a funcionalidade UC0007_VisualizarRelatórioErros;
1. Retorna para o passo 7 do fluxo principal.

#### FA03
**Cadastrar caso de uso**

1. No passo 4, o testador seleciona a opção de cadastrar um novo caso de uso;
1. Inicia a funcionalidade UC000X_CadastrarCasodeUso;
1. Retorna para o passo 7 do fluxo principal.
#### FA04
**Cadastrar cenário**

1. No passo 4, o testador seleciona a opção de cadastrar um novo cenário;
1. Inicia a funcionalidade UC0004_CadastrarCenários;
1. Retorna para o passo 7 do fluxo principal.

#### FA05
**Listar cenário**

1. No passo 4, o testador seleciona a opção de visualizar cenários;
1. Inicia a funcionalidade UC000X_VisualizarCenários;
1. Retorna para o passo 7 do fluxo principal.

#### FA06
**Listar caso de uso**

1. No passo 4, o testador seleciona a opção de visualizar casos de uso;
1. Inicia a funcionalidade UC000X_VisualizarCasosUsos;
1. Retorna para o passo 7 do fluxo principal.

### 4.3 Fluxo de Exceções
Não se aplica.

## 5.Bloco de dados
### BD01
**Tarefas**

| Campo                      | Tipo         | Obrigatório | Entrada/Saida | Observações |
|----------------------------|--------------|-------------|---------------|-------------|
| Identificador              | Numérico     | Sim         |         Saida | Número da tarefa no GAS |
| Situação                   | Alphanumérico| Sim         |         Saida | Status da tarefa no GAS |
| Prioridade                 | Alphanumérico| Sim         |         Saida | Prioridade da tarefa no GAS |
| Título                     | Alphanumérico| Sim         |         Saida | Título da tarefa no GAS |
| Atribuído para             | Alphanumérico| Sim         |         Saida | Atribuição da tarefa no GAS |
| Selecionar Tarefa          | Imagem       | Sim         |       Entrada | N/A.                    |
| Relatório de Erros         | Imagem       | Sim         |       Entrada | Só deve ser exibido se a tarefa tiver um relatório de erros cadastrado. |

### BD02
**Menu**

| Campo                      | Tipo         | Obrigatório | Entrada/Saida | Observações |
|----------------------------|--------------|-------------|---------------|-------------|
| Cadastrar caso de uso              | Link     | Sim         |         Entrada |  |
| Cadastrar cenários                 | Link | Sim         |         Entrada |  |
| Listar cenários                 | Link | Sim         |         Entrada |  |
| Listar casos de uso              | Link     | Sim         |         Entrada |  |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
