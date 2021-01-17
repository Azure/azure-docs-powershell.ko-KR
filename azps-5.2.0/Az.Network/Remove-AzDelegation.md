---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDelegation.md
ms.openlocfilehash: 9d5f7960bb8f47a1f0d617cd4ba43db565ae2c79
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356728"
---
# <span data-ttu-id="f1af1-101">Remove-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="f1af1-101">Remove-AzDelegation</span></span>

## <span data-ttu-id="f1af1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1af1-102">SYNOPSIS</span></span>
<span data-ttu-id="f1af1-103">제공된 서브넷에서 서비스 위임이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-103">Removes a service delegation from the provided subnet.</span></span>

## <span data-ttu-id="f1af1-104">구문</span><span class="sxs-lookup"><span data-stu-id="f1af1-104">SYNTAX</span></span>

```
Remove-AzDelegation -Name <String> -Subnet <PSSubnet> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f1af1-105">설명</span><span class="sxs-lookup"><span data-stu-id="f1af1-105">DESCRIPTION</span></span>
<span data-ttu-id="f1af1-106">**Remove-AzDelegation** cmdlet은 위임이 있는 서브넷을 사용하여 해당 서브넷에서 명명된 위임이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-106">The **Remove-AzDelegation** cmdlet takes in a Subnet with delegations and removes the named delegation from that subnet.</span></span>

## <span data-ttu-id="f1af1-107">예제</span><span class="sxs-lookup"><span data-stu-id="f1af1-107">EXAMPLES</span></span>

### <span data-ttu-id="f1af1-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f1af1-108">Example 1</span></span>
```powershell
# Add a delegation to an existing subnet
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Add-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet

# Remove the delegation
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet = Remove-AzDelegation -Name "myDelegation" -Subnet $subnet
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="f1af1-109">이 예제에서는 "기존 서브넷에 위임 _추가"_ 아래에 있는 전반부는 [Add-AzDelegation과 동일합니다.](./Add-AzDelegation.md)</span><span class="sxs-lookup"><span data-stu-id="f1af1-109">In this example, the first half (found under _"Add a delegation to an existing subnet"_) is identical to [Add-AzDelegation](./Add-AzDelegation.md).</span></span> <span data-ttu-id="f1af1-110">후반부에서는 처음 두 cmdlet이 관심 있는 서브넷을 검색하여 서버의 복사본으로 로컬 복사본을 새로 고치고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-110">In the second half, the first two cmdlets retrieve the subnet of interest, refreshing the local copy with what's on the server.</span></span> <span data-ttu-id="f1af1-111">세 번째 cmdlet은 _mySubnet에서_ 전반부에 만든 위임을 제거하고 업데이트된 서브넷을 _$subnet._</span><span class="sxs-lookup"><span data-stu-id="f1af1-111">The third cmdlet removes the delegation that was created in the first half from _mySubnet_ and stores the updated subnet in _$subnet_.</span></span> <span data-ttu-id="f1af1-112">최종 cmdlet은 제거된 위임으로 서버를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-112">The final cmdlet updates the server with the removed delegation.</span></span>

## <span data-ttu-id="f1af1-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f1af1-113">PARAMETERS</span></span>

### <span data-ttu-id="f1af1-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1af1-114">-DefaultProfile</span></span>
<span data-ttu-id="f1af1-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f1af1-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f1af1-116">-Name</span></span>
<span data-ttu-id="f1af1-117">위임의 이름</span><span class="sxs-lookup"><span data-stu-id="f1af1-117">The name of the delegation</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f1af1-118">-Subnet</span><span class="sxs-lookup"><span data-stu-id="f1af1-118">-Subnet</span></span>
<span data-ttu-id="f1af1-119">위임 제거 서브넷</span><span class="sxs-lookup"><span data-stu-id="f1af1-119">The subnet from which to remove the delegation</span></span>

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

### <span data-ttu-id="f1af1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1af1-120">CommonParameters</span></span>
<span data-ttu-id="f1af1-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f1af1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1af1-122">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f1af1-122">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1af1-123">입력</span><span class="sxs-lookup"><span data-stu-id="f1af1-123">INPUTS</span></span>

### <span data-ttu-id="f1af1-124">System.String</span><span class="sxs-lookup"><span data-stu-id="f1af1-124">System.String</span></span>

### <span data-ttu-id="f1af1-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f1af1-125">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="f1af1-126">출력</span><span class="sxs-lookup"><span data-stu-id="f1af1-126">OUTPUTS</span></span>

### <span data-ttu-id="f1af1-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="f1af1-127">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

## <span data-ttu-id="f1af1-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f1af1-128">NOTES</span></span>

## <span data-ttu-id="f1af1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f1af1-129">RELATED LINKS</span></span>

<span data-ttu-id="f1af1-130">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [New-AzDelegation](./New-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="f1af1-130">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[New-AzDelegation](./New-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>