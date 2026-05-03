# 57 Agents Contabilidade — Claude Code para contadores

**57 subagentes especializados** para contadores brasileiros, prontos para serem usados no Claude Code. Cada agente e um especialista em uma rotina especifica do escritorio contabil — apuracoes, obrigacoes acessorias, fechamento, recuperacao de creditos, IRPF, atendimento fiscal — que atua proativamente quando o contexto da conversa bate com sua especialidade.

## Como instalar

1. Clone este repo:
   ```bash
   git clone https://github.com/asv-digital/agents-contadores.git
   ```

2. Copie os agentes para o seu projeto Claude Code:
   ```bash
   cp -r agents-contadores/agents/* /caminho/do/seu/projeto/.claude/agents/
   ```

   Ou, para uso global: `~/.claude/agents/`.

3. Reinicie o Claude Code (`/exit` e abra de novo). Confirme com `/agents`.

## Como usar

- **Automatico**: "preciso apurar o DAS do Simples deste mes" -> Claude delega pro agente `apuracao-simples-nacional`.
- **Manual**: "use o agente `recuperacao-creditos-pis-cofins` para analisar 5 anos retroativos do meu cliente".
- **Em pipeline**: `revisao-fiscal-cruzamento-sped` -> identifica divergencia -> `malha-fina-pj-diagnostico` -> responde intimacao.

## Catalogo (57 agentes)

### Apuracoes tributarias
01 Simples Nacional · 02 Lucro Presumido · 03 Lucro Real · 04 MEI
05 ICMS/ICMS-ST · 06 IPI · 07 ISS · 08 PIS/COFINS Cumulativo · 09 PIS/COFINS Nao-Cumulativo
10 IRRF Folha · 11 INSS Empresa · 12 Retencoes do tomador

### SPED e obrigacoes acessorias
13 ECD · 14 ECF · 15 EFD ICMS/IPI · 16 EFD Contribuicoes · 17 EFD-Reinf
18 DCTFWeb · 19 DIRF · 20 DIMOB · 21 DMED

### eSocial e folha
22 eSocial Admissao · 23 Rescisao · 24 Afastamentos · 25 Eventos periodicos
26 Folha mensal · 27 Ferias e 13 · 28 Calculo de rescisao CLT · 29 FGTS

### Contabilidade e fechamento
30 Plano de contas (CPC) · 31 Lancamentos padrao · 32-35 Conciliacoes (banco, cartao, fornecedores, clientes)
36 Fechamento mensal · 37 Balancete · 38 DRE gerencial · 39 Fluxo de caixa · 40 Imobilizado e depreciacao

### Analise, diagnostico e recuperacao
41 Analise de regime tributario · 42 Recuperacao PIS/COFINS · 43 Cruzamento SPED
44 Malha fina PF · 45 Malha fina PJ · 46 Due diligence · 47 Valuation PME

### IRPF
48 IRPF completa · 49 Ganho de capital · 50 Aluguel/carne-leao · 51 Investimentos em bolsa

### Operacional / Cliente
52 Abertura de empresa · 53 Alteracao contratual · 54 Encerramento/baixa
55 Parcelamento RFB · 56 Resposta a fiscalizacao/intimacao

### Reforma Tributaria (57) — NOVO
57 CBS / IBS / Imposto Seletivo (EC 132/2023 + LC 214/2025) — simulacao de transicao 2026-2033

## Avisos legais

- Os agentes refletem a legislacao vigente em 2026 e fazem referencia a normas especificas (LC 123/2006, IN RFB n 2.005/2021, EC 132/2023, LC 214/2025, CPC, CLT, etc.).
- Outputs gerados sao **rascunhos operacionais**; o contador responsavel deve revisar e assumir a responsabilidade tecnica (CFC).
- Templates e exemplos usam dados ficticios.

## Licenca

Uso permitido para clientes ASV Digital / Bravy. Nao redistribuir sem autorizacao.
