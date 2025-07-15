# system-upgrade-controller-helm
[![Artifact Hub](https://img.shields.io/endpoint?url=https://artifacthub.io/badge/repository/system-upgrade-controller)](https://artifacthub.io/packages/search?repo=system-upgrade-controller)

## Overview

This repository provides a Helm chart for deploying the [system-upgrade-controller](https://github.com/rancher/system-upgrade-controller) on Kubernetes clusters. The system-upgrade-controller automates the upgrade of nodes and system components, making cluster management safer and more efficient.

## Features
- Automated node and system component upgrades
- Customizable upgrade plans
- Safe, rolling upgrades with minimal disruption

## Installation

1. **Add the Helm repository:**
   ```sh
   helm repo add system-upgrade-controller https://kube-the-home.github.io/system-upgrade-controller-helm/
   helm repo update
   ```
2. **Install the chart:**
   ```sh
   helm install my-upgrade-controller system-upgrade-controller/system-upgrade-controller
   ```

## Upgrading
To upgrade the chart, run:
```sh
helm upgrade my-upgrade-controller system-upgrade-controller/system-upgrade-controller
```

## Uninstalling
To uninstall the release:
```sh
helm uninstall my-upgrade-controller
```

## Chart Structure
- `Chart.yaml`: Chart metadata
- `values.yaml`: Default configuration values
- `templates/`: Kubernetes manifest templates (RBAC, Deployment, ConfigMap, etc.)

## Configuration
See [values.yaml](charts/system-upgrade-controller/values.yaml) for all configurable options and their defaults. You can override any value using the `--set` flag or by providing a custom `values.yaml` file.

## Example: Custom Upgrade Plan
You can define custom upgrade plans by creating Kubernetes resources that the controller will process. See the [system-upgrade-controller documentation](https://github.com/rancher/system-upgrade-controller#usage) for examples.

## Contributing
Contributions, issues, and feature requests are welcome! Please open an issue or submit a pull request.

## License
This project is licensed under the terms of the LICENSE file in this repository.
