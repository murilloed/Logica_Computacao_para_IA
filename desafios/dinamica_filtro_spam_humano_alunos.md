# Dinâmica: O Filtro de Spam Humano

## Você vai treinar uma inteligência artificial sem usar computador

**Duração:** 60 minutos  
**Organização:** grupos de 5 estudantes  
**Tema:** lógica, inteligência artificial e classificação de e-mails

---

## 1. Sua missão

Nesta atividade, **você será parte de um algoritmo de inteligência artificial** responsável por separar mensagens legítimas de mensagens indesejadas.

Seu grupo receberá exemplos de e-mails que já foram classificados como:

- **SPAM:** mensagem indesejada ou tentativa de golpe;
- **CAIXA DE ENTRADA:** mensagem considerada legítima.

Você deverá observar esses exemplos, encontrar padrões e criar uma fórmula de pontuação. Depois, seu algoritmo será colocado à prova com mensagens que você ainda não viu.

## 2. O que você vai aprender

Ao participar da dinâmica, você poderá:

- entender como uma inteligência artificial aprende com exemplos;
- diferenciar dados de treino e dados de teste;
- criar uma regra de classificação usando atributos e pesos;
- testar se uma regra funciona em situações novas;
- reconhecer falsos positivos e falsos negativos;
- compreender viés e superajuste (*overfitting*);
- analisar criticamente uma decisão automática.

---

## 3. Como a atividade vai funcionar

| Tempo | Etapa | O que você fará |
|---:|---|---|
| 0–5 min | Introdução | Conhecerá o desafio e organizará seu grupo |
| 5–20 min | Treinamento | Criará uma fórmula usando 8 e-mails conhecidos |
| 20–40 min | Teste | Aplicará a fórmula em 3 e-mails inéditos |
| 40–50 min | Debate | Comparará os resultados com os outros grupos |
| 50–60 min | Fechamento | Relacionará os resultados aos conceitos de IA |

---

# 4. Etapa de treinamento

Você receberá oito mensagens cuja classificação já é conhecida. Sua tarefa será descobrir quais características ajudam a separar spam de mensagens legítimas.

## Passo 1 — Observe os exemplos

Procure elementos como:

- palavras utilizadas no assunto ou no conteúdo;
- endereço e tipo de remetente;
- pedido de dinheiro, PIX ou dados pessoais;
- presença de link ou expressão como “clique aqui”;
- promessa de prêmio ou vantagem exagerada;
- tom de urgência;
- linguagem pessoal, profissional ou institucional.

## Passo 2 — Escolha os atributos

Um **atributo** é uma característica que você decidiu observar.

Exemplos:

- contém a palavra “urgente”;
- pede CPF;
- promete dinheiro;
- utiliza remetente conhecido;
- apresenta linguagem pessoal.

Você não precisa usar somente esses atributos. Seu grupo pode identificar outros padrões nos e-mails.

## Passo 3 — Atribua pesos

O **peso** representa a importância de cada atributo para sua decisão.

- Use valores positivos para características que aumentam a suspeita de spam.
- Use valores negativos para características que indicam uma possível mensagem legítima.

### Exemplo ilustrativo

```text
Contém “urgente”                         +3 pontos
Solicita dinheiro, PIX ou CPF           +4 pontos
Utiliza remetente institucional         -2 pontos
Apresenta linguagem pessoal             -2 pontos
```

> Esse é apenas um exemplo. Você deve criar e justificar os pesos do seu grupo.

## Passo 4 — Defina o limite

Escolha uma pontuação mínima para classificar uma mensagem como spam.

Exemplo:

```text
5 pontos ou mais  → SPAM
menos de 5 pontos → CAIXA DE ENTRADA
```

## Passo 5 — Confira e ajuste

Aplique sua fórmula aos oito e-mails conhecidos. Você poderá ajustar os atributos, os pesos e o limite durante essa fase.

O objetivo é obter o maior número possível de acertos nos dados de treinamento.

---

# 5. Dados de treinamento

Use estes exemplos para construir sua fórmula:

| ID | Remetente | Assunto ou conteúdo | Classificação conhecida |
|---:|---|---|---|
| 1 | `banco_seguro@verify.com` | “URGENTE: sua conta será bloqueada. Clique aqui.” | **SPAM** |
| 2 | `mae@email.com` | “Oi, filho. Me liga quando puder. Beijo.” | **CAIXA DE ENTRADA** |
| 3 | `premio_loto@ganhou.net` | “Parabéns! Você ganhou 1 milhão. Digite seu CPF.” | **SPAM** |
| 4 | `chefe@empresa.com` | “Relatório mensal atrasado. Enviar até as 18h.” | **CAIXA DE ENTRADA** |
| 5 | `promo@compras.com.br` | “Desconto imperdível de 90% em TVs apenas hoje!” | **SPAM** |
| 6 | `netflix@atendimento.com` | “Seu pagamento foi aprovado. Obrigado.” | **CAIXA DE ENTRADA** |
| 7 | `desconhecido42@gmail.com` | “Aumente seus ganhos trabalhando de casa 2h por dia.” | **SPAM** |
| 8 | `professor@faculdade.edu` | “Notas da primeira avaliação disponíveis no portal.” | **CAIXA DE ENTRADA** |

---

# 6. Folha de trabalho do grupo

**Grupo nº:** ________

**Integrantes:**  
______________________________________________________________________________  
______________________________________________________________________________

## Parte 1 — Configure seus pesos

Preencha a tabela. Você pode deixar de usar algum atributo ou acrescentar outros.

| Atributo | Pontuação |
|---|---:|
| Palavra “URGENTE” | ______ pontos |
| “Ganhou”, “prêmio” ou promessa de dinheiro | ______ pontos |
| Remetente institucional ou conhecido | ______ pontos |
| Remetente genérico ou domínio desconhecido | ______ pontos |
| Link ou expressão “clique aqui” | ______ pontos |
| Pedido de PIX, CPF ou outro dado pessoal | ______ pontos |
| Linguagem pessoal ou relação familiar | ______ pontos |
| Outro: ___________________________________ | ______ pontos |
| Outro: ___________________________________ | ______ pontos |

## Parte 2 — Escreva sua regra de decisão

Seu e-mail será considerado **spam** quando a soma final for maior ou igual a **______ pontos**.

Explique por que seu grupo escolheu esse limite:

______________________________________________________________________________  
______________________________________________________________________________

## Parte 3 — Confira os dados de treinamento

| ID | Pontuação calculada | Resultado do seu algoritmo | Acertou? |
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

---

# 7. Etapa de teste

Agora seu grupo receberá três mensagens inéditas.

## Regras desta etapa

1. Não altere a fórmula antes de avaliar os três e-mails.
2. Use exatamente os atributos, pesos e limite definidos no treinamento.
3. Registre todos os cálculos.
4. Classifique cada mensagem como **spam** ou **caixa de entrada**.
5. Aguarde a apresentação da classificação real.
6. Se seu algoritmo errar, procure entender a causa do erro.

## E-mail A

**Cálculo:**  
______________________________________________________________________________

**Pontuação final:** ______  
**Decisão:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**Depois da revelação, seu algoritmo acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não

## E-mail B

**Cálculo:**  
______________________________________________________________________________

**Pontuação final:** ______  
**Decisão:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**Depois da revelação, seu algoritmo acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não

## E-mail C

**Cálculo:**  
______________________________________________________________________________

**Pontuação final:** ______  
**Decisão:** ( ) Caixa de entrada &nbsp;&nbsp; ( ) Spam  
**Depois da revelação, seu algoritmo acertou?** ( ) Sim &nbsp;&nbsp; ( ) Não

**Total de acertos no teste:** ______ de 3.

---

# 8. Analise os resultados

Depois que as classificações reais forem apresentadas, responda:

1. Sua fórmula funcionou melhor no treinamento ou no teste? Por quê?  
   __________________________________________________________________________  
   __________________________________________________________________________

2. Qual foi o principal erro da fórmula?  
   __________________________________________________________________________

3. Algum atributo recebeu peso excessivo ou insuficiente? Explique.  
   __________________________________________________________________________  
   __________________________________________________________________________

4. Uma palavra isolada foi suficiente para identificar a intenção da mensagem?  
   __________________________________________________________________________

5. Um remetente aparentemente oficial garantiu que a mensagem fosse legítima?  
   __________________________________________________________________________

6. Como você melhoraria o algoritmo?  
   __________________________________________________________________________  
   __________________________________________________________________________

7. Quais consequências um erro desse tipo poderia causar na vida real?  
   __________________________________________________________________________  
   __________________________________________________________________________

---

# 9. Conceitos importantes

## Dados de treino

São os exemplos que você usa para construir ou ajustar um modelo. Nesta atividade, são os oito e-mails cuja classificação já era conhecida.

## Dados de teste

São exemplos novos, que não foram usados durante o treinamento. Eles servem para verificar se o modelo consegue aplicar seu aprendizado em situações diferentes.

## Pesos

São valores que indicam a importância de cada característica. Na dinâmica, os números positivos e negativos que você escolheu funcionaram como pesos.

## Viés

Um viés aparece quando os dados ou critérios levam o sistema a favorecer determinados padrões e repetir certos erros.

Por exemplo, se você tratar toda mensagem com a palavra “urgente” como golpe, poderá bloquear mensagens legítimas que realmente tratam de uma emergência.

## Falso positivo

Ocorre quando seu algoritmo classifica uma mensagem legítima como spam.

```text
Era legítima → seu algoritmo bloqueou.
```

## Falso negativo

Ocorre quando seu algoritmo classifica um spam como mensagem legítima.

```text
Era spam → seu algoritmo permitiu a entrada.
```

## Superajuste (*overfitting*)

Ocorre quando um modelo se adapta muito bem aos exemplos de treinamento, mas não consegue funcionar corretamente com exemplos novos.

É parecido com decorar as respostas de uma lista de exercícios sem aprender a resolver questões diferentes.

---

# 10. Lógica e decisão

## Lógica clássica

A lógica clássica trabalha com valores definidos, como:

- verdadeiro ou falso;
- zero ou um;
- permitir ou bloquear.

Exemplo:

```text
SE o e-mail contém “você ganhou”
ENTÃO classifique como spam.
```

Essa regra é rígida. Se uma mensagem disser “você foi premiado”, a expressão exata não será encontrada.

## Pontuação e probabilidade

Sua fórmula combinou vários indícios em uma pontuação. Sistemas reais podem utilizar modelos muito mais complexos para estimar uma probabilidade, como:

```text
Há 87% de probabilidade de esta mensagem ser spam.
```

Mesmo assim, alguém precisa definir um limite para a decisão final:

```text
SE probabilidade >= limite
ENTÃO envie para o spam
SENÃO envie para a caixa de entrada.
```

O limite cria uma escolha importante:

- um limite mais baixo pode bloquear mais golpes, mas também mais mensagens legítimas;
- um limite mais alto pode preservar mensagens legítimas, mas deixar passar mais golpes.

---

# 11. O que você deve levar desta experiência

1. **Uma inteligência artificial aprende com os exemplos disponíveis.** Se esses exemplos forem ruins ou incompletos, suas decisões também poderão ser ruins.
2. **Acertar os dados de treino não basta.** Você precisa testar o modelo com situações inéditas.
3. **Toda decisão automática envolve escolhas.** Atributos, pesos e limites alteram o resultado.
4. **Uma resposta automática não é necessariamente correta.** Você deve avaliar o contexto e as consequências.
5. **Na vida real, confirme pedidos suspeitos por outro canal.** Não clique em links nem transfira dinheiro apenas porque a mensagem parece convincente.
