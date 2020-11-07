---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHub.md
ms.openlocfilehash: f758197a0d2b3f6a62071a139e8a5fc67acc50c9
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711657"
---
# <span data-ttu-id="928e9-101">Get-AzureRmVirtualHub</span><span class="sxs-lookup"><span data-stu-id="928e9-101">Get-AzureRmVirtualHub</span></span>

## <span data-ttu-id="928e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="928e9-102">SYNOPSIS</span></span>
<span data-ttu-id="928e9-103">이름별로 Azure VirtualHub를 가져옵니다. ResourceGroupName 또는 ResourceGroupName/구독으로 모든 가상 허브가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="928e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="928e9-104">SYNTAX</span></span>

### <span data-ttu-id="928e9-105">ListBySubscriptionId (기본값)</span><span class="sxs-lookup"><span data-stu-id="928e9-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzureRmVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="928e9-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928e9-106">ListByResourceGroupName</span></span>
```
Get-AzureRmVirtualHub -ResourceGroupName <String> [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="928e9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="928e9-107">DESCRIPTION</span></span>
<span data-ttu-id="928e9-108">이름별로 Azure VirtualHub를 가져옵니다. ResourceGroupName 또는 ResourceGroupName/구독으로 모든 가상 허브가 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="928e9-109">예제의</span><span class="sxs-lookup"><span data-stu-id="928e9-109">EXAMPLES</span></span>

### <span data-ttu-id="928e9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="928e9-110">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzureRmVirtualHub -ResourceGroupName "testRG" -Name "westushub"

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="928e9-111">위의 방법으로 Azure에서 해당 리소스 그룹의 서쪽에 있는 리소스 그룹 "testRG", 가상 WAN, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="928e9-112">가상 허브에는 주소 공간 "10.0.1.0/24"가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="928e9-113">그런 다음 해당 ResourceGroupName 및 Context.resourcename을 사용 하 여 가상 허브를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

## <span data-ttu-id="928e9-114">변수</span><span class="sxs-lookup"><span data-stu-id="928e9-114">PARAMETERS</span></span>

### <span data-ttu-id="928e9-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="928e9-115">-DefaultProfile</span></span>
<span data-ttu-id="928e9-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="928e9-117">-이름</span><span class="sxs-lookup"><span data-stu-id="928e9-117">-Name</span></span>
<span data-ttu-id="928e9-118">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-118">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="928e9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="928e9-119">-ResourceGroupName</span></span>
<span data-ttu-id="928e9-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-120">The resource group name.</span></span>

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

### <span data-ttu-id="928e9-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="928e9-121">CommonParameters</span></span>
<span data-ttu-id="928e9-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="928e9-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="928e9-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="928e9-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="928e9-124">입력</span><span class="sxs-lookup"><span data-stu-id="928e9-124">INPUTS</span></span>

### <span data-ttu-id="928e9-125">않아야</span><span class="sxs-lookup"><span data-stu-id="928e9-125">None</span></span>

## <span data-ttu-id="928e9-126">출력</span><span class="sxs-lookup"><span data-stu-id="928e9-126">OUTPUTS</span></span>

### <span data-ttu-id="928e9-127">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="928e9-127">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="928e9-128">상속자</span><span class="sxs-lookup"><span data-stu-id="928e9-128">NOTES</span></span>

## <span data-ttu-id="928e9-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="928e9-129">RELATED LINKS</span></span>
