---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100181300"
---
# <span data-ttu-id="c73e0-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c73e0-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="c73e0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c73e0-102">SYNOPSIS</span></span>
<span data-ttu-id="c73e0-103">새 CosmosDB VirtualNetworkRule 개체(PSVirtualNetworkRule)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c73e0-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="c73e0-104">구문</span><span class="sxs-lookup"><span data-stu-id="c73e0-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c73e0-105">설명</span><span class="sxs-lookup"><span data-stu-id="c73e0-105">DESCRIPTION</span></span>
<span data-ttu-id="c73e0-106">새 CosmosDB VirtualNetworkRule 개체(PSVirtualNetworkRule)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c73e0-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="c73e0-107">예제</span><span class="sxs-lookup"><span data-stu-id="c73e0-107">EXAMPLES</span></span>

### <span data-ttu-id="c73e0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c73e0-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="c73e0-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c73e0-109">PARAMETERS</span></span>

### <span data-ttu-id="c73e0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c73e0-110">-DefaultProfile</span></span>
<span data-ttu-id="c73e0-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c73e0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73e0-112">-Id</span><span class="sxs-lookup"><span data-stu-id="c73e0-112">-Id</span></span>
<span data-ttu-id="c73e0-113">서브넷의 리소스 ID(예: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span><span class="sxs-lookup"><span data-stu-id="c73e0-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="c73e0-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="c73e0-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="c73e0-115">가상 네트워크에 vnet 서비스 엔드포인트를 사용하도록 설정하기 전에 방화벽 규칙을 만들지 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="c73e0-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c73e0-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c73e0-116">CommonParameters</span></span>
<span data-ttu-id="c73e0-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c73e0-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c73e0-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c73e0-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c73e0-119">입력</span><span class="sxs-lookup"><span data-stu-id="c73e0-119">INPUTS</span></span>

### <span data-ttu-id="c73e0-120">없음</span><span class="sxs-lookup"><span data-stu-id="c73e0-120">None</span></span>

## <span data-ttu-id="c73e0-121">출력</span><span class="sxs-lookup"><span data-stu-id="c73e0-121">OUTPUTS</span></span>

### <span data-ttu-id="c73e0-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="c73e0-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="c73e0-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c73e0-123">NOTES</span></span>

## <span data-ttu-id="c73e0-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c73e0-124">RELATED LINKS</span></span>
