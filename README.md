# Teste Ansible PHPRio

## 1. Crie o inventory
- Duplique o arquivo `inventory.yml.example` como `inventory.yml`.
- Preencha o IP da VPS.

## 2. Crie o arquivo secrets
- Duplique o arquivo `vars/secrets.yml.example` como `vars/secrets.yml`.
- Preencha com o hash da senha desejada para o usuário `phprio` que será criado. Você pode usar o comando a seguir para gerar um hash:
  ```
  $ openssl passwd -6
  ```

## 3 Execute os playbooks
```
$ ansible-playbook -i inventory.yml setup_server.yml -e=@vars/secrets.yml
$ ansible-playbook -i inventory.yml install_docker.yml 
```
