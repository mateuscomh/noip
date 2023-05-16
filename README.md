# noip

----
DNS dinamico no IP, script a ser adicionado no DNU/LINUX no /etc/init.d

- Requer instalacao e configuracao do client NOIP2

## Instalação no-ip Linux

- git clone https://github.com/mateuscomh/noip
- cd noip
- sudo cp noip2 /etc/init.d/
- chmod +x /etc/init.d/noip2
- update-rc.d noip2 defaults
- sudo cp noip-duc-linux.tar.gz /usr/local/src
- cd /usr/local/src
- sudo tar xzvf noip-duc-linux.tar.gz
- sudo apt install make gcc
- sudo make
- sudo make install

*Insira o login (email) de acesso a conta No-IP;
*Insira a senha de acesso a conta No-IP;

O sistema informará caso você possua mais de um hostname. Tecle “n” para que o instalador permita escolher entre os hostnames cadastrados. Tecle “y” (sim) ou “n” (não) para definir o hostname que deseja utilizar nesta instalação. Defina o tempo de atualização do DDNS (entre 1 e 30 minutos). Então, tecle “y” para executar um update padrão e, por fim, tecle Enter para criar um arquivo de configuração.

---
Feitos os procedimentos, adicionar no crontab a execução do script conforme demanda
Exemplo ultima linha do crontab

``` 0 * * * * root bash /etc/init.d/noip2 
#executa a cada hora a atualização ```
