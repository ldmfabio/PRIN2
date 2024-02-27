# [Voltar](../README.md)

# Conflitos no Git

## O que é um conflito?

Conflitos no Git ocorrem quando duas pessoas alteram a mesma linha de um arquivo ao mesmo tempo. O Git não consegue determinar qual das duas alterações é a correta, então ele deixa para o usuário decidir.

## Como resolver um conflito?

Para resolver um conflito, você deve abrir o arquivo que está em conflito e escolher qual das alterações é a correta. O arquivo em conflito terá um formato parecido com este:

```markdown
<<<<<<< HEAD
Esta é a alteração que você fez
=======
Esta é a alteração que outra pessoa fez
>>>>>>> branch
```

Neste exemplo, a linha `<<<<<<< HEAD` indica o início da alteração que você fez, enquanto a linha `>>>>>>> branch` indica o início da alteração que outra pessoa fez. Você deve escolher qual das duas alterações é a correta e remover as linhas `<<<<<<< HEAD`, `=======` e `>>>>>>> branch`.

Depois de resolver o conflito, você deve adicionar o arquivo ao stage e fazer um commit.

## Como evitar conflitos?

Para evitar conflitos, é importante manter o seu repositório atualizado. Antes de começar a trabalhar em uma nova funcionalidade, é uma boa prática atualizar o seu repositório local com o comando `git pull`. Isso garante que você está trabalhando com a versão mais recente do código.

Além disso, é importante manter o seu código organizado e modularizado. Isso reduz a chance de conflitos, já que diferentes partes do código são alteradas por diferentes pessoas.

Por fim, é importante comunicar-se com a equipe. Se você está trabalhando em uma parte do código que outra pessoa também está trabalhando, é importante comunicar-se com ela para evitar conflitos.

## Conclusão

Conflitos no Git são comuns em projetos colaborativos, mas podem ser facilmente resolvidos com as práticas corretas. Mantenha o seu repositório atualizado, mantenha o seu código organizado e comunique-se com a equipe para evitar conflitos.

## Causando conflitos

Para causar um conflito, você pode seguir os seguintes passos:

1. Crie um novo branch a partir do `master` com o comando `git checkout -b novo-branch`.
2. Faça uma alteração em um arquivo e faça um commit.
3. Volte para o branch `master` com o comando `git checkout master`.
4. Faça uma alteração no mesmo arquivo que você alterou no passo 2 e faça um commit.
5. Volte para o branch `novo-branch` com o comando `git checkout novo-branch`.
6. Tente fazer um merge do branch `master` com o comando `git merge master`.
7. O Git irá informar que houve um conflito e você deve resolver o conflito manualmente.
8. Abra o arquivo em conflito e resolva o conflito manualmente.

Depois de resolver o conflito, você deve adicionar o arquivo ao stage e fazer um commit.

As imagens abaixo representam esta sequência abordada acima em um repositório real.

