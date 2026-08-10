# Dinâmica: O Filtro de Spam Humano

## Treinando uma inteligência artificial sem computadores

**Público:** 15 alunos  
**Duração:** 60 minutos  
**Organização:** 3 grupos de 5 alunos  
**Tema:** lógica, aprendizado de máquina, dados de treino e teste, pesos, vieses e erros de classificação

---

## 1. Objetivos de aprendizagem

Ao final da dinâmica, os estudantes deverão ser capazes de:

- compreender que um modelo de inteligência artificial aprende padrões a partir de dados;
- diferenciar dados de treino e dados de teste;
- construir uma regra de classificação baseada em atributos e pesos;
- reconhecer falsos positivos e falsos negativos;
- identificar situações de viés e superajuste (*overfitting*);
- comparar regras binárias da lógica clássica com decisões graduais ou probabilísticas.

## 2. Materiais necessários

- 3 cópias da tabela de dados de treino;
- 3 cópias da folha de respostas dos grupos;
- 3 cópias dos dados de teste, mantidas com o professor até a fase de validação;
- canetas ou lápis;
- quadro e marcador ou giz;
- cronômetro.

> **Importante:** não entregue os dados de teste no início. Eles devem permanecer inéditos até a terceira etapa.

## 3. Preparação da sala

1. Organize a turma em **3 grupos de 5 alunos**.
2. Entregue a cada grupo os **dados de treino** e uma **folha de respostas**.
3. Explique que os grupos representarão algoritmos de aprendizado de máquina responsáveis pelo filtro de spam de um serviço de e-mail.
4. Mantenha os três e-mails de teste escondidos até o momento indicado.

---

## 4. Cronograma da atividade

| Tempo | Etapa | Atividade |
|---:|---|---|
| 0–5 min | Introdução | Apresentação do problema e da missão dos grupos |
| 5–20 min | Treinamento | Construção da fórmula de pontuação com os 8 exemplos conhecidos |
| 20–40 min | Teste e validação | Aplicação da fórmula em 3 e-mails inéditos |
| 40–50 min | Debate | Comparação dos resultados e discussão dos erros |
| 50–60 min | Fechamento conceitual | Dados de treino e teste, pesos, vieses, erros e superajuste |

**Duração total:** 60 minutos.

---

# 5. Roteiro do professor

## Etapa 1 — Introdução (5 minutos)

### Conceito

Explique que uma inteligência artificial não nasce sabendo distinguir um e-mail legítimo de um golpe. Para aprender, ela precisa observar exemplos em um **conjunto de dados de treino**.

A partir desses exemplos, o sistema procura características que ajudam a estimar se uma nova mensagem é legítima ou spam.

### Missão

Apresente o desafio à turma:

> Hoje vocês serão o algoritmo de aprendizado de máquina de um filtro de spam. A missão de cada grupo é criar uma fórmula capaz de classificar mensagens como **spam** ou **caixa de entrada**.

## Etapa 2 — Fase de treinamento (15 minutos)

Entregue os oito e-mails previamente classificados.

Cada grupo deverá:

1. observar palavras, remetentes, pedidos e outros elementos recorrentes;
2. selecionar atributos relevantes para a classificação;
3. atribuir pontos positivos aos sinais de spam;
4. atribuir pontos negativos aos sinais de mensagens legítimas;
5. definir um limite de pontuação a partir do qual a mensagem será classificada como spam;
6. testar a fórmula nos oito exemplos de treino e ajustá-la para obter o maior número possível de acertos.

### Exemplo de regra

- contém a palavra “urgente”: **+3 pontos**;
- solicita dinheiro, PIX, CPF ou clique em link: **+4 pontos**;
- utiliza domínio institucional conhecido: **−2 pontos**;
- contém saudação pessoal ou relação familiar: **−2 pontos**;
- resultado igual ou superior a **5 pontos**: classificar como spam.

> A fórmula acima é apenas um exemplo. Os grupos devem criar e justificar os próprios pesos.

## Etapa 3 — Teste e validação (20 minutos)

Entregue os três e-mails inéditos. Informe que os grupos não poderão alterar a fórmula antes de classificá-los.

Cada grupo deverá:

1. aplicar exatamente a fórmula criada na fase de treinamento;
2. registrar o cálculo realizado para cada mensagem;
3. decidir entre **caixa de entrada** e **spam**;
4. comparar a previsão do algoritmo com a classificação real;
5. identificar o tipo de erro, quando houver.

### A reviravolta: o “bug” da IA

Os casos foram construídos para expor limitações da fórmula:

- uma mensagem legítima utiliza termos urgentes e solicita dinheiro;
- uma tentativa de golpe emprega linguagem formal e evita palavras muito óbvias;
- uma mensagem institucional pode parecer legítima apenas por causa do remetente.

Os estudantes poderão perceber que uma fórmula eficiente nos dados conhecidos pode falhar diante de situações novas.

## Etapa 4 — Debate (10 minutos)

Peça que cada grupo apresente:

- o limite utilizado para classificar spam;
- os principais atributos e pesos escolhidos;
- a classificação dos três e-mails de teste;
- o erro mais relevante produzido pela fórmula;
- uma possível melhoria para o algoritmo.

### Perguntas norteadoras

1. Os três grupos produziram os mesmos resultados? Por quê?
2. Qual atributo recebeu maior peso?
3. Uma palavra isolada é suficiente para determinar a intenção da mensagem?
4. O remetente aparentemente oficial garante que o e-mail seja verdadeiro?
5. O que acontece quando os dados de treino não representam bem o mundo real?
6. Seria melhor bloquear mais mensagens suspeitas ou evitar o bloqueio de mensagens legítimas?
7. Quem deve responder pelas consequências de uma decisão automática incorreta?

## Etapa 5 — Fechamento conceitual (10 minutos)

Apresente os seguintes conceitos:

### Dados de treino e dados de teste

- **Dados de treino:** exemplos usados para construir ou ajustar o modelo.
- **Dados de teste:** exemplos inéditos usados para avaliar se o modelo funciona em situações novas.

Um modelo não deve ser avaliado somente com os mesmos dados utilizados durante seu aprendizado.

### Pesos e vieses

Os valores atribuídos pelos grupos, como `+3` ou `−2`, representam a importância dada a cada característica. De maneira simplificada, eles funcionam como **pesos**.

Se os exemplos ou critérios favorecerem certos padrões de forma inadequada, o sistema poderá desenvolver um **viés** e repetir erros de maneira sistemática.

### Falso positivo

Ocorre quando uma mensagem legítima é classificada como spam.

**Exemplo:** bloquear o e-mail verdadeiro do irmão que sofreu um acidente.

### Falso negativo

Ocorre quando uma mensagem de spam é classificada como legítima.

**Exemplo:** permitir a entrada do golpe da herança internacional.

### Superajuste (*overfitting*)

Ocorre quando o modelo se adapta excessivamente aos exemplos de treino, mas não consegue generalizar seu aprendizado para dados novos.

Na dinâmica, isso acontece quando a fórmula acerta os oito primeiros e-mails, mas falha nos três casos inéditos.

---

# 6. Material dos grupos — Dados de treino

> Use os exemplos abaixo para criar a fórmula de pontuação.

| ID | Remetente | Assunto ou conteúdo | Classificação real |
|---:|---|---|---|
| 1 | `banco_seguro@verify.com` | “URGENTE: Sua conta será bloqueada. Clique aqui.” | **SPAM** |
| 2 | `mae@email.com` | “Oi, filho. Me liga quando puder. Beijo.” | **CAIXA DE ENTRADA** |
| 3 | `premio_loto@ganhou.net` | “Parabéns! Você ganhou 1 milhão. Digite seu CPF.” | **SPAM** |
| 4 | `chefe@empresa.com` | “Relatório mensal atrasado. Enviar até as 18h.” | **CAIXA DE ENTRADA** |
| 5 | `promo@compras.com.br` | “Desconto imperdível de 90% em TVs apenas hoje!” | **SPAM** |
| 6 | `netflix@atendimento.com` | “Seu pagamento foi aprovado. Obrigado.” | **CAIXA DE ENTRADA** |
| 7 | `desconhecido42@gmail.com` | “Aumente seus ganhos trabalhando de casa 2h por dia.” | **SPAM** |
| 8 | `professor@faculdade.edu` | “Notas da primeira avaliação disponíveis no portal.” | **CAIXA DE ENTRADA** |

---

# 7. Material reservado ao professor — Dados de teste

> Entregue esta seção somente após a conclusão da fase de treinamento.

## E-mail A — Aviso de manutenção

**Remetente:** `suporte@bancobrasil.com`  
**Conteúdo:** “Aviso de manutenção programada no sistema no próximo domingo.”  
**Classificação proposta para a dinâmica:** caixa de entrada.

## E-mail B — Pedido urgente do irmão

**Remetente:** `irmao@email.com`  
**Conteúdo:** “URGENTE! Bati o carro, quebrei o braço e preciso de 500 reais para o guincho agora! PIX na chave celular...”  
**Classificação proposta para a dinâmica:** caixa de entrada.

## E-mail C — Herança internacional

**Remetente:** `contato@heranca-internacional.org`  
**Conteúdo:** “Prezado senhor, notificamos que há um fundo financeiro esquecido em seu nome após auditoria jurídica.”  
**Classificação proposta para a dinâmica:** spam.

### Orientação ao professor

- O **e-mail B** é legítimo no cenário da atividade, mas tende a ser bloqueado por conter “urgente”, dinheiro e PIX. Se isso ocorrer, será um **falso positivo**.
- O **e-mail C** é spam, mas utiliza linguagem formal e não contém palavras explícitas como “ganhou”. Se for aceito, será um **falso negativo**.
- O objetivo não é encontrar uma fórmula perfeita, mas compreender por que modelos podem errar ao receber dados diferentes dos exemplos de treino.

> Em uma situação real, mesmo uma mensagem aparentemente legítima deve ser verificada por outro canal antes de clicar em links, transferir dinheiro ou fornecer dados pessoais.

---

# 8. Folha de respostas dos grupos

**Grupo nº:** ________

**Integrantes:**  
______________________________________________________________________________  
______________________________________________________________________________

## Parte 1 — Configuração dos pesos

Atribuam valores positivos aos sinais de spam e valores negativos aos sinais de mensagem legítima.

| Atributo | Pontuação |
|---|---:|
| Palavra “URGENTE” | ______ pontos |
| “Ganhou”, “prêmio” ou promessa de dinheiro | ______ pontos |
| Remetente institucional ou conhecido | ______ pontos |
| Remetente genérico ou domínio desconhecido | ______ pontos |
| Link ou expressão “clique aqui” | ______ pontos |
| Pedido de PIX, CPF ou outro dado pessoal | ______ pontos |
| Linguagem pessoal ou relação familiar | ______ pontos |
| Outro atributo: __________________________ | ______ pontos |
| Outro atributo: __________________________ | ______ pontos |

### Regra de decisão

O e-mail será considerado **spam** quando a soma final for maior ou igual a **______ pontos**.

### Conferência nos dados de treino

| ID | Pontuação calculada | Resultado do algoritmo | Acertou? |
|---:|---:|---|:---:|
| 1 | ______ | ____________________ | ( ) Sim ( ) Não |
| 2 | ______ | ____________________ | ( ) Sim ( ) Não |
| 3 | ______ | ____________________ | ( ) Sim ( ) Não |
| 4 | ______ | ____________________ | ( ) Sim ( ) Não |
| 5 | ______ | ____________________ | ( ) Sim ( ) Não |
| 6 | ______ | ____________________ | ( ) Sim ( ) Não |
| 7 | ______ | ____________________ | ( ) Sim ( ) Não |
| 8 | ______ | ____________________ | ( ) Sim ( ) Não |

**Total de acertos no treinamento:** ______ de 8.

## Parte 2 — Teste de estresse

### E-mail A — Aviso de manutenção do banco

**Cálculo dos pontos:**  
______________________________________________________________________________

**Resultado do algoritmo:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**O sistema acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não

### E-mail B — Irmão pedindo PIX após um acidente

**Cálculo dos pontos:**  
______________________________________________________________________________

**Resultado do algoritmo:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**O sistema acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não  
**Se errou, o resultado foi:** ( ) Falso positivo

### E-mail C — Notificação de herança internacional

**Cálculo dos pontos:**  
______________________________________________________________________________

**Resultado do algoritmo:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**O sistema acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não  
**Se errou, o resultado foi:** ( ) Falso negativo

## Parte 3 — Reflexão do grupo

1. Qual foi o principal erro da fórmula?  
   __________________________________________________________________________

2. Qual atributo recebeu peso excessivo ou insuficiente?  
   __________________________________________________________________________

3. Como o algoritmo poderia ser melhorado?  
   __________________________________________________________________________

4. A fórmula funcionou melhor no treinamento ou no teste? Por quê?  
   __________________________________________________________________________  
   __________________________________________________________________________

---

# 9. Slides rápidos para a abertura

## Slide 1 — Lógica de Computação para IA

### O fim do “sim ou não” perfeito?

Como sistemas computacionais usam dados e critérios para classificar situações reais.

## Slide 2 — Regras e aprendizado

Na programação tradicional, o programador costuma definir regras explícitas.

Em muitos sistemas de aprendizado de máquina, fornecemos exemplos e resultados esperados para que o modelo ajuste parâmetros e encontre padrões.

## Slide 3 — A missão de hoje

Hoje vocês não serão programadores de linhas de código.

Vocês serão os treinadores de um filtro de spam e precisarão transformar exemplos em uma regra de decisão.

---

# 10. Lógica clássica, lógica difusa e probabilidade

## Lógica clássica

Trabalha com valores definidos, como:

- verdadeiro ou falso;
- zero ou um;
- permite ou bloqueia.

Exemplo:

> Se o e-mail contém a expressão exata “você ganhou”, então bloqueie.

Uma regra fixa pode ser rígida: se a mensagem disser “você foi premiado”, a expressão original não será encontrada.

## Lógica difusa

Permite representar graus de pertinência entre `0` e `1`. Um e-mail pode, por exemplo, apresentar um grau elevado de “aparência promocional”, sem que essa característica seja simplesmente verdadeira ou falsa.

## Decisão probabilística

Representa incerteza por meio de probabilidades. Um modelo pode estimar, por exemplo:

> Há 87% de probabilidade de esta mensagem ser spam.

Se o limite de decisão for 80%, o sistema enviará a mensagem para a pasta de spam.

> **Nota conceitual:** lógica difusa e probabilidade não são sinônimos. A lógica difusa representa graus de pertencimento ou intensidade; a probabilidade representa incerteza sobre eventos. Ambas ajudam a modelar situações que não se encaixam bem em regras binárias simples.

## Relação com a dinâmica

A soma dos pesos produz uma pontuação gradual. Entretanto, a decisão final continua binária porque o grupo define um limite:

```text
se pontuação >= limite:
    classificar como spam
senão:
    enviar para a caixa de entrada
```

A qualidade do resultado dependerá dos exemplos, dos atributos escolhidos, dos pesos e do limite de decisão.

---

# 11. Síntese para encerramento

Finalize com quatro ideias:

1. **Um modelo aprende com os exemplos disponíveis.** Dados incompletos ou pouco representativos podem gerar decisões ruins.
2. **Acertar os dados de treino não é suficiente.** O modelo precisa funcionar com dados inéditos.
3. **Todo limite envolve uma escolha.** Um filtro mais rigoroso pode bloquear golpes, mas também mensagens legítimas.
4. **Resultados automáticos precisam de avaliação crítica.** Contexto, segurança, qualidade dos dados e consequências humanas devem ser considerados.
