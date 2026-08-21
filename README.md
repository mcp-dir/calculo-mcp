# Calculadora Jurídica

### Calculadora Jurídica para Claude, ChatGPT e agentes de IA

Calculadoras jurídicas automáticas: atualização monetária e liquidação de débitos (correção por IPCA, INPC, IGP-M, SELIC, TR e outros índices oficiais + juros, multa e honorários), com índices buscados ao vivo no BACEN e IBGE. Sem credencial; hospedado pela plataforma. Ideal para liquidação de sentença, execução, ação de cobrança e atualização de aluguel/pensão.

- 📊 **16 ferramentas**
- ✏️ **Leitura e escrita**
- 💬 **Funciona com qualquer cliente MCP**: Claude Desktop, Cursor, VS Code, Cline, Continue
- 🔑 **Login via magic-link (sem senha)**

[English version](README.en.md) · [Documentação completa](docs/) · [Skill pra agentes](skills/)

---

## Instalar em 1 clique

### Claude (Web e Desktop)

A Anthropic unificou a instalação de MCPs em `claude.ai/customize/connectors`. **O mesmo link serve pra Claude Web e Claude Desktop** (basta estar logado):

[➕ Abrir no Claude e conectar](https://claude.ai/new?modal=add-custom-connector#settings/customize-connectors)

**Manual** (se o deeplink não abrir): [claude.ai/customize/connectors](https://claude.ai/customize/connectors?surface=cowork) → **+** → **Adicionar conector personalizado** → cole **Nome** `Calculadora Jurídica` e **URL** `https://api.mcp.ai/p_calculo`.

### Cursor

[➕ Instalar Calculadora Jurídica no Cursor](cursor://anysphere.cursor-deeplink/mcp/install?name=calculo&config=eyJ1cmwiOiJodHRwczovL2FwaS5tY3AuYWkvcF9jYWxjdWxvIn0=)

### VS Code (Copilot Chat)

[➕ Instalar Calculadora Jurídica no VS Code](vscode:mcp/install?name=calculo&config=%7B%22type%22%3A%22http%22%2C%22url%22%3A%22https%3A%2F%2Fapi.mcp.ai%2Fp_calculo%22%7D)

### ChatGPT, Manus, OpenClaw e mais 40+ clientes

Funciona em qualquer cliente MCP que suporte **MCP over HTTP**. A URL do servidor é sempre:

```
https://api.mcp.ai/p_calculo
```

Detalhes por cliente: [INSTALL.md](INSTALL.md).

---

## Exemplos de uso

```
Atualize R$ 10.000 de 10/03/2024 até hoje pelo INPC com juros de 1% ao mês
Qual o fator de correção do IGP-M entre janeiro e dezembro de 2025?
Liquide esta sentença: parcelas de débito + abatimentos, IPCA-E + juros + honorários de 10%
```

---

## 16 ferramentas disponíveis

| Tool | Descrição |
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

Detalhe de cada tool: [docs/ferramentas.md](docs/ferramentas.md)

---

## Preços

Grátis.

---

## Privacidade & LGPD

- **Sub-processadores**: Banco Central do Brasil (BACEN SGS), IBGE, IPEADATA, o LLM host que você escolher (Claude, ChatGPT, Cursor, agente próprio). Lista completa em [docs/privacidade-lgpd.md](docs/privacidade-lgpd.md).
- Os dados retornados pelas tools são enviados ao **LLM host que você escolher**, sub-processador fora do nosso controle. Recomendamos planos com opt-out de treinamento.

---

## Perguntas frequentes

**O servidor é open source?**
O servidor é proprietário (hosted). Este repositório é o wrapper público com manifestos, docs e skills — tudo MIT.

**Posso usar com agente próprio (não Claude/Cursor)?**
Sim — qualquer cliente que suporte MCP over HTTP. URL: `https://api.mcp.ai/p_calculo`.


---

## Suporte

- 📧 [calculo@mcp.ai](mailto:calculo@mcp.ai)
- 🐛 [GitHub Issues](https://github.com/mcp-dir/calculo-mcp/issues)
- 📄 [docs/](docs/)

---

## Licença

MIT — veja [LICENSE](LICENSE). O servidor MCP em `api.mcp.ai/p_calculo` é proprietário (hosted); este repositório (manifestos, docs, skills) é MIT.
