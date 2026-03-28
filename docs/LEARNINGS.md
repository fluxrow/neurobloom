# NeuroBloom — Learnings & Decisões

> Decisões tomadas, por quê, e o que não repetir. Leia antes de cada sessão.

---

## Sessão 01 — 2026-03-27

---

### DECISÃO: A Fase 0 é a fundação de tudo

- Sem onboarding profundo, todas as camadas seguintes ficam genéricas
- Funciona SEM laudo (maioria das famílias não tem) E absorve laudos quando existem
- Deve ser capaz de substituir, em partes, o que um profissional faria na primeira consulta
- Precisa ser acessível para uma mãe sozinha às 23h, sem formação técnica
- Baseada em estudos públicos, não em um único caso real

---

### DECISÃO: O público-alvo real é quem não tem acesso

A realidade do Brasil:
- Tratamento ABA completo (20–40h/semana) pode custar R$ 30.000/mês
- Renda familiar média brasileira: R$ 2.808 (IBGE 2022)
- Ter plano de saúde não garante acesso — negativas, filas, redes sem especialistas
- SUS especializado inexistente fora das metrópoles
- O app não é complemento para quem já tem tudo — é a única ferramenta para quem não tem nada

**Implicações de design:**
- Offline-first obrigatório
- Funciona em celular de entrada
- Sessões de 3–5 minutos máximo
- Linguagem de pai, não de prontuário
- Gera relatórios exportáveis para uso com profissionais e planos de saúde

---

### DECISÃO CRÍTICA: Universos Temáticos (skinning por interesse especial)

O app usa "universos temáticos" baseados no interesse especial de cada criança.
A atividade pedagógica é sempre a mesma — o que muda é o universo visual, sonoro e narrativo.

**Exemplos:**
- Trem → atividades em estações, vagões, trilhos
- Abelhas → colmeia, flores, mel
- Baleias → oceano, profundezas, sons de cetáceos
- Chaleira → cozinha, vapor, chá

**Base científica:** ABA e ESDM provam que intervenção centrada no interesse especial tem resultado superior.

**Motor fixo, universo variável:**
- Motor pedagógico idêntico em todos os universos
- O que muda: visuais, sons, personagens, narrativa, metáforas
- Pais escolhem no cadastro, trocam quando o interesse mudar
- Expansão futura: universos customizados pelos pais

**Dado único gerado:** correlação universo × domínio × performance — inexistente em qualquer estudo clínico.

---

### DECISÃO CRÍTICA: Moment Cards — conteúdo situacional cotidiano

**A ideia:** depois do cadastro/questionário completo, o app gera automaticamente um banco de "Moment Cards" — conteúdo pronto para situações cotidianas desafiadoras, personalizado com o universo temático do filho.

**Como funciona na prática:**
1. A criança se recusa a escovar os dentes (situação real, momento de crise)
2. O pai abre o app → acessa "Momento: Escovar os dentes"
3. O app exibe/narra: "O trem está chegando na Estação dos Dentes Brilhantes! O maquineiro precisa da sua ajuda para escovar antes de partir!"
4. A resistência é desarmada pelo interesse especial
5. A atividade básica é realizada — com menos conflito

**Por que isso é revolucionário:**
- Não é terapia agendada — é intervenção no segundo exato em que a crise está acontecendo
- Usa o hiperfoco como chave de desbloqueio natural
- Os pais não precisam improvisar — têm conteúdo pronto e personalizado
- Funciona offline, no celular, em segundos
- Transforma o "não" em engajamento sem confronto

**Categorias de Moment Cards (base para brainstorm):**
- Higiene: escovar dentes, tomar banho, lavar mãos, cortar unhas
- Alimentação: experimentar comida nova, sentar à mesa, tomar remédio
- Transições: hora de dormir, sair de casa, trocar de atividade, acabar o videogame
- Escola: hora de estudar, fazer tarefa, se despedir dos pais
- Regulação: crise/meltdown iminente, frustração, sobrecarga sensorial
- Social: cumprimentar alguém, esperar a vez, dividir brinquedo

**Relação com o questionário (Fase 0):**
- Quais situações cotidianas geram mais conflito? (pergunta obrigatória no onboarding)
- Quais Moment Cards são mais urgentes para essa família?
- O universo temático já definido alimenta automaticamente o conteúdo de cada card

**Dado que isso gera:**
- Quais Moment Cards são mais usados por perfil de comorbidade
- Quais situações são universalmente difíceis vs. específicas por perfil
- Eficácia do universo temático em cada tipo de situação cotidiana

---

### DECISÃO: Dados — foco interno por enquanto

- Não abrir para pesquisadores externamente ainda
- Construir a base, validar a metodologia, garantir volume e consistência
- Com o tempo: maior banco de dados longitudinal sobre neurodivergência do Brasil

---

### DECISÃO: Construir de dentro pra fora

Antes de qualquer tela, mapear a realidade vivida pelas famílias.
Fontes: estudos qualitativos brasileiros, não frameworks clínicos externos.

---

### O Que Não Fazer

- Não criar questionário genérico de TEA — mapear combinações específicas de comorbidades
- Não prometer cura ou resultados garantidos
- Não substituir o profissional na narrativa — sempre complementar
- Não ignorar processamento sensorial — afeta ~90% e determina o design do próprio app
- Não criar modelo "premium para quem tem tudo / básico para quem não tem" — replica desigualdade
- Não fazer Moment Cards genéricos — precisam usar o universo real da criança

---

### Referências-Chave

- ABA: Frontiers in Pediatrics 2025
- ESDM: RCT validado desde 18 meses
- Interoceptividade: Mahler IC Curriculum, PMC9045986
- Microbioma: Frontiers in Microbiology 2025
- Comorbidades: DSM-5, Canal Autismo BR
- TDAH + TEA: 50–70% comorbidade
- Dupla excepcionalidade: pepsic.bvsalud.org, Instituto Inclusão Brasil
- Custo tratamento BR: Jusbrasil 2024, Autismo e Realidade 2023
- Realidade das famílias: Retratos do Autismo no Brasil 2023 (Genial Care + Tismoo, n=2.200)
