# ansible-rancher-centos7

```
ssh-copy-id -i .ssh/id_rsa.pub root@tk2-228-23543.vs.sakura.ne.jp
cat > roles/user/defaults/main.yml << EOT
{{your_password}}
EOT
ansible all --inventory-file=/etc/ansible/hosts -m ping
ansible-playbook provisioning.yml --syntax-check
ansible-playbook provisioning.yml
ssh root@tk2-228-23543.vs.sakura.ne.jp
docker run -d --restart=unless-stopped -p 8080:8080 rancher/server
```

http://tk2-228-23543.vs.sakura.ne.jp:8080/
