# Avaliação e Métricas

## Como Avaliar seu Agente

A avaliação pode ser feita de duas formas complementares:

1. **Testes estruturados:** Você define perguntas e respostas esperadas;
2. **Feedback real:** Pessoas testam o agente e dão notas.

---

## Métricas de Qualidade

| Métrica | O que avalia | Exemplo de teste |
|---------|--------------|------------------|
| **Assertividade** | O agente realizou o cálculo corretamente? | Informar renda e gastos e verificar o saldo correto |
| **Segurança** | O agente evita inventar dados ou armazenar informações? | Perguntar algo fora do escopo e verificar se ele informa a limitação |
| **Coerência** | A resposta faz sentido e está clara para o usuário? | Solicitar cálculo de orçamento diário e verificar se a explicação é compreensível |

---

## Exemplos de Cenários de Teste

Crie testes simples para validar seu agente:

### Solicitar cálculo de orçamento diário e verificar se a explicação é compreensível
- **Pergunta:** "Se eu ganhar 2500 reais e gastar 1800, quanto sobra?"
- **Resposta esperada:** 700 reais
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 2: Estimativa de gastos mensais
- **Pergunta:** "Se eu gastar 100 reais por semana, quanto gasto no mês?"
- **Resposta esperada:** 400 reais
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 3: Pergunta fora do escopo
- **Pergunta:** "Qual a previsão do tempo?"
- **Resposta esperada:** O agente informa que trata apenas de cálculos financeiros.
- **Resultado:** [ ] Correto  [ ] Incorreto

### Teste 4: Informação inexistente
- **Pergunta:** Quanto sobra do meu dinheiro?
- **Resposta esperada:** O agente solicita mais informações (renda e gastos).
- **Resultado:** [ ] Correto  [ ] Incorreto

---

## Resultados

Após os testes, registre suas conclusões:

**O que funcionou bem:**
- [Liste aqui]

**O que pode melhorar:**
- [Liste aqui]

---

## Métricas Avançadas (Opcional)

Para quem quer explorar mais, algumas métricas técnicas de observabilidade também podem fazer parte da sua solução, como:

- Latência e tempo de resposta;
- Consumo de tokens e custos;
- Logs e taxa de erros.

Ferramentas especializadas em LLMs, como [LangWatch](https://langwatch.ai/) e [LangFuse](https://langfuse.com/), são exemplos que podem ajudar nesse monitoramento. Entretanto, fique à vontade para usar qualquer outra que você já conheça!
