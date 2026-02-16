# ansible-roles-roboshop
ansible-roles-roboshop

- Have to install `sudo dnf install ansible` before running the ansible playbook
- Have to install `pip3.9 install botocore boto3` before running the ansible playbook
- `aws configure`

### To launch EC2 instances
```shell
ansible-playbook -i localhost, \
 -e '{ "INSTANCES":["mongodb", "catalogue", "redis", "user", "cart", "mysql", "shipping", "rabbitmq", "payment", "frontend"]}' \
  roboshop.yaml
```

### Delete Route53 Records and EC2 instances
```shell
ansible-playbook -i localhost, \
 -e '{ "INSTANCES":["mongodb", "catalogue", "redis", "user", "cart", "mysql", "shipping", "rabbitmq", "payment", "frontend"], "ACTION": "destroy"}' \
  roboshop.yaml
```

ansible-playbook -i localhost, \
-e '{ "INSTANCES":["mongodb"], "ACTION": "destroy"}' \
roboshop.yaml


```shell
ansible-playbook -i localhost, -e '{ "INSTANCES":["mongodb"]}' roboshop.yaml
```


- `ansible-playbook -e component=mongodb anisble-roles-roboshop.yaml`
- `ansible-playbook -e component=catalogue anisble-roles-roboshop.yaml`


--- have to do from rabbitmq

