## Install requirements:
```bash
ansible-galaxy install -r requirements.yaml
```

## Config
```bash
cp inventory_dist.yaml inventory.yaml
```
... and fill it with correct data. Groups `new` and `prepared` should have the same hosts but the `new` group used by 
`prepare-host` playbook and `prepared` for any others

## Run with --check and --diff mode for only see what happened:
```bash
ansible-playbook -i inventory.yaml monitoring-playbook.yaml --diff --check
```

## Run prepare-host
```bash
ansible-playbook -i inventory.yaml prepare-host-playbook.yaml
```

## Run docker
```bash
ansible-playbook -i inventory.yaml docker-playbook.yaml
```

## Run postgres
```bash
ansible-playbook -i inventory.yaml postgres-playbook.yaml
```

## Run redis
```bash
ansible-playbook -i inventory.yaml redis-playbook.yaml
```

## Run metrics
```bash
ansible-playbook -i inventory.yaml metrics-playbook.yaml
```

## Run syncthing
```bash
ansible-playbook -i inventory.yaml syncthing-playbook.yaml
```
