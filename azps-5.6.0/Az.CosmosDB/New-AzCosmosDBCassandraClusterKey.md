---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: 9afcffc281c48e0235c814b352e65ae47e5f4337
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102009744"
---
# <span data-ttu-id="5b1da-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="5b1da-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="5b1da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5b1da-102">SYNOPSIS</span></span>
<span data-ttu-id="5b1da-103">새 CosmosDB Cassandra 클러스터 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b1da-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="5b1da-104">구문</span><span class="sxs-lookup"><span data-stu-id="5b1da-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5b1da-105">설명</span><span class="sxs-lookup"><span data-stu-id="5b1da-105">DESCRIPTION</span></span>
<span data-ttu-id="5b1da-106">**New-AzCosmosDBCassandraClusterKey는** 새 CosmosDB Cassandra 클러스터 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5b1da-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="5b1da-107">예제</span><span class="sxs-lookup"><span data-stu-id="5b1da-107">EXAMPLES</span></span>

### <span data-ttu-id="5b1da-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5b1da-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="5b1da-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="5b1da-109">PARAMETERS</span></span>

### <span data-ttu-id="5b1da-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5b1da-110">-DefaultProfile</span></span>
<span data-ttu-id="5b1da-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5b1da-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5b1da-112">-Name</span><span class="sxs-lookup"><span data-stu-id="5b1da-112">-Name</span></span>
<span data-ttu-id="5b1da-113">Cassandra 클러스터 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5b1da-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="5b1da-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="5b1da-114">-OrderBy</span></span>
<span data-ttu-id="5b1da-115">Cassandra 클러스터 키의 순서.</span><span class="sxs-lookup"><span data-stu-id="5b1da-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="5b1da-116">가능한 값은 다음과 같습니다. 'Asc', 'Desc'</span><span class="sxs-lookup"><span data-stu-id="5b1da-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="5b1da-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5b1da-117">CommonParameters</span></span>
<span data-ttu-id="5b1da-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5b1da-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5b1da-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="5b1da-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5b1da-120">입력</span><span class="sxs-lookup"><span data-stu-id="5b1da-120">INPUTS</span></span>

### <span data-ttu-id="5b1da-121">없음</span><span class="sxs-lookup"><span data-stu-id="5b1da-121">None</span></span>

## <span data-ttu-id="5b1da-122">출력</span><span class="sxs-lookup"><span data-stu-id="5b1da-122">OUTPUTS</span></span>

### <span data-ttu-id="5b1da-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="5b1da-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="5b1da-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5b1da-124">NOTES</span></span>

## <span data-ttu-id="5b1da-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5b1da-125">RELATED LINKS</span></span>
