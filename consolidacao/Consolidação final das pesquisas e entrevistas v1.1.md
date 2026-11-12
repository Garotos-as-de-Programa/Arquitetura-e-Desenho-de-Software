# PROJETO LATTICE PEOPLE PLATFORM

**Entregáveis:** Consolidação da Elicitação e Lista Geral de Requisitos\
**Responsável:** Clara\
**Data:** 10 de novembro de 2026\
**Versão:** 1.1, de 11 de novembro de 2026 (inclusão dos questionários; ver seção 10)

---

## PARTE 1 — CONSOLIDAÇÃO DA ELICITAÇÃO

## 1. Introdução

A elicitação de requisitos é a etapa responsável por identificar, organizar e compreender as necessidades dos usuários e demais partes interessadas em relação ao sistema. Seu objetivo é transformar necessidades, expectativas e problemas em informações que possam orientar o desenvolvimento da solução.

Este documento consolida os levantamentos relacionados à Lattice People Platform, uma plataforma voltada à gestão de pessoas e ao acompanhamento do desempenho e desenvolvimento dos colaboradores.

A consolidação considera a pesquisa documental sobre legislação, regulamentações e normas aplicáveis, além de informações de referência sobre funcionalidades de plataformas de gestão de pessoas.

A partir da versão 1.1, a consolidação incorpora também os resultados de **dois questionários** aplicados a pessoas diferentes das entrevistadas:

| Fonte | Respondente | Perfil |
|-------|-------------|--------|
| Questionário 1 (Q1) | Mariana Costa Ribeiro, Coordenadora de Operações, Distribuidora Alfa Logística | Gestora, avalia 12 liderados |
| Questionário 2 (Q2) | Rafael Almeida Nunes, Analista de DHO, Hospital Exemplo Vida | RH/DHO, organiza as avaliações |

As respostas completas estão em `questionarios/Questionario-1-Respostas.md` e `questionarios/Questionario-2-Respostas.md`, e a análise detalhada em `questionarios/Sintese-dos-Questionarios.md`. Nas seções a seguir, a indicação "(Q1)" ou "(Q2)" aponta a origem de cada informação acrescentada, seguida do número da pergunta quando aplicável.

## 2. Objetivo do sistema

O sistema tem como objetivo centralizar e facilitar os processos de gestão de pessoas de uma organização, permitindo acompanhar o desempenho dos colaboradores, estabelecer objetivos, realizar avaliações, compartilhar feedbacks e apoiar o desenvolvimento profissional.

A plataforma deverá proporcionar maior organização, transparência e eficiência nos processos de Recursos Humanos, reunindo informações relevantes em um ambiente centralizado.

## 3. Partes interessadas (stakeholders)

Foram identificados os seguintes perfis como possíveis partes interessadas:

| Stakeholder | Participação no sistema | Confirmação nos questionários |
|-------------|-------------------------|-------------------------------|
| Administrador do sistema | Gerencia configurações, usuários e permissões. | Não avaliado. |
| Profissional de RH | Gerencia avaliações, pesquisas, relatórios e processos de pessoas. | Confirmado (Q2). O respondente organiza as avaliações e quer centralizar a criação dos questionários e a escolha dos avaliadores. |
| Gestor | Acompanha equipes, define objetivos e realiza avaliações. | Confirmado (Q1). A respondente avalia liderados e quer acompanhar a equipe por competência. |
| Colaborador | Consulta seus objetivos, avaliações, feedbacks e informações de desenvolvimento. | Confirmado indiretamente. Os dois respondentes incluem o próprio colaborador entre quem vê suas notas e o PDI (Q1 e Q2, pergunta 10). |
| Diretoria | Acompanha indicadores e relatórios para apoiar decisões. | Restrito. Nenhum respondente marcou a diretoria entre quem pode ver notas e PDI individuais (Q1 e Q2, pergunta 10): o acesso deve ser apenas a indicadores agregados. |

Esses perfis representam uma identificação inicial de stakeholders e deverão ser confirmados com representantes da organização que utilizará o sistema. Os questionários confirmaram os perfis de gestor e de RH. Os perfis de administrador e de diretoria ainda precisam de validação.

## 4. Necessidades identificadas

Com base no objetivo proposto e na pesquisa documental, foram organizadas as seguintes necessidades:

1. Centralizar informações relacionadas aos colaboradores.
2. Permitir o acompanhamento de objetivos e resultados individuais e de equipes.
3. Organizar processos de avaliação de desempenho.
4. Facilitar o envio e o recebimento de feedbacks.
5. Permitir o reconhecimento de colaboradores.
6. Apoiar o desenvolvimento profissional por meio de planos e acompanhamento de ações.
7. Permitir a realização de pesquisas de engajamento e satisfação.
8. Disponibilizar relatórios para gestores e profissionais de RH.
9. Controlar o acesso às informações conforme o perfil do usuário.
10. Proteger os dados pessoais e sensíveis dos colaboradores.
11. Permitir o atendimento aos direitos dos titulares de dados pessoais.
12. Oferecer uma interface acessível e de fácil utilização.

Os questionários acrescentaram as seguintes necessidades:

13. Reaproveitar, em um novo ciclo, as informações já registradas no ciclo anterior, sem exigir novo preenchimento (Q1, pergunta 16).
14. Acompanhar, por setor, as etapas do ciclo pendentes ou atrasadas, para cobrar os gestores antes do fim do prazo (Q2, pergunta 15).
15. Permitir o uso pelo celular por profissionais que não trabalham no computador, como equipes de plantão (Q2, perguntas 3, 14 e 15).
16. Garantir o anonimato nas avaliações entre colegas, sem que o gestor identifique quem respondeu (Q2, pergunta 16; Q1 e Q2, pergunta 9).

### Situação das necessidades após os questionários

| Necessidade | Situação | Evidência |
|-------------|----------|-----------|
| 1. Centralizar informações | Confirmada | Q1 e Q2 usam planilhas, formulários e e-mail, e Q2 também papel e chat (pergunta 3). |
| 2. Acompanhar objetivos | Confirmada | PDI com metas, prazos e status recebeu nota 5 de Q1 e Q2 (pergunta 6h). |
| 3. Organizar avaliações | Confirmada | Juntar as notas no resultado final "dá muito trabalho": média 4,5 (pergunta 5b). |
| 4. Feedbacks | Confirmada | Consultar feedbacks anteriores é difícil: média 1,5 (pergunta 5a). |
| 5. Reconhecimento | Baixa prioridade | Badges e conquistas: média 2,5 (pergunta 6l). |
| 6. Desenvolvimento profissional | Confirmada | Q1 quer saber quem precisa de treinamento antes da avaliação (pergunta 15). |
| 7. Pesquisas de engajamento | Não avaliada | Fora das perguntas do questionário. |
| 8. Relatórios | Confirmada | Visão da equipe por competência: média 4,5 (pergunta 6g). |
| 9. Controle de acesso | Confirmada | Notas e PDI visíveis só ao colaborador, ao gestor direto e ao RH/DHO (pergunta 10). |
| 10. Proteção de dados | Confirmada, com ponto em aberto | Não há consenso sobre o prazo de guarda: "enquanto durar o vínculo" (Q1) × "até 5 anos" (Q2) (pergunta 11). |
| 11. Direitos dos titulares | Não avaliada | Fora das perguntas do questionário. |
| 12. Interface fácil | Confirmada | O sistema não deve exigir novo preenchimento a cada ciclo (Q1, pergunta 16). |

## 5. Problemas e oportunidades de melhoria

Considerando o cenário de uma organização que realiza processos de gestão de pessoas, foram levantados problemas potenciais que a plataforma poderá ajudar a reduzir. A coluna "Confirmado nos questionários" indica se o problema foi observado pelos respondentes (escala de 1 a 5 da pergunta 5).

| Problema potencial | Oportunidade de melhoria | Confirmado nos questionários |
|--------------------|--------------------------|------------------------------|
| Informações distribuídas em diferentes ferramentas. | Centralização dos dados em uma única plataforma. | Sim. Q1 e Q2 usam ao menos três ferramentas (pergunta 3), e perda de informação ou retrabalho tem média 3,5 (pergunta 5f). |
| Dificuldade de acompanhar objetivos individuais. | Painel de acompanhamento de metas e resultados. | Sim. O acompanhamento do PDI tem média 2,5 (pergunta 5c). |
| Avaliações realizadas manualmente. | Organização e automatização do fluxo de avaliações. | Sim. A consolidação manual tem média 4,5 (pergunta 5b). |
| Falta de registro organizado de feedbacks. | Histórico de feedbacks e reconhecimento. | Sim. A consulta a ciclos anteriores tem média 1,5 (pergunta 5a). |
| Dificuldade de acompanhar o desenvolvimento dos colaboradores. | Planos individuais de desenvolvimento. | Sim. Q1 só descobre as lacunas da equipe depois da avaliação (pergunta 15). |
| Relatórios elaborados manualmente. | Geração de relatórios e indicadores. | Sim. Q1 monta planilhas para ver a equipe por competência (pergunta 15). |
| Acesso indiscriminado a informações pessoais. | Controle de acesso por perfil e permissões. | Indiretamente. Os dois respondentes restringem a visibilidade das notas (pergunta 10), mas não relatam ocorrência. |
| Risco de tratamento inadequado de dados pessoais. | Recursos de privacidade, segurança e gestão de dados. | Indiretamente. Não há consenso sobre o prazo de guarda dos dados (pergunta 11). |

Problemas observados nos questionários e ausentes da lista anterior:

| Problema observado | Oportunidade de melhoria | Fonte |
|--------------------|--------------------------|-------|
| O que é conversado nas reuniões 1:1 não é aproveitado na avaliação nem no PDI. | Registro de 1:1 integrado à avaliação e ao PDI. | Média 1,5 (pergunta 5e) |
| Perguntas da avaliação pouco adequadas a cada cargo ou área. | Questionários personalizáveis por cargo, área e senioridade. | Média 2,5 (pergunta 5d); nota 5 de Q1 e Q2 para a funcionalidade (pergunta 6a) |
| O gestor preenche tudo de novo a cada ciclo. | Pré-preenchimento com os dados do ciclo anterior. | Q1, pergunta 16 |
| O RH não enxerga quais avaliações estão atrasadas em cada setor. | Painel de pendências por setor, com lembretes aos gestores. | Q2, pergunta 15 |
| Profissionais sem computador ficam fora do processo digital. | Acesso pelo navegador do celular. | Q2, perguntas 3, 14 e 15 |

## 6. Expectativas dos usuários

A partir dos perfis de stakeholders identificados, foram estabelecidas expectativas preliminares. Os itens com indicação de fonte foram acrescentados a partir dos questionários.

**Administrador**

- Gerenciar usuários e permissões.
- Configurar os módulos da plataforma.
- Manter o controle de acesso às informações.

**Profissional de Recursos Humanos**

- Organizar avaliações e pesquisas.
- Acompanhar indicadores de desempenho e engajamento.
- Consultar relatórios consolidados.
- Administrar informações dos colaboradores.
- Criar e publicar os questionários de avaliação (Q2, pergunta 7).
- Definir os avaliadores das avaliações entre colegas (Q2, pergunta 8).
- Acompanhar por setor as avaliações atrasadas e cobrar os gestores (Q2, pergunta 15).
- Exibir resultados anônimos só a partir de 5 respostas (Q2, pergunta 9).

**Gestor**

- Acompanhar o desempenho da equipe.
- Definir e monitorar objetivos.
- Realizar avaliações e fornecer feedbacks.
- Ver a equipe por competência e saber quem precisa de treinamento antes da avaliação (Q1, perguntas 6g e 15).
- Participar, com o RH, da definição dos questionários (Q1, pergunta 7).
- Aprovar os colegas indicados pelo avaliado para a avaliação entre pares (Q1, pergunta 8).
- Não precisar preencher de novo, a cada ciclo, o que já foi informado (Q1, pergunta 16).

**Colaborador**

- Consultar suas avaliações e objetivos.
- Receber e fornecer feedbacks.
- Acompanhar seu desenvolvimento profissional.
- Consultar informações relacionadas ao seu desempenho.
- Responder às avaliações e acompanhar o PDI pelo celular, quando não trabalha no computador (Q2, perguntas 14 e 15).
- Receber lembretes pelo próprio sistema e, conforme preferência, por e-mail ou celular (Q1 e Q2, pergunta 12).

**Diretoria**

- Consultar indicadores gerais.
- Acompanhar resultados das equipes.
- Utilizar informações consolidadas no processo decisório.
- Sem acesso a notas e PDI individuais, apenas a indicadores agregados (Q1 e Q2, pergunta 10).

Essas expectativas deverão ser validadas com usuários reais. As expectativas de gestor e de RH foram parcialmente validadas pelos questionários. As de administrador, colaborador e diretoria seguem pendentes.

## 7. Requisitos legais e normativos identificados

A pesquisa documental identificou normas e legislações relevantes para o desenvolvimento da plataforma.

| Legislação ou norma | Relação com o sistema |
|---------------------|-----------------------|
| Lei nº 13.709/2018 — LGPD | Proteção de dados pessoais e sensíveis, direitos dos titulares e responsabilidades no tratamento de dados. |
| Regulamentações da ANPD | Orientações e obrigações relacionadas à proteção de dados pessoais. |
| CLT | Observância das obrigações trabalhistas aplicáveis aos processos de gestão de pessoas. |
| Lei nº 14.611/2023 | Igualdade salarial e critérios remuneratórios entre mulheres e homens. |
| Lei nº 9.029/1995 | Proibição de práticas discriminatórias nas relações de trabalho. |
| Lei nº 13.146/2015 — LBI | Acessibilidade e inclusão de pessoas com deficiência. |
| Marco Civil da Internet | Princípios e regras aplicáveis ao uso da internet e à proteção de dados no ambiente digital. |
| NR-1 | Requisitos relacionados à gestão de riscos ocupacionais, conforme a aplicabilidade ao contexto da organização. |
| ISO/IEC 25010 | Referência para características e avaliação da qualidade do produto de software. |
| ISO/IEC/IEEE 15288 | Referência para processos do ciclo de vida de sistemas. |

As leis e regulamentações aplicáveis devem ser observadas conforme o contexto e as operações efetivamente realizadas pela organização. As normas ISO constituem referências técnicas e não devem ser tratadas automaticamente como obrigações legais.

Os questionários reforçam dois pontos ligados à LGPD. O primeiro é o prazo de guarda dos dados de avaliação: os respondentes divergem (pergunta 11), e o prazo deve ser definido pela organização com apoio jurídico, considerando a eliminação ao fim da finalidade (arts. 15 e 16). O segundo é a restrição de acesso aos dados individuais apenas a quem precisa deles (pergunta 10), coerente com os princípios de finalidade e necessidade (art. 6º).

## 8. Requisitos não funcionais e preocupações de qualidade

A consolidação também identificou características importantes para a qualidade da plataforma:

- **Segurança:** proteção contra acesso não autorizado.
- **Privacidade:** tratamento adequado de dados pessoais. Nas avaliações entre colegas, o gestor não pode identificar quem respondeu, e os resultados só aparecem a partir de um número mínimo de respostas, configurável: 3 para Q1, 5 para Q2 (Q2, pergunta 16; Q1 e Q2, pergunta 9).
- **Usabilidade:** facilidade de utilização pelos diferentes perfis. O sistema não deve pedir de novo informações já registradas (Q1, pergunta 16).
- **Acessibilidade:** possibilidade de utilização por pessoas com diferentes necessidades.
- **Confiabilidade:** funcionamento consistente da plataforma.
- **Desempenho:** respostas adequadas durante as operações.
- **Manutenibilidade:** facilidade de correção e evolução do sistema.
- **Compatibilidade:** funcionamento nos ambientes e navegadores definidos para a solução. O uso principal é no computador (Q1), mas as tarefas do colaborador também devem funcionar no navegador do celular (Q2, perguntas 14 e 15).
- **Integridade:** notas de um ciclo encerrado não podem ser alteradas pelo gestor (Q2, pergunta 16).

## 9. Contribuição dos questionários

### 9.1 Funcionalidades mais e menos valorizadas (pergunta 6, escala 1 a 5)

| Funcionalidade | Q1 | Q2 | Média |
|----------------|----|----|-------|
| Questionários diferentes por cargo, área e senioridade | 5 | 5 | 5,0 |
| PDI com metas, prazos e status | 5 | 5 | 5,0 |
| Lembretes automáticos de prazos | 5 | 5 | 5,0 |
| Avaliação entre colegas, anônima | 4 | 5 | 4,5 |
| Comparação de resultados entre ciclos | 5 | 4 | 4,5 |
| Visão da equipe por competência | 5 | 4 | 4,5 |
| Avaliação do gestor pelos liderados | 3 | 4 | 3,5 |
| Gráficos comparando autoavaliação e nota do gestor | 4 | 3 | 3,5 |
| Registro das reuniões 1:1 ligado ao PDI | 4 | 3 | 3,5 |
| Avaliação por pessoas externas | 3 | 2 | 2,5 |
| Integração com ferramentas do dia a dia | 2 | 3 | 2,5 |
| Reconhecimento simbólico (badges) | 2 | 3 | 2,5 |

### 9.2 Pontos em que os respondentes divergiram

| Tema | Q1 | Q2 | Encaminhamento |
|------|----|----|----------------|
| Periodicidade do ciclo (pergunta 4) | Anual | Semestral | Ciclo com periodicidade configurável. |
| Quem cria os questionários (pergunta 7) | RH e gestor | Somente o RH | O RH publica, e o gestor propõe competências da sua área. |
| Quem escolhe os avaliadores do 360º (pergunta 8) | Avaliado indica, gestor aprova | O RH | O avaliado indica, o gestor aprova e o RH pode ajustar. |
| Mínimo de respostas anônimas (pergunta 9) | 3 | 5 | Valor configurável, com padrão 3. |
| Prazo de guarda dos dados (pergunta 11) | Enquanto durar o vínculo | Até 5 anos | Em aberto; definir com a organização e apoio jurídico. |
| Dispositivo (pergunta 14) | Computador | Computador e celular | Uso principal no computador, com as tarefas do colaborador funcionando no celular. |

Os dois respondentes concordaram em não exibir ranking de desempenho: Q1 o considera negativo e Q2, indiferente (pergunta 13).

## 10. Histórico de versões

| Versão | Data | Alteração |
|--------|------|-----------|
| 1.0 | 10/11/2026 | Versão inicial, com base na pesquisa documental e em referências de plataformas de gestão de pessoas. |
| 1.1 | 11/11/2026 | Inclusão dos questionários Q1 e Q2: fontes na introdução; confirmação dos stakeholders; necessidades 13 a 16 e situação de cada necessidade; confirmação dos problemas e novos problemas observados; expectativas de RH, gestor, colaborador e diretoria; observações de LGPD e de requisitos não funcionais; seção 9. O conteúdo da versão 1.0 foi mantido. |
