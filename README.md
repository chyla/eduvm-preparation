# EduVM

This is repository with EduVM configuration.


## Getting Started

### Prerequisites

To use it you will have to:

1. configure SSH connection to the machine with 'eduvm' user that authenticates via keys and have sudo enabled,
2. install Ansible,
3. create production file,
4. run Ansible with the machine as the target.


## Deployment

To install Ansible please use the Python venv module:

```
$ python3 -m venv venv
$ source venv/bin/activate
(venv) $ pip install wheel
(venv) $ pip install ansible
```

In 'production' file specify machine IP, eg:

```
[machines]
192.168.57.7
```

To configure the machine run the Ansible like that:

```
(venv) $ ansible-playbook -i production eduvm.yml -u eduvm -b --become-method=sudo
```

## Authors

* **Adam Chyła** - [chyla.org](https://chyla.org/)

