---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDelegation.md
ms.openlocfilehash: 05ed0d27dc1d004c2d9a1c5221795af708b812d7
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044755"
---
# <span data-ttu-id="fb13b-101">New-AzDelegation</span><span class="sxs-lookup"><span data-stu-id="fb13b-101">New-AzDelegation</span></span>

## <span data-ttu-id="fb13b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb13b-102">SYNOPSIS</span></span>
<span data-ttu-id="fb13b-103">서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-103">Creates a service delegation.</span></span>

## <span data-ttu-id="fb13b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb13b-104">SYNTAX</span></span>

```
New-AzDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="fb13b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="fb13b-105">DESCRIPTION</span></span>
<span data-ttu-id="fb13b-106">**새 AzDelegation** cmdlet은 서브넷에 추가할 수 있는 서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-106">The **New-AzDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="fb13b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="fb13b-107">EXAMPLES</span></span>

### <span data-ttu-id="fb13b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb13b-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzVirtualNetwork $vnet
```

<span data-ttu-id="fb13b-109">첫 번째 cmdlet은 서브넷에 추가 하 여 $delegation 변수에 저장할 수 있는 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="fb13b-110">두 번째와 세 번째 cmdlet은 위임할 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="fb13b-111">네 번째 cmdlet은 만들어진 위임을 해당 서브넷에 추가 하 고, 최종 cmdlet은 업데이트 된 구성을 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="fb13b-112">변수</span><span class="sxs-lookup"><span data-stu-id="fb13b-112">PARAMETERS</span></span>

### <span data-ttu-id="fb13b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb13b-113">-DefaultProfile</span></span>
<span data-ttu-id="fb13b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fb13b-115">-이름</span><span class="sxs-lookup"><span data-stu-id="fb13b-115">-Name</span></span>
<span data-ttu-id="fb13b-116">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-116">The name of the delegation</span></span>

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

### <span data-ttu-id="fb13b-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="fb13b-117">-ServiceName</span></span>
<span data-ttu-id="fb13b-118">서브넷을 위임할 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-118">The name of the service to which the subnet should be delegated</span></span>

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

### <span data-ttu-id="fb13b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb13b-119">CommonParameters</span></span>
<span data-ttu-id="fb13b-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb13b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb13b-121">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb13b-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb13b-122">입력</span><span class="sxs-lookup"><span data-stu-id="fb13b-122">INPUTS</span></span>

### <span data-ttu-id="fb13b-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="fb13b-123">System.String</span></span>

## <span data-ttu-id="fb13b-124">출력</span><span class="sxs-lookup"><span data-stu-id="fb13b-124">OUTPUTS</span></span>

### <span data-ttu-id="fb13b-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="fb13b-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="fb13b-126">상속자</span><span class="sxs-lookup"><span data-stu-id="fb13b-126">NOTES</span></span>

## <span data-ttu-id="fb13b-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb13b-127">RELATED LINKS</span></span>

<span data-ttu-id="fb13b-128">[추가-AzDelegation](./Add-AzDelegation.md) 
 [Get-AzDelegation](./Get-AzDelegation.md) 
 [제거-AzDelegation](./Remove-AzDelegation.md) 
 [Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md) 
 [Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md) 
 [Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="fb13b-128">[Add-AzDelegation](./Add-AzDelegation.md)
[Get-AzDelegation](./Get-AzDelegation.md)
[Remove-AzDelegation](./Remove-AzDelegation.md)
[Get-AzVirtualNetwork](./Get-AzVirtualNetwork.md)
[Get-AzVirtualNetworkSubnetConfig](./Get-AzVirtualNetworkSubnetConfig.md)
[Set-AzVirtualNetwork](./Set-AzVirtualNetwork.md)</span></span>