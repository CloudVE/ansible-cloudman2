# Generic Docker Container Boot Playbook
This playbook can be used to launch an arbitrary docker container on a VM.
It will first make sure that docker is installed on the target VM and then run
the desired container on the VM.

Playbook Variables
-------------------

| Variable              | Description                       | Example                                               |
|-----------------------|-----------------------------------|-------------------------------------------------------|
| docker_container_name | Name to give the docker container | cloudman-boot                                         |
| docker_boot_image     | Image to run                      | cloudve/cloudman-boot:latest                          |
| docker_volumes        | An array of volume mounts         | ['/var/run/docker.sock:/var/run/docker.sock']         |
| docker_ports          | An array of port mappings         | ['8913:9000', '5678:5678']                            |
| docker_env            | A dict of env vars                | {'CM_SKIP_CLOUDMAN': 'False', 'MY_OTHER_VAR': 'test'} |
