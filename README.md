# Development

<details>
  <summary>OS X</summary>

 - install [homebrew][link#homebrew]

    ```bash
    /bin/bash -c "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/HEAD/install.sh)"
    ```

- install [qemu][link#qemu]

    ```bash
    brew install qemu
    ```

- install [vagrant][link#vagrant] and  [vagrant-libvirt][link#vagrant-libvirt]
    
    1. update path 
        ```bash
        echo 'export PATH="/usr/local/opt/libiconv/bin:$PATH"' >> ~/.zshrc  && \
        echo 'export LDFLAGS="-L/usr/local/opt/libiconv/lib"' >> ~/.zshrc && \
        echo 'export CPPFLAGS="-I/usr/local/opt/libiconv/include"' >> ~/.zshrc && \
        echo 'export VAGRANT_DEFAULT_PROVIDER=kvm' >> ~/.zshrc  && \
        echo 'export CONFIGURE_ARGS="with-ldflags=-L/opt/vagrant/embedded/lib with-libvirt-lib=$(brew --prefix libvirt)/lib with-libvirt-include=$(brew --prefix libvirt)/include"' >> ~/.zshrc && \
        echo 'export PATH="/opt/vagrant/embedded/bin:$PATH"' >> ~/.zshrc
        ```

    2. install
        ```bash
        brew install --cask vagrant && \
        brew install libiconv gcc libvirt && \
        vagrant plugin install vagrant-libvirt
        ```

- install [packer][link#packert]

    ```bash
    brew tap hashicorp/tap  && \
    brew install hashicorp/tap/packer
    ```
    
</details>

[link#homebrew]: https://brew.sh/
[link#qemu]: https://www.qemu.org/
[link#vagrant]: https://www.vagrantup.com/
[link#vagrant-libvirt]: https://github.com/vagrant-libvirt/vagrant-libvirt
[link#packer]: https://www.packer.io/

[link#dart]: https://dart.dev/
[link#protobuf]: https://developers.google.com/protocol-buffers
