---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: cbb560b04219b0a77c9158afe3b76b1b9461cdb1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101967947"
---
# <span data-ttu-id="9ac78-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="9ac78-101">Get-AzDelegation</span></span>

## <span data-ttu-id="9ac78-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9ac78-102">SYNOPSIS</span></span>
<span data-ttu-id="9ac78-103">주어진 서브넷에서 위임(또는 모든 위임)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="9ac78-104">구문</span><span class="sxs-lookup"><span data-stu-id="9ac78-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9ac78-105">설명</span><span class="sxs-lookup"><span data-stu-id="9ac78-105">DESCRIPTION</span></span>
<span data-ttu-id="9ac78-106">**Get-AzDelegation** cmdlet은 서브넷에서 명명된 위임을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="9ac78-107">위임이 지정되지 않고 제공된 서브넷의 모든 위임이 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="9ac78-108">예제</span><span class="sxs-lookup"><span data-stu-id="9ac78-108">EXAMPLES</span></span>

### <span data-ttu-id="9ac78-109">1: 특정 위임 검색</span><span class="sxs-lookup"><span data-stu-id="9ac78-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="9ac78-110">첫 번째 줄은 관심 있는 서브넷을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="9ac78-111">두 번째 줄은 "myDelegation"이라는 위임에 대한 위임 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="9ac78-112">2: 모든 서브넷 위임 검색</span><span class="sxs-lookup"><span data-stu-id="9ac78-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $subnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="9ac78-113">첫 번째 줄은 관심 있는 서브넷을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="9ac78-114">두 번째 줄은 $delegations _mySubnet에_ 모든 위임 목록을 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="9ac78-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9ac78-115">PARAMETERS</span></span>

### <span data-ttu-id="9ac78-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9ac78-116">-DefaultProfile</span></span>
<span data-ttu-id="9ac78-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9ac78-118">-Name</span><span class="sxs-lookup"><span data-stu-id="9ac78-118">-Name</span></span>
<span data-ttu-id="9ac78-119">위임의 이름</span><span class="sxs-lookup"><span data-stu-id="9ac78-119">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac78-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="9ac78-120">-Subnet</span></span>
<span data-ttu-id="9ac78-121">서브넷</span><span class="sxs-lookup"><span data-stu-id="9ac78-121">The subnet</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9ac78-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9ac78-122">CommonParameters</span></span>
<span data-ttu-id="9ac78-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9ac78-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9ac78-124">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9ac78-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9ac78-125">입력</span><span class="sxs-lookup"><span data-stu-id="9ac78-125">INPUTS</span></span>

### <span data-ttu-id="9ac78-126">System.String</span><span class="sxs-lookup"><span data-stu-id="9ac78-126">System.String</span></span>

### <span data-ttu-id="9ac78-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="9ac78-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="9ac78-128">출력</span><span class="sxs-lookup"><span data-stu-id="9ac78-128">OUTPUTS</span></span>

### <span data-ttu-id="9ac78-129">Microsoft.Azure.Commands.Network.Models.PSD</span><span class="sxs-lookup"><span data-stu-id="9ac78-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="9ac78-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9ac78-130">NOTES</span></span>

## <span data-ttu-id="9ac78-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9ac78-131">RELATED LINKS</span></span>

<span data-ttu-id="9ac78-132">[Add-AzDelegation](./Add-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="9ac78-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>
