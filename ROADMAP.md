# upgrade/ROADMAP.md



## Play with post ssh pause

* This should be longish after major upgrades, shorter when not configuration changes have taken place

## Safe option requires aptitude

### references

* `aptitude` and `apt-get` work the same for many tasks, but for the most tricky cases, such as distribution upgrades (`apt-get dist-upgrade` vs. `aptitude full-upgrade`), they have different rules, and aptitude's rules are nearly always better in practice where they disagree.

```shell
TASK [upgrade : Debian | Upgrade Debian based systems to the latest package versions] ************************
skipping: [centos6]
skipping: [centos7]
 [WARNING]: Could not find aptitude. Using apt-get instead.
```

## Enable debug of reboot_results by default?

```shell
TASK [reboot : restarting stretch64 -- 127.0.0.1:2222] *******************************************************
changed: [stretch64]
changed: [xenial64]
changed: [trusty64]
changed: [precise64]
changed: [bionic64]
changed: [centos6]
changed: [centos7]

TASK [reboot : Debug the value of reboot_results variable] ***************************************************
skipping: [stretch64]
skipping: [centos6]
skipping: [centos7]
skipping: [xenial64]
skipping: [trusty64]
skipping: [bionic64]
skipping: [precise64]
```

