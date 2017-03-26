systemd-gpio
------------

Requirements:

  - WiringPi "gpio" utility
  - Some GPIO attached buttons
  - Distro that uses systemd (eg Raspbian)

Set Up:

  - cp gpio-trigger@.service /etc/systemd/system
  - mkdir /etc/systemd-gpio
  - cp examples/shutdown /etc/systemd-gpio
  - systemctl reenable gpio-trigger@shutdown

You may create an environment file with any name in /etc/systemd-gpio
and then enable it as gpio-trigger@name-you-used.
