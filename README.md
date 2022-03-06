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
- install [vagrant][link#vagrant]

    ```bash
    brew install --cask vagrant && \
    brew install libiconv gcc libvirt
    ```

- update path 

    ```bash
    echo 'export PATH="/usr/local/opt/libiconv/bin:$PATH"' >> ~/.zshrc  && \
    echo 'export LDFLAGS="-L/usr/local/opt/libiconv/lib"' >> ~/.zshrc && \
    echo 'export CPPFLAGS="-I/usr/local/opt/libiconv/include"' >> ~/.zshrc && \
    echo 'export VAGRANT_DEFAULT_PROVIDER=kvm' >> ~/.zshrc
    ```

- install [vagrant-libvirt][link#vagrant-libvirt]

    1. find out `ruby version` 

    ```bash
    /opt/vagrant/embedded/bin/ruby --version
    ```

    2. install 

    ```bash
    CONFIGURE_ARGS='with-ldflags=-L/opt/vagrant/embedded/lib with-libvirt-include=/usr/local/include/libvirt with-libvirt-lib=/usr/local/lib' \
    GEM_HOME=~/.vagrant.d/gems/<YOUR RUBY VERSION HERE> \
    GEM_PATH=$GEM_HOME:/opt/vagrant/embedded/gems \
    PATH=/opt/vagrant/embedded/bin:$PATH \
    vagrant plugin install vagrant-libvirt
    ```

</details>

[link#homebrew]: https://brew.sh/
[link#qemu]: https://www.qemu.org/
[link#vagrant]: https://www.vagrantup.com/

[link#dart]: https://dart.dev/
[link#protobuf]: https://developers.google.com/protocol-buffers
[link#vagrant-libvirt]:: https://lunar.computer/posts/vagrant-libvirt-macos/

