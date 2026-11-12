# [Marco 3] Síntese dos Requisitos das Entrevistas

**Projeto:** Sistema de Gestão de Competências
**Etapa:** 1ª Etapa – Levantamento de Requisitos
**Responsável pela elicitação:** Clara Morais Jorge Ribeiro
**Versão:** 2.0 (IDs alinhados à Lista Geral Consolidada `RF-001` a `RF-051` e `RNF-001` a `RNF-016`)

## 1. Fontes

| Fonte | Entrevistado | Função / Empresa | Data | Duração | Consentimento | Áudio |
|-------|--------------|------------------|------|---------|---------------|-------|
| Entrevista 1 (E1) | Victor Hugo Alves de Jesus | Assistente de TI, EBM Incorporações | 25/10/2026 (conforme TCLE), 12:30 | 30 min | Aceito | Não |
| Entrevista 2 (E2) | Kaique Caio de Sousa | Analista de Qualidade, Unimed Goiânia (Tecnologia) | 05/11/2026, 21:17 | 45 min | Sim | Sim |

Os dois entrevistados atuam como avaliados. O Entrevistado 2 também avalia terceiros, pois acompanha o onboarding de três novos QAs.

## 2. Cenário atual e dores identificadas

Os dois relatam um processo semelhante: autoavaliação, avaliação top-down (gestor para liderado), reuniões 1:1 e PDI. Tudo corre em planilhas, formulários, e-mail e Teams.

| Dor | Fonte(s) |
|-----|----------|
| Informação descentralizada (planilhas, chats, e-mails, PDFs) | Entrevista 1, Entrevista 2 |
| Sem histórico centralizado; a linha do tempo entre ciclos é difícil de consultar | Entrevista 1, Entrevista 2 |
| Perda de informação e retrabalho (arquivos sobrescritos; pontos de 1:1 esquecidos) | Entrevista 1, Entrevista 2 |
| Consolidação lenta: autoavaliação e notas do gestor ficam em planilhas ou abas separadas | Entrevista 2 |
| PDI é a etapa que trava e vira "apenas um arquivo guardado"; as metas ficam em um campo de texto | Entrevista 1, Entrevista 2 |
| Questionário genérico e "engessado", sem especificidade técnica | Entrevista 1, Entrevista 2 |
| Desconexão entre o acompanhamento (1:1) e a avaliação formal | Entrevista 1 |
| Sem avaliação entre pares formalizada no sistema | Entrevista 2 |

## 3. Requisitos Funcionais Derivados das Entrevistas

> **Nota de rastreabilidade:** Os identificadores abaixo utilizam a numeração unificada da [Marco3_Lista_Geral_de_Requisitos_Lattice.docx](file:///c:/Users/kaiqu/Documents/Arquitetura-e-Desenho-de-Software/Marco3_Lista_Geral_de_Requisitos_Lattice.docx) (`RF-001` a `RF-051`).

### RF-003 – Perfis e autorização (Plataforma centralizada por perfil)

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-003 |
| Título | Perfis e autorização |
| Descrição | Como colaborador, gestor ou RH/DHO, eu quero registrar e consultar avaliações, feedbacks, registros de 1:1 e PDI em um único sistema com acesso controlado por perfil, para não depender de planilhas, e-mails e chats soltos. |
| Critérios de aceitação | 1. Existem os perfis colaborador, gestor e RH/DHO.<br>2. Avaliações, feedbacks, registros de 1:1 e PDI são criados e consultados dentro do sistema, sem arquivo externo.<br>3. Um usuário sem permissão não visualiza dados de avaliação de outro colaborador (RN-01). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q7, Q10, Q18, Q24), Entrevista 2 (Q7, Q10, Q18, Q24) |
| Status | Consolidado |

### RF-007 e RF-009 – Catálogo de competências e personalização por perfil

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-007, RF-009 |
| Título | Catálogo de competências e personalização de questionários por cargo, área e senioridade |
| Descrição | Como gestor ou RH, eu quero cadastrar competências técnicas e comportamentais e vincular questionários a cargo, área e senioridade, para avaliar habilidades específicas de cada função. |
| Critérios de aceitação | 1. É possível incluir competências técnicas (ex.: ferramentas de teste) e comportamentais por cargo e área (RF-007).<br>2. Um questionário pode ser associado a cargo, área e senioridade (RF-009).<br>3. Ao iniciar um ciclo, cada avaliado recebe o questionário correspondente ao seu perfil. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q11, Q12), Entrevista 2 (Q11, Q12, Q24) |
| Status | Consolidado |

### RF-008 – Modelos de questionários (Escala numérica, múltipla escolha e texto livre)

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-008 |
| Título | Modelos de questionários |
| Descrição | Como gestor ou RH, eu quero criar, editar e duplicar questionários com escala numérica de 1 a 5, múltipla escolha e texto livre, para medir o domínio de competências e registrar justificativas e feedbacks. |
| Critérios de aceitação | 1. O sistema oferece os três tipos de pergunta (escala de 1 a 5, múltipla escolha e texto livre).<br>2. É possível criar, editar e duplicar questionários.<br>3. Respostas fora da escala de 1 a 5 são rejeitadas. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q12: escala e texto livre), Entrevista 2 (Q12: escala, múltipla escolha e texto livre) |
| Status | Consolidado |

### RF-012, RF-013, RF-014 e RF-020 – Ciclos de avaliação, autoavaliação, avaliação pelo gestor e acompanhamento de etapas

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-012, RF-013, RF-014, RF-020 |
| Título | Configuração de ciclos, autoavaliação, avaliação pelo gestor e status de etapas |
| Descrição | Como RH ou gestor, eu quero conduzir ciclos periódicos configuráveis com autoavaliação, avaliação do gestor e acompanhamento de etapas, para formalizar a avaliação de competências de cada colaborador. |
| Critérios de aceitação | 1. O ciclo tem periodicidade, etapas, participantes e prazos configuráveis (RF-012).<br>2. O colaborador preenche sua autoavaliação no ciclo aberto (RF-013) e o gestor avalia seus liderados (RF-014).<br>3. O sistema exibe o status por colaborador e etapa: não iniciado, em andamento, concluído ou atrasado (RF-020). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q3, Q4, Q6, Q13), Entrevista 2 (Q3, Q4, Q6, Q13) |
| Status | Consolidado |

### RF-015 – Avaliação entre pares (360º com proteção de identidade)

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-015 |
| Título | Avaliação entre pares |
| Descrição | Como colaborador, eu quero avaliar e ser avaliado por colegas que trabalham comigo com proteção de identidade, para ter uma visão mais completa de minhas entregas técnicas e comportamentais sem receio de retaliação. |
| Critérios de aceitação | 1. É possível atribuir avaliadores pares para um avaliado em um ciclo aberto.<br>2. As respostas seguem a proteção de identidade e agregação mínima (RF-019, RF-044, RNF-005, RN-04). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q14, Q16, Q17), Entrevista 2 (Q13, Q14, Q16, Q17) |
| Status | Consolidado |

### RF-021 – Consolidação automática

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-021 |
| Título | Consolidação automática dos resultados |
| Descrição | Como gestor ou RH, eu quero que o sistema consolide autoavaliação, avaliação do gestor e avaliações de pares habilitadas em um resultado final, para eliminar a junção manual de planilhas. |
| Critérios de aceitação | 1. O resultado consolidado é gerado automaticamente sem copiar dados entre arquivos.<br>2. Reúne as avaliações concluídas das fontes habilitadas para o colaborador no ciclo. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q9), Entrevista 2 (Q8, Q9) |
| Status | Consolidado |

### RF-023 – Histórico de avaliações

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-023 |
| Título | Histórico de avaliações |
| Descrição | Como colaborador ou gestor autorizado, eu quero consultar resultados de ciclos anteriores em ordem cronológica, para acompanhar a evolução sem procurar PDFs ou e-mails antigos. |
| Critérios de aceitação | 1. O sistema lista os ciclos anteriores concluídos para consulta por usuário autorizado.<br>2. Dados de ciclos encerrados ficam bloqueados para edição comum (RF-022, RN-03). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q20), Entrevista 2 (Q10, Q20, Q24) |
| Status | Consolidado |

### RF-025, RF-026 e RF-027 – Feedback, Reuniões 1:1 e vínculo 1:1–avaliação–PDI

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-025, RF-026, RF-027 |
| Título | Registro de feedback, reuniões 1:1 e vínculo com avaliação e PDI |
| Descrição | Como gestor ou colaborador, eu quero registrar feedbacks e os pontos discutidos nas reuniões 1:1 no mesmo sistema e relacioná-los aos resultados da avaliação e às ações do PDI, para que o conversado alimente o PDI sem perda de histórico. |
| Critérios de aceitação | 1. É possível registrar e consultar feedbacks associados a colaborador e ciclo (RF-025).<br>2. É possível registrar reuniões 1:1, encaminhamentos e periodicidade configurável (RF-026).<br>3. Registros de 1:1 podem ser vinculados aos resultados da avaliação e às ações do PDI (RF-027). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q3, Q4, Q7, Q9, Q24), Entrevista 2 (Q3, Q17) |
| Status | Consolidado |

### RF-028, RF-029 e RF-030 – Criação, metas, acompanhamento e consulta de PDI

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-028, RF-029, RF-030 |
| Título | Plano Individual de Desenvolvimento (PDI) estruturado |
| Descrição | Como colaborador ou gestor, eu quero criar, consultar e acompanhar o PDI com ações, responsáveis, prazos, status e progresso, para que o plano não vire apenas um arquivo estático esquecido. |
| Critérios de aceitação | 1. Cada ação do PDI possui responsável, prazo, status (Não iniciado, Em andamento, Concluído) e progresso (RF-028, RF-029, RN-05).<br>2. O PDI é consultável pelo próprio colaborador e pelos perfis autorizados (RF-030, RN-01). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q8, Q21, Q22, Q23), Entrevista 2 (Q21, Q22, Q23) |
| Status | Consolidado |

### RF-031 – Reconhecimento simbólico

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-031 |
| Título | Badges e conquistas simbólicas individuais |
| Descrição | Como colaborador, eu quero receber badges individuais ao concluir etapas importantes do PDI, sem ranking entre pessoas, para manter o engajamento no desenvolvimento. |
| Critérios de aceitação | 1. O sistema concede badges individuais.<br>2. Nenhum badge ou tela gera ranking ou classificação pública entre colaboradores (RN-07). |
| Prioridade | Could |
| Fonte(s) | Entrevista 1 (Q25), combinado com restrição da Entrevista 2 (Q26) |
| Status | Consolidado |

### RF-032 – Comparativo autoavaliação–gestor (Gráfico de radar)

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-032 |
| Título | Comparativo visual autoavaliação–gestor |
| Descrição | Como colaborador ou gestor, eu quero visualizar a comparação entre a autoavaliação e a avaliação do gestor (ex.: em gráfico de radar), para identificar claramente onde há divergência de percepção. |
| Critérios de aceitação | 1. Exibe as notas da autoavaliação e do gestor lado a lado ou sobrepostas por competência.<br>2. Disponível para o colaborador e seu gestor autorizado. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q15), Entrevista 2 (Q15) |
| Status | Consolidado |

### RF-033 – Evolução entre ciclos

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-033 |
| Título | Comparação de competências e resultados entre ciclos |
| Descrição | Como colaborador ou gestor, eu quero comparar o ciclo atual com ciclos anteriores, para medir a evolução nos pontos fortes e nos pontos a desenvolver. |
| Critérios de aceitação | 1. Permite comparar dois ou mais ciclos concluídos por competência.<br>2. Destaca a variação entre os períodos. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q19, Q21), Entrevista 2 (Q19, Q21) |
| Status | Consolidado |

### RF-034 – Matriz de habilidades

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-034 |
| Título | Matriz de habilidades por equipe e competência |
| Descrição | Como gestor, eu quero visualizar uma matriz de habilidades da minha equipe por competência, para identificar quem domina determinada habilidade técnica (ex.: SQL, Postman) e quem precisa de treinamento. |
| Critérios de aceitação | 1. Exibe visão da equipe por competência e lacunas de desenvolvimento.<br>2. Não gera ranking público de desempenho geral (RN-07). |
| Prioridade | Must *(subiu de Should para Must após confirmação nos Questionários Q1 e Q2)* |
| Fonte(s) | Entrevista 2 (Q21); confirmado por Q1 e Q2 |
| Status | Consolidado |

### RF-037 – Notificações no sistema

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-037 |
| Título | Notificações internas sobre prazos e pendências |
| Descrição | Como colaborador ou gestor, eu quero receber notificações e lembretes automáticos sobre prazos de ciclos e ações do PDI, para atualizar o progresso a tempo. |
| Critérios de aceitação | 1. O sistema notifica os usuários quando prazos de etapas do ciclo ou ações do PDI se aproximam.<br>2. Canais adicionais (e-mail/push) são tratados como opcionais em RF-038 (Could). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q23, Q27), Entrevista 2 (Q23, Q27) |
| Status | Consolidado |

### RF-050 e RF-051 – Integrações opcionais de tarefas e agenda

| Campo | Conteúdo |
|-------|----------|
| ID Consolidado | RF-050, RF-051 |
| Título | Integração futura de ações do PDI com ferramentas de tarefas (RF-050) e de 1:1 com calendário corporativo (RF-051) |
| Descrição | Como colaborador ou gestor, eu quero poder integrar futuramente as ações do PDI com ferramentas de tarefas (ex.: Azure DevOps) e o agendamento de 1:1 com o calendário corporativo (ex.: Teams/Outlook). |
| Critérios de aceitação | 1. Permite envio opcional de ação do PDI para ferramenta de tarefas (RF-050).<br>2. Permite envio opcional de agendamento de 1:1 para calendário corporativo (RF-051). |
| Prioridade | Could |
| Fonte(s) | Entrevista 1 (Q25 – Teams/Outlook), Entrevista 2 (Q5, Q25 – Azure DevOps) |
| Status | Consolidado |

---

## 4. Requisitos Não Funcionais Derivados das Entrevistas

| ID Consolidado | Requisito | Critério de verificação | Prioridade | Fonte(s) | Status |
|----------------|-----------|-------------------------|------------|----------|--------|
| RNF-003 | **Autorização no servidor.** Negar operações sem permissão independentemente da interface. | Requisições sem autorização de perfil/vínculo são recusadas pelo servidor. | Must | Entrevista 1 (Q18), Entrevista 2 (Q18); Q1/Q2 | Consolidado |
| RNF-005 e RF-044 | **Anonimato 360º.** Não expor identidade de respondentes a gestores ou colegas em relatórios e interfaces. | Relatórios e interfaces de avaliação de pares exibem apenas agregados que atinjam o limiar mínimo e não revelam autoria. | Must | Entrevista 1 (Q16, Q17), Entrevista 2 (Q16, Q17); Q2; PD | Consolidado |
| RNF-006 e RF-046 | **Integridade e trilha de auditoria.** Preservar consistência de dados e registrar alterações relevantes sem revelar autores de respostas anônimas. | Edições concorrentes não sobrescrevem arquivos; ações relevantes geram log com data e responsável. | Must | Entrevista 1 (Q9), Entrevista 2 (Q9, Q18); PD | Consolidado |
| RNF-008 | **Responsividade móvel.** Permitir uso em navegador móvel sem rolagem horizontal em telas de 360 px. | Nas entrevistas o foco foi consulta rápida de alertas; após Q2, foi ampliado para cobrir as tarefas do colaborador como *Should*. | Should | Entrevista 1 (Q27), Entrevista 2 (Q27); ampliado por Q2 | Consolidado |
| RNF-009 | **Compatibilidade.** Funcionamento nas versões atuais de Chrome, Edge, Firefox e navegador móvel. | Fluxos principais executados sem erro nos navegadores de referência em ambiente desktop e móvel. | Should | Entrevista 1 (Q27), Entrevista 2 (Q27); PD (ISO/IEC 25010) | Consolidado |
| RNF-012 | **Usabilidade.** Fluxos diretos, sem burocracia ou preenchimento redundante. | Meta proposta: 90% de usuários de teste concluírem tarefas essenciais sem ajuda; reaproveitamento apoiado por RF-024. | Should | Entrevista 1 (Q26); PD (ISO/IEC 25010) | Consolidado |
| RNF-013 e RF-049 | **Retenção e descarte (LGPD).** Aplicar política de retenção configurável por organização conforme fundamento jurídico. | Descarte ou conservação seguem a política configurada e as exceções legais. | Must | Entrevista 1 (Q18), Entrevista 2 (Q18); Q1/Q2; PD | Consolidado |

---

## 5. Regras de Negócio Identificadas nas Entrevistas

| ID Consolidado | Regra | Fonte(s) nas Entrevistas |
|----------------|-------|--------------------------|
| RN-01 | Só usuários autorizados visualizam avaliações individuais, feedbacks e PDI conforme papel e vínculo hierárquico (colaborador, gestor direto e RH/DHO). Na avaliação top-down (gestor–liderado), a transparência é mantida. | Entrevista 1 (Q16, Q18), Entrevista 2 (Q16, Q18) |
| RN-02 | Questionários são vinculados ao público-alvo (cargo/área/senioridade) e a versão aplicada é preservada. | Entrevista 1 (Q11, Q12), Entrevista 2 (Q11, Q12) |
| RN-03 | Cada ciclo define participantes, etapas e prazos; após encerramento, notas ficam bloqueadas para edição comum. | Entrevista 1 (Q3, Q6), Entrevista 2 (Q3, Q6, Q9) |
| RN-04 | Na avaliação 360º entre pares, respostas anônimas não são expostas individualmente; o gestor visualiza apenas médias consolidadas e feedbacks sem identificação de autoria. | Entrevista 1 (Q16, Q17), Entrevista 2 (Q16, Q17) |
| RN-05 | O PDI possui ações com responsável, prazo, progresso e status, conectadas à avaliação e às reuniões 1:1. | Entrevista 1 (Q3, Q22, Q23, Q24), Entrevista 2 (Q22, Q23) |
| RN-07 | O sistema não expõe notas publicamente à equipe e o reconhecimento simbólico (badges) não gera ranking ou classificação entre colaboradores. | Entrevista 1 (Q25), Entrevista 2 (Q26) |

---

## 6. Encaminhamento dos Pontos Levantados nas Entrevistas

1. **Periodicidade do ciclo (D-01):** E1 relatou 3 a 6 meses e E2 relatou ciclo semestral. Consolidado em `RF-012` com periodicidade e datas configuráveis pelo RH.
2. **Autoria dos questionários (D-02) e escolha de avaliadores 360º (D-03):** Complementados pelos questionários Q1 e Q2 e consolidados em `RF-010` e `RF-018`.
3. **Limiar de anonimato (D-04):** Complementado por Q1 (mínimo 3) e Q2 (mínimo 5), consolidado em `RF-019` e `RF-044`.
4. **Papéis de RH, DP e DHO (D-05):** Unificados no perfil `RH/DHO` com autorização explícita (`RF-003`, `RN-01`).
5. **Prazo de retenção (D-06):** Tratado como política configurável por organização (`RF-049`, `RNF-013`) conforme fundamentação da Pesquisa Documental (`PD`).
6. **Perspectiva de Gestor e RH fora de TI:** Como E1 e E2 tinham perfil predominantemente de avaliados na área de TI, os Questionários Q1 (Gestora de Operações/Logística) e Q2 (Analista de DHO/Saúde) supriram essa lacuna na [questionarios/Sintese-dos-Questionarios.md](file:///c:/Users/kaiqu/Documents/Arquitetura-e-Desenho-de-Software/questionarios/Sintese-dos-Questionarios.md) e na [Marco3_Consolidacao_da_Elicitacao_Lattice.docx](file:///c:/Users/kaiqu/Documents/Arquitetura-e-Desenho-de-Software/Marco3_Consolidacao_da_Elicitacao_Lattice.docx).

