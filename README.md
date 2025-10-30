# installing-kali-linux-and-vulnerable-metasploit-in-vmware.
kali-vm-metasploitable-repo/
├── README.md               <- this file
├── scripts/
│   ├── download_kali_vm.sh <- helper: download Kali prebuilt VM "https://www.kali.org/get-kali/#kali-virtual-machines"
│   ├── import_vmdk_vmware.sh <- helper to generate a basic VMware . "https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion"
│   └── verify_checksum.sh  <- helper to verify SHA256 sums 
└── vagrant/
    └── Vagrantfile_metasploitable3_example <- downloading link for metasploitable vm "https://sourceforge.net/projects/metasploitable/"
# Steps to import kali linux and metasploitable into vmware 
1.Open VMware Workstation or VMware Fusion on your computer.
2. To import Kali (OVA): choose File → Open and select the downloaded Kali .ova file, then follow the VMware import wizard to add the VM.
3. To install Kali from ISO instead of OVA: choose File → New Virtual Machine, select the Kali ISO when prompted, and follow the installer steps.
4. To add Metasploitable (VMDK): create a new virtual machine and when asked for a disk choose the option to use an existing virtual disk and select the Metasploitable .vmdk file from the downloads folder.
5. If VMware asks for a virtual machine folder or name, enter Metasploitable2 (or any name you prefer) and finish the new VM wizard.
6. Make sure the network adapter for both VMs is set to Host-only or an isolated network so they are not exposed to the internet.
7. Configure recommended VM resources: at least 2 CPU cores and 2–4 GB RAM for Metasploitable; 2+ CPU cores and 4+ GB RAM for Kali (increase RAM if you plan to run multiple VMs).
8. After import, power on each VM from the VMware UI by selecting the VM and clicking Power on.
9. Default login credentials: check the Kali download page for the current Kali username/password, and use msfadmin / msfadmin for Metasploitable2 (verify after boot).
10. Take a clean snapshot of each VM immediately after first successful boot so you can revert to a clean state later.
11. Never connect the vulnerable Metasploitable VM to a bridged or public network; keep it isolated in your lab.
12. If you need to edit VM settings later, right-click the VM in VMware and choose Settings (or Virtual Machine Settings) to change CPU, RAM, and network options.
13. If something goes wrong, shut down the VM, revert to the snapshot, and try importing again.
