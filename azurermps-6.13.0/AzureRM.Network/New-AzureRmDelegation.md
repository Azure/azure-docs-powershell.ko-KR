---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermdelegation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmDelegation.md
ms.openlocfilehash: 9912d41cd9e2600c55d378fbb88510a0defaaa85
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532424"
---
# <span data-ttu-id="5dc1f-101">New-AzureRmDelegation</span><span class="sxs-lookup"><span data-stu-id="5dc1f-101">New-AzureRmDelegation</span></span>

## <span data-ttu-id="5dc1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dc1f-102">SYNOPSIS</span></span>
<span data-ttu-id="5dc1f-103">서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-103">Creates a service delegation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dc1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dc1f-104">SYNTAX</span></span>

```
New-AzureRmDelegation -Name <String> -ServiceName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5dc1f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5dc1f-105">DESCRIPTION</span></span>
<span data-ttu-id="5dc1f-106">**새 AzureRmDelegation** cmdlet은 서브넷에 추가할 수 있는 서비스 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-106">The **New-AzureRmDelegation** cmdlet creates a service delegation that can be added to a subnet.</span></span>

## <span data-ttu-id="5dc1f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5dc1f-107">EXAMPLES</span></span>

### <span data-ttu-id="5dc1f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5dc1f-108">Example 1</span></span>
```powershell
PS C:\> $delegation = New-AzureRmDelegation -Name "myDelegation" -ServiceName "Microsoft.Sql/servers"
PS C:\> $vnet = Get-AzureRmVirtualNetwork -Name "myVNet" -ResourceGroupName "myResourceGroup"
PS C:\> $subnet = Get-AzureRmVirtualNetworkSubnetConfig -Name "mySubnet" -VirtualNetwork $vnet
PS C:\> $subnet.Delegations.Add($delegation)
PS C:\> Set-AzureRmVirtualNetwork $vnet
```

<span data-ttu-id="5dc1f-109">첫 번째 cmdlet은 서브넷에 추가 하 여 $delegation 변수에 저장할 수 있는 위임을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-109">The first cmdlet creates a delegation that can be added to a subnet, and stores it in the $delegation variable.</span></span> <span data-ttu-id="5dc1f-110">두 번째와 세 번째 cmdlet은 위임할 서브넷을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-110">The second and third cmdlets retrieve the subnet to be delegated.</span></span> <span data-ttu-id="5dc1f-111">네 번째 cmdlet은 만들어진 위임을 해당 서브넷에 추가 하 고, 최종 cmdlet은 업데이트 된 구성을 서버로 보냅니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-111">The fourth cmdlet adds the created delegation to the subnet of interest, and the final cmdlet sends the updated configuration to the server.</span></span>

## <span data-ttu-id="5dc1f-112">변수</span><span class="sxs-lookup"><span data-stu-id="5dc1f-112">PARAMETERS</span></span>

### <span data-ttu-id="5dc1f-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dc1f-113">-DefaultProfile</span></span>
<span data-ttu-id="5dc1f-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5dc1f-115">-이름</span><span class="sxs-lookup"><span data-stu-id="5dc1f-115">-Name</span></span>
<span data-ttu-id="5dc1f-116">위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-116">The name of the delegation</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dc1f-117">-ServiceName</span><span class="sxs-lookup"><span data-stu-id="5dc1f-117">-ServiceName</span></span>
<span data-ttu-id="5dc1f-118">서브넷을 위임할 서비스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-118">The name of the service to which the subnet should be delegated</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dc1f-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dc1f-119">CommonParameters</span></span>
<span data-ttu-id="5dc1f-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dc1f-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="5dc1f-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dc1f-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dc1f-122">입력</span><span class="sxs-lookup"><span data-stu-id="5dc1f-122">INPUTS</span></span>

### <span data-ttu-id="5dc1f-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5dc1f-123">System.String</span></span>

## <span data-ttu-id="5dc1f-124">출력</span><span class="sxs-lookup"><span data-stu-id="5dc1f-124">OUTPUTS</span></span>

### <span data-ttu-id="5dc1f-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span><span class="sxs-lookup"><span data-stu-id="5dc1f-125">Microsoft.Azure.Commands.Network.Models.PSDelegation</span></span>

## <span data-ttu-id="5dc1f-126">상속자</span><span class="sxs-lookup"><span data-stu-id="5dc1f-126">NOTES</span></span>

## <span data-ttu-id="5dc1f-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dc1f-127">RELATED LINKS</span></span>
<span data-ttu-id="5dc1f-128">[추가-AzureRmDelegation](./Add-AzureRmDelegation.md) 
 [Get-AzureRmDelegation](./Get-AzureRmDelegation.md) 
 [제거-AzureRmDelegation](./Remove-AzureRmDelegation.md) 
 [Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md) 
 [Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md) 
 [Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span><span class="sxs-lookup"><span data-stu-id="5dc1f-128">[Add-AzureRmDelegation](./Add-AzureRmDelegation.md)
[Get-AzureRmDelegation](./Get-AzureRmDelegation.md)
[Remove-AzureRmDelegation](./Remove-AzureRmDelegation.md)
[Get-AzureRmVirtualNetwork](./Get-AzureRmVirtualNetwork.md)
[Get-AzureRmVirtualNetworkSubnetConfig](./Get-AzureRmVirtualNetworkSubnetConfig.md)
[Set-AzureRmVirtualNetwork](./Set-AzureRmVirtualNetwork.md)</span></span>
