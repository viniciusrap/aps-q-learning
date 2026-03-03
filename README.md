# aps-q-learning
## Análise dos Resultados – Taxi Driver

Foram testadas três configurações diferentes para os hiperparâmetros α (learning rate), ε (epsilon-greedy) e γ (discount factor) no algoritmo Q-Learning. A comparação foi realizada com base nas curvas de aprendizado geradas, considerando o número do episódio no eixo X e a recompensa acumulada no eixo Y.

### Configuração 1

A curva apresenta forte instabilidade nos episódios iniciais, com recompensas bastante negativas, o que é esperado devido à fase de exploração do agente. A partir de aproximadamente 1000 episódios, observa-se uma convergência gradual, com estabilização próxima de recompensas próximas de zero ou levemente positivas.

O aprendizado ocorre de forma consistente, porém com algumas oscilações ao longo do treinamento.

### Configuração 2

Esta configuração apresenta aprendizado inicial relativamente rápido, porém com maior variabilidade ao longo dos episódios. Mesmo após a convergência, observa-se maior número de quedas bruscas na recompensa acumulada.

Essa instabilidade indica que o agente continua explorando excessivamente ou que a taxa de aprendizado é alta o suficiente para gerar oscilações frequentes na Q-table.

### Configuração 3

A terceira configuração apresenta uma convergência mais suave e estável em comparação às demais. Após a fase inicial de exploração, a curva se estabiliza mais rapidamente e mantém menor variabilidade ao longo dos episódios finais.

O comportamento indica que houve um melhor equilíbrio entre exploração e explotação, permitindo que a política aprendida fosse mantida de forma mais consistente.

---

## Comparação das Curvas de Aprendizado

Comparando as três curvas:

- A Configuração 2 apresenta maior oscilação após a convergência.
- A Configuração 1 apresenta convergência estável, porém mais lenta.
- A Configuração 3 demonstra melhor estabilidade e menor variabilidade na fase final do treinamento.

---

## Melhor Configuração

A melhor configuração foi a **Configuração 3**, pois apresentou:

- Convergência mais consistente;
- Menor variabilidade na fase final;
- Recompensas acumuladas mais estáveis ao longo dos episódios finais.

Essa configuração conseguiu equilibrar adequadamente o fator de aprendizado (α), o nível de exploração (ε) e o desconto de recompensas futuras (γ), resultando em uma política mais estável para o ambiente Taxi Driver.

---

## Melhor Q-table

A melhor Q-table obtida foi a correspondente à **Configuração 3** (`q_table-3.csv`), pois está associada à curva de aprendizado com melhor estabilidade e convergência.

Como a política final utilizada pelo agente é derivada diretamente da Q-table (via argmax das ações), uma curva mais estável indica uma Q-table mais consistente e representativa da política ótima aprendida.
