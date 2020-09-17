# Prometheus push gateway

## Requirements

```bash
pip install ansible
```
## Variables

```yaml
prometheus_push_gateway:
  version: "0.18.1"
  user: "pushgateway"
  group: "pushgateway"
  install_path: "/usr/local/bin"
  install_binary_name: "prometheus-push-gateway"
  listen_address: "0.0.0.0:9101"
```

## Example Usage

Add the following to a file like `playbook.yaml`:

```yaml
- hosts: monitoring
  roles:
    - role: "mateothegreat.prometheus_push_gateway"
      vars:
        prometheus_push_gateway:
          version: "0.18.1"
          user: "pushgateway"
          group: "pushgateway"
          install_path: "/usr/local/bin"
          install_binary_name: "prometheus-push-gateway"
          listen_address: "0.0.0.0:9101"
```

Run with `ansible-playbook -i <your inventory file> playbook.yaml`.

# Contact

You can reach out to me at https://matthewdavis.io.
