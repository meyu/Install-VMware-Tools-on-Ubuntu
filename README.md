所為何來
=
安裝 VMware Tools 於 VMware 上之 Ubuntu 虛擬主機，使虛擬主機能變更解析度、與實體主機共享剪貼簿和資料夾，並支援 VMware 的快照功能 (Snapshot)。

適用環境
=
實體主機：Windows 7 / Window 8 / OS X 10.8  
虛擬主機：Ubuntu 12.04 / Ubuntu 12.10 (Server & Desktop)  
虛擬平台：VMware Workstation 9 / VMware Fusion 5  

安裝方式
=
登入 Ubuntu (虛擬主機)。  
點選 VMware 工具列選單 (實體主機)：Virtual Machine > Install VMware Tools。  
此時，虛擬主機將會載入虛擬的 VMware Tools 安裝光碟。  
於終端機中 (虛擬主機)，輸入以下指令，以掛載光碟：
```bash
sudo mkdir /mnt/cdrom &&
sudo mount /dev/cdrom /mnt/cdrom
```
輸入以下指令，以解壓縮安裝檔：
```bash
tar xzvf /mnt/cdrom/VMwareTools-9.2.2-893683.tar.gz -C /tmp/
```
注意：9.2.2-893683 為本文示範版本，請依所得版本自行更改。  
輸入以下指令進行安裝 (參數 -d，意指以預設值進行安裝)：
```bash
sudo /tmp/vmware-tools-distrib/vmware-install.pl -d
```
完成後，請重新開機 (虛擬主機)：
```bash
sudo reboot
```
DONE.

<br>
<br>

補充說明
=
* 同樣步驟可用來更新、移除 VMware Tools。


參考資源
=
* [Installing VMware Tools in an Ubuntu virtual machine](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=1022525)
* [Overview of VMware Tools](http://kb.vmware.com/selfservice/microsites/search.do?language=en_US&cmd=displayKC&externalId=340)
