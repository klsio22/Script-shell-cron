# Script-shell-cron
script cron para agendamento de limpeza de caches de buffer de memoria no linux

## comando para limpeza manual da memoria : 
sudo sync sudo sysctl vm.drop_caches=3

## para visualiazer consumo da memoria em tempo real:
watch -n 1 free -m

## Comandos cron:
" sudo su cat /var/log/syslog | grep cron " cron para visualizar historico(logs) no cron

" crontab -e " para escolher editor dentro do terminal

" crontab -l " para visualizar listas de crons

## scripit para criar agendamento: 

" #!/bin/bash
#limpando cache
#o seguinte comando é o responsável pela limpeza
echo 3 > /proc/sys/vm/drop_caches "

## abra o contab com o comando "crontab -e"  e adiciona o tempo : 
#mm HH DD MM DS tarefa
30 * * * * local do arquivo .sh (nesse caso eu coloquei para limpar de 30 em 30 minutos independente das horas, dia, mes etc ...)

