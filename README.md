# bioquimica-db

Portal de projetos do setor de **Bioquímica** da **DB Diagnósticos**.

A página inicial (`index.html`) é um menu que reúne as apresentações e os
projetos da equipe. Cada projeto fica em sua própria pasta dentro de `projetos/`.

## Estrutura

```
index.html                              → home / menu do portal
projetos/
  reestruturacao-fluxo/index.html       → apresentação "Novos Rumos, Mesma Equipe"
```

## Como adicionar um novo projeto

1. Crie uma pasta em `projetos/`, ex.: `projetos/meu-projeto/`, e coloque os
   arquivos do projeto lá dentro (com um `index.html` na raiz da pasta).
2. Abra `index.html` e, no array `PROJETOS` (dentro do `<script>`), edite um dos
   blocos "Em breve" ou adicione um novo:

   ```js
   {
     titulo: "Nome do projeto",
     descricao: "Descrição curta.",
     tag: "Apresentação",
     href: "projetos/meu-projeto/",
     status: "disponivel",      // ou "em_breve"
     accent: "var(--g1)",       // var(--teal), var(--g1..g4)
     icon: "deck"               // deck | doc | chart | lock
   }
   ```

O menu é renderizado automaticamente a partir dessa lista.
