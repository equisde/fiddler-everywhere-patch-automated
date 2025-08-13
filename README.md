## [中文翻译版](README_CN.md)

# Fiddler Everywhere Patch (Automated)
Guides you to Patch Fiddler Everywhere on Windows Automatically. 
> Parent Repo: https://github.com/msojocs/fiddler-everywhere-enhance

## What and How?
This's a  a patch for Telerik Fiddler Everywhere. It can grant you a trial that doesn't expire. The trial has every feature. 
This's the guide for applying patch automatically. 

![Unlimited Trial](https://github.com/user-attachments/assets/e9c83778-27fa-456a-96e6-07bb0cd7f4ad)

---

## Feature Updates
> [!TIP]
> Now supports changing patch server port (Useful if port conflitcts encountered)

> [!TIP]
> Now supports changing default user profile (fake) for FE (incl - email, fname, lname, country-code, provider)

---

> [!IMPORTANT]
> Linux Automated Patching is Supported Now!

> [!WARNING]
> The new patch want to write files in a directory inside FE app itself. So you need to give write permissions in Linux. See [#27](https://github.com/auto-yui-patch/fiddler-everywhere-patch-automated/issues/27) for more. And feel free to drop your suggestion to automate the process.

> [!IMPORTANT]
> ### Update Notice: Support for Syncing forks with upstream repo: [READ MORE](#scheduled-syncing-forks-with-upstream-repo)

---

## Get Started.
 > [!TIP]
 > You must always check if your fork is up to date so no fails. (We reccomend you enable [Scheduled upstream pulling](#scheduled-syncing-forks-with-upstream-repo))

 * How even this Automated Patching Works?
   - Well, this automated patch do the same that you do mannually for patching. It downloads fiddler everywhere extract it. Remove, Replace, Edit, Move files and then, the patched application is ready.

 * Workflow Dispatch? or Workflow Dispatch Latest?
   - Latest Version - Workflow Dispatch - Patch the latest version, and upload as artifact.
   - Custom Version - Workflow Dispatch - Allows you to select a compatible version (5.9.0 +) and patch  and upload as a workflow artifact.

> [!TIP]
> We highly reccomend you to use ***Latest Version - Workflow Dispatch***, which patch the latest available version.
> ***Custon Version - Workflow Dispatch*** allows you to select a version starting from 5.9.0 + too.

---

### With `Latest Version - Workflow Dispatch` 
[![](https://github.com/auto-yui-patch/fiddler-everywhere-patch-automated/actions/workflows/cp_latest_dispatch.yml/badge.svg)](https://github.com/auto-yui-patch/fiddler-everywhere-patch-automated/actions/workflows/cp_latest_dispatch.yml)

  - Fork this repo.
  - Go to actions tab, Select `Latest Version - Workflow Dispatch` workflow.
  - Trigger it with `workflow dispatch`
  - After a successful trigger download artifact that named like `Fiddler-Everywhere-VX.X.X-Patched`
  - Extract it. Run it

  * *Here how you do it...*

    https://github.com/user-attachments/assets/437c3448-1ea2-4c99-9123-e56b1665a37b


### With `Custom Version - WorkFlow Dispatch` 
[![](https://github.com/auto-yui-patch/fiddler-everywhere-patch-automated/actions/workflows/cp_dispatch.yml/badge.svg)](https://github.com/auto-yui-patch/fiddler-everywhere-patch-automated/actions/workflows/cp_dispatch.yml)

  - Fork this repo
  - Go to actions tab, Select `Custom Version - Workflow Dispatch` workflow.
  - Trigger it with `workflow diaptch` providing the version you want to patch
  - After a successful trigger download artifact that named like `Fiddler-Everywhere-VX.X.X-Patched`
  - Extract it. Run it

  > [!WARNING]
  > Please Note that Only Versions Up to 5.9.0 `( 5.9.0 + )` are supported.
  
  > You can find a list of releases here - [Release History](https://www.telerik.com/support/whats-new/fiddler-everywhere/release-history)

  * *Here how you do it...*

    https://github.com/user-attachments/assets/1e9fa214-b9c9-469c-83f0-e5ae4527d2f7

---

### Scheduled Syncing Forks with Upstream Repo
  FE Patch `1.0.8` adds support to sync your repo with upstream repo - scheduled (default: every 6 hours) 
  > [!NOTE]
  > Tnx: [lobe-chat](https://github.com/lobehub/lobe-chat) & [ous50](https://github.com/ous50)

  > [!IMPORTANT]
  >  - For this upstream pulling action to work, you need to enable [Upstream Sync](.github/workflows/cp_pull_upstream.yml) Github Action.
  >  - And the action'll create an issue in your fork if pulling is unsuccesfull. So you need to enable `issues` for your fork with your repositories settings (`Settings` `-->` `General` `-->` `Features` `Issues`)
  >  - For more information on how this action works: [lobe-chat's Sync Feature Wiki - en-US](https://github.com/lobehub/lobe-chat/wiki/Upstream-Sync) & [lobe-chat's Sync Feature Wiki - zh-CN](https://github.com/lobehub/lobe-chat/wiki/Upstream-Sync.zh-CN)

  > [!TIP]
  >  - You can change schedule by editing `- cron: '0 */6 * * *'` in [cp_pull_upstream.yml](.github/workflows/cp_pull_upstream.yml)
  >  - For more information on `- cron` of Github Actions, visit [Github Documentation - Scheduling Actions](https://docs.github.com/en/actions/writing-workflows/choosing-when-your-workflow-runs/events-that-trigger-workflows#schedule)

  > [!CAUTION]
  >  - IF you use another method (maybe a Github App), to sync your forks with upstream repos, (for ex: [Pull by Wei](https://github.com/wei/pull)), you should disable the `Upstream Sync` action by going through, `Actions` `-->` `Upstream Sync` `-->` `Right Top Menu [...]` `-->` `Disable Workflow`
  >  - For more information on how to disable a workflow: [Github Documentation on Disabling & Enabling Workflows](https://docs.github.com/en/actions/managing-workflow-runs-and-deployments/managing-workflow-runs/disabling-and-enabling-a-workflow)

---

> [!NOTE]
> For Generic `Linux` and `MacOS` instructions, use [source repository](https://github.com/msojocs/fiddler-everywhere-enhance)

> [!CAUTION]
> Please don't use this patch for illegal matters. And we'd love if you can buy and support the officials: [Please Support](https://www.telerik.com/purchase/fiddler)
