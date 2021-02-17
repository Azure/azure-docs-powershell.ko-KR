---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206773"
---
# <span data-ttu-id="3002c-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="3002c-101">New-AzDelegation</span></span>

## <span data-ttu-id="3002c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3002c-102">SYNOPSIS</span></span>
<span data-ttu-id="3002c-103">서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-103">Creates a service delegation.</span></span>

## <span data-ttu-id="3002c-104">구문</span><span class="sxs-lookup"><span data-stu-id="3002c-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="3002c-105">설명</span><span class="sxs-lookup"><span data-stu-id="3002c-105">DESCRIPTION</span></span>
<span data-ttu-id="3002c-106">**New-AzDelegation** cmdlet은 서브넷에 추가할 수 있는 서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="3002c-107">예제</span><span class="sxs-lookup"><span data-stu-id="3002c-107">EXAMPLES</span></span>

### <span data-ttu-id="3002c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="3002c-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="3002c-109">첫 번째 cmdlet은 서브넷에 추가할 수 있는 위임을 만들고 $delegation 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="3002c-110">두 번째 및 세 번째 cmdlet은 위임할 서브넷을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="3002c-111">네 번째 cmdlet은 만든 위임이 관심 있는 서브넷에 추가하고 최종 cmdlet은 업데이트된 구성을 서버에 전송합니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="3002c-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="3002c-112">PARAMETERS</span></span>

### <span data-ttu-id="3002c-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3002c-113">-DefaultProfile</span></span>
<span data-ttu-id="3002c-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3002c-115">-Name</span><span class="sxs-lookup"><span data-stu-id="3002c-115">-Name</span></span>
<span data-ttu-id="3002c-116">위임의 이름</span><span class="sxs-lookup"><span data-stu-id="3002c-116">The name of the delegation</span></span>

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

### <span data-ttu-id="3002c-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="3002c-117">-ServiceName</span></span>
<span data-ttu-id="3002c-118">서브넷을 위임해야 하는 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="3002c-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3002c-119">CommonParameters</span></span>
<span data-ttu-id="3002c-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3002c-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3002c-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="3002c-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3002c-122">입력</span><span class="sxs-lookup"><span data-stu-id="3002c-122">INPUTS</span></span>

### <span data-ttu-id="3002c-123">System.String</span><span class="sxs-lookup"><span data-stu-id="3002c-123">System.String</span></span>

## <span data-ttu-id="3002c-124">출력</span><span class="sxs-lookup"><span data-stu-id="3002c-124">OUTPUTS</span></span>

### <span data-ttu-id="3002c-125">Microsoft.Azure.Commands.Network.Models.PSD위임</span><span class="sxs-lookup"><span data-stu-id="3002c-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="3002c-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3002c-126">NOTES</span></span>

## <span data-ttu-id="3002c-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3002c-127">RELATED LINKS</span></span>

<span data-ttu-id="3002c-128">[Add-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [Remove-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="3002c-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>