# Casos de Uso Essenciais

**Projeto:** Sistema de Gestão de Competências
**Etapa:** Marco 4, item "Diagrama de casos de uso (Cap. 6 Larman)"
**Versão:** 0.1
**Base:** `Documento_de_Visao_Sistema_de_Gestao_de_Competencias.docx` (FT-01 a FT-19 e pontos R01 a R13), `Lista de Requisitos inicial.pdf`, `Sintese-das-Entrevistas.md`, `pesquisa-documental-legal.docx`, `BPMN.png` e `PROCESSO_REQUISITOS.md`

## 1. Como este documento está organizado

Seguimos o estilo de Larman: casos de uso no nível de **objetivo do usuário** (uma tarefa que o ator conclui em uma sessão e que tem valor para ele), escritos como **caixa-preta** (o que o sistema faz, não como faz) e com o formato proporcional à importância. O Documento de Visão (seção 9) pede que os casos de uso detalhem as funcionalidades **FT-01 a FT-19**; a tabela da seção 3 mostra a ligação.

| Formato | Quando usamos | Casos de uso |
|---------|---------------|--------------|
| Completo (*fully dressed*) | Núcleo do sistema, com risco ou regra de negócio relevante | UC01, UC02, UC05, UC06, UC08, UC09 |
| Informal (*casual*) | Essencial, mas sem regra delicada | UC03, UC04, UC07, UC10 |
| Resumido (*brief*) | Apoio, prioridade menor ou ainda dependente de decisão | UC11 a UC23 |

**Responsáveis pelos casos de uso completos** (cada integrante tem pelo menos um):

| Integrante | Caso de uso completo |
|------------|----------------------|
| Clara | UC01 – Configurar questionário |
| Kaique | UC02 – Configurar e iniciar ciclo de avaliação |
| Miguel | UC05 – Avaliar par com anonimato (360º) |
| Ighor | UC06 – Consolidar e compartilhar resultado do ciclo |
| Victor Hugo | UC08 – Registrar reunião 1:1; UC09 – Elaborar PDI |

**Atenção aos identificadores.** Há quatro famílias de IDs nos documentos do grupo, e duas parecem iguais:

| Formato do ID | Documento de origem | Exemplo |
|---------------|---------------------|---------|
| FT-nn | Documento de Visão (funcionalidades) | FT-04 |
| RFnn, RNFnn, RNnn (sem hífen, 2 dígitos) | Síntese das entrevistas, adotada pela Visão | RF06 |
| RF-nnn, RNF-nnn (com hífen, 3 dígitos) | Lista de Requisitos inicial | RF-017 |
| RF-PRIV-nnn, RNF-ACESS-001 | Pesquisa documental; presentes também na Lista e na Visão | RF-PRIV-001 |

**RF06 (síntese) e RF-006 (lista geral) são requisitos diferentes.** Este documento usa os IDs exatamente como nos documentos de origem.

## 2. Atores

Alinhados à seção 3.1 do Documento de Visão.

| Ator | Tipo | Descrição | Fonte |
|------|------|-----------|-------|
| Colaborador | Primário | Responde autoavaliação, avalia pares, consulta resultados e conduz o próprio PDI. Um mesmo colaborador pode ser avaliado e avaliador de pares. | Entrevistas 1 e 2, Visão |
| Gestor direto | Primário | Avalia liderados, conduz reuniões 1:1, compartilha resultados e acompanha o PDI da equipe. | Entrevistas 1 e 2, Visão |
| RH / DP / DHO | Primário | Configura questionários e ciclos, mantém o cadastro de colaboradores, acompanha a execução e define políticas de dados. A divisão de papéis entre RH, DP e DHO está em aberto (ponto R03 da Visão). | Entrevistas 1 e 2, Visão |
| Administrador do sistema | Primário | Responsável técnico na organização: gerencia contas, perfis e permissões e consulta os logs de segurança. | Visão, Lista (RF-005), Consolidação |
| Avaliador par | Papel | Colaborador que avalia um colega de forma anônima (UC05). | Visão |
| Avaliador externo (cliente, parceiro) | Primário, a validar | Previsto no escopo mínimo, sem validação nas entrevistas (ponto R02 da Visão). | Visão |
| Serviço de notificações (e-mail) | De apoio | Entrega lembretes e avisos. | RF14 |
| Teams / Outlook | De apoio (Could) | Agenda convites de 1:1. | RF19 |
| Azure DevOps | De apoio (Could) | Recebe metas do PDI como tarefas. | RF18 |
| Tempo (relógio do sistema) | Externo | Dispara lembretes e encerra prazos. | RF14, RF15 |

Interessados sem interação direta, conforme a Visão: a organização cliente e o encarregado de dados (definem finalidade, base legal e retenção), a diretoria (indicadores gerais), a professora da disciplina e a ANPD, que fiscaliza a conformidade com a LGPD.

## 3. Lista de casos de uso

Prioridade do caso de uso = a maior prioridade das funcionalidades da Visão que ele realiza.

| ID | Caso de uso | Ator principal | Prior. | FT (Visão) | Síntese e pesquisa documental | Lista geral | Formato |
|----|-------------|----------------|--------|------------|-------------------------------|-------------|---------|
| UC01 | Configurar questionário | RH | Must | FT-02 | RF03, RF04 | RF-016 (parcial) | Completo |
| UC02 | Configurar e iniciar ciclo de avaliação | RH | Must | FT-03 | RF05, RF06, RF14 | RF-015, RF-016 | Completo |
| UC03 | Realizar autoavaliação | Colaborador | Must | FT-03 | RF05, RF04 | RF-017 | Informal |
| UC04 | Avaliar liderado | Gestor | Must | FT-03 | RF05, RF04, RN02 | RF-017 | Informal |
| UC05 | Avaliar par com anonimato (360º) | Colaborador | Must | FT-04, FT-06 | RF06, RN01, RN03, RNF04, RF-PRIV-005 | RF-017 (parcial), RNF-014 | Completo |
| UC06 | Consolidar e compartilhar resultado do ciclo | Gestor | Must | FT-07, FT-12 | RF07, RF02, RN03, RN04 | RF-018, RF-019 | Completo |
| UC07 | Consultar resultado, comparação e histórico | Colaborador | Must | FT-08, FT-09, FT-12 | RF02, RF08, RF09, RF10 | RF-018, RF-019 | Informal |
| UC08 | Registrar reunião 1:1 | Gestor | Must | FT-16 | RF16 | **nenhum** | Completo |
| UC09 | Elaborar PDI | Colaborador | Must | FT-13 | RF13, RF10, RF16 | RF-024, RF-025, RF-027 | Completo |
| UC10 | Acompanhar PDI e registrar check-in | Colaborador | Must | FT-13, FT-14 | RF13, RF15, RF14 | RF-026, RF-027 | Informal |
| UC11 | Acompanhar progressão (dashboard individual) | Colaborador | Must | FT-10 | RF11 | RF-033 (parcial) | Resumido |
| UC12 | Consultar matriz de habilidades da equipe | Gestor | Should | FT-11 | RF12, RN05 | RF-035 (parcial) | Resumido |
| UC13 | Acessar o sistema e gerenciar contas e perfis | Administrador do sistema | Must | FT-01 | RF17, RN04 | RF-001 a RF-005 | Resumido |
| UC14 | Enviar notificações e lembretes | Tempo | Must | FT-15 | RF14, RF15 | **nenhum** | Resumido |
| UC15 | Auditar acessos e alterações | RH ou Administrador | Must | FT-17 | RNF03, RNF05 | RNF-012 | Resumido |
| UC16 | Atender requisição de titular de dados | Colaborador | Must | FT-17 | RNF07, RF-PRIV-001 | RF-037 a RF-039, RF-041 | Resumido |
| UC17 | Definir política de retenção de dados | RH | Must | FT-17 | RNF07, RF-PRIV-003 | RNF-013 | Resumido |
| UC18 | Enviar meta do PDI ao Azure DevOps | Colaborador | Could | FT-18 | RF18 | **nenhum** | Resumido |
| UC19 | Agendar 1:1 no Teams/Outlook | Gestor | Could | FT-18 | RF19 | **nenhum** | Resumido |
| UC20 | Conceder conquista simbólica (badge) | Colaborador | Could | FT-19 | RF20, RN06 | RF-023 (relacionado) | Resumido |
| UC21 | Avaliar o gestor e fornecer feedback externo | Colaborador / Avaliador externo | Should | FT-05 | sem requisito na síntese | **nenhum** | Resumido |
| UC22 | Classificar dados sensíveis | Administrador do sistema | Must | FT-17 | RF-PRIV-004 | RF-040 | Resumido |
| UC23 | Manter cadastro mínimo de colaboradores e hierarquia | RH | Must | FT-01 | premissa da Visão (4.3) | RF-006 a RF-009 | Resumido |

**Cobertura das funcionalidades da Visão:** todas as 19 têm ao menos um caso de uso.

| FT | Casos de uso | FT | Casos de uso |
|----|--------------|----|--------------|
| FT-01 | UC13, UC23 | FT-11 | UC12 |
| FT-02 | UC01 | FT-12 | UC06, UC07 |
| FT-03 | UC02, UC03, UC04 | FT-13 | UC09, UC10 |
| FT-04 | UC05 | FT-14 | UC10 |
| FT-05 | UC21 | FT-15 | UC14 |
| FT-06 | UC05, UC06 | FT-16 | UC08 |
| FT-07 | UC06 | FT-17 | UC15, UC16, UC17, UC22 |
| FT-08 | UC06, UC07 | FT-18 | UC18, UC19 |
| FT-09 | UC07 | FT-19 | UC20 |
| FT-10 | UC11 | | |

Os requisitos não funcionais RNF01 (web em desktop) e RNF02 (acesso móvel básico) valem para todos os casos de uso e não geram um caso de uso próprio.

Ligação com as dores do BPMN: D1 (sem histórico) → UC06, UC07; D2 (metas esquecidas) → UC09, UC10, UC14; D3 (1:1 desconectada) → UC08, UC09; D4 (consolidação lenta) → UC06; D5 (questionário genérico) → UC01; D6 (informação descentralizada) → todos, por estarem em uma única plataforma.

## 4. Casos de uso completos

### UC01 – Configurar questionário

- **Responsável:** Clara
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** RH. Ainda não se sabe se o gestor também cria questionários (ponto R06 da Visão); até lá, assumimos que o gestor só consulta.
- **Interessados e interesses:**
  - RH: montar questionários sem refazer planilhas a cada ciclo.
  - Gestor: perguntas específicas para a função da equipe (ex.: ferramentas de teste para QA).
  - Colaborador: ser avaliado nas competências do próprio cargo, não em perguntas genéricas.
- **Pré-condições:** RH autenticado; cargos, áreas e níveis de senioridade cadastrados.
- **Garantia de sucesso:** questionário salvo, associado a cargo, área e senioridade, e disponível para ser usado em ciclos. Questionários já usados não têm as respostas antigas alteradas.
- **Cenário principal de sucesso:**
  1. O RH escolhe criar um questionário novo ou duplicar um existente.
  2. O sistema pede nome, descrição e público (cargo, área e senioridade).
  3. O RH adiciona uma competência ou pergunta, escolhe o tipo (escala numérica de 1 a 5, múltipla escolha ou texto livre) e a categoria (técnica ou comportamental).
  4. Para perguntas de escala, o RH ativa a justificativa em texto livre.
  5. O RH repete os passos 3 e 4 até concluir.
  6. O RH pré-visualiza o questionário como o respondente verá.
  7. O RH salva.
  8. O sistema valida e publica o questionário.
- **Extensões:**
  - 3a. A escala informada não é de 1 a 5: o sistema rejeita e mostra o intervalo aceito.
  - 7a. O questionário não tem perguntas ou não tem público: o sistema bloqueia a publicação e indica o que falta.
  - 7b. O questionário já foi usado em um ciclo: o sistema cria uma **nova versão** e mantém a anterior intacta para o histórico.
  - \*a. A sessão expira durante a edição: o sistema preserva o rascunho.
- **Requisitos especiais:** poucos cliques e sem campos repetidos (RNF06); versões antigas preservadas (RNF05).
- **Variações de tecnologia e dados:** tipos de pergunta (escala, múltipla escolha, texto livre); categorias técnica e comportamental.
- **Frequência:** algumas vezes por semestre.
- **Requisitos realizados:** RF03, RF04, RNF05, RNF06. **Visão:** FT-02. **Lista geral:** RF-016 (parcial: a lista não detalha tipos de pergunta nem personalização por cargo e senioridade).

### UC02 – Configurar e iniciar ciclo de avaliação

- **Responsável:** Kaique
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** RH
- **Interessados e interesses:**
  - RH: iniciar o ciclo sem montar e enviar planilhas por e-mail (dor D6) e acompanhar quem está atrasado.
  - Gestor: receber suas avaliações pendentes já atribuídas.
  - Colaborador: saber o que fazer e até quando.
- **Pré-condições:** RH autenticado; pelo menos um questionário publicado (UC01); colaboradores e gestores diretos cadastrados.
- **Garantia de sucesso:** ciclo criado com período, etapas, prazos, participantes e questionários; avaliações atribuídas; participantes notificados; início registrado.
- **Cenário principal de sucesso:**
  1. O RH cria um ciclo informando nome e período.
  2. O RH escolhe as etapas: autoavaliação, avaliação do gestor, 360º por pares e reunião de feedback, e define o prazo de cada uma.
  3. O RH seleciona os participantes (por área, cargo ou individualmente).
  4. O sistema associa a cada participante o questionário do seu cargo e nível, por etapa.
  5. Se o 360º estiver ativo, o RH define como os pares são escolhidos e o número máximo de pares por avaliado.
  6. O sistema mostra um resumo com as inconsistências encontradas.
  7. O RH confirma o início.
  8. O sistema cria as avaliações, registra o início e dispara as notificações (UC14).
  9. O RH acompanha o status de cada etapa por colaborador.
- **Extensões:**
  - 4a. Um cargo não tem questionário: o sistema lista a pendência e impede o início para esses participantes até que seja resolvida (UC01).
  - 6a. Um colaborador não tem gestor direto: o sistema sinaliza e exclui o colaborador até a correção.
  - 6b. Prazos incoerentes (fim antes do início, etapas fora de ordem): o sistema rejeita.
  - 6c. Um avaliado não tem pares suficientes para o 360º: o sistema avisa e permite seguir sem a etapa para ele.
  - 9a. O RH prorroga um prazo: o sistema notifica os envolvidos e registra quem alterou e quando.
- **Requisitos especiais:** período e prazos configuráveis, com ciclo semestral como padrão mas sem fixar a periodicidade (ponto a validar 1 da síntese); alterações registradas (RNF03).
- **Frequência:** um ciclo por semestre; acompanhamento diário durante o ciclo.
- **Requisitos realizados:** RF05, RF06, RF14, RNF03. **Visão:** FT-03. **Lista geral:** RF-015, RF-016.

### UC05 – Avaliar par com anonimato (360º)

- **Responsável:** Miguel
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** Colaborador (no papel de avaliador de par)
- **Interessados e interesses:**
  - Avaliador: dar feedback sincero sem medo de retaliação.
  - Avaliado: receber uma visão justa e útil das suas entregas.
  - Gestor: entender o cenário da equipe, sem identificar quem escreveu o quê.
  - RH: um 360º que a equipe considere seguro.
- **Pré-condições:** ciclo ativo com etapa 360º; o colaborador foi designado como par do avaliado; prazo aberto.
- **Garantia de sucesso:** respostas salvas e enviadas sem vínculo exibível entre autor e resposta. Nenhum perfil (gestor, RH ou administrador) consegue identificar o autor em tela, relatório ou exportação.
- **Cenário principal de sucesso:**
  1. O avaliador abre suas avaliações pendentes e escolhe a avaliação de par.
  2. O sistema informa que as respostas são anônimas e quem verá os resultados agregados.
  3. O sistema apresenta o questionário de pares.
  4. O avaliador responde (escala de 1 a 5, múltipla escolha e texto livre).
  5. O avaliador revisa e envia.
  6. O sistema grava a resposta **separada da identidade do autor**, registrando apenas que o avaliador concluiu a etapa.
  7. O sistema atualiza o progresso do ciclo, sem revelar quem respondeu o quê.
- **Extensões:**
  - 2a. O avaliador não conhece o avaliado e quer recusar: o sistema permite recusar, se o RH habilitou, e avisa o RH sem expor o motivo ao avaliado (quem define os pares e se o par pode recusar é o ponto R06 da Visão).
  - 4a. O avaliador salva rascunho e retoma depois.
  - 4b. A nota está fora da escala: o sistema rejeita.
  - 5a. O prazo já encerrou: o sistema bloqueia o envio e informa.
  - 6a. Falha no envio: o sistema mantém o rascunho e avisa o avaliador.
- **Requisitos especiais:**
  - Nenhuma tela, relatório ou exportação revela o autor (RNF04).
  - Logs de acesso e trilha de auditoria **não podem permitir ligar uma resposta anônima a uma pessoa**. A pesquisa documental (seção 5) aponta esse conflito entre anonimato e auditoria: o registro de acesso fica em estrutura separada da resposta.
  - Resultados do 360º só aparecem quando houver um número mínimo de respostas, para impedir reidentificação em grupos pequenos (LGPD, art. 12; RF-PRIV-005). O valor mínimo está em aberto (ponto R10 da Visão); a pesquisa cita ao menos 3 respondentes no Lattice.
- **Frequência:** uma vez por ciclo, para cada par designado (vários avaliados por pessoa).
- **Riscos apontados nas entrevistas:** tempo gasto por todos avaliarem todos e maturidade da equipe para dar e receber feedback.
- **Requisitos realizados:** RF06, RF04, RN01, RN03, RNF04, RF-PRIV-005. **Visão:** FT-04, FT-06 (riscos R08, R09 e R10). **Lista geral:** RF-017 e RNF-014 apenas em parte; a lista não tem requisito de avaliação 360º nem de anonimato nas respostas.

### UC06 – Consolidar e compartilhar resultado do ciclo

- **Responsável:** Ighor
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** Gestor direto
- **Interessados e interesses:**
  - Gestor: fechar a avaliação sem juntar planilhas na mão (dor D4).
  - Colaborador: receber um resultado completo e claro, com a devolutiva.
  - RH: ciclos encerrados com dados íntegros e no histórico.
- **Pré-condições:** o prazo das etapas obrigatórias encerrou ou elas foram concluídas; o gestor já avaliou o colaborador (UC04).
- **Garantia de sucesso:** relatório final gerado e compartilhado; reunião de feedback registrada; ciclo do colaborador encerrado; dados do ciclo preservados e não sobrescritos.
- **Cenário principal de sucesso:**
  1. O gestor abre o resultado consolidado de um liderado.
  2. O sistema reúne autoavaliação, avaliação do gestor e 360º (quando houver) sem cópia manual de dados.
  3. O sistema exibe o gráfico de radar com a autoavaliação sobreposta à nota do gestor, os pontos fortes e a desenvolver e a comparação com o ciclo anterior, quando existir.
  4. O gestor revisa e inclui um comentário final.
  5. O gestor realiza a reunião de feedback e registra data e pontos tratados.
  6. O gestor compartilha o resultado com o colaborador.
  7. O sistema libera a visualização ao colaborador e o notifica (UC14).
  8. O sistema encerra o ciclo do colaborador e grava o resultado no histórico, sem permitir sobrescrita.
- **Extensões:**
  - 2a. Há etapas pendentes: o sistema mostra o que falta; o gestor aguarda, ou o RH prorroga ou encerra com as pendências assinaladas.
  - 2b. O 360º tem menos respostas que o mínimo: o sistema não exibe as médias do 360º e mostra apenas a contagem de respostas.
  - 6a. Pode ser necessária revisão do RH antes do compartilhamento; isso ainda não foi decidido.
  - 8a. Correção após o encerramento: só por **reabertura** feita pelo RH, com registro da versão anterior e de quem alterou.
- **Requisitos especiais:**
  - A avaliação do gestor é identificada (RN02).
  - Em avaliações anônimas o gestor vê só médias e comentários misturados (RN03).
  - O resultado só é visível ao colaborador, ao gestor direto e ao RH/DP/DHO (RN04), sem ranking entre colaboradores (RN05).
  - Alterações registradas com versão anterior (RNF05, RNF03).
- **Frequência:** uma vez por ciclo, para cada liderado.
- **Requisitos realizados:** RF07, RF05, RF08, RF09, RF10, RF02, RN02, RN03, RN04, RN05, RNF05. **Visão:** FT-07, FT-08, FT-12. **Lista geral:** RF-018, RF-019.

### UC08 – Registrar reunião 1:1

- **Responsável:** Victor Hugo
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** Gestor direto (o colaborador também pode registrar)
- **Interessados e interesses:**
  - Gestor e colaborador: não depender da memória na hora de montar o PDI (dor D3).
  - RH: histórico de acompanhamento ligado à avaliação formal.
- **Pré-condições:** gestor e colaborador autenticados e com vínculo ativo.
- **Garantia de sucesso:** registro com data, pauta e pontos discutidos, vinculado a competências ou metas do PDI, salvo no histórico e visível aos dois.
- **Cenário principal de sucesso:**
  1. O gestor seleciona o colaborador e escolhe registrar um novo 1:1.
  2. O sistema exibe o contexto: pontos do último 1:1 e metas do PDI com seu status.
  3. Gestor e colaborador informam data e pauta.
  4. Durante ou depois da reunião, registram os pontos discutidos.
  5. Vinculam pontos a competências ou a metas do PDI.
  6. O gestor salva.
  7. O sistema grava o registro no histórico e o deixa disponível aos dois.
- **Extensões:**
  - 3a. O colaborador adiciona itens à pauta antes da reunião.
  - 5a. Um ponto não se liga a nenhuma competência ou meta: o sistema permite salvá-lo sem vínculo.
  - 6a. Edição posterior: o sistema mantém a versão anterior (RNF05).
  - \*a. Perda de conexão: o sistema preserva o rascunho.
- **Requisitos especiais:** cadência configurável, pois as entrevistas citam 1:1 quinzenal e ciclos de 3 a 6 meses (ponto a validar 1); se o RH vê o conteúdo dos 1:1 ainda não foi decidido.
- **Frequência:** quinzenal por colaborador.
- **Observação:** os 1:1 não fazem parte das funcionalidades mínimas do enunciado; entram por justificativa da Entrevista 1, conforme o processo (seção 3.4).
- **Requisitos realizados:** RF16, RF02, RN04, RNF05. **Visão:** FT-16. **Lista geral:** nenhum requisito de 1:1.

### UC09 – Elaborar PDI

- **Responsável:** Victor Hugo
- **Escopo:** Sistema de Gestão de Competências
- **Nível:** objetivo do usuário
- **Ator principal:** Colaborador, com o gestor direto como validador
- **Interessados e interesses:**
  - Colaborador: um plano que não vire "apenas um arquivo guardado" (dor D2).
  - Gestor: metas claras, ligadas ao que foi avaliado e conversado.
  - RH/DP: PDI estruturado e acompanhável.
- **Pré-condições:** resultado do ciclo compartilhado (UC06) com pontos a desenvolver.
- **Garantia de sucesso:** PDI com pelo menos uma meta com descrição, prazo e status "Não iniciado", confirmado pelo gestor, com lembretes agendados.
- **Cenário principal de sucesso:**
  1. O colaborador abre o PDI do ciclo.
  2. O sistema mostra os pontos a desenvolver da avaliação e os registros de 1:1 do período.
  3. O colaborador cria uma meta a partir de um ponto a desenvolver (ou uma meta livre).
  4. Informa descrição, prazo e competência relacionada.
  5. Repete os passos 3 e 4.
  6. O colaborador envia o PDI ao gestor.
  7. O gestor revisa, ajusta as metas e confirma.
  8. O sistema grava o PDI com todas as metas em "Não iniciado" e agenda os lembretes de prazo (UC14).
- **Extensões:**
  - 3a. O gestor também pode criar metas.
  - 4a. O prazo está no passado: o sistema rejeita.
  - 7a. O gestor pede ajuste: o PDI volta ao colaborador com o comentário.
  - 1a. Não há resultado compartilhado ainda: o sistema permite criar metas livres e as liga aos pontos a desenvolver depois.
- **Requisitos especiais:** o PDI nunca é um campo único de texto (RF13); só colaborador, gestor direto e RH/DP/DHO o veem (RN04). A estrutura do PDI no Lattice (RF-CRES-005, RF-CRES-006) serve de referência, mas trilhas de carreira estão fora do escopo (Won't have da Visão, seção 5.3).
- **Frequência:** uma vez por ciclo, com revisões ao longo dele.
- **Requisitos realizados:** RF13, RF10, RF16, RF14, RN04. **Visão:** FT-13. **Lista geral:** RF-024, RF-025, RF-027.

## 5. Casos de uso informais

### UC03 – Realizar autoavaliação

O colaborador abre a avaliação pendente do ciclo (UC02) e responde ao questionário do seu cargo e nível, com escala de 1 a 5 e justificativa em texto livre quando houver. Pode salvar rascunho e voltar. Ao revisar e enviar, o sistema grava a resposta, marca a etapa como concluída e atualiza o status visto pelo RH. 
*Alternativas:* o prazo venceu, então o sistema bloqueia o envio e o RH pode reabrir a etapa; há pergunta obrigatória sem resposta, então o sistema indica quais faltam; a nota está fora da escala, então o sistema rejeita. 
*Requisitos:* RF05, RF04, RF14. Visão: FT-03. Lista geral: RF-017.

### UC04 – Avaliar liderado

O gestor vê a lista de liderados com a avaliação pendente, abre cada um e responde ao questionário correspondente, justificando as notas em texto livre. A avaliação do gestor é **identificada**, sem anonimato (RN02). Ao enviar, o sistema grava e atualiza o progresso do ciclo. 
*Alternativas:* o gestor salva rascunho; o colaborador ainda não fez a autoavaliação, então o sistema avisa mas permite avaliar (se o gestor deve ver a autoavaliação antes ou depois de escrever a sua ainda não foi decidido); o prazo venceu, então o envio é bloqueado. 
*Requisitos:* RF05, RF04, RN02. Visão: FT-03. Lista geral: RF-017.

### UC07 – Consultar resultado, comparação e histórico

O colaborador abre o resultado de um ciclo já compartilhado e vê o gráfico de radar com a autoavaliação sobreposta à nota do gestor, os pontos fortes e as competências a desenvolver (separando técnicas e comportamentais). Seleciona outro ciclo para comparar e o sistema destaca a variação por competência (melhora, queda ou estabilidade). Também consulta a linha do tempo dos ciclos anteriores, com notas, feedbacks, metas e PDI de cada período. O gestor faz o mesmo para os seus liderados. 
*Alternativas:* não há ciclo anterior, então o sistema mostra só o atual; o resultado ainda não foi compartilhado, então fica indisponível; alguém tenta abrir dados de outro colaborador sem permissão, então o sistema nega o acesso e registra a tentativa (RNF03). 
*Requisitos:* RF02, RF08, RF09, RF10, RN04, RN05. Visão: FT-08, FT-09, FT-12. Lista geral: RF-018, RF-019.

### UC10 – Acompanhar PDI e registrar check-in

Na periodicidade configurada (sugestão mensal), o sistema pede o check-in (UC14). O colaborador abre o PDI, atualiza o status de cada meta (Não iniciado, Em andamento, Concluído) e registra o progresso. O gestor vê a atualização, pode comentar e o check-in fica no histórico. 
*Alternativas:* uma meta venceu sem atualização, então o sistema envia novo lembrete; o colaborador precisa mudar um prazo, então o sistema pede o novo prazo e registra a alteração; atualizar o status deve ser possível em poucos cliques (meta de usabilidade proposta, a validar: até 3 cliques, RNF06). 
*Requisitos:* RF13, RF15, RF14, RNF06. Visão: FT-13, FT-14 (os check-ins são Should; o acompanhamento do status das metas é Must). Lista geral: RF-026, RF-027.

## 6. Casos de uso resumidos

| ID | Caso de uso | Descrição em uma frase | Requisitos |
|----|-------------|------------------------|------------|
| UC11 | Acompanhar progressão | O colaborador vê, na tela inicial, o status das metas do PDI e um gráfico de evolução das competências ao longo dos ciclos. | RF11; FT-10 |
| UC12 | Consultar matriz de habilidades da equipe | O gestor filtra por competência (ex.: SQL, Postman) e vê o nível de cada pessoa da equipe, sem ordenar por desempenho geral. | RF12, RN05; FT-11 |
| UC13 | Acessar o sistema e gerenciar contas e perfis | O usuário entra com credenciais individuais e o administrador cria, edita, ativa e desativa contas e atribui os perfis colaborador, gestor direto, RH/DP/DHO e administrador, que definem o que cada um enxerga. | RF17, RN04; FT-01; RF-001 a RF-005 |
| UC14 | Enviar notificações e lembretes | O sistema avisa prazos de etapas do ciclo, de metas do PDI e de check-ins, por um canal ainda a definir (ponto R07 da Visão). | RF14, RF15; FT-15 |
| UC15 | Auditar acessos e alterações | O RH ou o administrador consulta quem acessou e quem alterou avaliações, PDI e feedbacks, com usuário, data/hora e ação. O registro de acesso fica separado das respostas anônimas (R09). | RNF03, RNF05; FT-17; RNF-012 |
| UC16 | Atender requisição de titular de dados | O colaborador pede acesso, correção, eliminação ou portabilidade dos seus dados, e o RH atende com registro e prazo (LGPD, art. 18). | RNF07, RF-PRIV-001; FT-17; RF-037 a RF-039, RF-041 |
| UC17 | Definir política de retenção de dados | O RH configura quanto tempo cada tipo de dado é guardado e o sistema elimina ou anonimiza ao fim do prazo. Nenhuma fonte definiu o prazo (ponto R05 da Visão). | RNF07, RF-PRIV-003; FT-17; RNF-013 |
| UC18 | Enviar meta do PDI ao Azure DevOps | O colaborador envia uma meta como tarefa para o quadro de trabalho via API. | RF18; FT-18 |
| UC19 | Agendar 1:1 no Teams/Outlook | O gestor cria, a partir do sistema, o convite do 1:1 no calendário. | RF19; FT-18 |
| UC20 | Conceder conquista simbólica | Ao concluir marcos do PDI, o colaborador ganha badges individuais que não geram ranking (R11). | RF20, RN06; FT-19 |
| UC21 | Avaliar o gestor e fornecer feedback externo | O colaborador avalia o próprio gestor (avaliação ascendente) e o avaliador externo responde a um questionário próprio, ambos com a proteção de identidade a definir. Sem evidência nas entrevistas, vem do escopo mínimo (ponto R02 da Visão). | FT-05; escopo mínimo; Lattice RF-DESEMP-008 |
| UC22 | Classificar dados sensíveis | O administrador marca campos como dado sensível, com acesso restrito e base legal registrada por finalidade. | RF-PRIV-004; FT-17; RF-040 |
| UC23 | Manter cadastro mínimo de colaboradores e hierarquia | O RH cadastra ou importa colaboradores, cargo, área, senioridade e gestor direto, que são pré-condição do UC01 e do UC02. A forma (importação ou manual) está em aberto. | Visão 4.3; FT-01; RF-006 a RF-009 |
