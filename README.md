# IDM Activation Script

An open-source tool for activating and resetting trial periods for [Internet Download Manager](https://www.internetdownloadmanager.com/)

# Disclaimer

I want to clarify that I am not the original author of this script. My main purpose in creating this repository is to simplify the process for Chinese users. Furthermore, out of respect for the original authors' work, I have ensured that they are credited.

# Features
* Freezes IDM trial and uses registry key locking for activation
* Activation and trial remain even after IDM updates are installed.

* Resets IDM trial
* Fully open-source
* Based on a transparent batch script

# Latest Version of IAS

Latest version - v1.2 (Feb 12, 2024)

[GitHub](https://github.com/iemabdullah/IDM-Activation-Script)

# Download / How to Use It?

First, install the latest version of [Internet Download Manager](https://www.internetdownloadmanager.com/). If there are any previous crack patches, please make sure to remove or uninstall them.

Next, follow these steps to activate it.

# Log
* 📌 This activation option is currently unavailable in the script. Please use the "Freeze Trial" option to lock the 30-day trial period for life.

# Method 1 - PowerShell

(Recommended)

* Right-click the Windows Start menu and select "PowerShell" or "Terminal" (do not select "CMD Command Prompt").

* Copy and paste the following code and press Enter

``shell

iex(irm is.gd/iAS)

```

Or

```shell

iwr -useb https://raw.githubusercontent.com/iemabdullah/IDM-Activation-Script/main/IAS.ps1 | iex

```

Or

```shell

iwr -useb https://is.gd/iAS | iex

```

* You will see the activation options. Please follow the on-screen instructions.

* That's all. # Method 2 - Traditional

* Download the file from [GitHub](https://github.com/iemabdullah/IDM-Activation-Script/archive/refs/heads/main.zip)

* Right-click the downloaded compressed file and extract it.

* Right-click the downloaded compressed file and extract `IAS.cmd`.

* You will see activation options; follow the on-screen instructions.

* That's all.

# Information
## Freeze the Trial

* IDM offers a 30-day trial period. You can use this option in the script to lock this trial period indefinitely, so you don't need to reset it again, and your trial period will never expire.

* This method requires an internet connection when applying this option.

* IDM updates can be installed directly without freezing again.

## Activation

(***Currently not working correctly**)

* This script uses a registry locking method to activate Internet Download Manager (IDM).

* This method requires an internet connection during activation.

* IDM updates can be installed directly without reactivation.

* After activation, if IDM starts displaying the activation prompt screen under certain circumstances, simply run the activation option again; there's no need to use the reset option.

## Reset IDM Activation/Trial

* Internet Download Manager offers a 30-day trial period, which you can use this script to reset activation/trial at any time.

* This option can also be used to restore the status if IDM reports fake serial number keys and other similar errors.

## Operating System Requirements

* This project supports Windows 7/8/8.1/10/11 and their corresponding server versions.

* Running IAS using PowerShell is supported on Windows 8 and later.

## Advanced Information

* To activate in unattended mode, run the script with the /act parameter.

* To freeze the trial in unattended mode, run the script with the /frz parameter.

* To reset in unattended mode, run the script with the /res parameter.

# How Does It Work?

* IDM stores trial and activation-related data in various registry keys. Some of these registry entries are locked to prevent tampering, and the data is stored in a specific pattern to track counterfeit serial number issues and remaining trial days. To activate it, the script here simply generates these registry entries by triggering some downloads in IDM, identifies them, and locks them so that IDM cannot edit or view them. This way, IDM won't display a warning that it was activated using a counterfeit serial number.

# Troubleshooting

* Browser integration fix: [Chrome](https://www.internetdownloadmanager.com/register/new_faq/bi9.html) - [Firefox](https://www.internetdownloadmanager.com/register/new_faq/bi4.html)

# Changelog

## v1.2

* Added an activation option with a randomly generated name, email, and key from registration details, along with a warning that this option doesn't work for some users and recommends using the frozen trial option.

## v1.1

* After the IDM 6.42b3 update, a fake serial number pop-up appeared when activating with IAS. Therefore, we removed the activation option and replaced it with a "Freeze Trial" option to permanently lock the 30-day trial period.

* The script now disables the quick edit feature in the CMD window using PowerShell without editing the registry. Thanks to @abbodi1406 for the code and @awuctl for the idea.

* The code used to restart the script via conhost.exe to avoid the terminal application has now been merged into the code that disables quick edit. Thanks to @abbodi1406.

Updated full code from [WindowsAddict](https://massgrave.dev/idm-activation-script)

## v1.0

* Added code to restart the script using conhost.exe when the script is running from a terminal application.

* Fixed an issue when retrieving the current user account security identifier (SID).

## v0.9

* Fixed an issue where the script failed to activate and reset IDM on non-administrator user accounts.

* Fixed an issue where the script incorrectly displayed that IDM was already activated.

* Fixed an issue that could cause fake serial number pop-ups. The script will also display information to allow you to run the activation option again without using the reset option.

* IDM registry scan and locking code is now written in PowerShell.

* The script update checker code has been added to the script.

* The script will now temporarily disable quick edit mode because users often click within the script window, which can cause the script to pause.

* The script will back up CLSISD registry entries before performing operations on them.

* Added numerous bug checks for better problem identification.

## v0.8

* Moved the project to [Github](https://github.com/iemabdullah/IDM-Activation-Script)

* Minor bug fixes

* Added information to inform users when the script is deleting a large number of empty registry entries.

# Screenshots

![IAS](https://github.com/lstprjct/IDM-Activation-Script/assets/88411318/fafdb481-c497-464f-b1e6-9a4254eaf880)

![IAS_Freeze_Trial](https://github.com/lstprjct/IDM-Activation-Script/assets/88411318/76b36582-8cf4-4d1e-870f-6e8e57c80a87)

# Acknowledgements

| | |

| ------------------------------------------- | ------------------------------------------------------------ |

| Dukun Cabul | The original researcher of the reset and activation logic in this IDM trial, who created an Autoit tool for these methods. [IDM-AIO_2020_Final](https://nsaneforums.com/topic/371047-discussion-internet-download-manager-fixes/page/8/#comment-1632062) |

| AveYo aka BAU | [reg_own lean and mean snippet](https://pastebin.com/XTPt0JSC) |

| [abbodi1406](https://github.com/abbodi1406) | Coding help |

| WindowsAddict | Original author of [IAS](https://github.com/WindowsAddict/IDM-Activation-Script) |

Thanks to IAS users for their attention, feedback, and assistance.


------------------------------------------------------------------------

Made with love ❤️
