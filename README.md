## Ansible Execution Environment
- Container for interacting with Ansible and Terraform
```sh
# build
ansible-builder build -t ghcr.io/joe-7195/ee:latest

# login
echo $CR_PAT | podman login ghcr.io -u joe-7195 --password-stdin

# upload
podman push ghcr.io/joe-7195/ee:latest
```
