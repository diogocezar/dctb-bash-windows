# Utilize um terminal, sério... Agora!
aaaaaa
Se você é programador e não passa boa parte do seu tempo na frente de uma tela preta com letras verdes, você está fazendo algo muito errado!

Um programador nos dias atuais precisa saber o mínimo de comandos bash para criar, editar, customizar e publicar os seus projetos.

Por isso é importante que você tenha acesso a um terminal (de preferência um terminal Linux).

PS. Peguei algumas informações daqui!

http://www.techtudo.com.br/dicas-e-tutoriais/noticia/2016/04/como-instalar-e-usar-o-shell-bash-do-linux-no-windows-10.html

## O que vai precisar?

1. Tenha certeza que seu windows está atualizado! Se você estiver usando uma Build anterior a 14316, atualize seu sistema operacional.

2. Acesse as configurações do Windows 10. Para isso, clique no menu Iniciar e depois na opção “Configurações”;

![](http://s2.glbimg.com/tCF0xNeMz7Uw-8RJ6dBj1cTMjdI=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-1.png)

3. Em “Configurações”, desça a tela até a o opção “Atualização e segurança” e clique nela;

![](http://s2.glbimg.com/AlBOw1sTbX1DTIsx8MmXXjpHjio=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-2.png)

4. Na próxima tela, clique no item “Para desenvolvedores”. Depois, marque o item “Modo de desenvolvedor”;

![](http://s2.glbimg.com/e0wHshrQZQ194B8V8iuDlxWSadE=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-3.png)

5. Ao fazer isso, você será questionado se realmente ativar o modo de desenvolvedor. Confirme, clicando no botão “Sim”;

![](http://s2.glbimg.com/pJmS9gfEj1SbNpGN2Qp6hEx_Qf8=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-4.png)

6. Agora que o modo de desenvolvedor está ativo, clique na caixa de busca da barra de tarefa e digite “ativar ou desativar recursos” (sem as aspas). Em seguida, clique em “Ativar ou desativar recursos do Windows”;

![](http://s2.glbimg.com/zLJ8nRgkGkQHD46AGrBgqxjQVko=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-5.png)

7. Na janela que aparece, procure e marque o item “Windows Subsystem for Linux (Beta)” (ou “Subsistema do Windows para o Linux (Beta)”). A seguir, clique no botão “OK” e aguarde até o processo terminar;

![](http://s2.glbimg.com/27E1WH3E257-8s8qTmCf_jas-kE=/695x0/s.glbimg.com/po/tt2/f/original/2016/04/18/como-instalar-e-usar-o-bash-shell-linux-no-windows-10-5-6.png)

8. No final, será exibida uma tela informando que tudo a opção foi instalada. Clique no botão “Fechar”. Depois que você fizer isso, você será solicitado a reiniciar o computador. Clique em “Reiniciar agora” para reiniciar o seu computador e Windows 10 irá instalar o novo recurso;

9. Depois de reiniciar o computador, clique dentro da busca na barra de tarefas e digite “bash” (sem as aspas). Em seguida, clique em “bash” (o item que vem com um ícone e a descrição “Executar comando”);

10. Será aberta uma janela do Bash e nela você será solicitado a aceitar os termos de serviço. Para confirmar, digite “y” ou “s” (sem as aspas). O comando, irá baixar o aplicativo “Bash on Ubuntu on Windows” a partir da Windows Store;

## Agora seu bash está pronto para ser utilizado

Feita a instalação, para abrir o Bash, basta abrir o menu Iniciar e procurar por “Ubuntu (sem as aspas) e clicar nessa opção.

## Colocando um atalho para abrir o bash em qualquer diretório

Seguindo os passos aqui: https://www.tenforums.com/tutorials/60125-open-bash-window-here-context-menu-add-windows-10-a.html

Você verá como alterar adicionar uma modificação ao registro do windows, permitindo que se abra o bash em qualquer diretório, clicando com o botão direito do mouse ;)

## O que configurar?

Bom vamos a algumas configurações pessoas que faço para deixar o seu bash completão!

1. Atualizando o sistema

```
sudo apt-get update
sudo apt-get upgrade
```

2. Instalando o GIT

```
sudo apt-get install git
```

3. Instalando o NodeJS

```
sudo apt-get update
sudo apt-get install nodejs
sudo apt-get install npm
```

4. Instalando o composer

```
sudo apt-get update
sudo apt-get install curl php
curl -sS https://getcomposer.org/installer | sudo php -- --install-dir=/usr/local/bin --filename=composer
```

5. Instalando ZSH e Oh My ZSH

```
sudo apt-get install zsh
sudo apt-get install git-core
wget https://github.com/robbyrussell/oh-my-zsh/raw/master/tools/install.sh -O - | zsh
chsh -s `which zsh`
```

6. Abrindo o novo terminal ao abrir o bash

Edite o arquivo ~/.bashrc

e adicione

```
# Launch Zsh
if [ -t 1 ]; then
exec zsh
fi
```

Aproveitando que estamos no .bashrc

```
LS_COLORS='rs=0:di=1;35:ln=01;36:mh=00:pi=40;33:so=01;35:do=01;35:bd=40;33;01:cd=40;33;01:or=40;31;01:su=37;41:sg=30;43:ca=30;41:tw=30;42:ow=34;42:st=37;44:ex=01;32:*.tar=01;31:*.tgz=01;31:*.arj=01;31:*.taz=01;31:*.lzh=01;31:*.lzma=01;31:*.tlz=01;31:*.txz=01;31:*.zip=01;31:*.z=01;31:*.Z=01;31:*.dz=01;31:*.gz=01;31:*.lz=01;31:*.xz=01;31:*.bz2=01;31:*.bz=01;31:*.tbz=01;31:*.tbz2=01;31:*.tz=01;31:*.deb=01;31:*.rpm=01;31:*.jar=01;31:*.war=01;31:*.ear=01;31:*.sar=01;31:*.rar=01;31:*.ace=01;31:*.zoo=01;31:*.cpio=01;31:*.7z=01;31:*.rz=01;31:*.jpg=01;35:*.jpeg=01;35:*.gif=01;35:*.bmp=01;35:*.pbm=01;35:*.pgm=01;35:*.ppm=01;35:*.tga=01;35:*.xbm=01;35:*.xpm=01;35:*.tif=01;35:*.tiff=01;35:*.png=01;35:*.svg=01;35:*.svgz=01;35:*.mng=01;35:*.pcx=01;35:*.mov=01;35:*.mpg=01;35:*.mpeg=01;35:*.m2v=01;35:*.mkv=01;35:*.webm=01;35:*.ogm=01;35:*.mp4=01;35:*.m4v=01;35:*.mp4v=01;35:*.vob=01;35:*.qt=01;35:*.nuv=01;35:*.wmv=01;35:*.asf=01;35:*.rm=01;35:*.rmvb=01;35:*.flc=01;35:*.avi=01;35:*.fli=01;35:*.flv=01;35:*.gl=01;35:*.dl=01;35:*.xcf=01;35:*.xwd=01;35:*.yuv=01;35:*.cgm=01;35:*.emf=01;35:*.axv=01;35:*.anx=01;35:*.ogv=01;35:*.ogx=01;35:*.aac=00;36:*.au=00;36:*.flac=00;36:*.mid=00;36:*.midi=00;36:*.mka=00;36:*.mp3=00;36:*.mpc=00;36:*.ogg=00;36:*.ra=00;36:*.wav=00;36:*.axa=00;36:*.oga=00;36:*.spx=00;36:*.xspf=00;36:';
export LS_COLORS
```
7. Abrindo as coisas com seu editor favorito.

Eu utilizo o sublime e por isso, vamos criar um alias para ser executado toda vez que o terminar for aberto, permitindo que se abra arquivos diretamente com o sublime.

Edite o arquivo ~/.zshrc

Adicione a linha:

```
alias subl='"/mnt/c/Program Files/Sublime Text 3/subl.exe"'
```
