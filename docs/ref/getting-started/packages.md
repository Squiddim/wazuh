# Packages

This page lists the supported operating systems and architectures for Wazuh Server and Agent packages. Before installing Wazuh, verify that your platform and architecture are compatible with the available packages.

## Server

### Amazon Linux

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Amazon Linux|2023|✔️|✔️|
|Amazon Linux|2|✔️|✔️|

### Ubuntu

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Ubuntu|24.04|✔️|✔️|
|Ubuntu|22.04|✔️|✔️|

### Red Hat

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Red Hat|10|✔️|✔️|
|Red Hat|9|✔️|✔️|

## Agent

### Amazon Linux

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Amazon Linux|2023|✔️|✔️|
|Amazon Linux|2|✔️|✔️|
|Amazon Linux|1|✔️|✔️|

### Ubuntu

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Ubuntu|24.04|✔️|✔️|
|Ubuntu|22.04|✔️|✔️|
|Ubuntu|20.04|✔️|✔️|
|Ubuntu|18.04|✔️|✔️|

### Windows

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Windows|11|✔️|✔️|
|Windows|10|✔️|✔️|
|Windows Server|2025|✔️||
|Windows Server|2022|✔️||
|Windows Server|2019|✔️||
|Windows Server|2016|✔️||
|Windows Server|2012 R2|✔️||
|Windows Server|2008 R2|✔️||

### macOS

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|macOS|15|✔️|✔️|
|macOS|14|✔️|✔️|

### Red Hat

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Red Hat|10|✔️|✔️|
|Red Hat|9|✔️|✔️|
|Red Hat|8|✔️|✔️|
|Red Hat|7|✔️|✔️|
|Red Hat|6|✔️||

### CentOS

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|CentOS Stream|10|✔️|✔️|
|CentOS Stream|9|✔️|✔️|
|CentOS Stream|8|✔️|✔️|
|CentOS|8|✔️|✔️|
|CentOS|7|✔️|✔️|
|CentOS|6|✔️||

### Oracle Linux

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Oracle Linux|9|✔️|✔️|
|Oracle Linux|8|✔️|✔️|
|Oracle Linux|7|✔️||
|Oracle Linux|6|✔️||

### Debian

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Debian|13|✔️|✔️|
|Debian|12|✔️|✔️|
|Debian|11|✔️|✔️|
|Debian|10|✔️|✔️|
|Debian|9|✔️||
|Debian|8|✔️||
|Debian|7|✔️||

### Fedora

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Fedora|42|✔️|✔️|
|Fedora|41|✔️|✔️|

### SUSE

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|OpenSUSE Leap|15|✔️|✔️|
|SLES|15|✔️|✔️|

### AlmaLinux

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|AlmaLinux|10|✔️|✔️|
|AlmaLinux|9|✔️|✔️|
|AlmaLinux|8|✔️|✔️|

### Rocky Linux

|Platform|Version|x86_64|aarch64|
|--|--|:--:|:--:|
|Rocky Linux|10|✔️|✔️|
|Rocky Linux|9|✔️|✔️|
|Rocky Linux|8|✔️|✔️|

---

## Package Download

Wazuh packages are available in different repositories depending on the release stage:

### Development packages

Development packages are available in the internal development bucket:

```bash
# Development bucket structure
s3://xdrsiem-packages-dev-internal/development/wazuh/5.x/main/packages/

# Example download
aws s3 cp s3://xdrsiem-packages-dev-internal/development/wazuh/5.x/main/packages/wazuh-manager_<version>_<arch>.deb .
```

### Pre-release packages (5.x and later)

Pre-release packages for version 5.x and later are available in the staging bucket:

```bash
# Pre-release bucket structure
s3://xdrsiem-packages-staging/pre-release/5.x/

# Example download
aws s3 cp s3://xdrsiem-packages-staging/pre-release/5.x/wazuh-manager_<version>_<arch>.deb .
```

### Production packages (5.x and later)

Production packages for version 5.x and later are available in the production bucket:

```bash
# Production bucket structure
s3://xdrsiem-packages/production/5.x/

# Example download
aws s3 cp s3://xdrsiem-packages/production/5.x/wazuh-manager_<version>_<arch>.deb .
```

**Note**: Replace `<version>` with the target version (e.g., `5.0.0-1`) and `<arch>` with your architecture (e.g., `amd64`, `x86_64`, `aarch64`, `arm64`). Adjust the package name and file extension for your component and platform:

- **Manager**: `wazuh-manager` (`.deb`, `.rpm`)
- **Agent**: `wazuh-agent` (`.deb`, `.rpm`, `.pkg`, `.msi`)
- **Architectures**: `amd64`/`x86_64` (64-bit Intel/AMD), `aarch64`/`arm64` (64-bit ARM)
