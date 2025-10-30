# installing-kali-linux-and-vulnerable-metasploit-in-vmware.
kali-vm-metasploitable-repo/
├── README.md               <- this file
├── scripts/
│   ├── download_kali_vm.sh <- helper: download Kali prebuilt VM "https://www.kali.org/get-kali/#kali-virtual-machines"
│   ├── import_vmdk_vmware.sh <- helper to generate a basic VMware . "https://www.vmware.com/products/desktop-hypervisor/workstation-and-fusion"
│   └── verify_checksum.sh  <- helper to verify SHA256 sums 
└── vagrant/
    └── Vagrantfile_metasploitable3_example <- downloading link for metasploitable vm "https://sourceforge.net/projects/metasploitable/"
