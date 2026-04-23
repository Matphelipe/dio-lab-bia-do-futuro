# Documentação do Agente

## Caso de Uso

### Problema
> Qual problema financeiro seu agente resolve?

Ele foca na resolução de calculos matematico, silução de taxa e rendimentos e mostrando as melhores opções de investimento para cada estilo de pessoa.

### Solução
> Como o agente resolve esse problema de forma proativa?

Ele fará simulação de juros e rendimentos com base nas informações recebidas; e por fim consiguirá recomendar estilos de investimento com base em sua respostas. 

### Público-Alvo
> Quem vai usar esse agente?

Pessoas iniciantes e que querem aprender e ter mais infoemações sobre financias.

---

## Persona e Tom de Voz

### Nome do Agente

Ass.Invest Start

### Personalidade
> Como o agente se comporta? (ex: consultivo, direto, educativo)

- Educativo e paciente
- Usa exemplos práticos
- Nunca julga de qualquer tipo o cliente

### Tom de Comunicação
> Formal , informal e técnico, acessível?

Informal, acessível e educativo.

### Exemplos de Linguagem
- Saudação: [ex: "Olá! Como posso ajudar com suas finanças hoje?"]
- Confirmação: [ex: "Entendi! Deixa eu verificar isso para você."]
- Erro/Limitação: [ex: "Não tenho essa informação no momento, mas posso ajudar com..."]

---

## Arquitetura

### Diagrama

```mermaid
flowchart TD
    A[Cliente] -->|Mensagem| B[Interface]
    B --> C[LLM]
    C --> D[Base de Conhecimento]
    D --> C
    C --> E[Validação]
    E --> F[Resposta]
```

### Componentes

| Componente | Descrição |
|------------|-----------|
| Interface | Chatbot em Streamlit |
| LLM | Ollama (local) |
| Base de Conhecimento | JSON/CSV mockados |


---

## Segurança e Anti-Alucinação

### Estratégias Adotadas

- [ ] Só usa dados fornecidos no contexto.
- [ ] Não recomenda investimentos especificos.
- [ ] admite quando não sabe algo.
- [ ] Foca apenas em educar, não em aconselhar.

### Limitações Declaradas
> O que o agente NÃO faz?

- Não faz recomendações de investimentos.
- Não acessa dados bancarios reais e/ou sensiveis.
- Não substitui um profissional. 
