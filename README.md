# Adicionar um script para iniciar junto com o sistema linux via systemd (alternativa ao rc.local)

Crie o serviço na pasta systemd.

``` bash
touch /lib/systemd/system/seu_script_pessoal.service
```
adicione o conteúdo abaixo ao arquivo .service

``` bash
[Unit]
Description=Startup Script
[Service]
ExecStart=/caminho/para/o/seu/script.sh
[Install]
WantedBy=multi-user.target
```

OBS: Adicione quantas linhas Exec Start for necessárias. <br>
necessário uma linha para cada scritp que for executar.
