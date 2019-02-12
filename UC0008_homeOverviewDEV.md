# Especificação de Caso de Uso: Home (Desenvolvedor)

## 1. Descrição do Caso de Uso

## 2.Pré-condições
O usuário estar logado com a permissão de desenvolvedor.

## 3.Pós-condições
Não se aplica.

## 4. Fluxo de eventos
### 4.1 Fluxo Principal

#### FP
1. Desenvolvedor aciona a funcionalidade de Home;
1. Sistema exibe as tarefas do GAS que estão no status "Aguardando Correções" e o menu de utilização; **[[BD01](#bd01)]**, **[[BD02](#bd02)]**
1. Sistema exibe as tarefas do GAS que estão no status "Aguardando Correções" atribuídas para o desenvolvedor logado; **[[BD01](#bd01)]**
1. Desenvolvedor seleciona a opção de visualizar relatório de erros para uma tarefa; **[[FA02](#fa02)]**
1. Inicia a funcionalidade UC0009_VisualizarRelatórioDEV;
1. O caso de uso é finalizado.

### 4.2 Fluxo Alternativo

#### FA05
**Listar cenário**

1. No passo 4, o desenvolvedor seleciona a opção de visualizar cenários;
1. Inicia a funcionalidade UC000X_VisualizarCenários;
1. Retorna para o passo 7 do fluxo principal.

#### FA06
**Listar caso de uso**

1. No passo 4, o desenvolvedor seleciona a opção de visualizar casos de uso;
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
| Relatório de Erros         | Imagem       | Sim         |       Entrada | Só deve ser exibido se a tarefa tiver um relatório de erros cadastrado. |

### BD02
**Menu**

| Campo                      | Tipo         | Obrigatório | Entrada/Saida | Observações |
|----------------------------|--------------|-------------|---------------|-------------|
| Listar cenários                 | Link | Sim         |         Entrada |  |
| Listar casos de uso              | Link     | Sim         |         Entrada |  |

## 6. Requisitos Legais
Não se aplica.

## 7. Regras de Negócio
Não se aplica.

## 8. Documentos Relacionados
Não se aplica.
