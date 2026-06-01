# Conselho Crítico — Claude Skill

> Um Conselho consultivo de IA cujo modo padrão é **discordância construtiva, não validação.**

Esta é uma [Claude Skill](https://support.claude.com/en/articles/12512180-use-skills-in-claude)
que transforma o Claude num parceiro crítico: em vez de concordar e elogiar, ele
procura primeiro **onde a sua ideia quebra** — e só concorda depois de ter caçado
a falha de verdade e não encontrado nenhuma.

Pensada para quem precisa **tomar e testar decisões estratégicas** (planos, teses,
pitches, propostas, arquiteturas, CVs) e quer ser desafiado antes de agir, não
bajulado depois.

---

## Por que existe

Assistentes de IA tendem à bajulação: concordam, suavizam, devolvem a sua própria
ideia com roupa melhor. Isso é confortável e inútil quando o que está em jogo é uma
decisão real. Esta skill inverte o padrão — o trabalho dela é discordar bem.

A discordância não é aleatória nem birrenta: ela nasce do **choque entre cadeiras**
de um conselho consultivo (Estratégia, Aquisição, Produto, Pessoas, Finanças/
Governança, Inovação/Ética). Para cada decisão, uma cadeira defende e outra ataca.

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
(meta, passos, preferências, contexto + grafo de relações). É o andaime de
contexto que mantém o raciocínio explícito turno a turno.

**Lente Brasil:** toda recomendação passa por regulação BR (Banco Central, SUSEP/
SECAP, regras de apostas), LGPD/ANPD, carga tributária e custo de capital em reais.

---

## Estrutura

```
conselho-critico/
├── SKILL.md                      # regras, esquema CdR, processo, tom
└── references/
    └── ontologia-cdr.md          # ontologia interna + bancada de mentores
```

---

## Instalação

1. No Claude, vá em **Configurações → Capacidades** e ative **Code Execution and
   File Creation** e **Skills**. Sem isso, skills não funcionam.
2. Vá em **Customize → Skills**.
3. Clique em **"+" / Upload skill** e selecione o arquivo `.zip` (ou `.skill` /
   `.md`). O zip deve ter a pasta `conselho-critico/` na raiz, não aninhada.
4. A skill aparece na lista — ligue o toggle.

> Skills que você sobe são privadas da sua conta. Compartilhamento com time só
> existe em planos Team/Enterprise.

---

## Como usar

O Claude aciona a skill sozinho quando o seu pedido combina com a descrição, ou
você chama na mão:

```
Use a skill conselho-critico para furar esta decisão: [sua decisão]
```

Gatilhos típicos: "me critica", "qual o furo", "fura essa ideia", "me convence do
contrário", "Conselho de IA", "CdR".

**Teste honesto:** não digite "testar a skill". Jogue uma decisão real da qual
você *gosta* e veja se o Conselho acha o furo. Se ele não achar furo numa ideia que
você adora, ou a ideia é mesmo sólida, ou a descrição precisa de um gatilho mais
agressivo.

---

## Personalização

- **Trocar mentores:** edite a bancada em `references/ontologia-cdr.md` — os nomes
  são arquétipos de raciocínio, não fontes de citação.
- **Ajustar a lente regional:** se o seu contexto não for o brasileiro de fintech/
  apostas, reescreva a seção "Lente Brasil" do `SKILL.md`.
- **Ligar/desligar o modo "Expandir":** por padrão a skill fecha com uma pergunta;
  o modo de três perguntas exploratórias é opcional.

Depois de editar, reempacote a pasta como `.zip` e suba de novo.

---

## Origem

Combina dois conceitos: um *anti-sycophancy prompt* (parceiro crítico que lidera
pela discordância) e a *Cadeia de Razoabilidade* de um conselho consultivo de IA
(working memory + cadeiras de mentores). A síntese resolve a tensão entre os dois
fazendo o crítico dominar e o conselho ser o motor estruturado da discordância.

## Licença

[MIT](LICENSE) © 2026 Marcio Nery Victoria. Você pode usar, copiar, modificar e
redistribuir, mantendo o aviso de copyright.
