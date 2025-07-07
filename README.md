> [!WARNING]
> This extension is **no longer actively maintained**.
> 
> I originally created this extension for [Lens/OpenLens](https://github.com/andrea-falco/lens-multi-pod-logs), and later adapted it for [Freelens](https://github.com/freelensapp/freelens) upon request from the FreeLens developers.
> However, FreeLens updates frequently introduce breaking changes that require constant adjustments.
> 
> As I do not use FreeLens myself, I’m unable to dedicate the time necessary to keep this extension up to date with each release.
>
> Feel free to fork this project if you'd like to maintain or improve it.<br>Contributions are also welcome, but please be aware that I may not be able to respond promptly to issues or pull requests.

# Multi Pod Logs Freelens Extension
A [Freelens](https://github.com/freelensapp/freelens) extension that enables you to see logs from multiple pods *(and multiple containers within the pod)* on Kubernetes.

<p align="center">
 <img src="https://img.shields.io/github/license/andrea-falco/freelens-multi-pod-logs" /> <img src="https://img.shields.io/npm/dw/%40andrea-falco%2Ffreelens-multi-pod-logs" /> <img src="https://img.shields.io/npm/dt/%40andrea-falco%2Ffreelens-multi-pod-logs" />
 <br>
 <a href="https://ko-fi.com/A0A8J3CMJ"><img src="https://ko-fi.com/img/githubbutton_sm.svg" /></a>
</p>

## 🚧 Requirements
- Freelens `>= 1.0.0`
- [stern](https://github.com/stern/stern/releases) `>= 1.30.0`
> ⚠️ This extension uses `stern` under the hood, so it needs to be installed on your computer for the extension to work.
> If you don't know how to install it you can follow [these steps](STERN.md).

## 🧰 Installing
Just make sure Freelens is running, and follow these simple steps:

 1. Go to Extensions view (`Menu -> File -> Extensions`)
 2. Enter the name of this extension, `@andrea-falco/freelens-multi-pod-logs`
 3. Click on the **Install** button
 4. Make sure the extension is enabled

![install-by-name](img/install.png)

---

## 🚀 Features
After completing the installation, you will see a new action **Multi Pod Logs** for the menu below:
- Deployments
- StatefulSets
- ReplicaSets
- DaemonSets

![multi-pod-logs-menu](img/deployment-menu.png)

The new action will open a new terminal where all the logs coming from all the containers of all the pods of the resource will be shown.

## ⚙️ Preferences
Some extension behaviors and parameters can be adjusted from the Freelens preferences page, in the appropriate section dedicated to the extension:

![preferences](img/preferences.png)

## 🎨 Colored logs
If you're using Windows 10/11 *(and PowerShell as terminal in Freelens)* and you don't see colored pod logs, you can enable colors running this command:

```
Set-ItemProperty HKCU:\Console VirtualTerminalLevel -Type DWORD 1
```

Then restart Freelens.

---

## Upgrading
To upgrade to a newer release, go to the Extensions view, uninstall the extension, and then re-install it again.

## Uninstalling
Go to the Freelens Extensions view and click the **Uninstall** button next to this extension.
