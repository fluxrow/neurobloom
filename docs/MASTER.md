# NeuroBloom — Master Document

> Plataforma mobile-first para potencializar o desenvolvimento de crianças e adultos no espectro autista, com personalização profunda por perfil de comorbidades.

---

## Visão do Produto

**Tagline:** Potencializar cada mente. Honrar cada caminho.

**Problema central:** A maioria das famílias com filhos no espectro não tem acesso a terapias especializadas. O NeuroBloom é a ferramenta estruturada para quem não tem nada — e o complemento inteligente para quem tem.

**North Star Metric:** Progressos reais conquistados pela criança, celebrados pelos pais, registrados pelo app — semana a semana.

---

## Realidade das Famílias Brasileiras

| Dado | % | Implicação de design |
|------|---|----------------------|
| Medo do futuro a longo prazo | 79% | Painel mostra marcos de autonomia, não atividades |
| Dificuldades financeiras | 73% | App é ferramenta principal, não complemento. Offline-first. |
| Sem tempo para descanso | 68% | Sessões de 3–5 min. Celebrações como notificação para os pais. |
| Sem contato prévio com TEA | 64% | Funciona sem laudo. Linguagem de pai, não de prontuário. |
| Relação fragilizada com saúde | recorrente | Gera relatórios exportáveis para médico e plano de saúde. |

Custo real do tratamento: R$ 20.000–30.000/mês. Renda média BR: R$ 2.808.
86% das cuidadoras são mulheres. 1 em cada 4 está no espectro ela mesma.

---

## Princípios Inegociáveis

1. **Baseado em evidências** — medicina, estudos e terapias reais. Sem achismo.
2. **Não substitui profissionais** — somos o que acontece nas outras 23h do dia.
3. **Personalização real** — não "tem TEA": qual combinação exata de comorbidades, nível de suporte, pontos fortes, perfil sensorial.
4. **Acessível** — funciona sem laudo. Para famílias sem acesso a terapeutas.
5. **Multimodal** — voz, texto, imagem, toque, animação, vibração.
6. **Dados com propósito** — cada família constrói o maior banco de dados sobre neurodivergência do Brasil.

---

## Os Dois Pilares de Inovação

### 1. Universos Temáticos
O interesse especial não é decoração — é o canal de aprendizado.
Motor pedagógico fixo. Universo visual/sonoro/narrativo variável por criança.
- Pais escolhem no cadastro, trocam quando o interesse mudar
- Base científica: ABA e ESDM provam que intervenção centrada no interesse especial tem resultado superior
- Dado único: correlação universo × domínio × performance

### 2. Moment Cards
Conteúdo situacional pronto para crises cotidianas, usando o universo da criança.
Pai abre o app no momento exato do conflito — app entrega narrativa personalizada em segundos.

**Exemplo:** criança recusa escovar dentes (universo: trens)
> "Apito! O Expresso da Madrugada está chegando na Estação dos Dentes Brilhantes! O maquineiro [nome] precisa escovar antes da partida! 🚂"

Categorias: higiene, alimentação, transições, escola, regulação emocional, social.
Ver: `MomentCards/MOMENT-CARDS-OVERVIEW.md`

---

## Arquitetura de Camadas

| Camada | Nome | Foco |
|--------|------|------|
| **0** | Mapeamento do Perfil | DNA NeuroBloom — funciona sem laudo, absorve laudo |
| **1** | Fundação e Regulação Sensorial | Sono, alimentação, rotinas, integração sensorial |
| **2** | Habilidades Funcionais | Comunicação, atenção, imitação, AVDs |
| **3** | Potencial e Talentos | Cognitivo, criativo, acadêmico, altas habilidades |
| **4** | Social e Autonomia | Habilidades sociais, teoria da mente, independência |

**Moment Cards:** camada transversal. Ativa em qualquer momento do dia, fora das sessões formais.

---

## Base Metodológica

### Evidência Nível A — Core
- **ABA** — micro-passos, reforço positivo, coleta de dados contínua
- **ESDM** — relacional, baseado em jogo, pais como co-terapeutas

### Complementar Validado
- Floortime / DIR + RDI
- Terapia Ocupacional + Integração Sensorial
- Interoceptividade (Mahler/IC) — o 8º sentido

### Abordagens Emergentes Monitoradas
- Eixo intestino-cérebro / microbioma
- Neurofeedback / biofeedback
- IA adaptativa e digital biomarkers
- TMS/tDCS — informativo
- Modulação endocanabinoide — informativo

---

## Mapa de Comorbidades

| Comorbidade | Prevalência no TEA |
|-------------|-------------------|
| Processamento sensorial (SPD) | ~90% |
| TDAH | 50–70% |
| Distúrbio de sono | 50–80% |
| Epilepsia | ~25% |
| Ansiedade | ~28% |
| Altas Habilidades (AH/SD) | ~17% |
| TOC | ~17% |
| TDE (dislexia/disgrafia) | 5–10% |

**Caso real interno:** TEA N1 + TDAH + TDE + Altas Habilidades.

---

## Estrutura do Vault

```
/NeuroBloom/
├── MASTER.md
├── ROADMAP.md
├── LEARNINGS.md
├── AGENTE.md
├── Fase0/
│   └── FASE0-OVERVIEW.md
├── MomentCards/
│   └── MOMENT-CARDS-OVERVIEW.md
└── Metodologia/ (a popular)
```

---

## Stack Técnico (a definir)
- Mobile: React Native ou Flutter
- Backend: a definir
- IA/ML: motor adaptativo por perfil + geração de Moment Cards
- Dados: criptografados, LGPD-compliant, offline-first

---

## Time
- **Cauã Farias** — fundador | GitHub: `fbcfarias`
- Repo: https://github.com/fluxrow/neurobloom

---

*Atualizado: 2026-03-27 — Sessão 01 completa*
