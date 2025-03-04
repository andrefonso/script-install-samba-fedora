### Procedimentos para execução de Script de instalação/configuração do Samba e de compartilhamento de arquivos no Fedora
---

1) Criar o diretório **myscripts** na _home_ executando o seguinte comando:</br>
```sh
mkdir /home/andre/myscripts
```
2) Dentro do diretório _myscripts_ crie com o _Nano_ um arquivo de script com o nome **smbinstall** copiando para dentro dele o conteúdo do arquivo _smbinstall_ disponível neste repositório.</br>

3) Dar permissões de execução ao script antes de executá-lo usando o seguinte comando:</br>
```sh
sudo chmod +x smbinstall
```
4) Alterar o proprietário e o grupo do arquivo **smbinstall** para o do usuário usando os seguintes comandos:</br>
   ```
   sudo chown andre smbinstall
   sudo chown :andre smbinstall
   ```
5) Para que o script seja executável a partir de qualquer local, seguir os procedimentos abaixo:</br>
   -  Editar o arquivo _.bashrc_ usando o comando abaixo:</br>
   ```sh
   sudo nano .bashrc
   ```

   - Incluir no final do arquivo a seguinte linha:</br>
   ```sh
   PATH=$PATH:~/myscripts
   ```
    
   - Salvar o arquivo utilizando `CTRL+O` fechar o nano utilizando `CTRL+X`</br>
   
   - Para o comando PATH incluído acima surtir efeito, digite o seguinte comando:</br>
   ```sh
   source .bashrc
   ```
  
6) O último passo é a execução do Script que fará a instalação do Samba e as configurações necessárias para compartilhamento de arquivos.
   Para isso utilize o seguinte comando:</br>
```sh
sudo smbinstall
```
