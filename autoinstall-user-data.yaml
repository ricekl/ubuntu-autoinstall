#cloud-config
# See the autoinstall documentation at:
# https://canonical-subiquity.readthedocs-hosted.com/en/latest/reference/autoinstall-reference.html
autoinstall:
  apt:
    disable_components: []
    fallback: offline-install
    geoip: true
    mirror-selection:
      primary:
      - country-mirror
      - arches:
        - amd64
        - arm64
        - i386
        uri: http://archive.ubuntu.com/ubuntu/
      - arches:
        - armhf
        - powerpc
        - ppc64el
        - riscv64
        - s390x
        uri: http://ports.ubuntu.com/ubuntu-ports
    preserve_sources_list: false
    security:
    - arches:
      - amd64
      - arm64
      - i386
      uri: http://security.ubuntu.com/ubuntu/
    - arches:
      - armhf
      - powerpc
      - ppc64el
      - riscv64
      - s390x
      uri: http://ports.ubuntu.com/ubuntu-ports
  codecs:
    install: false
  drivers:
    install: false
  identity:
    hostname: srv01-ubuntu
    password: $6$a1pIFsPK8KRLX63j$JoM7F1VwwZDNC0z/H2qKjUzx9hhOaelRZ2wPAbf0apsOGDbiDh1W46IFzMkpVCNrGoIxPWSp98/CHPvAhJ7B5/
    realname: rickard
    username: rickard
  kernel:
    package: linux-generic-hwe-24.04
  keyboard:
    layout: se
    toggle: null
    variant: nodeadkeys
  locale: en_US.UTF-8
  network:
    ethernets:
      enp0s3:
        match:
          macaddress: 08:00:27:bb:ce:85
        set-name: enp0s3
    version: 2
  oem:
    install: auto
  source:
    id: ubuntu-desktop-minimal
    search_drivers: false
  ssh:
    allow-pw: true
    authorized-keys: []
    install-server: false
  storage:
    config:
    - ptable: gpt
      serial: VBOX_HARDDISK_VB8af3dbe7-406ff8fa
      path: /dev/sda
      preserve: false
      name: ''
      grub_device: false
      id: disk-sda
      type: disk
    - device: disk-sda
      size: 1127219200
      wipe: superblock
      flag: boot
      number: 1
      preserve: false
      grub_device: true
      offset: 1048576
      path: /dev/sda1
      id: partition-0
      type: partition
    - device: disk-sda
      size: 1024458752
      wipe: superblock
      number: 2
      preserve: false
      offset: 1128267776
      path: /dev/sda2
      id: partition-1
      type: partition
    - device: disk-sda
      size: 10240393216
      wipe: superblock
      number: 3
      preserve: false
      offset: 2152726528
      path: /dev/sda3
      id: partition-2
      type: partition
    - device: disk-sda
      size: 2048917504
      wipe: superblock
      number: 4
      preserve: false
      offset: 12393119744
      path: /dev/sda4
      id: partition-3
      type: partition
    - device: disk-sda
      size: 28506587136
      wipe: superblock
      number: 5
      preserve: false
      offset: 14442037248
      path: /dev/sda5
      id: partition-4
      type: partition
    - fstype: fat32
      volume: partition-0
      preserve: false
      id: format-0
      type: format
    - fstype: ext4
      volume: partition-1
      preserve: false
      id: format-1
      type: format
    - fstype: ext4
      volume: partition-2
      preserve: false
      id: format-2
      type: format
    - fstype: ext4
      volume: partition-3
      preserve: false
      id: format-3
      type: format
    - fstype: ext4
      volume: partition-4
      preserve: false
      id: format-4
      type: format
    - path: /
      device: format-4
      id: mount-4
      type: mount
    - path: /boot
      device: format-1
      id: mount-1
      type: mount
    - path: /var
      device: format-2
      id: mount-2
      type: mount
    - path: /tmp
      device: format-3
      id: mount-3
      type: mount
    - path: /boot/efi
      device: format-0
      id: mount-0
      type: mount
  timezone: Europe/Stockholm
  updates: security
  version: 1
