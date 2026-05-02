---
document_type: parecer_terapeutico_ocupacional
version: v1.0
layout: A4
author: {{NOME_PROFISSIONAL}}
automation_ready: true
---

<br><br><br><br><br><br>

<div style="font-size:0.85em; line-height:1.5;">

# Declaração – {{MES_EXTENSO}}

<br>

**Ribeirão Preto, {{DIA}} de {{MES_EXTENSO}} de {{ANO}}.**

<br><br>

O presente documento refere-se ao parecer terapêutico ocupacional do paciente **{{NOME_PACIENTE}}**, cujo responsável legal é **{{NOME_RESPONSAVEL}}**.

O paciente possui diagnóstico de:
- **Transtorno do Espectro Autista** (CID: {{CID_TEA}})
- **Transtorno do Processamento Sensorial**, apresentando alterações como:
  - {{ALTERACOES_COMPORTAMENTAIS}}
  - {{ALTERACOES_PSICOMOTORAS}}
  - {{OUTRAS_OBSERVACOES_CLINICAS}}

Diante do quadro clínico apresentado, há **indicação para intervenção em Terapia Ocupacional com frequência de {{FREQUENCIA_SEMANAL}}**. Para continuidade do processo terapêutico e evolução do paciente, **certifico a necessidade de seguimento do atendimento de Terapia Ocupacional por tempo indeterminado**, considerando os objetivos terapêuticos em andamento.

<br>

As sessões são realizadas na seguinte unidade terapêutica: **{{NOME_CLINICA}}** - {{ENDERECO_COMPLETO}}, {{CIDADE}} - {{ESTADO}}, CEP: {{CEP}}.

<br><br>

## Registro de Sessões Realizadas no Período

<br>

{{LISTA_SESSOES}}

<!--
Formato esperado para {{LISTA_SESSOES}}:

DD/MM/AAAA - R${{VALOR_SESSAO}} - Terapia Ocupacional
DD/MM/AAAA - R${{VALOR_SESSAO}} - Terapia Ocupacional
...

Quantidade esperada: entre 16 e 20 sessões
-->

<br><br><br>

<br>

<div align="center">
  <img src="assinatura-carol.png" alt="Assinatura" width="320" style="display:block; margin:0 auto;" />
</div>

<div align="center" style="font-size:0.85em; line-height:1.4;">
{{NOME_PROFISSIONAL}}<br>
Terapeuta Ocupacional<br>
{{ESPECIALIZACOES_INLINE}}<br>
Registro Profissional: {{REGISTRO_CONSELHO}}<br>
Contato: {{CONTATO}}
</div>

</div>

<br>

---

## ⚙️ METADADOS PARA AUTOMAÇÃO

```yaml
placeholders:
  MES_EXTENSO: "Fevereiro"
  DIA: "02"
  ANO: "2026"

  NOME_PACIENTE: "Tomás Rollemberg Cipriano"
  NOME_RESPONSAVEL: "José Carlos Garcia Cipriano"

  CID_TEA: "F84 / 6A02"

  ALTERACOES_COMPORTAMENTAIS:
    - "agitação"
    - "brincar repetitivo"

  ALTERACOES_PSICOMOTORAS: "alterações psicomotoras"
  OUTRAS_OBSERVACOES_CLINICAS: "motricidade fina comprometida"

  FREQUENCIA_SEMANAL: "4x/semana"

  NOME_CLINICA: "Affettività"
  ENDERECO_COMPLETO: "Rua Otto Benz, 864, bairro Nova Ribeirânia"
  CIDADE: "Ribeirão Preto"
  ESTADO: "SP"
  CEP: "14096-580"

  VALOR_SESSAO: "85,00"

  NOME_PROFISSIONAL: "Caroline Leone"
  ESPECIALIZACOES: |
    Analista do Comportamento Aplicada  
    Integração Sensorial de Ayres
  ESPECIALIZACOES_INLINE: "Analista do Comportamento Aplicada | Integração Sensorial de Ayres"
  REGISTRO_CONSELHO: "CREFITO 3/17817-TO"
  CONTATO: "(16) 98140-0253"
```
