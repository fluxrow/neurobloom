# Fase 0 — Modelo Conceitual do Perfil

> Estrutura inicial para transformar respostas do onboarding em um perfil utilizável pelo motor de personalização.

---

## Princípio

O modelo de dados do NeuroBloom precisa representar duas coisas ao mesmo tempo: a realidade complexa da criança e o grau de confiança que temos sobre cada informação. O sistema não deve tratar autorrelato, laudo clínico e inferência como se fossem a mesma coisa.

---

## Entidades principais

### `child_profile`

Núcleo do perfil da criança.

Campos sugeridos:

- `child_id`
- `first_name`
- `birth_date` ou `age_range`
- `primary_caregiver_name`
- `created_at`
- `updated_at`

### `diagnostic_profile`

Como o app enxerga o quadro neurodesenvolvimental atual.

Campos sugeridos:

- `asd_status` — confirmado, em investigação, suspeita, não informado
- `support_level` — 1, 2, 3, não informado
- `diagnoses_confirmed[]`
- `conditions_suspected[]`
- `evidence_confidence` — baixo, médio, alto
- `evidence_sources[]` — laudo, cuidador, escola, terapeuta

### `sensory_profile`

Leitura por canal sensorial.

Campos sugeridos:

- `auditory_sensitivity`
- `visual_sensitivity`
- `tactile_sensitivity`
- `movement_seeking`
- `food_texture_selectivity`
- `transition_tolerance`
- `sensory_notes`

### `communication_profile`

Como a criança entende, expressa e prefere receber instruções.

Campos sugeridos:

- `expressive_language_level`
- `receptive_language_level`
- `aac_usage`
- `preferred_instruction_channel`
- `reading_level`
- `writing_level`
- `symbol_support_needed`

### `regulation_profile`

Estado de atenção, autorregulação e sinais internos.

Campos sugeridos:

- `attention_span_pattern`
- `frustration_tolerance`
- `meltdown_frequency`
- `shutdown_frequency`
- `impulsivity_level`
- `interoception_awareness`
- `common_triggers[]`
- `effective_calming_strategies[]`

### `functional_profile`

Rotinas e AVDs observáveis.

Campos sugeridos:

- `sleep_quality`
- `feeding_profile`
- `bath_independence`
- `toilet_independence`
- `dressing_independence`
- `hygiene_independence`
- `routine_predictability`
- `high_friction_moments[]`

### `strengths_profile`

Interesses especiais, motivadores e potenciais.

Campos sugeridos:

- `special_interests[]`
- `natural_rewards[]`
- `observed_strengths[]`
- `giftedness_signals[]`
- `favorite_topics[]`
- `preferred_activity_formats[]`

### `family_context`

Condições reais de implementação.

Campos sugeridos:

- `caregiver_structure`
- `school_context`
- `therapies_in_place[]`
- `time_available_per_day`
- `financial_constraints`
- `support_network_strength`
- `family_goals_short_term[]`

### `medical_context`

Restrições, medicação e cuidados especiais.

Campos sugeridos:

- `medications[]`
- `epilepsy_flag`
- `sleep_disorder_flag`
- `allergies_or_food_restrictions[]`
- `medical_alerts[]`

---

## Objetos derivados

### `neurobloom_dna`

Síntese legível da criança.

Campos sugeridos:

- `profile_summary`
- `primary_needs[]`
- `primary_strengths[]`
- `engagement_anchors[]`
- `sensory_cautions[]`
- `recommended_entry_layers[]`

### `personalization_output`

Decisões iniciais do sistema.

Campos sugeridos:

- `session_duration_recommendation`
- `reinforcement_style`
- `starter_activity_types[]`
- `parent_coaching_priorities[]`
- `ui_accessibility_rules[]`
- `week_1_goals[]`

### `confidence_map`

Mapa de confiança por atributo relevante.

Campos sugeridos:

- `field_name`
- `value`
- `confidence_level`
- `source_type`
- `source_reference`
- `last_verified_at`

---

## Regras do modelo

- Todo campo importante deve registrar origem da informação.
- O sistema deve suportar ausência parcial de dados sem travar personalização.
- Hipótese não pode ser exibida ao cuidador como fato consumado.
- O modelo precisa ser atualizável ao longo do tempo, não apenas no onboarding.
- Perfis devem aceitar contradição temporária até revisão posterior.

---

## Exemplo de leitura de produto

Uma criança com TEA em investigação, alta busca por movimento, dificuldade de transição, linguagem receptiva boa, expressão verbal parcial, hiperfoco em mapas e sinais de altas habilidades pode gerar:

- sessões de 3 a 5 minutos
- instruções visuais com voz opcional
- atividades com mapas como motivador
- reforço imediato e transições previsíveis
- prioridade de camada 1 para regulação e camada 2 para comunicação funcional

---

## Próximo passo

Traduzir esse modelo conceitual em:

1. tipos de resposta do questionário
2. pesos e regras de inferência
3. estrutura persistível para backend
4. primeira versão do motor de personalização
