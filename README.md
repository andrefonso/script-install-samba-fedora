### Procedimentos para baixa/execução de Script de instalação/configuração do Samba e de compartilhamento de arquivos no Fedora
---

1) Criar o diretório **myscripts** na _home_ executando o seguinte comando:</br>
  `mkdir /home/andre/myscripts`
2) Baixar o arquivo contendo o script de instalação chamado _smbinstall_ e salvá-lo no diretório que foi criado</br>

3) Dar permissões de execução ao script antes de executá-lo usando o seguinte comando:</br>
  `chmod +x smbinstall` </br>
4) Alterar o proprietário e o grupo do arquivo **smbinstall** para o do usuário usando os seguintes comandos:</br>
   ```
   sudo chown andre smbinstall
   sudo chown :andre smbinstall
   ```
5) Para que o script seja executável a partir de qualquer local, seguir os procedimentos abaixo:</br>
   -  Editar o arquivo _.bashrc_ usando o comando abaixo:</br>
    `sudo nano .bashrc`

   - Incluir no final do arquivo a seguinte linha:</br>
     `PATH=$PATH:~/myscripts`
     
   - Salvar o arquivo utilizando `CTRL+O` fechar o nano utilizando `CTRL+X`
  
6) O último passo é a execução do Script que fará a instalação do Samba e as configurações necessárias para compartilhamento de arquivos.
   Para isso utilize o seguinte comando:</br>
   `smbinstall`
