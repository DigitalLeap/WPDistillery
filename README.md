A great and easy way for us to setup WordPress with the following:

- LayersWP
- Layers Pro (activated)
- Layers Updated (activated)
- WordPress SEO
- Redirection
- WP Security Audit Log
- Gravity Forms
- WooCommerce

For additional information, visit the [Official WPDistillery Website](https://wpdistillery.org). The Documentation on wpdistillery.org is synced with the Github repository files.

## Setup
To setup a new project running Scotch Box and WordPress, simply follow these steps:

1. Run the following command inside your project root to clone both Scotch Box and WPDistillery and move them to the right place:

  ```
  git clone https://github.com/DigitalLeap/wpscotch.git && mv wpscotch/Vagrantfile Vagrantfile && mv wpscotch/wpdistillery wpdistillery2 && rm -rf wpscotch && mv wpdistillery2 wpdistillery
  ```

2. Run `vagrant up` inside your project root

Done! You can now access your project at https://localhost.dev/ or http://192.168.33.10/.

## Additional Information

### Auto Update WordPress and Plugins
If you want to automatically update WordPress and all Plugins on every `vagrant up` you can remove the comment character at line 26 inside the Vagrantfile.

### Windows Support
Using Windows? No Problem! WPDistillery will detect if you're using Windows and if so, automatically convert all files using dos2unix.

### Vagrant commands
* `vagrant up` will start the machine. The first ever `vagrant up` in your project will also install Scotch Box and execute provisioning
* `vagrant provision` will execute provisioning. This is where WPDistillery runs its core function which is installing and configuring WordPress according to `config.yml`. Before that, it will also update WP-CLI and set the upload size to 64MB. Normally `vagrant provision` should not be executed manually but can be used to re-run the WPDistillery setup in case you want to re-install WordPress.
* `vagrant reload` will restart vagrant. This is required for changes made in the Vagrantfile to take effect.
* `vagrant halt` will shut down the running machine.
* More informations can be found at [vagrantup.com](https://vagrantup.com).

## About

* Author: Flurin Dürst ([Website](https://flurinduerst.ch), [Mail](mailto:flurin@flurinduerst.ch), [Twitter](https://twitter.com/flurinduerst))
* Contributors:
  * [@ShaneShipston](https://github.com/ShaneShipston)
  * [@drawcard](https://github.com/drawcard)

### Contribution
* Fork it
* Create your feature branch
* Commit your changes
* Push to the branch
* Create new Pull Request

Feel free to contact me if you have questions or need any advice.
