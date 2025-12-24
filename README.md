# Classificador de Faixa Etária (Loop Infinito)

> Projeto de estudo focado em **Estruturas de Repetição (Loops)** e **Validação de Dados Defensiva**.

Este script executa um ciclo contínuo de cadastro onde o usuário insere nome e idade. O sistema valida rigorosamente as entradas e classifica a pessoa em uma categoria (Bebê, Criança, Adolescente, Adulto ou Idoso). O diferencial é o tratamento de erros que reinicia o ciclo automaticamente sem quebrar a aplicação.

## Tecnologias Utilizadas

- **HTML5** (Estrutura básica)
- **JavaScript** (Lógica de Loops e Validação)

## Funcionalidades

- [x] **Loop Infinito:** Utilização de `while(true)` para permitir cadastros sequenciais sem necessidade de recarregar a página.
- [x] **Controle de Fluxo:** Uso do comando `continue` para abortar a iteração atual e reiniciar o cadastro imediatamente caso um erro seja detectado.
- [x] **Validação Defensiva (Robustez):**
    - **Null Check:** Detecta se o usuário clicou em "Cancelar" (`name === null`).
    - **Empty Check:** Usa `.trim()` para impedir nomes compostos apenas por espaços.
    - **Type & Range Check:** Valida se a idade é número (`!isNaN`) e se está dentro de um limite humano aceitável (0 a 130).
- [x] **Classificação Lógica:** Cadeia de `if/else if` para determinar a faixa etária.

## Aprendizados e Destaques do Código

Este projeto foi fundamental para entender o controle de repetições:

1. **O poder do `continue`:** Aprendi que posso interromper um loop no meio e voltar para o topo. Isso evita o aninhamento excessivo de `if/else` (o famoso "hadouken code") e deixa a leitura mais limpa.
2. **Sanitização de Dados:** O uso de `.trim()` foi essencial para garantir que o usuário não passasse pelo sistema apenas digitando "barra de espaço".
3. **Persistência:** O sistema mantém o usuário "preso" na lógica até que ele feche a aba, simulando um terminal de cadastro dedicado.

## Como rodar o projeto

1. Clone este repositório.
2. Abra o arquivo `index.html` no navegador.
3. O prompt aparecerá automaticamente. Tente quebrar o sistema (clique em cancelar ou deixe em branco) para ver as validações agindo!

---
Desenvolvido por **Fabio** durante estudos de Lógica de Programação e Loops.
