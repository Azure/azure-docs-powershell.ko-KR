---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDelegation.md
ms.openlocfilehash: 4b6f253da0c2494db49883402be8f39f5ef80ae4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700610"
---
# <span data-ttu-id="82a5a-101">Get-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="82a5a-101">Get-AzDelegation</span></span>

## <span data-ttu-id="82a5a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82a5a-102">SYNOPSIS</span></span>
<span data-ttu-id="82a5a-103">지정 된 서브넷에 대 한 위임 (또는 모든 위임)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

## <span data-ttu-id="82a5a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82a5a-104">SYNTAX</span></span>

```
Get-AzDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82a5a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="82a5a-105">DESCRIPTION</span></span>
<span data-ttu-id="82a5a-106">**Get-AzDelegation** cmdlet은 서브넷에서 명명 된 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-106">The **Get-AzDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="82a5a-107">위임을 지정 하지 않으면 제공 된 서브넷에 대 한 모든 위임이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="82a5a-108">예제의</span><span class="sxs-lookup"><span data-stu-id="82a5a-108">EXAMPLES</span></span>

### <span data-ttu-id="82a5a-109">1: 특정 위임 검색</span><span class="sxs-lookup"><span data-stu-id="82a5a-109">1: Retrieving a specific delegation</span></span>
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

<span data-ttu-id="82a5a-110">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="82a5a-111">두 번째 줄은 "myDelegation" 위임에 대 한 위임 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="82a5a-112">2: 모든 서브넷 위임을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzDelegation -Subnet $subnet
```

<span data-ttu-id="82a5a-113">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="82a5a-114">두 번째 줄에는 _Mysubnet_ 의 모든 위임 목록이 $delegations 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="82a5a-115">변수</span><span class="sxs-lookup"><span data-stu-id="82a5a-115">PARAMETERS</span></span>

### <span data-ttu-id="82a5a-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82a5a-116">-DefaultProfile</span></span>
<span data-ttu-id="82a5a-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82a5a-118">-이름</span><span class="sxs-lookup"><span data-stu-id="82a5a-118">-Name</span></span>
<span data-ttu-id="82a5a-119">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-119">The name of the delegation</span></span>

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

### <span data-ttu-id="82a5a-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="82a5a-120">-Subnet</span></span>
<span data-ttu-id="82a5a-121">서브넷</span><span class="sxs-lookup"><span data-stu-id="82a5a-121">The subnet</span></span>

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

### <span data-ttu-id="82a5a-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82a5a-122">CommonParameters</span></span>
<span data-ttu-id="82a5a-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82a5a-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82a5a-124">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82a5a-124">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82a5a-125">입력</span><span class="sxs-lookup"><span data-stu-id="82a5a-125">INPUTS</span></span>

### <span data-ttu-id="82a5a-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82a5a-126">System.String</span></span>

### <span data-ttu-id="82a5a-127">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="82a5a-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="82a5a-128">출력</span><span class="sxs-lookup"><span data-stu-id="82a5a-128">OUTPUTS</span></span>

### <span data-ttu-id="82a5a-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="82a5a-129">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="82a5a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="82a5a-130">NOTES</span></span>

## <span data-ttu-id="82a5a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82a5a-131">RELATED LINKS</span></span>

<span data-ttu-id="82a5a-132">[추가-AzDelegation](./Add-AzDelegation.md) 
 [새로운 AzDelegation](./New-AzDelegation.md) 
 [제거-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="82a5a-132">[Add-AzDelegation](./Add-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)</span></span>