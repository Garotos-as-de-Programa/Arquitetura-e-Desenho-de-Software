# Síntese dos Requisitos das Entrevistas

**Projeto:** Sistema de Gestão de Competências
**Etapa:** 1ª Etapa – Levantamento de Requisitos
**Responsável pela elicitação:** Clara Morais Jorge Ribeiro
**Versão:** 1.0

## 1. Fontes

| Fonte | Entrevistado | Função / Empresa | Data | Duração | Consentimento | Áudio |
|-------|--------------|------------------|------|---------|---------------|-------|
| Entrevista 1 | Victor Hugo Alves de Jesus | Assistente de TI, EBM Incorporações | não registrada (12:30) | 30 min | Aceito | Não |
| Entrevista 2 | Kaique Caio de Sousa | Analista de Qualidade, Unimed Goiânia (Tecnologia) | 05/11/2026, 21:17 | 45 min | Sim | Sim |

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

## 3. Requisitos Funcionais

### RF01 – Plataforma centralizada

| Campo | Conteúdo |
|-------|----------|
| ID | RF01 |
| Título | Plataforma centralizada |
| Descrição | Como colaborador, gestor ou RH, eu quero registrar e consultar avaliações, feedbacks, registros de 1:1 e PDI em um único sistema, para não depender de planilhas, e-mails e chats soltos. |
| Critérios de aceitação | 1. Avaliações, feedbacks, registros de 1:1 e PDI são criados e consultados dentro do sistema, sem arquivo externo.<br>2. O colaborador acessa tudo o que lhe diz respeito a partir de um único painel. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q7, Q10, Q24), Entrevista 2 (Q7, Q10, Q24) |
| Status | Proposto |

### RF02 – Histórico contínuo

| Campo | Conteúdo |
|-------|----------|
| ID | RF02 |
| Título | Histórico de ciclos e feedbacks |
| Descrição | Como colaborador, eu quero consultar o histórico de ciclos, metas e feedbacks anteriores, para acompanhar minha evolução sem procurar PDFs ou e-mails. |
| Critérios de aceitação | 1. O sistema lista os ciclos anteriores em ordem cronológica.<br>2. Cada ciclo exibe notas, feedbacks, metas e PDI do período.<br>3. Dados de ciclos encerrados não podem ser sobrescritos. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q20), Entrevista 2 (Q10, Q20, Q24) |
| Status | Proposto |

### RF03 – Questionários personalizáveis

| Campo | Conteúdo |
|-------|----------|
| ID | RF03 |
| Título | Criação e personalização de questionários |
| Descrição | Como gestor ou RH, eu quero criar e personalizar questionários de avaliação por cargo, área e nível de senioridade, para avaliar competências técnicas e comportamentais específicas de cada função. |
| Critérios de aceitação | 1. É possível criar, editar e duplicar questionários.<br>2. Um questionário pode ser associado a cargo, área e senioridade.<br>3. Ao iniciar um ciclo, cada avaliado recebe o questionário correspondente ao seu cargo e nível.<br>4. É possível incluir competências técnicas (ex.: ferramentas de teste) e comportamentais. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q11, Q12), Entrevista 2 (Q11, Q12, Q24) |
| Status | Proposto |

### RF04 – Tipos de pergunta

| Campo | Conteúdo |
|-------|----------|
| ID | RF04 |
| Título | Escala numérica, múltipla escolha e texto livre |
| Descrição | Como gestor ou RH, eu quero montar questionários com escala numérica, múltipla escolha e texto livre, para medir o domínio de competências e registrar justificativas e feedbacks. |
| Critérios de aceitação | 1. O sistema oferece os três tipos de pergunta.<br>2. A escala numérica é de 1 a 5, e respostas fora dela são rejeitadas.<br>3. Perguntas de escala permitem justificativa em texto livre associada à nota. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q12: escala e texto livre), Entrevista 2 (Q12: escala, múltipla escolha e texto livre) |
| Status | Proposto |

### RF05 – Ciclo de avaliação

| Campo | Conteúdo |
|-------|----------|
| ID | RF05 |
| Título | Ciclo com autoavaliação e avaliação do gestor |
| Descrição | Como RH ou gestor, eu quero conduzir ciclos periódicos com autoavaliação, avaliação do gestor e reunião de feedback, para formalizar a avaliação de competências de cada colaborador. |
| Critérios de aceitação | 1. O ciclo tem período e prazos configuráveis (a prática atual é semestral).<br>2. O ciclo contém as etapas de autoavaliação, avaliação do gestor e registro da reunião de feedback.<br>3. O RH vê o status de cada etapa por colaborador. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q3, Q13), Entrevista 2 (Q3, Q4, Q13) |
| Status | Proposto |

### RF06 – Avaliação 360º

| Campo | Conteúdo |
|-------|----------|
| ID | RF06 |
| Título | Avaliação 360º por pares |
| Descrição | Como colaborador, eu quero avaliar e ser avaliado por colegas que trabalham comigo, para ter uma visão mais completa de minhas entregas técnicas e comportamentais. |
| Critérios de aceitação | 1. É possível definir avaliadores pares para um avaliado em um ciclo.<br>2. Os pares respondem a um questionário próprio.<br>3. As respostas seguem as regras RN01, RN03 e o requisito RNF04 (anonimato). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q14), Entrevista 2 (Q13, Q14) |
| Status | Proposto |

### RF07 – Consolidação automática

| Campo | Conteúdo |
|-------|----------|
| ID | RF07 |
| Título | Consolidação automática dos resultados |
| Descrição | Como gestor ou RH, eu quero que o sistema consolide autoavaliação, avaliação do gestor e, quando houver, avaliação 360º em um relatório final, para eliminar a junção manual de planilhas. |
| Critérios de aceitação | 1. O relatório final é gerado sem copiar dados manualmente entre arquivos.<br>2. Ele reúne todas as avaliações concluídas do ciclo para o colaborador.<br>3. Alterações em respostas já enviadas ficam registradas (ver RNF05). |
| Prioridade | Must |
| Fonte(s) | Entrevista 2 (Q8, Q9) |
| Status | Proposto |

### RF08 – Gráfico de radar

| Campo | Conteúdo |
|-------|----------|
| ID | RF08 |
| Título | Gráfico de radar de percepções |
| Descrição | Como colaborador, eu quero ver um gráfico de radar com minha autoavaliação sobreposta à nota do gestor, para identificar visualmente onde há divergência de percepção. |
| Critérios de aceitação | 1. Os eixos do gráfico são as competências avaliadas.<br>2. Autoavaliação e avaliação do gestor aparecem como duas séries sobrepostas e distinguíveis.<br>3. O gráfico está disponível para o colaborador e para o gestor. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q15), Entrevista 2 (Q15) |
| Status | Proposto |

### RF09 – Comparação entre ciclos

| Campo | Conteúdo |
|-------|----------|
| ID | RF09 |
| Título | Comparação entre ciclos |
| Descrição | Como colaborador, eu quero comparar meu ciclo atual com o anterior, para medir minha evolução, principalmente nos pontos a desenvolver. |
| Critérios de aceitação | 1. É possível selecionar dois ciclos e comparar as notas por competência.<br>2. O sistema destaca a variação (melhora, queda ou estabilidade) em cada competência. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q19), Entrevista 2 (Q19) |
| Status | Proposto |

### RF10 – Pontos fortes e pontos a desenvolver

| Campo | Conteúdo |
|-------|----------|
| ID | RF10 |
| Título | Pontos fortes e pontos a desenvolver |
| Descrição | Como colaborador, eu quero ver destacados meus pontos fortes consolidados e as habilidades técnicas ou comportamentais em que devo focar no próximo ciclo, para direcionar meu desenvolvimento. |
| Critérios de aceitação | 1. O resultado do ciclo exibe uma lista de pontos fortes.<br>2. O resultado exibe uma lista de competências a desenvolver, separando técnicas e comportamentais. |
| Prioridade | Should |
| Fonte(s) | Entrevista 1 (Q19), Entrevista 2 (Q19) |
| Status | Proposto |

### RF11 – Dashboard individual

| Campo | Conteúdo |
|-------|----------|
| ID | RF11 |
| Título | Dashboard individual de progressão |
| Descrição | Como colaborador, eu quero um painel com o progresso das metas do PDI e a evolução das minhas competências, para acompanhar minha progressão de carreira. |
| Critérios de aceitação | 1. O painel mostra o status de progresso das metas do PDI.<br>2. O painel mostra um gráfico de evolução das competências ao longo dos ciclos.<br>3. O painel é acessível a partir da tela inicial do colaborador. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q21), Entrevista 2 (Q21, Q24) |
| Status | Proposto |

### RF12 – Matriz de habilidades

| Campo | Conteúdo |
|-------|----------|
| ID | RF12 |
| Título | Matriz de habilidades por competência |
| Descrição | Como gestor, eu quero ver um relatório por competência da minha equipe, para identificar quem domina uma habilidade (ex.: SQL, Postman) e quem precisa de treinamento. |
| Critérios de aceitação | 1. O gestor filtra a matriz por competência.<br>2. A matriz mostra o nível de cada colaborador da equipe naquela competência.<br>3. A matriz não ordena nem classifica colaboradores por desempenho geral (ver RN05). |
| Prioridade | Should |
| Fonte(s) | Entrevista 2 (Q21) |
| Status | Proposto |

### RF13 – PDI estruturado

| Campo | Conteúdo |
|-------|----------|
| ID | RF13 |
| Título | PDI com metas, prazos e status |
| Descrição | Como colaborador ou gestor, eu quero registrar o PDI como metas acompanháveis, com prazo e status, para que ele não vire apenas um arquivo guardado. |
| Critérios de aceitação | 1. Cada meta tem descrição, prazo e status (Não iniciado, Em andamento, Concluído).<br>2. As metas podem ser criadas a partir dos pontos a desenvolver da avaliação.<br>3. Colaborador e gestor conseguem atualizar o status das metas.<br>4. O PDI não é um campo único de texto. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q8, Q22, Q23), Entrevista 2 (Q22, Q23) |
| Status | Proposto |

### RF14 – Notificações e lembretes

| Campo | Conteúdo |
|-------|----------|
| ID | RF14 |
| Título | Notificações e lembretes automáticos |
| Descrição | Como colaborador, eu quero receber lembretes automáticos de prazos, para atualizar o status das metas do PDI e cumprir as etapas do ciclo. |
| Critérios de aceitação | 1. O sistema notifica quando o prazo de uma meta do PDI se aproxima e pede a atualização do status.<br>2. O sistema notifica sobre prazos das etapas do ciclo.<br>3. As notificações podem ser consultadas no celular (ver RNF02). |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q23, Q27), Entrevista 2 (Q23, Q27) |
| Status | Proposto |

### RF15 – Check-ins mensais do PDI

| Campo | Conteúdo |
|-------|----------|
| ID | RF15 |
| Título | Check-ins periódicos do PDI |
| Descrição | Como colaborador, eu quero fazer check-ins mensais das metas do PDI, para medir meu progresso ao longo do ciclo. |
| Critérios de aceitação | 1. O sistema solicita check-ins na periodicidade configurada (sugestão: mensal).<br>2. Cada check-in registra o progresso de cada meta e fica no histórico. |
| Prioridade | Should |
| Fonte(s) | Entrevista 2 (Q23) |
| Status | Proposto |

### RF16 – Registro de 1:1 integrado

| Campo | Conteúdo |
|-------|----------|
| ID | RF16 |
| Título | Registro de 1:1 integrado à avaliação e ao PDI |
| Descrição | Como gestor ou colaborador, eu quero registrar os pontos discutidos nas reuniões 1:1 no mesmo sistema da avaliação e do PDI, para que o conversado alimente o PDI sem eu precisar lembrar de cabeça. |
| Critérios de aceitação | 1. É possível registrar data, pauta e pontos de cada 1:1.<br>2. Os registros ficam consultáveis no histórico.<br>3. Pontos de um 1:1 podem ser vinculados a competências e a metas do PDI.<br>4. Ao montar o PDI, o sistema exibe os registros de 1:1 do período. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q3, Q9, Q24) |
| Status | Proposto |

> Obs.: reuniões 1:1 estão fora das funcionalidades mínimas do escopo. Este requisito entra por justificativa de fonte (Entrevista 1 o aponta como indispensável), conforme a seção 3.4 do processo.

### RF17 – Perfis de acesso

| Campo | Conteúdo |
|-------|----------|
| ID | RF17 |
| Título | Perfis de usuário e permissões |
| Descrição | Como RH, eu quero que o sistema distinga colaborador, gestor direto e RH/DP/DHO, para garantir que cada perfil acesse apenas o que lhe cabe. |
| Critérios de aceitação | 1. Existem os perfis colaborador, gestor direto e RH/DP/DHO.<br>2. As permissões de cada perfil seguem RN04.<br>3. Um usuário sem permissão não visualiza dados de avaliação de outro colaborador. |
| Prioridade | Must |
| Fonte(s) | Entrevista 1 (Q18), Entrevista 2 (Q18) |
| Status | Proposto |

### RF18 – Integração com Azure DevOps

| Campo | Conteúdo |
|-------|----------|
| ID | RF18 |
| Título | Integração via API com Azure DevOps |
| Descrição | Como colaborador, eu quero que as metas do PDI sejam enviadas como tasks para o quadro de trabalho do Azure DevOps, para acompanhá-las junto com minhas demandas do dia a dia. |
| Critérios de aceitação | 1. Uma meta do PDI pode ser enviada como task via API.<br>2. O status da meta e o da task ficam consistentes (sentido da sincronização a definir). |
| Prioridade | Could |
| Fonte(s) | Entrevista 2 (Q5, Q25) |
| Status | Proposto |

### RF19 – Integração com Teams/Outlook

| Campo | Conteúdo |
|-------|----------|
| ID | RF19 |
| Título | Agendamento de 1:1 pelo Teams/Outlook |
| Descrição | Como gestor ou colaborador, eu quero agendar os 1:1 diretamente pelo Teams/Outlook a partir do sistema, para não repetir o agendamento em outra ferramenta. |
| Critérios de aceitação | 1. A partir do sistema é possível criar um convite de 1:1 no calendário do Teams/Outlook.<br>2. O 1:1 agendado aparece vinculado ao registro correspondente (RF16). |
| Prioridade | Could |
| Fonte(s) | Entrevista 1 (Q25) |
| Status | Proposto |

### RF20 – Reconhecimento simbólico (gamificação)

| Campo | Conteúdo |
|-------|----------|
| ID | RF20 |
| Título | Badges e conquistas simbólicas |
| Descrição | Como colaborador, eu quero ganhar conquistas simbólicas ao concluir etapas importantes do PDI, para me manter engajado no plano de desenvolvimento. |
| Critérios de aceitação | 1. O sistema concede badges individuais ao concluir marcos do PDI.<br>2. Badges são exibidos apenas ao próprio colaborador e a quem tem acesso aos seus dados (RN04).<br>3. Badges não geram classificação entre colaboradores (RN06). |
| Prioridade | Could |
| Fonte(s) | Entrevista 1 (Q25) |
| Status | Proposto |

## 4. Requisitos Não Funcionais

| ID | Requisito | Critério de verificação | Prioridade | Fonte(s) | Status |
|----|-----------|------------------------|------------|----------|--------|
| RNF01 | **Plataforma web para desktop.** O sistema deve ser acessível por navegador em computador (ambiente Windows), que é o uso principal. | Todas as funcionalidades Must funcionam nas versões atuais dos principais navegadores em Windows. | Must | Entrevista 1 (Q27), Entrevista 2 (Q27) | Proposto |
| RNF02 | **Acesso móvel básico.** O sistema deve permitir consultar pelo celular notificações, alertas e prazos. | Em tela de celular, notificações e prazos são legíveis e consultáveis sem rolagem horizontal. | Could | Entrevista 1 (Q27), Entrevista 2 (Q27) | Proposto |
| RNF03 | **Logs de segurança e acesso.** O sistema deve registrar quem acessou e quem alterou dados de avaliação, PDI e feedbacks. | Cada acesso e alteração gera um registro com usuário, data/hora e ação, consultável pelo RH ou administrador. | Must | Entrevista 2 (Q18) | Proposto |
| RNF04 | **Anonimato técnico.** O sistema não deve exibir a identidade de respondentes de avaliações anônimas ao gestor, ao RH ou a qualquer outro perfil, em nenhuma tela, relatório ou exportação. | Teste de relatórios, telas e exportações de uma avaliação 360º não revela o autor de nenhuma nota ou comentário. | Must | Entrevista 1 (Q16, Q17), Entrevista 2 (Q16, Q17) | Proposto |
| RNF05 | **Integridade e persistência dos dados.** O sistema deve armazenar continuamente os dados de avaliação e impedir sobrescrita ou perda de informações. | Edições simultâneas não apagam dados de outro usuário; alterações em respostas enviadas ficam registradas com versão anterior preservada. | Must | Entrevista 2 (Q9, Q18), Entrevista 1 (Q9) | Proposto |
| RNF06 | **Usabilidade sem burocracia.** O sistema não deve exigir cliques excessivos nem campos redundantes, e não pode ser mais trabalhoso que a planilha atual. | Atualizar o status de uma meta do PDI em até 3 cliques *(métrica proposta, a validar)*; nenhum dado já informado é solicitado de novo no mesmo ciclo. | Must | Entrevista 1 (Q26) | Proposto |
| RNF07 | **Privacidade e conformidade com a LGPD.** O tratamento dos dados de avaliação deve seguir a LGPD, com acesso restrito e prazo de guarda definido. | Existe política de retenção documentada e aprovada; acessos seguem RN04. Prazo de retenção **a definir** (nenhum entrevistado o informou). | Must | Entrevista 1 (Q18), Entrevista 2 (Q18); complementar com a pesquisa documental | Proposto |

## 5. Regras de Negócio e Restrições

| ID | Regra | Prioridade | Fonte(s) | Status |
|----|-------|------------|----------|--------|
| RN01 | Na avaliação 360º (pares avaliando pares), as respostas são **anônimas**, para garantir sinceridade e evitar retaliação. | Must | Entrevista 1 (Q16), Entrevista 2 (Q16) | Proposto |
| RN02 | Na avaliação do gestor para o liderado, a identidade do avaliador **não é anônima**: a transparência é necessária. | Must | Entrevista 1 (Q16), Entrevista 2 (Q16) | Proposto |
| RN03 | Em avaliações anônimas, o gestor vê apenas as **médias consolidadas** e os **comentários em texto livre misturados**, sem identificar quem atribuiu cada nota ou escreveu cada texto. | Must | Entrevista 1 (Q17), Entrevista 2 (Q17) | Proposto |
| RN04 | Notas, feedbacks e PDI são visíveis **somente** ao próprio colaborador, ao seu gestor direto e ao RH/DP/DHO. Colegas e profissionais de outras áreas não têm acesso em nenhuma hipótese. | Must | Entrevista 1 (Q18), Entrevista 2 (Q18) | Proposto |
| RN05 | O sistema **não** deve expor notas publicamente a outros membros do time nem criar **rankings** de desempenho, para evitar competitividade negativa. | Must | Entrevista 2 (Q26); Entrevista 1 (Q18, no que se refere à visibilidade das notas) | Proposto |
| RN06 | Elementos de reconhecimento (badges) são individuais e **não podem gerar classificação** entre colaboradores. | Should | Entrevista 1 (Q25) combinada com Entrevista 2 (Q26) | Proposto |

## 6. Pontos a validar

1. **Periodicidade do ciclo:** a Entrevista 2 descreve ciclo semestral com 1 a 2 semanas de duração, e a Entrevista 1 fala em 3 a 6 meses, com 1:1s quinzenais. Ciclo e cadência de 1:1 devem ser configuráveis (RF05, RF16).
2. **Papéis de RH, DP e DHO:** a Entrevista 1 cita DHO nas entrevistas de seleção e gestão com DP no PDI, e a Entrevista 2 cita só RH. É preciso definir o papel de cada área no sistema (RF17, RN04).
3. **Prazo de retenção dos dados:** nenhum entrevistado definiu. Alinhar com a pesquisa documental (LGPD) (RNF07).
4. **Quem cria os questionários e define os avaliadores 360º:** as entrevistas não especificam se é RH, gestor ou ambos (RF03, RF06).
5. **Canal das notificações:** e-mail, no próprio sistema ou Teams (RF14).
6. **Gamificação × sem rankings:** RF20 e RN06 existem para conciliar os badges (Entrevista 1) com a restrição da Entrevista 2 (RN05).
7. **Avaliação no recrutamento:** a Entrevista 1 descreve verificação técnica e comportamental na seleção. Não foi registrada como requisito; decidir se entra no escopo ou se vira *Won't have*.
8. **Partes externas:** as perguntas sobre avaliadores externos (clientes, parceiros) não geraram requisito nas duas entrevistas. Essa fonte de feedback, prevista nas funcionalidades mínimas, deve ser coberta por outras fontes (questionários, Lattice).
9. **Risco da avaliação 360º:** os dois apontam maturidade da equipe para dar e receber feedback, e a Entrevista 1 aponta também o tempo gasto. Considerar isso no desenho do fluxo (RF06).
10. **Amostra:** as duas entrevistas são da área de TI e com perfil de avaliado. A visão de gestores e do RH deve vir de questionários ou de outras fontes.
11. **Registro da Entrevista 1:** falta a data da entrevista no registro, exigida no roteiro.
12. **Prioridades:** a prioridade MoSCoW é uma proposta baseada na frequência da demanda e nas funcionalidades mínimas, e precisa ser confirmada na revisão cruzada.
