# Scale Testing Ansible Tower using Docker Containers

## Create the docker containers

* Install docker-engine

* Build the docker image

```
cd docker
docker build -t linuxsimba/python-and-ssh -t linuxsimba/python-and-ssh:latest .

```

* Create the docker containers

```
ansible-playbook scale-containers.yml
```

It builds 21 containers by default.

* Run a test

```
ansible-playbook --private-key=./keys/ansible_test -i inventory.py demo.yml

```

## License
MIT
