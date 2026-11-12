# Sistema de Gestão de Competências (Análogo: Lattice People Platform)

Repositório oficial da disciplina de **Arquitetura e Desenho de Software — Levantamento, Análise e Especificação de Requisitos**.

## Equipe e Papéis

| Integrante | Papel Principal | Caso de Uso Completo (Cap. 6 Larman) |
|------------|-----------------|--------------------------------------|
| **Kaique Caio de Sousa** | Gerente do Projeto | `UC04` — Gerenciar ciclos de avaliação |
| **Clara Morais Jorge Ribeiro** | Responsável pela Elicitação | `UC03` — Configurar questionários |
| **Miguel Vitta** | Pesquisa Documental e Privacidade | `UC07` — Avaliar pares (avaliação 360º) |
| **Ighor Gonçalves Lima** | Analista do Sistema Análogo e Rastreabilidade | `UC14` — Registrar reunião 1:1 |
| **Victor Hugo Alves de Jesus** | Modelador de Processos (BPMN) | `UC15` — Gerenciar PDI |

---

## Organização por Marcos de Entrega

### Marco 1 — Processo de Requisitos e Pesquisa Documental
- **Processo de Engenharia de Requisitos:** [`processo/Marco1_PROCESSO_REQUISITOS.md`](./processo/Marco1_PROCESSO_REQUISITOS.md)
- **Pesquisa Documental e Legal (LGPD, ANPD, LBI, ISO/IEC 25010):** [`pesquisa-documental/Marco1_Pesquisa_Documental_Legal_Lattice.docx`](./pesquisa-documental/Marco1_Pesquisa_Documental_Legal_Lattice.docx)

### Marco 2 — Entrevistas, Questionários, BPMN e Sistema Análogo
- **Entrevistas (Transcrições e TCLE):**
  - [`entrevistas/Marco2_TCLE_Victor.pdf`](./entrevistas/Marco2_TCLE_Victor.pdf) — Termo de Consentimento Livre e Esclarecido (E1)
  - [`entrevistas/Marco2_Entrevista_1_Victor.pdf`](./entrevistas/Marco2_Entrevista_1_Victor.pdf) — Entrevista 1 (Victor Hugo — Assistente de TI)
  - [`entrevistas/Marco2_Entrevista_2_Kaique.pdf`](./entrevistas/Marco2_Entrevista_2_Kaique.pdf) — Entrevista 2 (Kaique Caio — Analista de Qualidade)
- **Questionários Aplicados:**
  - [`questionarios/Marco2_Questionario_1_Respostas.md`](./questionarios/Marco2_Questionario_1_Respostas.md) — Questionário 1 (Mariana Costa Ribeiro — Coordenadora de Operações)
  - [`questionarios/Marco2_Questionario_2_Respostas.md`](./questionarios/Marco2_Questionario_2_Respostas.md) — Questionário 2 (Rafael Almeida Nunes — Analista de DHO)
- **Modelagem BPMN do Processo Atual (Dores):**
  - [`bpmn/Marco2_BPMN_Processo_Atual_e_Dores.png`](./bpmn/Marco2_BPMN_Processo_Atual_e_Dores.png)
- **Pesquisa das Funcionalidades do Sistema Análogo (Lattice People Platform):**
  - [`sistema-analogo/Marco2_Requisitos_Funcionais_Lattice_People_Platform.docx`](./sistema-analogo/Marco2_Requisitos_Funcionais_Lattice_People_Platform.docx)

### Marco 3 — Consolidação das Sínteses, Lista Geral de Requisitos e Matriz Inicial
- **Sínteses por Fonte e Consolidação da Elicitação:**
  - [`entrevistas/Marco3_Sintese_das_Entrevistas.md`](./entrevistas/Marco3_Sintese_das_Entrevistas.md) — Síntese dos Requisitos das Entrevistas (`E1` e `E2`)
  - [`questionarios/Marco3_Sintese_dos_Questionarios.md`](./questionarios/Marco3_Sintese_dos_Questionarios.md) — Síntese dos Requisitos dos Questionários (`Q1` e `Q2`)
  - [`consolidacao/Marco3_Consolidacao_da_Elicitacao_Lattice.docx`](./consolidacao/Marco3_Consolidacao_da_Elicitacao_Lattice.docx) — **Consolidação Final da Elicitação (v2.0)**
  - [`consolidacao/Marco3_Consolidacao_Preliminar_v1.1.md`](./consolidacao/Marco3_Consolidacao_Preliminar_v1.1.md) e [`.pdf`](./consolidacao/Marco3_Consolidacao_Preliminar_v1.1.pdf) — Histórico da Consolidação Preliminar (v1.1)
- **Lista Geral e Matriz Inicial (`/requisitos`):**
  1. **Lista Geral de Requisitos (`RF-001` a `RF-051` e `RNF-001` a `RNF-016`):** [`requisitos/Marco3_Lista_Geral_de_Requisitos_Lattice.docx`](./requisitos/Marco3_Lista_Geral_de_Requisitos_Lattice.docx)
  2. **Matriz de Rastreabilidade Inicial (Requisitos × Fontes):** [`requisitos/Marco3_Matriz_de_Rastreabilidade_Inicial_Lattice.xlsx`](./requisitos/Marco3_Matriz_de_Rastreabilidade_Inicial_Lattice.xlsx)

### Marco 4 — Visão, Casos de Uso, Protótipos Figma, IEEE 830 / EOR e Matriz Final
1. **Documento de Visão (Cap. 7 Larman):** [`requisitos/Marco4_Documento_de_Visao_Lattice.docx`](./requisitos/Marco4_Documento_de_Visao_Lattice.docx)
2. **Diagrama de Casos de Uso UML (`UC01` a `UC29` — Cap. 6 Larman):** [`requisitos/Marco4_Diagrama_de_Casos_de_Uso_UML.docx`](./requisitos/Marco4_Diagrama_de_Casos_de_Uso_UML.docx)
3. **Casos de Uso Essenciais Detalhados (5 Casos de Uso Completos — 1 por integrante — Cap. 6 Larman):** [`requisitos/Marco4_Casos_de_Uso_Detalhados_Lattice.docx`](./requisitos/Marco4_Casos_de_Uso_Detalhados_Lattice.docx)
4. **Protótipos das Telas (`TELA-01` a `TELA-10` — Telas Exportadas do Figma):** [`requisitos/Marco4_Prototipos_Figma/`](./requisitos/Marco4_Prototipos_Figma/)
5. **Especificação de Requisitos de Software (IEEE 830 / EOR):** [`requisitos/Marco4_Especificacao_de_Requisitos_IEEE_830_Lattice.docx`](./requisitos/Marco4_Especificacao_de_Requisitos_IEEE_830_Lattice.docx)
6. **Matriz de Rastreabilidade Final Atualizada (Horizontal e Vertical):** [`requisitos/Marco4_Matriz_de_Rastreabilidade_Final_Lattice.docx`](./requisitos/Marco4_Matriz_de_Rastreabilidade_Final_Lattice.docx)

---

## Estrutura de Pastas do Repositório

```text
├── README.md
├── Entrega_Completa_Impressao_Lattice.pdf
├── processo/
│   └── Marco1_PROCESSO_REQUISITOS.md
├── pesquisa-documental/
│   └── Marco1_Pesquisa_Documental_Legal_Lattice.docx
├── entrevistas/
│   ├── Marco2_TCLE_Victor.pdf
│   ├── Marco2_Entrevista_1_Victor.pdf
│   ├── Marco2_Entrevista_2_Kaique.pdf
│   └── Marco3_Sintese_das_Entrevistas.md
├── questionarios/
│   ├── Marco2_Questionario_1_Respostas.md
│   ├── Marco2_Questionario_2_Respostas.md
│   └── Marco3_Sintese_dos_Questionarios.md
├── sistema-analogo/
│   └── Marco2_Requisitos_Funcionais_Lattice_People_Platform.docx
├── bpmn/
│   └── Marco2_BPMN_Processo_Atual_e_Dores.png
├── consolidacao/
│   ├── Marco3_Consolidacao_da_Elicitacao_Lattice.docx
│   ├── Marco3_Consolidacao_Preliminar_v1.1.md
│   └── Marco3_Consolidacao_Preliminar_v1.1.pdf
└── requisitos/
    ├── Marco3_Lista_Geral_de_Requisitos_Lattice.docx
    ├── Marco3_Matriz_de_Rastreabilidade_Inicial_Lattice.xlsx
    ├── Marco4_Documento_de_Visao_Lattice.docx
    ├── Marco4_Diagrama_de_Casos_de_Uso_UML.docx
    ├── Marco4_Casos_de_Uso_Detalhados_Lattice.docx
    ├── Marco4_Prototipos_Figma/
    ├── Marco4_Especificacao_de_Requisitos_IEEE_830_Lattice.docx
    └── Marco4_Matriz_de_Rastreabilidade_Final_Lattice.docx
```
