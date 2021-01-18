---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualhub
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualHub.md
ms.openlocfilehash: 5f65ec635c71e64fb0e16d6a7391f188c6e2582c
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495555"
---
# <span data-ttu-id="9ba73-101">Get-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9ba73-101">Get-AzVirtualHub</span></span>

## <span data-ttu-id="9ba73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ba73-102">SYNOPSIS</span></span>
<span data-ttu-id="9ba73-103">이름 및 ResourceGroupName으로 Azure VirtualHub를 얻거나 ResourceGroupName/Subscription에 의해 모든 Virtual Hubs를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-103">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="9ba73-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ba73-104">SYNTAX</span></span>

### <span data-ttu-id="9ba73-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="9ba73-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzVirtualHub [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9ba73-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba73-106">ListByResourceGroupName</span></span>
```
Get-AzVirtualHub [-ResourceGroupName <String>] [-Name <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ba73-107">설명</span><span class="sxs-lookup"><span data-stu-id="9ba73-107">DESCRIPTION</span></span>
<span data-ttu-id="9ba73-108">이름 및 ResourceGroupName으로 Azure VirtualHub를 얻거나 ResourceGroupName/Subscription에 의해 모든 Virtual Hubs를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-108">Gets an Azure VirtualHub by Name and ResourceGroupName or lists all Virtual Hubs by ResourceGroupName/Subscription.</span></span>

## <span data-ttu-id="9ba73-109">예제</span><span class="sxs-lookup"><span data-stu-id="9ba73-109">EXAMPLES</span></span>

### <span data-ttu-id="9ba73-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9ba73-110">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> Get-AzVirtualHub -ResourceGroupName "testRG" -Name "westushub"

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

<span data-ttu-id="9ba73-111">위의 경우 Azure의 해당 리소스 그룹에 리소스 그룹 "testRG", Virtual WAN 및 미국 서부의 Virtual Hub가 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-111">The above will create a resource group "testRG", a Virtual WAN and a Virtual Hub in West US in that resource group in Azure.</span></span> <span data-ttu-id="9ba73-112">가상 허브의 주소 공간은 "10.0.1.0/24"입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-112">The virtual hub will have the address space "10.0.1.0/24".</span></span>

<span data-ttu-id="9ba73-113">그런 다음 ResourceGroupName 및 ResourceName을 사용하여 가상 허브를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-113">It then gets the virtual hub using its ResourceGroupName and ResourceName.</span></span>

### <span data-ttu-id="9ba73-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="9ba73-114">Example 2</span></span>

```powershell
PS C:\> Get-AzVirtualHub -Name westushub*

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub1
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub1
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded

VirtualWan                : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualWans/myVirtualWAN
ResourceGroupName         : testRG
Name                      : westushub2
Id                        : /subscriptions/{subscriptionId}resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub2
AddressPrefix             : 10.0.1.0/24
RouteTable                : 
VirtualNetworkConnections : {}
Location                  : West US
Type                      : Microsoft.Network/virtualHubs
ProvisioningState         : Succeeded
```

<span data-ttu-id="9ba73-115">이 cmdlet은 필터링을 사용하여 가상 허브를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-115">This cmdlet gets the virtual hub using filtering.</span></span>

## <span data-ttu-id="9ba73-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9ba73-116">PARAMETERS</span></span>

### <span data-ttu-id="9ba73-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ba73-117">-DefaultProfile</span></span>
<span data-ttu-id="9ba73-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ba73-119">-Name</span><span class="sxs-lookup"><span data-stu-id="9ba73-119">-Name</span></span>
<span data-ttu-id="9ba73-120">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-120">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases: ResourceName, VirtualHubName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9ba73-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9ba73-121">-ResourceGroupName</span></span>
<span data-ttu-id="9ba73-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-122">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: True
```

### <span data-ttu-id="9ba73-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ba73-123">CommonParameters</span></span>
<span data-ttu-id="9ba73-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ba73-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ba73-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9ba73-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ba73-126">입력</span><span class="sxs-lookup"><span data-stu-id="9ba73-126">INPUTS</span></span>

### <span data-ttu-id="9ba73-127">없음</span><span class="sxs-lookup"><span data-stu-id="9ba73-127">None</span></span>

## <span data-ttu-id="9ba73-128">출력</span><span class="sxs-lookup"><span data-stu-id="9ba73-128">OUTPUTS</span></span>

### <span data-ttu-id="9ba73-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9ba73-129">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

## <span data-ttu-id="9ba73-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ba73-130">NOTES</span></span>

## <span data-ttu-id="9ba73-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ba73-131">RELATED LINKS</span></span>

[<span data-ttu-id="9ba73-132">New-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9ba73-132">New-AzVirtualHub</span></span>](./New-AzVirtualHub.md)

[<span data-ttu-id="9ba73-133">Remove-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9ba73-133">Remove-AzVirtualHub</span></span>](./Remove-AzVirtualHub.md)

[<span data-ttu-id="9ba73-134">Update-AzVirtualHub</span><span class="sxs-lookup"><span data-stu-id="9ba73-134">Update-AzVirtualHub</span></span>](./Update-AzVirtualHub.md)
