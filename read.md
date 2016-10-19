Playbook.yml
O arquivo é bem similar ao tradicional docker-compose.yml porém com algumas adições próprias do ansible(As primeiras linhas do arquivo por exemplo).  

Vars.yml
É aonde fica a variável que será usado no playbook.yml
Essa variável recebe o valor da variável contida no arquivo vault.yml

Vault.yml
É o arquivo que será encriptado 
contém o variável referenciada no arquivo vars.yml e o valor

Para encriptar
ansible-vault encrypt vault.yml
Para decriptar
ansible-vault decrypt vault.yml

Comandos importantes
docker stop $(docker ps -q)
docker rm $(docker ps -qa)
ansible-playbook playbook.yml