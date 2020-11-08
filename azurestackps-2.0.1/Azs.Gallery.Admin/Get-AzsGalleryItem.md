---
external help file: ''
Module Name: Azs.Gallery.Admin
online version: https://docs.microsoft.com/powershell/module/azs.gallery.admin/get-azsgalleryitem
schema: 2.0.0
ms.openlocfilehash: 5523dd35ae91b9fea7db5f2451401793cb6059c2
ms.sourcegitcommit: 199e9c800e58e88c4cbfd3f221bafe02b3e8294d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 06/24/2020
ms.locfileid: "94045265"
---
# <span data-ttu-id="57850-101">Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="57850-101">Get-AzsGalleryItem</span></span>

## <span data-ttu-id="57850-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57850-102">SYNOPSIS</span></span>
<span data-ttu-id="57850-103">특정 갤러리 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57850-103">Get a specific gallery item.</span></span>

## <span data-ttu-id="57850-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57850-104">SYNTAX</span></span>

### <span data-ttu-id="57850-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="57850-105">List (Default)</span></span>
```
Get-AzsGalleryItem [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="57850-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="57850-106">Get</span></span>
```
Get-AzsGalleryItem -Name <String> [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

### <span data-ttu-id="57850-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="57850-107">GetViaIdentity</span></span>
```
Get-AzsGalleryItem -InputObject <IGalleryIdentity> [-DefaultProfile <PSObject>] [-PassThru]
 [<CommonParameters>]
```

## <span data-ttu-id="57850-108">설명은</span><span class="sxs-lookup"><span data-stu-id="57850-108">DESCRIPTION</span></span>
<span data-ttu-id="57850-109">특정 갤러리 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57850-109">Get a specific gallery item.</span></span>

## <span data-ttu-id="57850-110">예제의</span><span class="sxs-lookup"><span data-stu-id="57850-110">EXAMPLES</span></span>

### <span data-ttu-id="57850-111">예제 1: Get-AzsGalleryItem</span><span class="sxs-lookup"><span data-stu-id="57850-111">Example 1: Get-AzsGalleryItem</span></span>
```powershell
PS C:\> Get-AzsGalleryItem -Name TestUbuntu.Test.1.0.0

Name                  Publisher  PublisherDisplayName ItemName ItemDisplayName       Version Summary
----                  ---------  -------------------- -------- ---------------       ------- -------
TestUbuntu.Test.1.0.0 TestUbuntu TestUbuntu           Test     Test.TestUbuntu.1.0.0 1.0.0   Create a simple VM
```

<span data-ttu-id="57850-112">이름으로 갤러리 항목을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="57850-112">Gets the gallery item by name.</span></span>

### <span data-ttu-id="57850-113">예제 2: 갤러리 항목 목록 표시</span><span class="sxs-lookup"><span data-stu-id="57850-113">Example 2: List Gallery Items</span></span>
```powershell
PS C:\> Get-AzsGalleryItem

Name                                       Publisher PublisherDisplayName  ItemName                  ItemDisplayName
----                                       --------- --------------------  --------                  ---------------
Canonical.UbuntuServer1804LTS-ARM.1.0.3    Canonical Canonical             UbuntuServer1804LTS-ARM   Ubuntu Server 1...
Microsoft.AddOnRP-WindowsServer.1.1910.3   Microsoft Microsoft             AddOnRP-WindowsServer     Microsoft Azure...
Microsoft.AdminOffer.6.0.0                 Microsoft Microsoft Corporation AdminOffer                Offer
Microsoft.AvailabilitySet-ARM.1.0.1        Microsoft Microsoft             AvailabilitySet-ARM       Availability Set
Microsoft.Connection-ARM.1.2.2             Microsoft Microsoft             Connection-ARM            Connection
Microsoft.CustomScriptExtension-arm.2.0.10 Microsoft Microsoft Corp.       CustomScriptExtension-arm Custom Script E...
Microsoft.DSC-arm.2.0.7                    Microsoft Microsoft Corp.       DSC-arm                   PowerShell Desi...
Microsoft.DnsZone-ARM.1.0.1                Microsoft Microsoft             DnsZone-ARM               DNS zone
Microsoft.Image-ARM.1.0.2                  Microsoft Microsoft             Image-ARM                 Image
Microsoft.KeyVault.1.0.14                  Microsoft Microsoft             KeyVault                  Key Vault
Microsoft.LoadBalancer-ARM.1.0.2           Microsoft Microsoft             LoadBalancer-ARM          Load Balancer
Microsoft.LocalNetworkGateway-ARM.1.0.3    Microsoft Microsoft             LocalNetworkGateway-ARM   Local network g...
Microsoft.ManagedDisk-ARM.1.0.2            Microsoft Microsoft             ManagedDisk-ARM           Managed Disks
Microsoft.NetworkInterface-ARM.1.0.4       Microsoft Microsoft             NetworkInterface-ARM      Network interface
Microsoft.NetworkSecurityGroup-ARM.1.0.4   Microsoft Microsoft             NetworkSecurityGroup-ARM  Network securit...
Microsoft.Offer.6.0.0                      Microsoft Microsoft Corporation Offer                     Offer
Microsoft.Plan.6.0.0                       Microsoft Microsoft Corporation Plan                      Plan
Microsoft.PublicIPAddress-ARM.1.0.2        Microsoft Microsoft             PublicIPAddress-ARM       Public IP address
Microsoft.PublicIPPool-ARM.1.0.0           Microsoft Microsoft             PublicIPPool-ARM          Public IP pool
Microsoft.ResourceGroup.6.0.0              Microsoft Microsoft             ResourceGroup             Resource group
Microsoft.RouteTable-ARM.1.0.2             Microsoft Microsoft             RouteTable-ARM            Route table
Microsoft.ScaleUnitNode-ARM.1.0.0          Microsoft Microsoft             ScaleUnitNode-ARM         Scale Unit Node
Microsoft.Snapshot-ARM.1.0.2               Microsoft Microsoft             Snapshot-ARM              Snapshot
Microsoft.StorageAccount-ARM.101.0.1       Microsoft Microsoft             StorageAccount-ARM        Storage account
Microsoft.StorageAccount-ARM.1.0.3         Microsoft Microsoft             StorageAccount-ARM        Storage account...
Microsoft.Template.6.0.0                   Microsoft Microsoft             Template                  Template deploy...
Microsoft.TenantSubscription.6.0.0         Microsoft Microsoft Corporation TenantSubscription        Subscription
Microsoft.VirtualMachine-ARM.1.0.2         Microsoft Microsoft             VirtualMachine-ARM        Virtual machine
Microsoft.VirtualNetwork-ARM.1.0.4         Microsoft Microsoft             VirtualNetwork-ARM        Virtual network
Microsoft.VirtualNetworkGateway-ARM.1.0.3  Microsoft Microsoft             VirtualNetworkGateway-ARM Virtual network...
microsoft.antimalware-windows-arm.1.0.0    microsoft Microsoft Corp.       antimalware-windows-arm   Microsoft Antim...
microsoft.custom-script2-linux-arm.3.0.0   microsoft Microsoft Corp.       custom-script2-linux-arm  Custom Script F...
microsoft.custom-script-linux-arm.2.0.50   microsoft Microsoft Corp.       custom-script-linux-arm   Custom Script F...
microsoft.docker-arm.1.1.0                 microsoft Microsoft             docker-arm                Docker
microsoft.vmss.7.1.7                       microsoft Microsoft             vmss                      Virtual machine...

```

<span data-ttu-id="57850-114">Azure 스택 갤러리에서 사용할 수 있는 모든 항목을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-114">Lists all the items available in the Azure Stack gallery.</span></span>

## <span data-ttu-id="57850-115">변수</span><span class="sxs-lookup"><span data-stu-id="57850-115">PARAMETERS</span></span>

### <span data-ttu-id="57850-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57850-116">-DefaultProfile</span></span>
<span data-ttu-id="57850-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57850-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57850-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="57850-118">-InputObject</span></span>
<span data-ttu-id="57850-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="57850-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="57850-120">-이름</span><span class="sxs-lookup"><span data-stu-id="57850-120">-Name</span></span>
<span data-ttu-id="57850-121">갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="57850-121">Identity of the gallery item.</span></span>
<span data-ttu-id="57850-122">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57850-122">Includes publisher name, item name, and may include version separated by period character.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: GalleryItemName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57850-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="57850-123">-PassThru</span></span>
<span data-ttu-id="57850-124">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-124">Returns true when the command succeeds</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Get, GetViaIdentity
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57850-125">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57850-125">-SubscriptionId</span></span>
<span data-ttu-id="57850-126">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="57850-126">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="57850-127">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-127">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="57850-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57850-128">CommonParameters</span></span>
<span data-ttu-id="57850-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57850-130">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57850-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57850-131">입력</span><span class="sxs-lookup"><span data-stu-id="57850-131">INPUTS</span></span>

### <span data-ttu-id="57850-132">IGalleryIdentity (Microsoft. PowerShell. 모델)</span><span class="sxs-lookup"><span data-stu-id="57850-132">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.IGalleryIdentity</span></span>

## <span data-ttu-id="57850-133">출력</span><span class="sxs-lookup"><span data-stu-id="57850-133">OUTPUTS</span></span>

### <span data-ttu-id="57850-134">Api20150401. IGalleryItem에 대 한 Microsoft Azure.</span><span class="sxs-lookup"><span data-stu-id="57850-134">Microsoft.Azure.PowerShell.Cmdlets.Gallery.Models.Api20150401.IGalleryItem</span></span>



## <span data-ttu-id="57850-135">상속자</span><span class="sxs-lookup"><span data-stu-id="57850-135">NOTES</span></span>

<span data-ttu-id="57850-136">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-136">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="57850-137">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="57850-137">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="57850-138">INPUTOBJECT <IGalleryIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="57850-138">INPUTOBJECT <IGalleryIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="57850-139">`[GalleryItemName <String>]`: 갤러리 항목의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="57850-139">`[GalleryItemName <String>]`: Identity of the gallery item.</span></span> <span data-ttu-id="57850-140">Publisher 이름, 항목 이름 등을 포함 하며 기간으로 구분 된 버전을 포함할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57850-140">Includes publisher name, item name, and may include version separated by period character.</span></span>
  - <span data-ttu-id="57850-141">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="57850-141">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="57850-142">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="57850-142">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="57850-143">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="57850-143">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="57850-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57850-144">RELATED LINKS</span></span>

