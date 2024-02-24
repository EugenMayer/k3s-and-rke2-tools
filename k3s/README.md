# WAT

Tools for k3s 

## Index

- [multipathd](./multipath/) config: Needed so the localpath based devices are not auto-mounted by ubuntu
- [shutdown helper](./shutdown/): k3s does not gracefully shutdown since it continues to run even if you run `systemctl k3s-server down`. All containers will be still running, which will block your k3s vm/box to shutdown/restart properly.
- [limits.conf](./sysctl/) fix max-open files - usually you will hit the linux default limit very fast with k8s

