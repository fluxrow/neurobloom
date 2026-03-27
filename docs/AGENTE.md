# 🤖 Instruções para o Agente — NeuroBloom

> Cole este prompt no agente do VS Code (AntiGravity/Claude Code) ao iniciar uma sessão no projeto.

---

## PROMPT DE INÍCIO DE SESSÃO

```
Leia os seguintes arquivos antes de qualquer coisa:

1. /Users/cauafarias/Documents/Fluxrow/NeuroBloom/MASTER.md
2. /Users/cauafarias/Documents/Fluxrow/NeuroBloom/ROADMAP.md
3. /Users/cauafarias/Documents/Fluxrow/NeuroBloom/LEARNINGS.md
4. /Users/cauafarias/Documents/Fluxrow/NeuroBloom/Fase0/FASE0-OVERVIEW.md

Após ler, confirme:
- O que o projeto é
- Em que fase estamos
- O que foi decidido e por quê
- Qual o próximo passo

Depois me pergunte: "Continuamos de onde paramos ou há algo novo?"
```

---

## Contexto Rápido (para o agente)

**Projeto:** NeuroBloom — plataforma mobile-first para TEA e comorbidades  
**GitHub:** https://github.com/fluxrow/neurobloom  
**Obsidian:** `/Users/cauafarias/Documents/Fluxrow/NeuroBloom/`  
**Fase atual:** 0-B — estrutura do onboarding profundo  
**Stack:** a definir (React Native ou Flutter)  
**Fundador:** Cauã Farias (`fbcfarias`)

---

## Protocolo de Fim de Sessão

Ao encerrar qualquer sessão de trabalho no NeuroBloom, o agente deve:

1. Atualizar `ROADMAP.md` — marcar o que foi feito, adicionar próximos passos
2. Atualizar `LEARNINGS.md` — registrar decisões tomadas e por quê
3. Atualizar `MASTER.md` — se algo estrutural mudou
4. Commitar e fazer push para o GitHub:

```bash
cd /tmp/neurobloom-init
git add .
git commit -m "sessão: [descrever o que foi feito]"
git push origin main
```

5. Confirmar: "Sessão encerrada. Obsidian atualizado. GitHub: commit [hash]. Próximo: [item]"

---

## Estrutura de Arquivos

```
/Fluxrow/NeuroBloom/
├── MASTER.md          ← visão, metodologia, princípios, mercado
├── ROADMAP.md         ← fases, status, histórico de sessões
├── LEARNINGS.md       ← decisões tomadas e o que não repetir
├── AGENTE.md          ← este arquivo
├── Fase0/
│   └── FASE0-OVERVIEW.md   ← estrutura do onboarding (em construção)
└── Metodologia/            ← (a popular)
```

---

## Regras do Projeto

- Português brasileiro sempre
- Código completo, nunca parcial
- Commits descritivos em português
- Não pedir confirmação para coisas óbvias
- Apontar problemas proativamente
- Não usar bullet points para explicações — prosa é melhor
