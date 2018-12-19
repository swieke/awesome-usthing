iOS Continuous Integration
===
## How it works

Xcode Server on Mac Mini monitor changes on master regularly and runs integration for each commit

Xcode Server: Repo Cloneing, Tests, Analyse, Cert Fetching, Call Fastlane script

Fastlane: Archive Building, Slack Message

For archive (binary) building, Fastlane is used to avoid image asset missing bug in Xcode Server

(Apple replied it's fixed already on our bug report, not tested yet)

## Remote Control from your computer

### Add Xcode Server connection

Xcode > Preferences > Accounts > Add > Xcode Server

Address: {Ask via slack}
Username: {Ask via slack}
Password: {Ask via slack}

### View Logs / Initiate build manually

Left Navigation Pane > Log Tab (last icon) > bmz147.ust.hk > USThing iOS Master

### If anything goes wrong

1. Try remote into Mac Mini using Screen Sharing
2. If still doesnt work, ssh into it and reboot it
3. If still doesnt work, call office staff to reboot physically.

## Upload build to iTunes

Recommended: Download ipa to your computer first, then upload via Application Loader

(Connection to apple servers is super slow on ust network)

```sh
$ scp <username>@<address>:~/USThing_iOS_Bin/USThing_{build_number}.ipa ~
```

## Upgrade Xcode version

Recommended: Download Xcode from developer.apple.com > Other Downloads, do not use Mac App Store version

After upgrade, run Xcode on Mac Mini via Screen Sharing, Xcode > Preferences > Xcode Server > "Upgrade" button
