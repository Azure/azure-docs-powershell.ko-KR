---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbvirtualnetworkrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBVirtualNetworkRule.md
ms.openlocfilehash: d60284cec84c1b0a023f06a77acfe794d8d5315f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212379"
---
# <span data-ttu-id="34035-101">New-AzCosmosDBVirtualNetworkRule</span><span class="sxs-lookup"><span data-stu-id="34035-101">New-AzCosmosDBVirtualNetworkRule</span></span>

## <span data-ttu-id="34035-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34035-102">SYNOPSIS</span></span>
<span data-ttu-id="34035-103">PSVirtualNetworkRule (새 CosmosDB VirtualNetworkRule 개체)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34035-103">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="34035-104">구문과</span><span class="sxs-lookup"><span data-stu-id="34035-104">SYNTAX</span></span>

```
New-AzCosmosDBVirtualNetworkRule -Id <String> [-IgnoreMissingVNetServiceEndpoint <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34035-105">설명은</span><span class="sxs-lookup"><span data-stu-id="34035-105">DESCRIPTION</span></span>
<span data-ttu-id="34035-106">PSVirtualNetworkRule (새 CosmosDB VirtualNetworkRule 개체)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34035-106">Create a new CosmosDB VirtualNetworkRule Object(PSVirtualNetworkRule).</span></span>

## <span data-ttu-id="34035-107">예제의</span><span class="sxs-lookup"><span data-stu-id="34035-107">EXAMPLES</span></span>

### <span data-ttu-id="34035-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="34035-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBVirtualNetworkRule -Id {id} -IgnoreMissingVNetServiceEndpoint 0
Id  IgnoreMissingVNetServiceEndpoint
--   --------------------------------
{id}                            False
```

## <span data-ttu-id="34035-109">변수</span><span class="sxs-lookup"><span data-stu-id="34035-109">PARAMETERS</span></span>

### <span data-ttu-id="34035-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34035-110">-DefaultProfile</span></span>
<span data-ttu-id="34035-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34035-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34035-112">-Id</span><span class="sxs-lookup"><span data-stu-id="34035-112">-Id</span></span>
<span data-ttu-id="34035-113">서브넷의 리소스 ID (예:/subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName})</span><span class="sxs-lookup"><span data-stu-id="34035-113">Resource ID of a subnet, for example: /subscriptions/{subscriptionId}/resourceGroups/{groupName}/providers/Microsoft.Network/virtualNetworks/{virtualNetworkName}/subnets/{subnetName}</span></span>

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

### <span data-ttu-id="34035-114">-IgnoreMissingVNetServiceEndpoint</span><span class="sxs-lookup"><span data-stu-id="34035-114">-IgnoreMissingVNetServiceEndpoint</span></span>
<span data-ttu-id="34035-115">가상 네트워크에 vnet 서비스 끝점을 사용 하도록 설정 하기 전에 방화벽 규칙을 만들지 여부를 나타내는 부울입니다.</span><span class="sxs-lookup"><span data-stu-id="34035-115">Boolean to indicate if to create firewall rule before the virtual network has vnet service endpoint enabled.</span></span>

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

### <span data-ttu-id="34035-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34035-116">CommonParameters</span></span>
<span data-ttu-id="34035-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="34035-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34035-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="34035-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34035-119">입력</span><span class="sxs-lookup"><span data-stu-id="34035-119">INPUTS</span></span>

### <span data-ttu-id="34035-120">않아야</span><span class="sxs-lookup"><span data-stu-id="34035-120">None</span></span>

## <span data-ttu-id="34035-121">출력</span><span class="sxs-lookup"><span data-stu-id="34035-121">OUTPUTS</span></span>

### <span data-ttu-id="34035-122">CosmosDB. PSVirtualNetworkRule/.</span><span class="sxs-lookup"><span data-stu-id="34035-122">Microsoft.Azure.Commands.CosmosDB.Models.PSVirtualNetworkRule</span></span>

## <span data-ttu-id="34035-123">상속자</span><span class="sxs-lookup"><span data-stu-id="34035-123">NOTES</span></span>

## <span data-ttu-id="34035-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34035-124">RELATED LINKS</span></span>
