# Base de Conhecimento

## Dados Utilizados

| Arquivo | Formato | Utilização no Agente |
|---------|---------|---------------------|
| `entrada_usuario` | Texto | Valores informados pelo usuário para cálculo financeiro |
| `valores_temporarios` | Variáveis em memória | Armazenamento temporário durante a execução do cálculo |
| `produtos_financeiros.json` | JSON | Sugerir produtos adequados ao perfil |
| `parametros_calculo` | Numérico | Dados utilizados para operações matemáticas |

---

## Adaptações nos Dados

> Você modificou ou expandiu os dados mockados? Descreva aqui.

O funcionamento do agente baseia-se apenas em:

Entrada direta do usuário
Processamento matemático imediato
Descarte dos dados após a resposta

---

## Estratégia de Integração

### Como os dados são carregados?
> Descreva como seu agente acessa a base de conhecimento.

Os dados são inseridos manualmente pelo usuário durante a interação com o agente.

Esses dados:

São recebidos via interface (Streamlit)
São processados imediatamente
São mantidos temporariamente em memória
São descartados após a resposta

Não há carregamento de arquivos JSON, CSV ou banco de dados.

### Como os dados são usados no prompt?
> Os dados vão no system prompt? São consultados dinamicamente?

Os dados fornecidos pelo usuário são incluídos diretamente no prompt enviado ao modelo de linguagem (Ollama).

Eles são utilizados apenas durante a execução da consulta.

Os dados:

Não são armazenados
Não são reutilizados
Não são persistidos
Não fazem parte de uma base de conhecimento permanente

O prompt é gerado dinamicamente a cada interação.

---

## Exemplo de Contexto Montado

> Mostre um exemplo de como os dados são formatados para o agente.

```
- Entrada: 
Renda mensal: 2500
Gastos: 1800

- Contexto
Você é um assistente financeiro.

O usuário informou:

Renda mensal: 2500 reais
Gastos totais: 1800 reais

Calcule:

- Quanto sobra do orçamento
- Explique o resultado de forma simples

- Resposta
Sobra 700 reais do seu orçamento mensal.
```
