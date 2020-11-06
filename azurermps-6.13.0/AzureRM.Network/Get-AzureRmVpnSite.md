---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVpnSite.md
ms.openlocfilehash: 0277e61a6b1b180691908b2e86c0050eb8d62b1d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529517"
---
# <span data-ttu-id="a2ba2-101">Get-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="a2ba2-101">Get-AzureRmVpnSite</span></span>

## <span data-ttu-id="a2ba2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2ba2-102">SYNOPSIS</span></span>
<span data-ttu-id="a2ba2-103">이름으로 Azure VpnSite 리소스를 가져오거나 ResourceGroup 또는 SubscriptionId의 모든 VpnSites를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-103">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

<span data-ttu-id="a2ba2-104">이는 Cortex 가상 허브를 사용 하 여 S2S 연결을 위해 Azure에 업로드 되는 고객 분기에 대 한 RM 표현입니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-104">This is an RM representation of customer branches that are uploaded to Azure for S2S connectivity with a Cortex virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a2ba2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="a2ba2-105">SYNTAX</span></span>

### <span data-ttu-id="a2ba2-106">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="a2ba2-106">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVpnSite [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a2ba2-107">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ba2-107">ListByResourceGroupName</span></span>
```
Get-AzureRmVpnSite -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2ba2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a2ba2-108">DESCRIPTION</span></span>
<span data-ttu-id="a2ba2-109">이름으로 Azure VpnSite 리소스를 가져오거나 ResourceGroup 또는 SubscriptionId의 모든 VpnSites를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-109">Gets an Azure VpnSite resource by name OR lists all VpnSites in a ResourceGroup or SubscriptionId.</span></span> 

## <span data-ttu-id="a2ba2-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a2ba2-110">EXAMPLES</span></span>

### <span data-ttu-id="a2ba2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a2ba2-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"

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

<span data-ttu-id="a2ba2-112">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="a2ba2-113">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a2ba2-114">사이트를 만든 후에는 Get-AzureRmVpnSite 명령을 사용 하 여 사이트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-114">Once the site is created, it gets the site using the Get-AzureRmVpnSite command.</span></span>

## <span data-ttu-id="a2ba2-115">변수</span><span class="sxs-lookup"><span data-stu-id="a2ba2-115">PARAMETERS</span></span>

### <span data-ttu-id="a2ba2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2ba2-116">-DefaultProfile</span></span>
<span data-ttu-id="a2ba2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba2-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a2ba2-118">-Name</span></span>
<span data-ttu-id="a2ba2-119">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-119">The resource name.</span></span>

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

### <span data-ttu-id="a2ba2-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2ba2-120">-ResourceGroupName</span></span>
<span data-ttu-id="a2ba2-121">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-121">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a2ba2-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2ba2-122">CommonParameters</span></span>
<span data-ttu-id="a2ba2-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2ba2-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a2ba2-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2ba2-125">입력</span><span class="sxs-lookup"><span data-stu-id="a2ba2-125">INPUTS</span></span>

### <span data-ttu-id="a2ba2-126">않아야</span><span class="sxs-lookup"><span data-stu-id="a2ba2-126">None</span></span>

## <span data-ttu-id="a2ba2-127">출력</span><span class="sxs-lookup"><span data-stu-id="a2ba2-127">OUTPUTS</span></span>

### <span data-ttu-id="a2ba2-128">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a2ba2-128">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

## <span data-ttu-id="a2ba2-129">상속자</span><span class="sxs-lookup"><span data-stu-id="a2ba2-129">NOTES</span></span>

## <span data-ttu-id="a2ba2-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2ba2-130">RELATED LINKS</span></span>
