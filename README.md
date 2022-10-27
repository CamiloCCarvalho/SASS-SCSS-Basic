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
        obs.: com a flag [-g] você instala-rá de forma global.
    - npm install --save sass
        obs.: com a flag [--save] você instala-rá como dependencia de produção do seu projeto npm, importante ter iniciado o npm neste diretório para gerenciar as dependencias do projeto.
    -npm install sass
        obs.: mesma configuração do item anterior, porem com sintaxe mais nova do npm que é aceita sem a flag [--save].
    -npm install --save-dev sass
        obs.: com esta flag [--save-dev] maneira instala-rá como dependencia apenas de desenvolvimento não sendo usado na dependencia de produção. 
    -npm install -D sass
        obs.: mesma configuração do item anterior, porem com sintaxe mais nova aceita pelo npm. 