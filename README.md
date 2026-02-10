My background is
- gentoo
- nixpkgs/nixos
- others
- vim-addon-manager (vam)
...

The requirements of today:
- use as much from whatever OS you are on,
  augment with whatever is most favorite package manager
  augment with compile from source (most likely to fail)
  to makes something work

Examples:

- Blender/Inkscape/ .. with python Plugin

- Vim (Neovim) With lua plugins and c++ tools (Youcomplete me)
  perl or whatever a plugin is using.

Its seriously no longer clear who is responsible to install a typescript or go language server:
- the os ?
- the editor ?
- ..

So how to cope with that ? My vision for the future is:

    environment = 
        with osx
        with brew
        with custom install into ~/.custom/
        with python into micromamba env XX

    environment.install(x)
    environment.install(y)

    ....

So that everybody can choose what works for him.
even brew vs nix vs gentoo whatever. Like installing C++ can be done by
buck2, nixpkgs, others, ... let the user choose with some dependency
analysis telling about issues ahead of time if found

There are many platforms and eco systems and sub universes such as
    - esp32
    - microcontroller
    - ...
The same code could be used in many different contexts

Imagine Python library with C and Rust dependencies cross compiled to
Android with ~/Android/SDK_3 and ~/Vulkan/SDK-5


Why is there no install-from-github-readme.md name/repo ?
Because the cross platform tools are missing ?

Why isn't there a a way to describe need env with ffmpeg, PHP 8, mysql .. ?
Ok docker comes close. But even here sometimes you want to mix and create an
env based on a configuration.
