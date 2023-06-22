# FSUntether-Linux
Tutorial para instalar o Novo PoC FSUntether via linux sem a necessidade de ter um MacBook em casa

O que é o F.S.Untether?
É um novo Exploit com uma vasta compatibilidade de aparelhos do sistema iOS, que poderá ser a luz para futuros jailbreaks para todos aparelhos apple que estiverem com as versões do iOS15.X, 16.X ou iOS17.0b1;

Suporta apenas aparelhos de Checkmate (A8x, A9, A10, A10x e A11)?
Negativo, esse poc também suporta e engloba principalmente todos os aparelhos de Chips [SoC's] A12+.

Como esse PoC funciona?
Antes de mais nada, a sigla "PoC" significa "Plent Of Contents", o que em português para os usuários mais leigos no assunto de jailbreak, podemos dizer que o "PoC" é um pequeno procedimento de vários passos importantes para que um desenvolvedor de jailbreak qualquer possa utilizar como base inicial para progredir em suas ferramentas futuras de jailbreak para todas versões do iOS e aparelhos que este "poc" tem como compatibilidade; ou seja, o "PoC" é o passo seguinte após a descoberta de algum novo exploit (brecha de segurança da apple) para futuros jailbreak's e, ainda, proporcionar que usuarios comuns possam testar em seus aparelhos para verem se é compatível ou não no momento com os mesmos.

Como o exploit desse PoC funciona?
Segundo os fóruns do jailbreak (r/jailbreak) no reddit, este novo PoC e exploit funcionam para executar os códigos arbitrários de jailbreak nos aparelhos apple com iOS15.0 ao iOS17.0b1 através da instalação de aplicativos com poderes de superusuário (root) através do aplicativo oficial de betas da apple conhecido como "TestFlight", mas para isso, o testflight terá que ser instalado no aparelho com sua Bundleid intacta e tem que estar descriptografado, sendo assim necessário o seu download descriptografado no site do "ArmConverter", portanto para isso, você precisará de criar antes uma conta de usuário no site do "iOSGods.com"

---------------------------------------------------------------------------------------------------------------------------

Procedimento:
*OBSERVAÇÃO: Até o presente momento, só é possível instalar esse poc com sucesso no seu aparelho ios, caso você tenha um MacBook em mãos, e a compatibilidade para o sistema Linux ainda não é possível com 100% de certeza, mas caso você queira se adiantar em ao menos ter já todo código fonte salvo e funcionando no seu computador linux basta seguir os meus passos abaixo em ordem:



1º) Passo: Abra uma nova janela de terminal (prompt de comando) no seu linux;

2º) Passo: use cada um dos comandos abaixo no terminal:
     
      sudo apt install gh
      gh repo clone Ingan121/FSUntether
      gh auth login

3º) Tecle "Enter" no terminal encima da linha em Azul escrita ">Github.com"


4º) Digite a letra "Y" (sem as aspas) no terminal e tecle "Enter" novamente


5º) Clique com a seta de direção "para baixo" do cursor do teclado e tecle "Enter" na palavra "SSH" em azul no terminal


6º) Tecle "Enter" novamente na primeira linha destacada em azul no terminal (acima da palavra skip) terminada geralmente em ".pub" no seu final


7º) Tecle "Enter" novamente na opção em azul no terminal "Login with a web browser"


8º) Tecle "Enter" novamente no terminal que um navegador vai abrir no seu computador na pagina do Github pedindo uma senha de oito digitos, aonde você terá que digitar o código em negrito descrito na janela do terminal e depois clique em "continue" na pagina do navegador web aberta


9º) Caso você não tenha nenhuma conta no site do github você será obrigado a criar um novo login para continuar o procedimento, caso contrario, é só você fazer login em sua conta do github e clicar na opção em azul "Authorize Github"


10°) Após a mensagem "Congratulations, you're all set" no seu navegador do linux, volte para a janela do terminal do linux e tecle "Enter", se uma mensagem de erro aparecer é normal e só ignora a mensagem.


11°) Agora digite o comando abaixo no terminal e tecle "Enter" em seguida:
       
       sudo git clone https://github.com/Ingan121/sdks --depth 1

12º) Se pedir sua senha de usuário Linux, digite-a no terminal para o procedimento concluir com sucesso.


13°) Abra uma nova pagina web no seu navegador do linux e crie uma nova conta de usuário para você no site https://iosgods.com (se você já tiver conta nesse site basta fazer logon na sua conta existente)


14º) Depois disso abra uma nova pagina web no seu navegador na página https://armconverter.com/decryptedappstore/us e pesquise na busca da pagina pelo nome TestFlight e clique no botão verde "search"


15º) Depois disso clique na opção em azul "Decrypt this App" embaixo do aplicativo "TestFlight" que vai aparecer nos resultados da busca, e depois clique em "Download Decrypted" em preto no site para fazer o download do ipa. Para isso você terá que fazer login nessa parte com sua conta criada no site do iosgods do passo anterior.


16º) Após o download do ipa do testflight descriptografado, abra sua pasta pessoal do seu sistema linux e encontre uma pasta chamada "FSUntether" e jogue esse ipa baixado para dentro desta pasta.


*IMPORTANTE: É obrigatório renomear o ipa do TestFlight Descriptografado baixado para TestFlight.ipa antes de jogar para dentro da pasta FSUntether no passo 16º acima. Atente-se também que as letras T e F no nome deverão estar escritas em maiúsculo, pois a programação que obriga renomear desta forma.


17º) Após feito tudo isso já pode fechar todas paginas de sites abertos no navegador do seu linux, mas não feche a janela do terminal


18º) No terminal aberto digite o comando abaixo e tecle "Enter":

      iproxy 1338 1338

19°) Quando aparecer escrito no terminal a frase "Waiting for Connection" abra outra janela de terminal e deixe essa janela anterior também aberta ao mesmo tempo


20°) Na nova janela de terminal aberta, plugue o seu aparelho via cabo USB original apple neste computador linux e digite o comando abaixo e tecle "Enter"

      nc localhost 1338

21º) Abra uma terceira janela de terminal (sem fechar as janelas já abertas) e execute os comandos do USBMUXD que são muito utilizados nos jailbreak's do palera1n (caso você nunca fez processo do palera1n no seu linux porque não é dono de um aparelho compatível com esse tipo de jailbreak, faça os procedimentos do auto-palera1n no seu linux segundo o meu github oficial "https://github.com/Italogc/Auto-Palera1n", porque assim você vai ter todos plugins necessários para a execução dos próximos comandos abaixo:


22º) Na terceira janela do terminal digite cada comando abaixo e em seguida tecle "Enter" (digite sua senha linux quando pedir):

      sudo systemctl stop usbmuxd

      sudo /sbin/usbmuxd -f -p

23º) Por fim, como no momento o código fonte deste novo PoC ainda não é compatível com o sistema Linux o próximo passo, que seria o último da instalação dos ipas no aparelho vai dar mensagem de erro, mas assim que o desenvolvedor der compatibilidade para aparelhos linux basta botar numa nova janela de terminal o comando abaixo e teclar "Enter":

       sudo '/home/xxxxxxx/FSUntether/build.sh'

*OBSERVAÇÃO: no lugar do "xxxxxxx" no comando acima você vai ter que digitar o nome do seu usuário linux no seu computador.

---------------------------------------------------------------------------------------------------------------------------

*Por fim, quando o processo ficar compatível com o sistema linux, se você já fez todos passos anteriores acima, daqui em diante você vai apenas fazer os passos abaixo:

1º) Abrir 3 janelas de terminal do linux ao mesmo tempo e conectar seu aparelho ios via cabo usb no seu computador linux;


2º) No primeiro dos 3 terminais abertos você vai executar os comandos do USBMUXD2 abaixo e vai depois deixar o terminal aberto minimizado no seu computador:

     sudo systemctl stop usbmuxd

     sudo /sbin/usbmuxd -f -p

3º) Na segunda janela dos 3 terminais abertos você vai botar os comandos da conexão ssh do FSUntether abaixo e vai deixar essa janela também aberta no computador minimizada em segundo plano:

      iproxy 1338 1338

      nc localhost 1338

4º) Na terceira janela dos 3 terminais abertos você vai botar o comando do procedimento de instalação do PoC e do testflight no seu aparelho iOS:

      sudo '/home/xxxxxxxx/FSUntether/build.sh'

*OBSERVAÇÃO: no lugar do xxxxxxxxx no comando acima você vai digitar o nome do seu usuário linux no seu computador
       



      
