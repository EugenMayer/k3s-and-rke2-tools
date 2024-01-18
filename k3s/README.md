# WAT

Tools for k3s 

## Index

- multipathd config: Needed so the localpath based devices are not auto-mounted by ubuntu
- shutdown helper: k3s does not gracefully shutdown since it continues to run even if you run `systemctl k3s-server down`. All containers will be still running, which will block your k3s vm/box to shutodwn/restart properly 
