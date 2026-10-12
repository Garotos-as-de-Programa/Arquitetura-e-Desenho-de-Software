# Processo de Engenharia de Requisitos

## 1. Visão Geral
Este documento descreve o processo de engenharia de requisitos adotado pela equipe para o desenvolvimento do sistema baseado na plataforma análoga **Lattice** (Gestão de Pessoas, Desempenho e Engajamento). O processo segue uma abordagem ágil e iterativa, garantindo entregas contínuas e alinhadas com os objetivos da disciplina.

## 2. Elicitação e Descoberta
A principal técnica utilizada para o levantamento inicial de requisitos será a **Pesquisa Documental**.
* **Análise do Sistema Análogo:** Investigação das funcionalidades do Lattice através de documentação oficial, tutoriais, casos de estudo e demonstrações da plataforma.
* **Brainstorming Interno:** Reuniões de equipa para debater e selecionar quais os módulos principais (ex: Avaliações de Desempenho, Metas/OKRs, Reuniões 1:1 e Feedback Contínuo) serão adaptados para o escopo do nosso projeto.

## 3. Análise e Priorização
Após o levantamento, os requisitos serão analisados e priorizados utilizando o método **MoSCoW**, de forma a definir o escopo do nosso Produto Mínimo Viável (MVP):
* **Must have (Deve ter):** Funcionalidades vitais e essenciais para o funcionamento básico do sistema.
* **Should have (Deveria ter):** Funcionalidades importantes que agregam valor, mas cuja ausência não impede o sistema de funcionar.
* **Could have (Poderia ter):** Funcionalidades desejáveis que serão implementadas apenas se houver tempo hábil.
* **Won't have (Não terá):** Funcionalidades que estão fora do escopo desta versão do projeto.

## 4. Especificação
Os requisitos serão especificados num formato ágil, utilizando **Histórias de Utilizador (User Stories)** para manter o foco no valor entregue ao utilizador.
* **Formato Padrão:** `Como [perfil de utilizador], eu quero [ação/funcionalidade] para que [motivo/valor].`
* **Critérios de Aceitação:** Cada História de Utilizador possuirá uma lista de condições claras e testáveis que devem ser cumpridas para que o requisito seja considerado concluído.

## 5. Validação
* Todas as Histórias de Utilizador e Critérios de Aceitação passarão por uma revisão por pares dentro da equipa.
* A validação final antes de entrar em desenvolvimento será feita pelo Gerente de Projetos (PM) e alinhada com as orientações dadas pela professora.

## 6. Gestão e Rastreabilidade
* **Ferramenta de Gestão:** O acompanhamento e rastreabilidade dos requisitos serão feitos através do **GitHub Projects (Kanban)**.
* **Fluxo de Trabalho:** Os requisitos levantados serão registados como *Issues* e mantidos na coluna **Backlog**. Conforme a prioridade, transitarão pelas colunas **To Do** (A Fazer), **In Progress** (Em Andamento), **Review** (Em Revisão) até chegarem a **Done** (Concluído).
* Esta abordagem garante que o código desenvolvido estará sempre ligado diretamente ao requisito que o originou.