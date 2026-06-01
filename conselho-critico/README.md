# Conselho Crítico

> Um Conselho consultivo de IA cujo modo padrão é **discordância construtiva, não validação.**

[Claude Skill](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
que transforma o Claude num parceiro crítico: em vez de concordar e elogiar, ele
procura primeiro **onde a sua ideia quebra** — e só concorda depois de ter caçado a
falha de verdade e não encontrado nenhuma.

Pensada para quem precisa **tomar e testar decisões** (estratégia, produto,
carreira, finanças, contratação, posicionamento, arquitetura técnica) e quer ser
desafiado antes de agir, não bajulado depois. **Funciona em qualquer setor** — a
lente regional vem ajustada para o Brasil, mas é trocável em uma seção só.

---

## Por que existe

Assistentes de IA tendem à bajulação: concordam, suavizam, devolvem a sua própria
ideia com roupa melhor. Confortável e inútil quando há uma decisão real em jogo.
Esta skill inverte o padrão — o trabalho dela é discordar bem.

A discordância não é aleatória: nasce do **choque entre cadeiras** de um conselho
consultivo (Estratégia, Aquisição, Produto, Pessoas, Finanças/Governança,
Inovação/Ética). Para cada decisão, uma cadeira defende e outra ataca.

---

## Como funciona

**7 regras de comportamento** (resumo):

1. Antes de concordar, nomeia uma premissa não testada.
2. A primeira resposta é o caso contrário mais forte, sem suavizar.
3. Não recua só porque você objetou — só diante de evidência, raciocínio ou
   restrição nova.
4. Ao revisar um trabalho, começa pelo ponto mais fraco.
5. Nomeia investimento emocional e pergunta se é sinal ou ruído.
6. Se não há furo, diz que não há — não inventa defeito.
7. Fecha com **uma** pergunta para você sentar antes de agir.

**Cadeia de Razoabilidade (CdR):** cada resposta começa com um cabeçalho enxuto
(meta, passos, preferências, contexto + grafo de relações). É o andaime de contexto
que mantém o raciocínio explícito turno a turno.

**Lente regional:** toda recomendação passa pela realidade regulatória, tributária
e de capital do mercado-alvo — Brasil por padrão (regulador do setor, LGPD/ANPD,
carga tributária, custo de capital em reais), trocável para outros países.

---

## Estrutura

```
conselho-critico/
├── conselho-critico.skill        # instalável: baixe e suba no Claude
├── SKILL.md                      # regras, esquema CdR, processo, tom
└── references/
    └── ontologia-cdr.md          # ontologia interna + bancada de mentores
```

---

## Instalação

1. No Claude: **Configurações → Capacidades** → ative **Code Execution and File
   Creation** e **Skills**.
2. **Customize → Skills → "+" / Upload skill** e selecione `conselho-critico.skill`.
3. Ligue o toggle.

---

## Como usar

O Claude aciona sozinho quando o pedido combina com a descrição, ou você chama na
mão:

```
Use a skill conselho-critico para furar esta decisão: [sua decisão]
```

Gatilhos típicos: "me critica", "qual o furo", "fura essa ideia", "me convence do
contrário", "Conselho de IA", "CdR".

**Teste honesto:** não digite "testar a skill". Jogue uma decisão real da qual você
*gosta* e veja se o Conselho acha o furo.

---

## Personalização

- **Trocar mentores:** edite a bancada em `references/ontologia-cdr.md`.
- **Adaptar a região:** reescreva a seção "Lente regional" do `SKILL.md` com os
  reguladores e a realidade tributária do mercado-alvo. O resto é universal.
- **Modo "Expandir":** por padrão fecha com uma pergunta; o modo de três perguntas
  exploratórias é opcional.

Depois de editar, reempacote a pasta como `.zip` / `.skill` e suba de novo.

## Licença

[MIT](../LICENSE) © 2026 Marcio Nery Victoria.
