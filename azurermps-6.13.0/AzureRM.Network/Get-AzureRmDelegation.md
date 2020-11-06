---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDelegation.md
ms.openlocfilehash: f3e8ef97ab618df37ba7d5adae107d65676ed29f
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533356"
---
# <span data-ttu-id="6a112-101">Get-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="6a112-101">Get-AzureRmDelegation</span></span>

## <span data-ttu-id="6a112-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6a112-102">SYNOPSIS</span></span>
<span data-ttu-id="6a112-103">지정 된 서브넷에 대 한 위임 (또는 모든 위임)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-103">Get a delegation (or all of the delegations) on a given subnet.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6a112-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6a112-104">SYNTAX</span></span>

```
Get-AzureRmDelegation [-Name <String>] -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6a112-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6a112-105">DESCRIPTION</span></span>
<span data-ttu-id="6a112-106">**Get-AzureRmDelegation** cmdlet은 서브넷에서 명명 된 위임을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-106">The **Get-AzureRmDelegation** cmdlet gets the named delegation from a subnet.</span></span> <span data-ttu-id="6a112-107">위임을 지정 하지 않으면 제공 된 서브넷에 대 한 모든 위임이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-107">If no delegation is named, it returns all of the delegations on the provided subnet.</span></span>

## <span data-ttu-id="6a112-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6a112-108">EXAMPLES</span></span>

### <span data-ttu-id="6a112-109">1: 특정 위임 검색</span><span class="sxs-lookup"><span data-stu-id="6a112-109">1: Retrieving a specific delegation</span></span>
```powershell
PS C:\> $subnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> Get-AzureRmDelegation -Name "myDelegation" -Subnet $subnet

ProvisioningState : Succeeded
ServiceName       : Microsoft.Sql/servers
Actions           : {}
Name              : myDelegation
Etag              : "thisisaguid"
Id                : /subscriptions/subId/resourceGroups/rg/providers/Microsoft.Network/virtualNetworks/myvnet/subnets/mySubnet/delegations/myDelegation
```

<span data-ttu-id="6a112-110">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-110">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="6a112-111">두 번째 줄은 "myDelegation" 위임에 대 한 위임 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-111">The second line shows the delegation information for the delegation called "myDelegation."</span></span>

### <span data-ttu-id="6a112-112">2: 모든 서브넷 위임을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-112">2: Retrieving all subnet delegations</span></span>
```powershell
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup" | Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet"
PS C:\> $delegations = Get-AzureRmDelegation -Subnet $subnet
```

<span data-ttu-id="6a112-113">첫 번째 줄은 원하는 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-113">The first line retrieves the subnet of interest.</span></span> <span data-ttu-id="6a112-114">두 번째 줄에는 _Mysubnet_ 의 모든 위임 목록이 $delegations 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-114">The second line stores a list of all of the delegations on _mySubnet_ in the $delegations variable.</span></span>

## <span data-ttu-id="6a112-115">변수</span><span class="sxs-lookup"><span data-stu-id="6a112-115">PARAMETERS</span></span>

### <span data-ttu-id="6a112-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6a112-116">-DefaultProfile</span></span>
<span data-ttu-id="6a112-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a112-118">-이름</span><span class="sxs-lookup"><span data-stu-id="6a112-118">-Name</span></span>
<span data-ttu-id="6a112-119">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-119">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6a112-120">-서브넷</span><span class="sxs-lookup"><span data-stu-id="6a112-120">-Subnet</span></span>
<span data-ttu-id="6a112-121">서브넷</span><span class="sxs-lookup"><span data-stu-id="6a112-121">The subnet</span></span>

```yaml
Type: PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6a112-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6a112-122">CommonParameters</span></span>
<span data-ttu-id="6a112-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6a112-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="6a112-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6a112-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6a112-125">입력</span><span class="sxs-lookup"><span data-stu-id="6a112-125">INPUTS</span></span>

### <span data-ttu-id="6a112-126">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="6a112-126">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="6a112-127">출력</span><span class="sxs-lookup"><span data-stu-id="6a112-127">OUTPUTS</span></span>

### <span data-ttu-id="6a112-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="6a112-128">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="6a112-129">상속자</span><span class="sxs-lookup"><span data-stu-id="6a112-129">NOTES</span></span>

## <span data-ttu-id="6a112-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6a112-130">RELATED LINKS</span></span>
<span data-ttu-id="6a112-131">[추가-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [새로운 AzureRmDelegation](./New-AzureRmDelegation.md) 
 [제거-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span><span class="sxs-lookup"><span data-stu-id="6a112-131">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[New-AzureRmDelegation](./New-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)</span></span>
