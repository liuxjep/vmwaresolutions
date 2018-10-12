---

copyright:

  years:  2016, 2018

lastupdated: "2018-09-20"

---

# 2.6 版的版本注意事項

此版本包括新增特性、元件更新、可用性加強功能及錯誤修正程式。如需不同版本的已修正問題、產品的已知問題以及使用 {{site.data.keyword.vmwaresolutions_full}} 之要訣的清單，請參閱 [{{site.data.keyword.vmwaresolutions_short}} dW Answers](https://developer.ibm.com/answers/topics/cloudvmw/){:new_window}。

## Spectre 及 Meltdown 補救

{{site.data.keyword.vmwaresolutions_short}} 發行來自 VMware 的修補程式，以回應與 Spectre 及 Meltdown 相關的漏洞（CVE-2017-5753、CVE-2017-5715 及 CVE-2017-5754）。

* CVEID: [CVE-2017-5753](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5753)
* CVEID: [CVE-2017-5715](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5715)
* CVEID: [CVE-2017-5754](http://cve.mitre.org/cgi-bin/cvename.cgi?name=CVE-2017-5754)

如需相關資訊，請參閱[處理 Spectre 及 Meltdown 漏洞](../vmonic/trbl_fix_spectre.html)。

## 使用 Intel Optane 的高效能選項

當您訂購新的實例時，或在起始部署之後新增 vSAN 叢集時，此版本提供針對 vSAN 儲存空間新增高效能快取的選項。

此選項可讓您將儲存空間容量磁碟數目從 8 增加到最大值 10。

「使用 Intel Optane 的高效能」選項僅適用於使用雙重 Intel Xeon Gold 5120 及雙重 Intel Xeon Gold 6140 處理器的自訂配置。

如需相關資訊，請參閱實例或叢集類型的適當訂購主題。

## 啟用公用或專用網路

您現在可以部署已啟用公用及專用網路介面卡 (NIC) 或已啟用僅限專用 NIC 的 vCenter Server 及 vCenter Server with Hybridity Bundle 實例，以及 VMware vSphere 叢集。當您將新的叢集新增至 vCenter Server 及 vCenter Server with Hybridity Bundle 實例時，也可以使用此選項。

部分附加程式服務需要公用 NIC，如果您選擇啟用僅限專用網路，則無法使用。

如需相關資訊，請參閱下列各主題中的_網路介面設定_ 小節：

* [訂購 vCenter Server 實例](../vcenter/vc_orderinginstance.html#network-interface-settings)
* [訂購 vCenter Server with Hybridity Bundle 實例](../vcenter/vc_hybrid_orderinginstance.html#network-interface-settings)
* [訂購新的 vSphere 叢集](../vsphere/vs_orderinginstances.html#network-interface-settings)

## 刪除 ESXi 伺服器

如果您符合 vCenter Server、vCenter Server with Hybridity Bundle 或 Cloud Foundation 實例的最低需求，則現在可以從這些實例中刪除任何 ESXi 伺服器。

如需 ESXi 伺服器需求的相關資訊，請參閱下列主題：

* [擴充及縮減 vCenter Server 實例的容量](../vcenter/vc_addingremovingservers.html)
* [擴充及縮減 vCenter Server with Hybridity Bundle 實例的容量](../vcenter/vc_hybrid_addingremovingservers.html)
* [擴充及縮減 Cloud Foundation 實例的容量](../sddc/sd_addingremovingservers.html)

## VMware vCenter Server 實例的更新

此版本會套用下列升級及改進項目：

* vSphere ESXi 6.5 Update 2c
* vCenter Server Appliance 6.5 Update 2c
* Platform Services Controller 6.5 Update 2c
* NSX for vSphere 6.4.1

## VMware vCenter Server with Hybridity Bundle 的更新項目

### 從 vCenter Server 實例中移除 Hybridity Bundle

您現在可以從 vCenter Server 實例中移除 Hybridity Bundle 授權。若要這樣做，您需要將 VMware NSX 及 VMware vSAN 租賃授權碼取代為「自帶授權 (BYOL)」碼，並開立支援問題單以取消租賃授權的費用。

如需相關資訊，請參閱[從 vCenter Server 實例中移除 Hybridity Bundle](../vcenter/vc_hybrid_deletingbundle.html)。

### vCenter Server with Hybridity Bundle 可用性

「事業夥伴」現在可以訂購 vCenter Server with Hybridity Bundle 實例。「事業夥伴」無法將現有 vCenter Server 實例升級至 vCenter Server with Hybridity Bundle 實例，而且無法從 vCenter Server with Hybridity Bundle 實例中移除 Hybridity Bundle。

如需相關資訊，請參閱下列主題：

* [vCenter Server with Hybridity Bundle 概觀](../vcenter/vc_hybrid_overview.html)
* [訂購 vCenter Server with Hybridity Bundle 實例](../vcenter/vc_hybrid_orderinginstance.html)

## VMware Cloud Foundation 實例的更新項目

此版本會套用下列升級及改進項目：

* vSphere ESXi 6.5 Update 2c
* vCenter Server Appliance 6.5 Update 2c
* Platform Services Controller 6.5 Update 2c
* NSX for vSphere 6.4.1

## 附加服務的更新項目

### HyTrust KeyControl on IBM Cloud

現在，HyTrust KeyControl on {{site.data.keyword.cloud_notm}} 服務可用於執行 vSphere 6.5 以及部署在或升級至 2.5 版及更新版本的 VMware Cloud Foundation 實例及 VMware vCenter Server 實例。此服務藉由自動化及簡化加密金鑰的生命週期，來簡化加密工作負載的管理。服務可以使用符合 FIPS 140-2 標準的加密，輕鬆地管理加密金鑰。使用此服務，您可以管理所有虛擬機器及加密資料儲存庫的加密金鑰，並將其調整為在大型部署中支援數千個加密工作負載。

您可以在訂購實例時訂購包含此服務的實例，或稍後將此服務新增至現有實例。

如需相關資訊，請參閱下列主題：
* [HyTrust KeyControl on {{site.data.keyword.cloud_notm}} 的元件及考量](../services/htkc_considerations.html)
* [管理 HyTrust KeyControl on {{site.data.keyword.cloud_notm}}](../services/managinghtkc.html)

### HyTrust CloudControl on IBM Cloud

現行版本會將 HyTrust CloudControl 5.4 安裝在所有新部署的實例。如需 HyTrust CloudControl 5.4 中新增特性的相關資訊，請參閱 [HyTrust CloudControl 5.4 版線上文件集](https://docs.hytrust.com/CloudControl/5.4.0/Online/index.html)。

### HyTrust DataControl on IBM Cloud

現行版本會將 HyTrust DataControl 4.2 安裝在所有新部署的實例。如需 HyTrust DataControl 4.2 中新增特性的相關資訊，請參閱 [HyTrust DataControl 4.x 新增功能](https://docs.hytrust.com/DataControl/4.2/Admin_Guide-4.2/Content/Books/aaCommon/New-Changed-4x.htm)。

### vSphere ESXi 6.5 版 Update 2c 的 Veeam on IBM Cloud 支援

從 2.6 版開始，新的實例及新的主機是使用 vSphere ESXi 6.5 版 Update 2c 所佈建。如果您使用 Veeam Backup and Replication，則 Veeam 會建議您將 Veeam on {{site.data.keyword.cloud_notm}} 實例更新為 9.5u3a 版或更新版本，以確保與 vSphere ESXi 6.5 Update 2c 的最佳相容性。

建議一併將已安裝 Veeam on {{site.data.keyword.cloud_notm}} 的現有 Cloud Foundation 實例更新為 9.5u3a 版或更新版本。

如需 Veeam on {{site.data.keyword.cloud_notm}} 的相關資訊，請參閱 [Veeam on {{site.data.keyword.cloud_notm}} 概觀](../services/veeam_considerations.html)。

### VMware HCX on IBM Cloud

現行版本會將 VMware HCX 3.5.1 R106 安裝至所有新部署的實例。如需 HCX 3.5.1 R106 中新增特性的相關資訊，請參閱 [VMware NSX Hybrid Connect 文件](https://docs.vmware.com/en/VMware-NSX-Hybrid-Connect/index.html)。

## 新的及更新的文件

### 參照架構文件
{{site.data.keyword.vmwaresolutions_short}} 架構文件已更新為包括用來瞭解您管理及操作 VMware 實例之責任的重要事項考量。

如需相關資訊，請參閱 [VMware 實例的後置部署考量](../archiref/solution/solution_considerations.md)。

## 使用者介面更新和加強功能

會更新使用者介面，並提供下列加強功能：

* 提供各種錯誤訊息及工具提示加強功能，以協助您在使用者介面上選取適當的設定。