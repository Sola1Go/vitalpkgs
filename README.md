# vitalpkgs - A Flake Providing Collection of Customized Nix Packages

This repostiroy hosts a collection of packages that are not (yet)
found in [nixpkgs](https://github.com/NixOS/nixpkgs/). They are not in
the upstream for several reasons:

1. The package has really small user group which does not justify the resources we pay by hosting on [nixpkgs](https://github.com/NixOS/nixpkgs/).
2. The package is not up-to-date on [nixpkgs](https://github.com/NixOS/nixpkgs/), though will likely be updated either by us or someone else.
3. The package needs some customization to work with nixvital powered NixOS machines.
4. The original software is written by us and it tends to serve only specific purposes. This is similar to No. 1.

This repo will be constantly maintained, and packages will be added
and removed based on the above reasons as well.

# Usage

This is designed as a Nix [Flake](https://nixos.wiki/wiki/Flakes) so
that you can easily include it in your projects. Specifically it
provides

1. An `overlay` that has all the packages.
2. You can also access (build, inspect, ...) a single package under
   `packages.<system>.<package-name>`.