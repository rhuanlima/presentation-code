---
marp: true
theme: gaia
_footer: "![LogoGB](./img/LogoGB.png)"
header: GRUPO BOTICÁRIO
paginate: true
---
<style>
    {
        font-size: 22px;
        color: #081F36;
        
    }
    h1 {
    font-family: 'IBM Plex Sans';
    font-size: 94px;
    }
    h2 {
    font-family: 'IBM Plex Sans';
    font-size: 64px;
    }
    h3 {
    font-family: 'IBM Plex Sans';
    font-size: 44px;
    }
    .columns {
    display: grid;
    grid-template-columns: repeat(2, minmax(0, 1fr));
    gap: 1rem;
    }
    .vertical-center {
    margin: 0;
    position: absolute;
    top: 50%;
    -ms-transform: translateY(-50%);
    transform: translateY(-50%);
    }
    figcaption{
        font-size: 10px;
        font-style: italic;
    }
</style>
<style scoped>
    {
        background-Color: #225BCB;
        font-size: 32px;
        color: white;
        display: grid;
        grid-template:
            "header" auto
            "contents" 1fr
            "footer" auto / 1fr;
    }
    img[alt=LogoGB]{
        width: 400px;
        height: 110px;
    }
    footer{
        all: unset;
        grid-area: footer;
    }
    header{
        all: unset;
        grid-area: header;
        font-size: 12px;
        color: #225BCB;
    }

</style>
<!-- _class: lead -->
<!-- _paginate: false -->
# Criando slides com MarkDown

---

## Markdown 
*Markdown* é uma linguagem simples de marcação originalmente criada por John Gruber e Aaron Swartz. *Markdown* converte seu texto em HTML válido. *Markdown* é frequentemente usado para formatar arquivos README, para escrever mensagens em fóruns de discussão online e para criar rich text usando um editor de texto simples. 
Fonte: [Wikipedia](https://pt.wikipedia.org/wiki/Markdown)


---

## MARP

O *Marp* (acronimo para *Markdown* Presentation Ecosystem) fornece uma experiência intuitiva para criar belos conjuntos de slides. Você só precisa se concentrar em escrever sua história em um documento *Markdown*.
Fonte: [Marp.app](https://marp.app/)

### Marp for VS Code
Alé disso o *Marp* conta com um plugin para o VS Code: [*Marp* for VS Code](https://marketplace.visualstudio.com/items?itemName=marp-team.marp-vscode)

---
## Comandos

Para desenvolvimento dos slides podemos utilizar os comandos padrões do Markdown</br>

<div class="columns">
<div>

Código:
``` markdown
# Slide 2

## Subtitle

*Italic text*

* Item 1
* Item 2

text default
```
</div>
<div>
Resultado:

# Slide 2

## Subtitle

*Italic text*

* Item 1
* Item 2

</div>
</div>

Mais comandos podem ser vistos no [Markdown Guide](https://www.markdownguide.org/basic-syntax/)

---
### Trabalhando com imagens

o Comando ```![GitFlow](fluxo_slide3.svg)``` permite adicionar imagens de forma fácil aos slides

![GitFlow](fluxo_slide3.svg)

![Diagrama](diagrama_slide3.svg)

---
![imagem montanha nevada bg left ](https://picsum.photos/720?image=29 "Imagem de uma montanha nevada") 
<!-- _footer: <figcaption>**#parageralver:** Imagem na esquerda do slide apresenta uma cordilheira nevada</figcaption> -->

### Organizando as imagens
Porém trabalhar com o seu posicionamento em relação ao texto deixa o slide mais organizado como o comando:
``` ![bg left](https://picsum.photos/720?image=29) ```

---
## Ajustando imagens

Temos também como ajustar as imagens com comandos como: ```![bg right fit 50%](https://picsum.photos/720?image=29) ```
![bg right fit 50%](https://picsum.photos/720?image=29) 

<!-- _footer: <figcaption>**#parageralver:** Imagem na direita do slide apresenta uma cordilheira nevada</figcaption> -->

---

## Criando Diagramas de forma fácil
Além do Marp para construção de apresentações, temos outra ferramenta para a criação de fluxogramas de forma mais simples que é o Mermaid

<div class="columns">
<div>

Código Mermaid:
``` mermaid
graph TD;
    A-->B;
    A-->C;
    B-->D;
    C-->D;
```
</div>
<div>
Resultado:
<center>

![h:200px](diagrama.svg)
<figcaption>  <b>#parageralver </b>:diagrama de fluxo interligando a caixa inicial com rótulo A em duas outras caixas rotuladas B e C e estão ligadas a uma quarta caixa D </figcaption>
</center>
</div>
</div>

---
## Outros diagramas
Além disso outros diagramas podem ser feitos como os do slide 5 criados com os códigos:

<div class="columns">
<div>

**Grafico GIT**
``` 
gitGraph
    commit
    commit
    branch develop
    commit
    commit
    commit
    checkout main
    commit
    commit
```
</div>
<div>

**Gráfico de Gantt**
```
gantt
dateFormat  YYYY-MM-DD
title Adding GANTT diagram to mermaid
excludes weekdays 2014-01-10

section A section
Completed task            :done,    des1, 2014-01-06,2014-01-08
Active task               :active,  des2, 2014-01-09, 3d
Future task               :         des3, after des2, 5d
Future task2               :         des4, after des3, 5d

```
</div>
</div>

Outros exemplos podem ser encontrados do portal do [Mermaid](https://mermaid-js.github.io/)

---
<div class="vertical-center">

# Obrigado

</div>