My background is
=====================
- gentoo
- nixpkgs/nixos
- others
- vim-addon-manager (vam)
...

The requirements of today:
=====================
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
=======================================================

    environment = 
        with osx
        with brew
        with custom install into ~/.custom/
        with python into micromamba env XX

    environment.install(x)
    environment.install(y)
    ....

Its not even clear whether you want a stateful environment (x install)
or a declarative one (write config, then run update). You might want both.

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

Want to stay up to date?
=======================

https://github.com/MarcWeber/crossy/issues/1
put a comment here what you care about.

The future
===========
/bin/(await gols) -> no idea :)

  
crazy cases
============
Todays dev envs are crazy complicated eg Nvim with nixos and either puppeteer
like  or prisma its even about syncing nixpkgs version with your package.json
because you have to sync some c dependencies !

Sometimes its best to drop nix* like and be done I agree. Putting an ego aside.

vscode / remote editing
===========================
Now plugins in the future should be installed on remote locations with
different compiler toolchains and architectures ? vscode solved it by
installing and stickting to nodejs ..


The future languages
=======================
Rust -> no lazy loading in browser
Go -> no openxr support (VR) ? Yes you could .. but nobody did
Lua -> jitting not on all architectures .. ok maybe is good enough.
Julia -> No GC, requires ahead of time compliation for mobile. Yes possible if
you feel experimental ..

So i want a language with lisp like features code = data blurring the lines
between package management, jitting, aot, interpreted cause honestly vscode
starts faster than any make build ...

And https://github.com/mun-lang/mun shows you can have hot reloading on structs
and function bodies native and webassembly.

So its imaginable to have a package dependency system describe the linux kernel,
hot patch it. Or use fast compilation till you're up and running.
Then have a second pass with clang getting the last 10% of performance boost
most don't really care about ... 

If you had buck2 like (full dependency tree packages and files) you can replace and patch functions and reload web servers anything.

I agree that provisioning systems and just replacing VMs is another way.

But the option to mix and history with master to provide legacy support eg old
file systems sounds interesting to me.

Systems like fuchsia os just reference files and download them.
And China is using harmony os which means you can send something to a service
on your PC and that will then fetch the package and start running it with
correct architecture. But fuchsia was only shipped on one product. Looks like
Android is here to stay in western world.


