---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 213c6616a143f7be64454f6538fac5d5c89afd54
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044868"
---
# <span data-ttu-id="a95b3-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="a95b3-101">Get-AzDelegation</span></span>

## <span data-ttu-id="a95b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a95b3-102">SYNOPSIS</span></span>
<span data-ttu-id="a95b3-103">지정 된 서브넷에 대 한 위임 (또는 모든 위임)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="a95b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a95b3-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a95b3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a95b3-105">DESCRIPTION</span></span>
<span data-ttu-id="a95b3-106">**Get-AzDelegation** cmdlet은 서브넷에서 명명 된 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="a95b3-107">위임을 지정 하지 않으면 제공 된 서브넷에 대 한 모든 위임이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="a95b3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a95b3-108">EXAMPLES</span></span>

### <span data-ttu-id="a95b3-109">1: 특정 위임 검색</span><span class="sxs-lookup"><span data-stu-id="a95b3-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="a95b3-110">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a95b3-111">두 번째 줄은 "myDelegation" 위임에 대 한 위임 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="a95b3-112">2: 모든 서브넷 위임을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="a95b3-113">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="a95b3-114">두 번째 줄에는 _Mysubnet_ 의 모든 위임 목록이 $delegations 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="a95b3-115">변수</span><span class="sxs-lookup"><span data-stu-id="a95b3-115">PARAMETERS</span></span>

### <span data-ttu-id="a95b3-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a95b3-116">-DefaultProfile</span></span>
<span data-ttu-id="a95b3-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a95b3-118">-이름</span><span class="sxs-lookup"><span data-stu-id="a95b3-118">-Name</span></span>
<span data-ttu-id="a95b3-119">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-119">The name of the delegation</span></span>

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

### <span data-ttu-id="a95b3-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="a95b3-120">-Subnet</span></span>
<span data-ttu-id="a95b3-121">서브넷</span><span class="sxs-lookup"><span data-stu-id="a95b3-121">The subnet</span></span>

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

### <span data-ttu-id="a95b3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a95b3-122">CommonParameters</span></span>
<span data-ttu-id="a95b3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a95b3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a95b3-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a95b3-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a95b3-125">입력</span><span class="sxs-lookup"><span data-stu-id="a95b3-125">INPUTS</span></span>

### <span data-ttu-id="a95b3-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a95b3-126">System.String</span></span>

### <span data-ttu-id="a95b3-127">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="a95b3-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="a95b3-128">출력</span><span class="sxs-lookup"><span data-stu-id="a95b3-128">OUTPUTS</span></span>

### <span data-ttu-id="a95b3-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="a95b3-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="a95b3-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a95b3-130">NOTES</span></span>

## <span data-ttu-id="a95b3-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a95b3-131">RELATED LINKS</span></span>

<span data-ttu-id="a95b3-132">[추가-AzDelegation](./Add-AzDelegation.md) 
 [새로운 AzDelegation](./New-AzDelegation.md) 
 [제거-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="a95b3-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>