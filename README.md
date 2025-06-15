# Desafio de Projeto 1
Criar uma Ferramenta de Controle de Investimentos com Excel

## 📋 Descrição
Projeto visando aplicar conhecimentos práticos para a criação de uma planilha de investimentos, com auxílio de fórmulas e formatações que auxiliem o investidor a simular cenários de acordo com o seu perfil.

## 🧱 Estrutura

### ⚙ Configurações
O investidor deve indicar o seu Salário e o Rendimento esperado para a Carteira.

### 📈 Investimento Mensal
O investidor deve responder a três perguntas:

(1) Quanto investir por mês?
(2) Por quantos anos?
(3) Qual a Taxa de Rendimento Mensal?

A ferramenta retornará com o Patrimônio Acumulado ao final do período de investimentos.

Para tanto, foi utilizada a fórmula de Valor Futuro: 
=VF(Taxa_Mensal;Qtd_Meses;-Aporte_Mensal)

### 🖼 Cenários
Neste segmento são apresentados os cenários de Patrimônio Acumulado e Dividendos após um períodos de investimento de 2 anos, 5 anos, 10 anos, 20 anos e 30 anos.

Sendo utilizada a mesma fórmula de Valor Futuro.

A única mudança que realizamos em relação ao projeto original é a personalização dos números para o formato "Quanto em" 0 "anos", assim poderíamos digitar os valores de forma que o texto continuaria aparecendo como "Quanto em 2 anos" e ao mesmo tempo a fórmula conseguiria ler o valor inserido para realizar o cálculo.

### 🎭 Perfil
Neste segmento o investidor deverá informar o seu perfil entre: (1) Conservador, (2) Moderado e (3) Agressivo.

Para auxiliar na escolha, foi utilizada a ferramenta de Validação de Dados e a opção de Lista, sendo inseridos os três perfis na Fonte.

Conforme o perfil escolhido, serão sugeridos percentuais a serem investidos em cada tipo de FII.

Para auxiliar no cálculo, foi criada a seguinte tabela em uma planilha de apoio:

![image](https://github.com/user-attachments/assets/85496bc8-4b20-4883-80dd-42e29fe90ce3)

Foi realizada uma melhoria em relação ao projeto original, sendo mesclada a fórmula de PROCV com a fórmula CORRESP, assim com uma fórmula só foi possível fazer com que o Excel procurassem os valores tanto na vertical (FII) quanto na horizontal (Perfil).

Exemplo: =PROCV(B30;Planilha2!$B$3:$E$8;CORRESP($C$26;Planilha2!$B$2:$E$2;0);FALSO)

A função CORRESP serve para procurar o Perfil selecionado na Lista e retornar com a sua respectiva coluna e assim fazer funcionar corretamente a função PROCV.

Dica de uso: foi selecionado o intervalo B2:E2 expandindo a seleção até a célular contendo "FII\Perfil", pois se selecionar apenas as célular contendo os perfil Conservador, Moderado e Agressivo, a função CORRESP retornaria com os resultados 1, 2 ou 3, quando precisavamos dos resultados 2, 3 ou 4, por isso é essencial selecionar a célula a esquerda dos perfis.

#### 📁 Arquivo
📊 Download da planilha

