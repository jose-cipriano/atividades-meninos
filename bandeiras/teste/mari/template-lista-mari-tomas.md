<br><br><br><br><br><br><br><br><br><br>

**Nome:** {{NOME_BENEFICIARIO}}  
**Profissional:** {{NOME_PROFISSIONAL}}  
**Terapia:** {{TIPO_TERAPIA}}  
**Mês de referência:** {{MES_EXTENSO}} de {{ANO}}

<div style="font-size:0.80em;">

| Datas       | Quantidade | Horário de Início | Horário de Término | Assinatura do Beneficiário | Valor por Sessão (R$) |
|------------|------------|-------------------|--------------------|-----------------------------|------------------------|
{{LINHAS_SESSOES}}

</div>

<br>

<div align="center">
  <img src="assinatura-mari.png" alt="Assinatura" width="92" style="display:block; margin:0 auto 0 auto;" />
</div>

<div align="center" style="font-size:0.65em; line-height:1.4;">
MARIANNE ANDREA BARBOSA FURTADO<br>
Psicóloga / CRP: 06/198709
</div>

---

Estrutura dos Campos Dinâmicos
1. Título
{{MES_EXTENSO}} = Mês por extenso (ex: Fevereiro)
{{ANO}} = Ano com 4 dígitos (ex: 2026)


2. Dados Fixos (customizáveis por beneficiário)
{{NOME_BENEFICIARIO}} = Nome do beneficiário (ex: Tomás Rollemberg Cipriano ou Tarso Rollemberg Cipriano)
{{NOME_PROFISSIONAL}} = Marianne Furtado
{{TIPO_TERAPIA}} = Psicoterapia


3. Linhas da Tabela (núcleo do template)
Cada linha deve seguir exatamente este padrão:
| DD/MM/AAAA | 1 | HH:MM | HH:MM |                     | 00,00 |
Exemplo:
| 02/02/2026 | 1 | 09:00 | 10:00 |                     | 85,00 |
Placeholder:
{{LINHAS_SESSOES}}
Regras:
Entre 16 e 20 linhas
Campo "Assinatura" deve permanecer vazio (espaço para assinatura manual)
Valores monetários com vírgula (padrão BR)


4. Rodapé Profissional
{{CARGO_PROFISSIONAL}} = Psicóloga

{{ESPECIALIZACAO_1}} = (não aplicável)
{{ESPECIALIZACAO_2}} = (não aplicável)

{{REGISTRO_PROFISSIONAL}} = CRP: 06/198709
{{CONTATO_PROFISSIONAL}} = (a definir)
⚙️ Diretrizes Técnicas para Uso com Claude Opus / Automação
1. Controle de Layout (A4 - 1 página)
Evitar textos longos fora da tabela
Limitar a tabela a no máximo 20 linhas
Não adicionar quebras extras (--- ou múltiplos <br>)
O espaçamento superior (10x <br>) é reservado para o cabeçalho do papel timbrado
2. Padronização para geração automatizada
Todos os campos usam {{PLACEHOLDER}}
Permite fácil substituição via:
Prompt estruturado
Script
Sub-agente
3. Regras de consistência
Datas sempre no formato DD/MM/AAAA
Horários fixos ou parametrizáveis
Quantidade sempre 1 (como no padrão do PDF)
Valores alinhados ao acordo mensal
4. Possível Prompt de Geração (futuro uso)
Exemplo de instrução para automação:
Gerar lista de presença com:
- Beneficiário: Tomás Rollemberg Cipriano
- Mês: Março 2026
- Datas: [lista]
- Horário início: 09:00
- Horário término: 10:00
- Valor: 85,00
💡 Observação Estratégica
Esse template já está preparado para evoluir para:
✔ Geração automática mensal
✔ Integração com PDFs (HTML → PDF)
✔ Uso em pipelines de reembolso
✔ Padronização auditável (importante para convênios)
✔ Reutilização para múltiplos beneficiários (Tomás e Tarso)
