# proxnix

Nix modules for configuring Proxmox homelabs.

## Goals

Create a set of Nix modules that enable declarative configuration and management of Proxmox-based homelab infrastructure. The project should make it easy to:

- Configure Proxmox nodes using NixOS
- Deploy and manage LXC containers declaratively
- Keep managed hosts up to date automatically

## Milestones

### 1. Define Proxmox Node with Nix

Create a NixOS configuration that can run Proxmox:

- Define a NixOS module for Proxmox VE
- Stand up a temporary test node to validate the configuration
- Document any manual steps required

### 2. Nix Binary Cache Container Module

Create a Nix module that deploys an LXC container running a simple Nix binary cache:

- Declarative configuration for the cache service
- Support for updates via the module

### 3. Automatic Host Updates

Create a method for automatically updating Nix-managed hosts:

- Scheduled or triggered rebuilds
- Safe rollback capability

### 4. Migrate Existing Proxmox Node

Safely migrate the existing Proxmox node to NixOS without data loss:

- Migrate existing containers to the temporary test node
- Reformat the original node with NixOS + Proxmox
- Migrate containers back
- Tear down temporary node

## Contributing

### License

All code must be released under an open source license of the contributors' choosing.

### Upstreaming

Where possible, contributions should be upstreamed to existing open source projects rather than maintained as standalone forks. This includes:

- NixOS modules that could benefit the broader community
- Bug fixes or improvements to upstream dependencies
- Documentation contributions to related projects

## References

- [Proxmox VE Documentation](https://pve.proxmox.com/pve-docs/)
- [Proxmox VE API](https://pve.proxmox.com/pve-docs/api-viewer/)
- [NixOS Manual](https://nixos.org/manual/nixos/stable/)
- [NixOS on Proxmox](https://nixos.wiki/wiki/Proxmox_Virtual_Environment)
- [nix-serve](https://github.com/edolstra/nix-serve) - Simple Nix binary cache server
- [Attic](https://github.com/zhaofengli/attic) - Multi-tenant Nix binary cache
- [Proxmox NixOS Container Guide](https://nixos.wiki/wiki/Proxmox_Linux_Container)
