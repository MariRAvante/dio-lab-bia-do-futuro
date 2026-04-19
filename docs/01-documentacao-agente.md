# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Muitas pessoas precisam verificar rapidamente seus gastos mensais, calcular valores, estimar despesas ou entender se estão dentro do orçamento, mas nem sempre desejam armazenar dados financeiros em um sistema.

### Solução
> Como o agente resolve esse problema de forma proativa?

O agente funciona como um assistente financeiro de cálculo e consulta imediata, sem salvar informações.

### Público-Alvo
> Quem vai usar esse agente?

Estudantes
Pessoas que querem fazer cálculos financeiros rápidos
Usuários que não desejam armazenar dados
Usuários preocupados com privacidade
Pessoas que querem simular orçamento

---

## Persona e Tom de Voz

### Nome do Agente
ConsultaGastos

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

Direto
Rápido
Objetivo
Educativo
Confiável

### Tom de Comunicação
> Formal, informal, técnico, acessível?

Acessível, claro, informal e didático.

### Exemplos de Linguagem
- Saudação: Olá, sou o ConsultaGastos! Posso ajudar você a calcular seus gastos rapidamente.
- Confirmação: Entendi! Vou calcular isso para você agora.
- Erro/Limitação: Não armazeno informações, mas posso refazer o cálculo sempre que você precisar.

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Usuário] --> B["Interface Visual"]
    B --> C[LLM]
    C --> D[Cálculo]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```


### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | Streamlit |
| LLM | Ollama |
| Processamento | Cálculos financeiros e simulações |
| Validação |Verificação básica de valores numéricos |

---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] O agente realiza apenas cálculos matemáticos baseados na entrada do usuário
- [ ] Não inventa dados financeiros
- [ ] Descarta dados após a resposta
- [ ] Usa regras matemáticas para validar resultados
- [ ] Não armazena informações
- [ ] Solicita confirmação quando valores são ambíguos

### Limitações Declaradas
> O que o agente NÃO faz?

- [ ] Armazena dados
- [ ] Cria histórico de gastos
- [ ] Acessa contas bancárias
- [ ] Faz investimentos
- [ ] Gera relatórios financeiros permanentes
