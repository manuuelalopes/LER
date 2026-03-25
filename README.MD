## Sistema de gestão de tarefas - Especificação de requisitos 

## 1. Introdução 

### 1.1  Proposito 
Este documento especifica os requisitos funcionais e não-funcionais para os Sistemas de gestão de tarefas (SGT). Seguindo o padrão IEEE 29148

### 1.2 Escopo 

O SGT permitirá que usuários criem, organizem e acompanhem tarefas pessoais e profissionais com sistema de prioridades e prazos. 


### 1.3 Definição de Acrônimos 

- **SGT**: Sistema de Gestões de tarefas 
- **RF**  : Requisitos Funcionais 
- **RNF**  : Requisitos não funcionais 
- **Sprint**  : Período de 2 semanas de Desenvolvimento 

## 2. Descrição Geral 

### 2.1 Perspectiva do produto

O SGT será uma aplicação web responsiva com sincronização em nuvem 

### 2.2 Funções Principais 

- Criação e edificação de tarefas 
- Organização por projetos e tags 
- Sistema de notificação 
- Relatório de produtividade 
  
## 3. Requisitos Específicos 

### 3.1 Requisitos Funcionais 

#### RF-001: Criação de Tarefas 

**Descrição** : O Sistema deve permitir que os usuarios criem tarefas com o título, descrição, data de vencimento, prioridade. 
**Prioridade** : Alta 
**Versão** : 1.0
**Data** :2026-03-25
**Rastreabilidade** : Derivado de Necessidades do Stackholder NS-001
**Critérios de Aceitação**

- [ ] Usuário pode criar, editar, e excluir tarefa 
- [ ] Formularios com campos obrigatorios (titulo) e opcionais 
- [ ] Níveis de prioridade: Baixa, Média, Alta urgente 
- [ ] Confirmação visual apos criação 
- [ ] Validação de dados da tarefa (Não permitir datas vazias) 

---

### RF-002: Organização por projetos 
*Descrição**: O sistema deve permitir agrupar tarefas em projetos personalizados
**Prioridade**: Média
**Versão**: 1.0
**Data** 2026-03-25
**Rastreabilidade**: Derivado de NS-002
**Critérios de Aceitação**:

- [ ] Usuário pode criar, renomear e excluir projetos
- [ ] Tarefas podem ser atribuidas a um ou mais projetos
- [ ] Visualização filtrada por projetos

--- 
### ### 3.2 Requsitos Não-Funcionais

#### RNF-001: Desempenho

**Descrição**: O sistema deve carregar a lista de tarefas em menos de 1 segundopara até 100 tarefas.
**Categoria**: Desempenho
**Prioridade**: Alta
**Versão**: 1.0
**Métrica**: Tempo de resposta < 1s para 95% das requisições

---

#### RNF-002: Segurança

**Descrição**: O sistema deve implementar autenticação  Oauth 2.0 e criptografia TLS 1.3
**Categoria**: Segurança
**Prioridade**: Crítica
**Versão**: 1.0
**Métrica**: Conformidade LGPD, GDPR

---

## 4. Controle de Versões

### Histórico de alterações 

|Versão|Data      |Autor  |Modificação   |
|------|----------|-------|--------------|
| 1.0  |2026-03-25|Diogotb|Versão Inicial|

### Rastreabilidade

Gráfico de Rastreabilidade

```mermaid

graph TD

    NS001['NS-001: Necessidade Stakeholder] --> RF001['RF-001: Criação Tarefas']
    RF001 --> TC001['TC-001: Teste Criação]

    NS002['NS-002: Organização'] --> RF002['RF-002: Projetos']
    RF002 --> TC002['TC-002: Teste Projetos']

```

