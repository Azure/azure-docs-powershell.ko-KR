---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVpnSite.md
ms.openlocfilehash: 44a40fb446904c8d1bfa40820ae34e0a4aca2caa
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184561"
---
# <span data-ttu-id="51dfc-101">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="51dfc-101">Get-AzVpnSite</span></span>

## <span data-ttu-id="51dfc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51dfc-102">SYNOPSIS</span></span>
<span data-ttu-id="51dfc-103">이름으로 Azure VpnSite 리소스를 얻거나 ResourceGroup 또는 SubscriptionId의 모든 VpnSite를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="51dfc-104">이는 Cortex 가상 허브와의 S2S 연결을 위해 Azure에 업로드된 고객 분기의 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

## <span data-ttu-id="51dfc-105">구문</span><span class="sxs-lookup"><span data-stu-id="51dfc-105">SYNTAX</span></span>

### <span data-ttu-id="51dfc-106">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="51dfc-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="51dfc-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51dfc-107">ListByResourceGroupName</span></span>
```
Get-AzVpnSite [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="51dfc-108">설명</span><span class="sxs-lookup"><span data-stu-id="51dfc-108">DESCRIPTION</span></span>
<span data-ttu-id="51dfc-109">이름으로 Azure VpnSite 리소스를 얻거나 ResourceGroup 또는 SubscriptionId의 모든 VpnSite를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="51dfc-110">예제</span><span class="sxs-lookup"><span data-stu-id="51dfc-110">EXAMPLES</span></span>

### <span data-ttu-id="51dfc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="51dfc-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

ResourceGroupName : testRG
Name              : testVpnSite
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="51dfc-112">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual WAN 리소스 그룹인 Virtual WAN이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="51dfc-113">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="51dfc-114">사이트가 만들어지면 Get-AzVpnSite 명령을 사용하여 사이트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-114">Once the site is created, it gets the site using the Get-AzVpnSite command.</span></span>

### <span data-ttu-id="51dfc-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="51dfc-115">Example 2</span></span>

```powershell
PS C:\> Get-AzVpnSite -Name test*

ResourceGroupName : testRG
Name              : testVpnSite1
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite1
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded

ResourceGroupName : testRG
Name              : testVpnSite2
Id                : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/vpnSites/testVpnSite2
Location          : eastus2euap
IpAddress         : 1.2.3.4
VirtualWan        : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
AddressSpace      : {192.168.2.0/24, 192.168.3.0/24}
BgpSettings       :
Type              : Microsoft.Network/vpnSites
ProvisioningState : Succeeded
```

<span data-ttu-id="51dfc-116">이 cmdlet은 "test"로 시작하는 모든 사이트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-116">This cmdlet gets all Sites that start with "test".</span></span>

## <span data-ttu-id="51dfc-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51dfc-117">PARAMETERS</span></span>

### <span data-ttu-id="51dfc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51dfc-118">-DefaultProfile</span></span>
<span data-ttu-id="51dfc-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dfc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="51dfc-120">-Name</span></span>
<span data-ttu-id="51dfc-121">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-121">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VpnSiteName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dfc-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="51dfc-122">-ResourceGroupName</span></span>
<span data-ttu-id="51dfc-123">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-123">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51dfc-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51dfc-124">CommonParameters</span></span>
<span data-ttu-id="51dfc-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51dfc-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51dfc-126">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51dfc-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51dfc-127">입력</span><span class="sxs-lookup"><span data-stu-id="51dfc-127">INPUTS</span></span>

### <span data-ttu-id="51dfc-128">없음</span><span class="sxs-lookup"><span data-stu-id="51dfc-128">None</span></span>

## <span data-ttu-id="51dfc-129">출력</span><span class="sxs-lookup"><span data-stu-id="51dfc-129">OUTPUTS</span></span>

### <span data-ttu-id="51dfc-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="51dfc-130">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="51dfc-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51dfc-131">NOTES</span></span>

## <span data-ttu-id="51dfc-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51dfc-132">RELATED LINKS</span></span>

[<span data-ttu-id="51dfc-133">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="51dfc-133">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="51dfc-134">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="51dfc-134">Remove-AzVpnSite</span></span>](./Remove-AzVpnSite.md)

[<span data-ttu-id="51dfc-135">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="51dfc-135">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
