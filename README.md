# Agentes para Contadores — 56 subagentes Claude Code

56 subagentes especializados para contadores brasileiros, prontos para serem usados no Claude Code. Cada agente é um especialista em uma rotina específica do escritório contábil — apurações, obrigações acessórias, fechamento, recuperação de créditos, IRPF, atendimento fiscal — que atua proativamente quando o contexto da conversa bate com sua especialidade.

## Como instalar

1. Clone este repo:
   ```bash
   git clone https://github.com/asv-digital/agents-contadores.git
   ```

2. Copie os agentes para o seu projeto Claude Code:
   ```bash
   cp -r agents-contadores/agents/* /caminho/do/seu/projeto/.claude/agents/
   ```

   Ou, para uso global, copie para `~/.claude/agents/`.

3. No Claude Code, eles passam a ser invocáveis automaticamente quando você pedir algo da especialidade do agente, ou explicitamente via Task tool.

## Como usar

- **Automático**: descreva sua necessidade. Ex.: "preciso apurar o DAS do Simples deste mês". O Claude vai delegar pro agente `apuracao-simples-nacional`.
- **Manual**: peça explicitamente. Ex.: "use o agente `recuperacao-creditos-pis-cofins` para analisar 5 anos retroativos do meu cliente".
- **Em pipeline**: encadeie agentes. Ex.: `revisao-fiscal-cruzamento-sped` → identifica divergência → `malha-fina-pj-diagnostico` → responde intimação.

## Catálogo (56 agentes)

### Apurações tributárias
01 Simples Nacional · 02 Lucro Presumido · 03 Lucro Real · 04 MEI
05 ICMS/ICMS-ST · 06 IPI · 07 ISS · 08 PIS/COFINS Cumulativo · 09 PIS/COFINS Não-Cumulativo
10 IRRF Folha · 11 INSS Empresa · 12 Retenções do tomador

### SPED e obrigações acessórias
13 ECD · 14 ECF · 15 EFD ICMS/IPI · 16 EFD Contribuições · 17 EFD-Reinf
18 DCTFWeb · 19 DIRF · 20 DIMOB · 21 DMED

### eSocial e folha
22 eSocial Admissão · 23 Rescisão · 24 Afastamentos · 25 Eventos periódicos
26 Folha mensal · 27 Férias e 13º · 28 Cálculo de rescisão CLT · 29 FGTS

### Contabilidade e fechamento
30 Plano de contas (CPC) · 31 Lançamentos padrão · 32-35 Conciliações (banco, cartão, fornecedores, clientes)
36 Fechamento mensal · 37 Balancete · 38 DRE gerencial · 39 Fluxo de caixa · 40 Imobilizado e depreciação

### Análise, diagnóstico e recuperação
41 Análise de regime tributário · 42 Recuperação PIS/COFINS · 43 Cruzamento SPED
44 Malha fina PF · 45 Malha fina PJ · 46 Due diligence · 47 Valuation PME

### IRPF
48 IRPF completa · 49 Ganho de capital · 50 Aluguel/carnê-leão · 51 Investimentos em bolsa

### Operacional / Cliente
52 Abertura de empresa · 53 Alteração contratual · 54 Encerramento/baixa
55 Parcelamento RFB · 56 Resposta a fiscalização/intimação

## Avisos legais

- Os agentes refletem a legislação vigente em 2026 e fazem referência a normas específicas (LC 123/2006, IN RFB nº 2.005/2021, CPC, CLT, etc.).
- Outputs gerados são **rascunhos operacionais**; o contador responsável deve revisar e assumir a responsabilidade técnica (CFC).
- Templates e exemplos usam dados fictícios.

## Licença

Uso permitido para clientes ASV Digital / Bravy. Não redistribuir sem autorização.
