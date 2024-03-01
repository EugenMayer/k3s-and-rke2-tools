# WAT

Tools for k3s

## Index

- [multipathd](./multipath/) config: Needed so the localpath based devices are not auto-mounted by ubuntu
  - deploy to `/etc/multipath.conf`
- [shutdown helper](./shutdown/): k3s does not gracefully shutdown since it continues to run even if you run `systemctl k3s-server down`. All containers will be still running, which will block your k3s vm/box to shutdown/restart properly.
  - deploy to `/etc/systemd/system/k3s-shutdown.service`
  - run `sudo systemctl daemon-reload && systemctl enable k3s-shutdown.service`
- [limits.conf](./sysctl/) fix max-open files - usually you will hit the linux default limit very fast with k8s
  - deploy to `/etc/security/limits.d/k8s.conf`
- [unattendend-updates](./unattendend-updates/) ensure we keep the system up to date
  - run `apt install unattended-upgrades`
  - deploy to `/etc/apt/apt.conf.d/20auto-upgrades`
  - deploy to `/etc/apt/apt.conf.d/50unattended-upgrades`
