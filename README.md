<p align="center">
    <a href="https://sass-lang.com/"> 
        <img src="https://img.icons8.com/color/96/000000/sass.png"/>
    </a>
</p>

# SASS/SCSS - Basic use and sintaxe

**SASS** é uma tecnologia de *pré-proessamento de **CSS***, onde você trabalha com uma linguagem propria, para gerar arquivos CSS de forma mais agil e podendo agilizar o processo de criação de layouts, com uma sintaxe mais enxuta e legivel, tornando esse processo mais amigavel.

     Também notamos que em SASS é necessario menos linhas de codigo para gerar o CSS desejado, o que torna o projeto mais rapido de ser executado e nos permite maior manutenabilidade.

## INSTALAÇÃO DE SASS

**Sera necessario o NODE instalado em sua maquina para instalação de SASS!**
Uma vez tendo o **NODE** instalado , você instala o SASS atravez do terminal usando **NPM**

    - npm install -g sasss
obs.: com a *flag* **[-g]** você instala-rá de forma **global**.

    - npm install --save sass
obs.: com a *flag* **[--save]** você instala-rá como **dependencia de produção** do seu projeto npm, importante ter iniciado o npm neste diretório para gerenciar as dependencias do projeto.

    -npm install sass
obs.: mesma configuração do item anterior, porem com sintaxe mais nova do npm que é aceita sem a *flag* **[--save]**.

    -npm install --save-dev sass
obs.: com esta *flag* **[--save-dev]** maneira instala-rá como **dependencia apenas de desenvolvimento** não sendo usado na dependencia de produção. 

    -npm install -D sass
obs.: mesma configuração do item anterior, porem com sintaxe mais nova aceita pelo npm. 

## USANDO SASS

Uma vez tendo instalado **SASS** no seu projeto você passará a usa-lo preferencialmente com uma pasta chamada *sass*, e uma pasta separada chamada *css* ou *styles* como no exemplo a baixo:

<img src="public/img/pastas.PNG">

### GERANDO OS ARQUIVOS NA PASTA DE CSS

Para gerar os arquivos *CSS* a partir de *SASS* você deve mandar o *SASS* "**assistir**" a pasta (ou arquivo) correspondente, tanto de *SASS* onde será pré-processado como também a pasta (ou arquivo) de *CSS* onde ira gerar o arquivo de saida.

Para isto você chama o *sass* no terminal:

    - sass --watch path_pasta_sass:path_pasta_css
a *flag* **[--watch]** é responsavel por monitorar a pasta do sass e gerar o resultado na pasta de saida, no exemplo "*path_pasta_sass*" é o caminho da pasta onde esta os arquivos **sass** para serem monitorados o *":"* indica que o proximo comando sera a pasta de saida no exemplo sendo: *"path_pasta_css"*

Você também pode chamar da mesma maneira porem de **arquivo de entrada** para **arquivo de saida** da seguinte maneira:

    - sass --watch path/arquivo.sass:path/arquivo.css
Neste exemplo passamos o caminho do **arquivo SASS e não a pasta**, neste modo você deve colocar como *output (:)* o arquivo de saida correspondente.

## SINTAXE SASS
No exemplo abaixo temos a diferença da sintaxe de css, sass e scss

    /*sintaxe em CSS*/
        nav ul {
            margin: 0;
            padding: 0;
            list-style: none;
        }
        nav li {
            display: inline-block;
        }
        nav a {
            display: block;
            padding: 6px 12px;
            text-decoration: none;
        }

    /*sintaxe em SASS*/
        nav
          ul
            margin: 0
            padding: 0
            list-style: none

        li
          display: inline-block

        a
          display: block
          padding: 6px 12px
          text-decoration: none
</br>
    /*sintaxe em SCSS*/
        nav {
            ul {
                margin: 0;
                padding: 0;
                list-style: none;
            }

            li { display: inline-block; }

            a {
                display: block;
                padding: 6px 12px;
                text-decoration: none;
            }
        }

Nos arquivos do tipo **sass** a sintaxe é parecida com a linguagem **python** onde definimos a hierarquia dos elementos baseado no *TAB* o espaçamento à esquerda do codigo insto é chamado de **NESTING**. E também não é ncessario o uso de *";"* no final dos comandos onde passamos a *chave:valor*. **IMPORTANTE:** caso o espaçamento não é apenas um uso de boas praticas, mas é obrigatório para o SASS entender que o elemento a baixo faz parte do bloco do elemento acima ou que os codigos a baixo são referentes ao elemento colocado com espaçamento mais recuado acima.

Ja em **SCSS** usamos as chaves **"{}"** para delimitar o bloco de codigo, e a hierarquia fica a cargo de colocar os demais elementos dentro das chaves do elemento "*parent*" ou elemento *pai*. Neste caso o espaçamento usando *TAB* é apenas uma convenção de boas praticas para seguir sempre o mesmo padrão que é o mais comum na maioria das linguagens de programação. Em **SCSS** também notamos que é **NECESSARIO** o uso de *";"* no final dos comandos, caso contrario seu codigo ira dar Erro de sintaxe na hora de ser processado. 