# vSphere Command and Control

This script contains several functions for managing VMware vSphere servers. Below are brief descriptions of each function:

# Install-PowerCLI

This function installs the PowerCLI module for PowerShell. The module can be used to manage vSphere servers from the command line. In order to use the other features you must run this or already have PowerCLI installed

## Parameters

- InstallerUrl: The URL to the PowerCLI installer zip file. By default, this is set to the latest version available on VMware's website.

# Get-VSphereInventory

This function retrieves information about the vSphere server's inventory, including ESXi hosts, virtual machines, datastores, and networks. The information is output as JSON.

# New-FolderSnapshot

This function creates a snapshot of all virtual machines in a specified folder.

## Parameters

- FolderName: The name of the folder containing the virtual machines to snapshot.
- SnapshotName: The name of the snapshot to create.
- SnapshotDescription: The description of the snapshot to create.

# New-VMSnapshotAll

This function creates a snapshot of all virtual machines on the vSphere server.

## Parameters

- vCenter: The vSphere server to create snapshots on.
- FolderName: The name of the folder containing the virtual machines to snapshot.
- SnapshotName: The name of the snapshot to create.
- SnapshotDescription: The description of the snapshot to create.

# Menu Options

## The menu options are as follows:

- 1: Install PowerCLI - Installs the PowerCLI module if it is not already installed.
- 2: Get vSphere Inventory - Retrieves the vSphere inventory and saves it as a JSON file in the current directory.
- 3: Create Folder Snapshot - Creates a snapshot of a specified folder.
- 4: Create VM Snapshot - Creates a snapshot of all VMs in a specified folder.
- 5: Restore VM to Snapshot - Restores a VM to a specified snapshot.
- q: Quit - Disconnects from the vCenter server and exits the script.

# Usage

- 1.  Open PowerShell and navigate to the directory where the script is saved.
- 2. Run the script by typing .\scriptname.ps1.
- 3. Follow the prompts to select the desired task from the menu.

# Notes

- This script requires the VMware PowerCLI module to be installed.
- The vSphere inventory will be saved as a JSON file in the current directory.
- When creating a folder or VM snapshot, the script will prompt for the folder name, snapshot name, and snapshot description.
- When restoring a VM to a snapshot, the script will prompt for the folder name, snapshot name, and VM name.
