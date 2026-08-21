# Calculadora Jurídica

### Calculadora Jurídica for Claude, ChatGPT and AI agents

Automatic Brazilian legal calculators: monetary correction and debt settlement (correction by IPCA, INPC, IGP-M, SELIC, TR and other official indices + interest, penalty and attorney fees), with indices fetched live from BACEN and IBGE. No credentials; platform-hosted. Built for judgment liquidation, enforcement, collection actions and rent/alimony updates.

- 📊 **16 tools**
- ✏️ **Read and write**
- 💬 **Works with any MCP client**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Magic-link login (no password)**

[Portuguese version](README.md) · [Full docs (PT-BR)](docs/)

---

## One-click install

### Claude (Web and Desktop)

[➕ Open in Claude and connect](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

Manual: [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Add custom connector** → name `Calculadora Jurídica`, URL `https://api.mcp.ai/p_calculo`.

### Cursor

[➕ Install in Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=calculo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYWxjdWxvIn0=)

### VS Code (Copilot Chat)

[➕ Install in VS Code](vscode:mcp/install?name=calculo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_calculo%22%7D)

### Any other MCP-over-HTTP client

```
https://api.mcp.ai/p_calculo
```

---

## 16 tools

| Tool | Description |
|---|---|
| `calculo_atualizar` | Atualização monetária / liquidação de débito judicial: corrige parcelas por um índice oficial (IPCA, INPC, IGP-M, SELIC, TR…) e aplica juros, multa e honorários. |
| `calculo_indice` | Consulta de índice oficial: fator de correção acumulado entre duas datas (mês inicial excluído, mês final incluído — convenção BACEN/IBGE). |
| `calculo_salario_minimo` | Salário mínimo nacional vigente de um ano (dinâmico, IPEADATA). |
| `calculo_aluguel` | Aluguéis em atraso (Lei 8.245/91): reajusta o aluguel ao longo do contrato pelo índice, corrige cada mês atrasado até hoje, aplica juros de mora (1% a.m.) e multa moratória. |
| `calculo_pensao` | Pensão alimentícia em atraso (art. |
| `calculo_trabalhista` | Verbas rescisórias / liquidação trabalhista (CLT): saldo de salário, aviso prévio indenizado (Lei 12.506/2011), 13º proporcional, férias proporcionais + 1/3, férias vencidas, multa de 40%/20% do FGTS, com descontos de… |
| `calculo_fgts` | Correção do FGTS (tese TR → INPC/IPCA-E, STF): por depósito calcula a diferença entre corrigir pelo índice de inflação vs pela TR, com juros de 3% a.a. |
| `calculo_dosimetria` | Dosimetria da pena (art. 68 CP, sistema trifásico): pena-base pelas circunstâncias judiciais (art. 59), pena intermediária por atenuantes/agravantes (Súmula 231 STJ), pena definitiva por causas de aumento/diminuição (… |
| `calculo_progressao` | Progressão de regime (LEP art. |
| `calculo_partilha` | Partilha de bens no divórcio por regime (Código Civil): apura a massa partilhável (bens − dívidas conforme o regime) e a quota de cada cônjuge, com torna por desequilíbrio. |
| `calculo_tempo_contribuicao` | Tempo de contribuição (CNIS): soma os vínculos contando concomitância uma vez e converte atividade especial em comum (fatores EC 103/2019, só até 13/11/2019). |
| `calculo_rmi` | RMI — Renda Mensal Inicial (pós-reforma EC 103/2019): média dos salários de contribuição × coeficiente (60% + 2% por ano acima de 20H/15M), com piso (salário mínimo) e teto (INSS). |
| `calculo_revisional` | Revisional de contrato bancário: recalcula o financiamento pela taxa média de mercado do BACEN (busca ao vivo por modalidade+mês) e apura o excedente por parcela (Price ou SAC). |
| `calculo_superendividamento` | Superendividamento (Lei 14.181/2021): % da renda comprometida, mínimo existencial (R$600, parametrizável), renda disponível e capacidade de pagamento de um plano de até 5 anos. |
| `calculo_rmc_rcc` | RMC/RCC — reserva de margem consignável de cartão (INSS, códigos 217/268): limites de 5% e restituição corrigida dos descontos. |
| `calculo_restituicao_inss` | Restituição de descontos indevidos no INSS (fraude associativa, códigos 280/304/310/378): soma as parcelas descontadas corrigidas. |

---

## Pricing

Free.

---

## License

MIT — see [LICENSE](LICENSE). The MCP server at `api.mcp.ai/p_calculo` is proprietary (hosted); this repo (manifests, docs, skills) is MIT.
