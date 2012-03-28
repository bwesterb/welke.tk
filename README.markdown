![welke.tk webpage](https://github.com/bwesterb/welke.tk/raw/master/doc/welke.tk.png)

Installation
============
1.  Clone `welke.tk` and all subpackages
    
    ```
    $ git clone https://github.com/bwesterb/welke.tk.git
    $ git submodule sync
    $ git submodule update
    ```
    
2.  Install various python packages.
    
    ```
    $ apt-get install python-yaml \
                      python-setuptools \
                      python-argparse # for python-2.6
    $ easy_install poster
    ```
    
3.  Configure and host `tkb.js`.
    
    ```
    $ cd /srv/default/webdocs # *or* your webdocs root
    $ ln -s /path/to/tkb.js tkb.js
    $ cd tkb.js
    $ cp config.js.example config.js
    $ vi config.js # set host to the host on which tkbd will run
    ```
    
4.  Set environment, create conifugration and run `tkbd`.
    
    ```
    $ source tkbd-environment.sh
    $ cp py/tkbd/setups/default mytkbdsetup.mirte
    $ vi mytkbdsetup.mirte
    $ mirte mytkbdsetup
    ```
