# claude-rpaplus

Coleção de **Claude Skills** da RPA Plus — instruções reutilizáveis que dão ao
Claude um comportamento, um contexto e um fluxo consistentes, sem você precisar
explicar tudo de novo a cada conversa.

Cada skill vive na própria pasta, com seu `SKILL.md`, seus arquivos de apoio e o
arquivo `.skill` pronto para instalar.

---

## Skills disponíveis

| Skill | O que faz |
|-------|-----------|
| [**conselho-critico**](./conselho-critico) | Conselho consultivo de IA em modo parceiro crítico: o padrão é discordância construtiva, não validação. Acha o furo da sua decisão antes de você agir. Funciona em qualquer setor. |

> Mais skills serão adicionadas aqui. Cada uma terá sua própria linha na tabela e
> sua própria pasta com README.

---

## Como instalar qualquer skill

1. No Claude: **Configurações → Capacidades** → ative **Code Execution and File
   Creation** e **Skills** (sem isso, skills não funcionam).
2. Entre na pasta da skill desejada e baixe o arquivo `.skill`.
3. No Claude: **Customize → Skills → "+" / Upload skill** e selecione o arquivo.
4. Ligue o toggle. O Claude passa a acionar a skill quando o pedido combinar com a
   descrição dela — ou você chama na mão.

---

## Estrutura do repositório

```
claude-rpaplus/
├── LICENSE
├── README.md                     # este índice
└── conselho-critico/             # uma pasta por skill
    ├── README.md
    ├── conselho-critico.skill
    ├── SKILL.md
    └── references/
        └── ontologia-cdr.md
```

## Licença

[MIT](LICENSE) © 2026 Marcio Nery Victoria. Use, copie, modifique e redistribua,
mantendo o aviso de copyright.
