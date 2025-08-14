# Build GApps for ATV by using Github Actions

## You need to know

### The arch of the ATV you are building to

We need the arch to build, the "ARCH" of the sheet below is you should
input in "Run Workflow" page.

| ARCH   | CPU architecture | Example devices                      |
|--------|-------------------|--------------------------------------|
| arm    | arm               | TVpad2                               |
| arm64  | arm64             | MeCool KM2 Plus                      |
| x86    | x86               | Nexus Player                         |
| x86_64 | x86_64            | Some device installed ATV for x86_64 |

### The android version of the ATV you are building to

Look at the sheet below, MindTheGapps stores different Android versions
in different branches. When building, you need to download the branch
you need instead of the default branch.

| Android Version        | Branch  | Android_VERSION (you need input in “Run Workflow” page.) |
|------------------------|---------|-----------------------------------------------------------|
| 16                     | baklava | 16.0.0                                                    |
| 15                     | vic     | 15.0.0                                                    |
| 13                     | tau     | 13.0.0                                                    |
| 14                     | upsilon | 14.0.0                                                    |
| 12L (12.1) — *NO A12*  | sigma   | 12.1.0                                                    |
| 11                     | rho     | 11.0.0                                                    |

This sheet only shows the existing branches. If the repository is not updated later, you can find content similar to `ANDROIDV=14.0.0` in `/build/gapps.sh` of different branches in <https://gitlab.com/MindTheGapps/vendor_gapps_tv>.

### (Android TV only) GApps Variants (copied from LineageOS.org)

Android TV MindTheGapps packages have two variants full and minimal:

`full` includes the Google Android TV (note, not Google TV) launcher and
recommendations applications.

`minimal` does not replace the included launcher or recommendations*, by
default LineageOS ATV builds utilize an Android 10 era non-GMS
launcher.*

Note: All shipping devices fit either of these packages, they only exist
to provide users the option of opt-ing out of Google's
launcher/recommendations.

## How to build

1.  Know the arch (e.g. arm64)

2.  Know the ANDROID_VERSION (e.g. 12.0.0)

3.  Know the branch (e.g. sigma)

4.  Type them in (Example)

![Show Example](https://raw.githubusercontent.com/mediateeee/action_MindTheGapps_for_ATV/main/example.png)

5.  Run workflow.

6.  Download in your Releases.
