adlink-manifest

  mkdir ~/lec-rb5-yocto-test
  cd ~/lec-rb5-yocto-test
  repo init -u git@github.com:trinws/adlink-manifest -b lec-rb5-yocto-kirkstone -m lec-rb5-yocto-kirkstone.xml
  repo sync

  cd ~/lec-rb5-yocto-test
  MACHINE=lec-rb5 DISTRO=rpb-wayland source meta-nix-backports/setup-nix.sh
  bitbake rpb-weston-image

