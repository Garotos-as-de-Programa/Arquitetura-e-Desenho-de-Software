# Processo de Engenharia de Requisitos

**Projeto:** Sistema de Gestão de Competências
**Etapa:** 1ª Etapa – Levantamento de Requisitos
**Sistema análogo:** Lattice (gestão de desempenho, feedback e metas)
**Versão:** 1.0

## 1. Visão Geral

Este documento descreve o processo de engenharia de requisitos adotado pela equipe no levantamento e na documentação dos requisitos do Sistema de Gestão de Competências, desde o entendimento do negócio até a especificação formal.

O sistema apoiará avaliações de competências de diferentes tipos (chefe–colaborador, por pares e 360º) e deverá ser implementado em plataforma **WEB**, com perspectiva futura de uso em dispositivos móveis, em **conformidade com a LGPD**.

O processo é iterativo e incremental: os requisitos são levantados, analisados, especificados e validados em ciclos curtos, acompanhados pelos marcos do cronograma (seção 9).

### Funcionalidades mínimas que orientam o levantamento

1. Questionários personalizáveis;
2. Múltiplas fontes de feedback (gestores, colegas, subordinados e partes interessadas externas);
3. Análise robusta (tendências, números e recursos visuais);
4. Confidencialidade e anonimato, com conformidade com a LGPD;
5. Acompanhamento contínuo (histórico dos feedbacks);
6. Planejamento de desenvolvimento (metas e acompanhamento de melhorias).

## 2. Papéis e Responsabilidades

| Membro | Papel | Responsabilidades |
|--------|-------|-------------------|
<<<<<<< HEAD
| [Nome] | Gerente do projeto | Coordena o Kanban, acompanha os marcos e valida a entrega final |
| [Nome] | Responsável pela elicitação | Roteiros e termo de consentimento; organiza entrevistas e questionários |
| [Nome] | Analista do sistema análogo | Levanta e sintetiza as funcionalidades do Lattice |
| [Nome] | Modelador de processos | Modela o processo atual em BPMN e identifica as dores |
| [Nome] | Responsável pela documentação e rastreabilidade | Mantém a lista geral de requisitos, a matriz de rastreabilidade e o repositório |
=======
| Kaique | Gerente do projeto | Coordena o Kanban, acompanha os marcos e valida a entrega final |
| Clara | Responsável pela elicitação | Roteiros e termo de consentimento; organiza entrevistas e questionários |
| Miguel | Analista do sistema análogo | Levanta e sintetiza as funcionalidades do Lattice |
| Victor Hugo | Modelador de processos | Modela o processo atual em BPMN e identifica as dores |
| Ighor | Responsável pela documentação e rastreabilidade | Mantém a lista geral de requisitos, a matriz de rastreabilidade e o repositório |
>>>>>>> 0c18a0f8e3c669c3445e708d11fc5181f6854024

Todos os membros participam das elicitações, das revisões cruzadas e dos commits. Os papéis definem quem lidera cada atividade, não quem a executa sozinho.

## 3. Elicitação e Descoberta

A elicitação combina as técnicas obrigatórias da etapa. Cada técnica gera um artefato versionado no repositório e uma síntese de requisitos.

### 3.1 Pesquisa documental (leis, regulamentações e normas)
- Levantamento de leis, regulamentações e normas aplicáveis, como a **LGPD** (Lei nº 13.709/2018) e a **ISO/IEC 25010** (qualidade de produto de software).
- Resultado: documento com as normas pesquisadas e os requisitos (principalmente não funcionais) que delas decorrem.

### 3.2 Entrevistas (2)
- Elaboração de roteiro semiestruturado antes das entrevistas.
- Registro de nome, função e telefone de cada entrevistado.
- Transcrição completa, anexada ao repositório.
- Resultado: síntese dos requisitos das entrevistas.

### 3.3 Questionários (2)
- Aplicados a pessoas **diferentes** das entrevistadas.
- Registro de nome, função e telefone de cada respondente, com as respostas anexadas.
- Resultado: síntese dos requisitos dos questionários.

### 3.4 Análise do sistema análogo (Lattice)
- Estudo das funcionalidades por documentação oficial, tutoriais, estudos de caso e demonstrações.
- Descrição das funcionalidades encontradas, anexada ao repositório.
- Resultado: síntese dos requisitos do sistema análogo, filtrada pelas funcionalidades mínimas do escopo (seção 1). Funcionalidades do Lattice fora desse escopo, como OKRs e reuniões 1:1, só entram se justificadas por outra fonte.

### 3.5 Modelagem do processo de negócio (BPMN)
- Modelagem do processo **atual** de avaliação de competências, destacando as principais dores.
- As dores identificadas servem de fonte para requisitos.

### 3.6 Técnicas complementares
- **Brainstorming interno:** para reunir e organizar os requisitos levantados, sem substituir as fontes externas.
- Outras técnicas (observação, prototipação, workshops) poderão ser usadas se houver tempo, e registradas como fonte.

### 3.7 Termo de Consentimento
Como entrevistas e questionários coletam dados pessoais, todo participante recebe e assina (ou aceita) um **termo de consentimento**, em coerência com a LGPD. O termo informa a finalidade da coleta, o uso restrito ao trabalho acadêmico e o direito de retirar o consentimento.

## 4. Análise e Priorização

Os requisitos levantados são analisados quanto a duplicidade, conflito, ambiguidade e viabilidade, e depois priorizados pelo método **MoSCoW**:

- **Must have (Deve ter):** essenciais para o funcionamento básico do sistema;
- **Should have (Deveria ter):** importantes, mas o sistema funciona sem eles;
- **Could have (Poderia ter):** desejáveis, se houver tempo hábil;
- **Won't have (Não terá):** fora do escopo desta versão.

A prioridade considera a frequência da demanda nas fontes, as funcionalidades mínimas do enunciado e as restrições (web e LGPD).

## 5. Especificação

### 5.1 Identificação e numeração
Cada requisito recebe um identificador único e permanente:
- **RF01, RF02, ...** – requisitos funcionais;
- **RNF01, RNF02, ...** – requisitos não funcionais (desempenho, usabilidade, segurança, privacidade e anonimato, conformidade com a LGPD, portabilidade para mobile, entre outros, usando as características da ISO/IEC 25010 como guia);
- **RN01, RN02, ...** – regras de negócio e restrições do domínio.

Um identificador nunca é reutilizado. Requisitos removidos ficam marcados como "cancelado".

### 5.2 Requisitos funcionais
Escritos como **Histórias de Usuário**, para manter o foco no valor entregue:

`Como [perfil de usuário], eu quero [ação/funcionalidade] para que [motivo/valor].`

Cada requisito funcional contém: identificador, história, critérios de aceitação, prioridade (MoSCoW) e fontes.

### 5.3 Requisitos não funcionais e restrições
Escritos de forma objetiva e **verificável**, com critério mensurável sempre que possível.
Exemplo: "RNF03 – O sistema não deve exibir ao gestor a identidade de respondentes anônimos em nenhum relatório."

### 5.4 Critérios de aceitação
Lista de condições claras e testáveis que devem ser cumpridas para o requisito ser considerado atendido, evitando termos vagos como "rápido", "fácil" ou "adequado" sem métrica.

### 5.5 Template de requisito

| Campo | Conteúdo |
|-------|----------|
| ID | RF00 |
| Título | Nome curto |
| Descrição | História de usuário ou enunciado |
| Critérios de aceitação | Lista de condições testáveis |
| Prioridade | Must / Should / Could / Won't |
| Fonte(s) | Ex.: Entrevista 1, Questionário 2, Lattice, LGPD |
| Status | Proposto / Validado / Cancelado |

### 5.6 Sínteses
Cada fonte (entrevistas, questionários e sistema análogo) gera uma síntese com requisitos redigidos de forma clara e não ambígua. Os requisitos das sínteses são consolidados na **lista geral de requisitos**.

## 6. Validação

- **Revisão cruzada:** cada artefato é revisado por pelo menos um membro que não o escreveu, via Pull Request ou comentário no repositório. A revisão verifica clareza, ausência de ambiguidade, consistência entre requisitos e presença de fonte.
- **Checklist de revisão:** o requisito é compreensível, único, verificável, tem critério de aceitação, tem prioridade e tem fonte.
- **Validação final:** feita pelo gerente do projeto antes da entrega, alinhada às orientações da professora.

## 7. Rastreabilidade

### 7.1 Matriz requisitos × fontes
É mantida uma matriz em que as linhas são os requisitos (RF/RNF/RN) e as colunas são as fontes (Entrevista 1, Entrevista 2, Questionário 1, Questionário 2, Sistema análogo, Pesquisa documental, BPMN, outras).

**Regra:** nenhum requisito entra na lista geral sem pelo menos uma fonte. A matriz é atualizada sempre que um requisito é criado, alterado ou cancelado.

### 7.2 Ligação com o Kanban
Os requisitos e as atividades também são registrados como *Issues* no GitHub Projects, identificadas pelo ID do requisito (ex.: "RF05 – Questionário personalizável"). Isso complementa a matriz e liga cada requisito às suas alterações no repositório.

## 8. Gestão de Mudanças e Versionamento

### 8.1 Ferramentas
- **Repositório:** GitHub, com todos os artefatos versionados.
- **Planejamento:** GitHub Projects (Kanban), com link no `README.md`.

### 8.2 Kanban
Colunas: **Backlog → A fazer → Em andamento → Em revisão → Concluído**. Cada cartão tem responsável e marco (Milestone 1, 2 ou 3).

### 8.3 Branches e commits
- Branch principal: `main`, sempre com o conteúdo revisado.
- Branches de trabalho por atividade: `entrevistas`, `bpmn`, `requisitos` etc., integradas via Pull Request com revisão.
- Mensagens de commit objetivas, no formato `tipo: descrição`, como `docs: adiciona transcrição da entrevista 1` ou `req: inclui RF07 e atualiza matriz`.
- Todos os membros fazem commits sob o próprio usuário.

### 8.4 Mudanças em requisitos
1. A mudança é proposta em uma Issue, com justificativa e fonte.
2. A equipe avalia o impacto nos demais requisitos e na matriz.
3. Aprovada, o requisito é alterado ou cancelado (nunca apagado), e a matriz é atualizada no mesmo commit.

### 8.5 Estrutura do repositório

```
/planejamento          Kanban (PDF e link)
/processo              Este documento
/pesquisa-documental   LGPD, ISO/IEC 25010 e outras normas
/entrevistas           Roteiro, termo de consentimento, transcrições, síntese
/questionarios         Modelo, respostas, síntese
/sistema-analogo       Funcionalidades do Lattice e síntese
/bpmn                  Processo atual e dores
/requisitos            Lista geral e matriz de rastreabilidade
README.md
```

## 9. Cronograma e Marcos

| Período | Atividades principais | Marco |
|---------|----------------------|-------|
| 30/09 a 07/10 | Formação do grupo, escolha do sistema análogo, repositório, Kanban, processo de requisitos, início da pesquisa documental | **Marco 1 – 07/10:** Kanban e processo publicados; sistema análogo registrado |
| 08/10 a 14/10 | 2 entrevistas, 2 questionários, rascunho do BPMN, funcionalidades do sistema análogo | **Marco 2 – 14/10:** entrevistas e questionários concluídos (preliminar); BPMN em rascunho |
| 15/10 a 20/10 | Sínteses, lista geral de requisitos, matriz de rastreabilidade, revisão cruzada, organização do repositório | **Marco 3 – 20/10:** todos os artefatos versionados e revisados |
| 21/10 | Entrega final da 1ª etapa | Artefatos impressos e envio do link do repositório |

## 10. Artefatos da Etapa

1. Planejamento em Kanban;
2. Definição do processo de requisitos (este documento);
3. Síntese dos requisitos das entrevistas;
4. Questionário preenchido (com respostas);
5. Síntese dos requisitos dos questionários;
6. Síntese dos requisitos do sistema análogo;
7. Lista geral de requisitos;
8. Matriz de rastreabilidade (requisitos × fontes).

<<<<<<< HEAD
Complementares: pesquisa documental, modelo BPMN e termo de consentimento.
=======
Complementares: pesquisa documental, modelo BPMN e termo de consentimento.
>>>>>>> 0c18a0f8e3c669c3445e708d11fc5181f6854024
