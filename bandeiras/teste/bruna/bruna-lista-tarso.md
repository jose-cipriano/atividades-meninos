<div style="font-size:0.70em; line-height:1.1;">

**LISTA DE PRESENÇA - {{MES_EXTENSO}} {{ANO}}** &emsp;&emsp;&emsp;&emsp; **Nome:** {{NOME_BENEFICIARIO}} &emsp; **Profissional:** {{NOME_PROFISSIONAL}} &emsp; **Terapia:** {{TIPO_TERAPIA}}

<table style="font-size:0.75em; line-height:1.0; border-collapse:collapse; width:100%;">
<tr style="height:14px;">
<th style="padding:1px 3px;">Data</th>
<th style="padding:1px 3px;">Qtd</th>
<th style="padding:1px 3px;">Horário Início</th>
<th style="padding:1px 3px;">Horário Término</th>
<th style="padding:1px 3px;">Responsável do Beneficiário</th>
<th style="padding:1px 3px;">Valor por Sessão (R$)</th>
</tr>
{{LINHAS_SESSOES}}
</table>

<!--
Formato de cada linha (HTML):
<tr style="height:14px;">
<td style="padding:1px 3px;">DD/MM/AAAA</td>
<td style="padding:1px 3px;">1</td>
<td style="padding:1px 3px;">HH:MM</td>
<td style="padding:1px 3px;">HH:MM</td>
<td style="padding:1px 3px;"></td>
<td style="padding:1px 3px;">42,50</td>
</tr>
-->

<br>

<div align="center">
  <img src="assinatura-bruna.png" alt="Assinatura" width="200" style="display:block; margin:0 auto;" />
</div>

<div align="center" style="font-size:0.75em; line-height:1.3;">
<strong>Bruna Fernandes Marques</strong><br>
Fisioterapeuta<br>
Crefito 3/273801-F
</div>

</div>

---

## ⚙️ METADADOS PARA AUTOMAÇÃO

```yaml
placeholders:
  MES_EXTENSO: "Fevereiro"
  ANO: "2026"

  NOME_BENEFICIARIO: "Tarso Rollemberg Cipriano"   # ou "Tomás Rollemberg Cipriano"
  NOME_PROFISSIONAL: "Bruna Fernandes Marques"
  TIPO_TERAPIA: "Fisioterapia"

  VALOR_SESSAO: "42,50"

  NOME_ASSINATURA: "Bruna Fernandes Marques"
  CARGO: "Fisioterapeuta"
  REGISTRO: "Crefito 3/273801-F"
```

### Regras de Horário por Cenário

```yaml
cenarios_horario:
  tarso_rollemberg_cipriano:
    # Sempre horário fixo
    horario_inicio: "10:00"
    horario_termino: "11:00"

  tomas_rollemberg_cipriano:
    # Se a mesma data aparece duas vezes na lista:
    primeira_ocorrencia:
      horario_inicio: "08:00"
      horario_termino: "09:00"
    segunda_ocorrencia:
      horario_inicio: "09:00"
      horario_termino: "10:00"
    # Se a data aparece apenas uma vez:
    data_unica:
      horario_inicio: "09:00"
      horario_termino: "10:00"
```

### Diretrizes de Layout

```yaml
layout:
  formato: A4
  max_sessoes: 34
  font_size_tabela: "0.75em"
  line_height_tabela: "1.0"
  row_height: "14px"
  cell_padding: "1px 3px"
  observacao: >
    A tabela usa HTML com altura de linha reduzida para
    comportar até 34 sessões em uma única página A4.
    O campo 'Responsável do Beneficiário' permanece em
    branco para assinatura manual.
```
