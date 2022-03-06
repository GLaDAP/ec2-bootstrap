# ec2-bootstrap

Script to bootstrap EC2 boxes for LDBC benchmark.
:warning: The script puts my public keys on the machine.

Fedora 35 x86_64 AMI: `ami-0133ad8c5d900ddef`.

```bash
curl -s https://raw.githubusercontent.com/szarnyasg/ec2-bootstrap/main/bootstrap.sh | bash && \
    ~/ec2-bootstrap/init.sh
```

The script will install the required packages, set up Docker and open a `tmux` session with additional installation/compilation jobs.

Notably, you need to build Umbra manually:

```
~/ec2-bootstrap/build-umbra-container.sh provide_umbra_url_here
```
