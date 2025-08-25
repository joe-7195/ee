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
- as of now this setup is a little more complex
  - now uses a python3.12 venv instead of system package python3.9
  - this allows installing pip packages that conflict with system ones
  - `/runner/venv/bin/` has been added at the front of PATH
  - this does not actually need to be a venv
  - but installing a second python version is definitely the way