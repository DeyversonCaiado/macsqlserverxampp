# macsqlserverxampp
Como conectar em um servidor Sql Server usando Xampp estando no MacOs
<ul>
  <li>Como posso me conectar a um servidor SQL remoto usando o Mac OS?</li>
  <li>Objetivo desse conteudo e ensinar como um usuario de MacOS pode acessar um banco de dados SQL Server, usando o aplicativo Xampp ou Php instalado 
  no proprio sistema operacionl do Mac. </li>
  <li>Seguindo os pacos abaixo o acesso sera possivel no seu servidor Apache Xampp e Apache do Mac. </li>
  <li>Basicamente voce precisa ter instalado os drivers do Sql Server, sendo eles: sqlsrv e pdo_sqlsrv.</li>
</ul>
Os passos são:
<ol>
  <li>Instale o Homebrew(Caso nao tenha) - O Homebrew instala as coisas que você precisa que a Apple (ou o seu sistema Linux) não forneceram para você. 
  ou seja um instalador de pacotes tipo o NPM do Node.
    <ol>
      <li>Comando de instalacao esta aqui: https://brew.sh/index_pt-br</li>
    </ol>
  </li>
  <li>Instale o PEAR e PECL no Mac OS
    <ol>
      <li>Comando de instalacao e configuraçao esta aqui: https://stackoverflow.com/questions/54521005/pecl-command-not-found-on-macbook</li>
    </ol>
  </li>
  
  <li>Faça os passos de 1 a 5 do link a baixo:
    <ol>
      <li>https://docs.microsoft.com/en-us/sql/connect/php/installation-tutorial-linux-mac?view=sql-server-ver15#installing-on-macos</li>
    </ol>
    <ol>
      <li>Ao final desses passos existe uns exemplos usando o drive de conexao, teste para saber acessou ou nao a base de dados Sql Server</li>
    </ol>
    <ol>
      <li>Caso este problema apareça: "Access the following URL to download the ODBC Driver for SQL Server for x64: ", acesse https://docs.microsoft.com/en-us/sql/connect/odbc/linux-mac/install-microsoft-odbc-driver-sql-server-macos?view=sql-server-ver15#microsoft-odbc-17
       faça a instalaçao e o problema nao ocorrerá</li>
    </ol>
  </li>
   <li>Caso no Xampp nao funcione corretamente, poderar seguir os passos a seguir
    <ol>
      <li>Conteudo original: https://www.fucyber.com/xampp-install-sql-server-driver-on-maxos/</li>
      <li>Download php_sqlsrv driver to php version https://github.com/Microsoft/msphpsql/releases/tag/v5.6.0</li>
      <li>Example php 7.1 Extract file Copy php_pdo_sqlsrv_71_nts.so and php_sqlsrv_71_nts.so to
/Application/XAMPP/xamppfiles/lib/php/extensions/no-debug-xxxx/</li>
      <li>Open php.ini (xamppfiles/etc/php.ini) insert extension
      extension=php_pdo_sqlsrv_71_nts.so
      extension=php_sqlsrv_71_nts.so</li>
      <li>Restart apache web server</li>
      <li>Check phpinfo()</li>
    </ol>
  </li>
</ol>
