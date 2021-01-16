---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98347138"
---
# <span data-ttu-id="770c4-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="770c4-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="770c4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="770c4-102">SYNOPSIS</span></span>
<span data-ttu-id="770c4-103">새 CosmosDB Cassandra 클러스터 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="770c4-104">구문</span><span class="sxs-lookup"><span data-stu-id="770c4-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="770c4-105">설명</span><span class="sxs-lookup"><span data-stu-id="770c4-105">DESCRIPTION</span></span>
<span data-ttu-id="770c4-106">**New-AzCosmosDBCassandraClusterKey는** 새 CosmosDB Cassandra 클러스터 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="770c4-107">예제</span><span class="sxs-lookup"><span data-stu-id="770c4-107">EXAMPLES</span></span>

### <span data-ttu-id="770c4-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="770c4-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="770c4-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="770c4-109">PARAMETERS</span></span>

### <span data-ttu-id="770c4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="770c4-110">-DefaultProfile</span></span>
<span data-ttu-id="770c4-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="770c4-112">-Name</span><span class="sxs-lookup"><span data-stu-id="770c4-112">-Name</span></span>
<span data-ttu-id="770c4-113">Cassandra 클러스터 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="770c4-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="770c4-114">-OrderBy</span></span>
<span data-ttu-id="770c4-115">Cassandra 클러스터 키의 순서입니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="770c4-116">가능한 값은 'Asc', 'Desc'입니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="770c4-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="770c4-117">CommonParameters</span></span>
<span data-ttu-id="770c4-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="770c4-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="770c4-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="770c4-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="770c4-120">입력</span><span class="sxs-lookup"><span data-stu-id="770c4-120">INPUTS</span></span>

### <span data-ttu-id="770c4-121">없음</span><span class="sxs-lookup"><span data-stu-id="770c4-121">None</span></span>

## <span data-ttu-id="770c4-122">출력</span><span class="sxs-lookup"><span data-stu-id="770c4-122">OUTPUTS</span></span>

### <span data-ttu-id="770c4-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="770c4-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="770c4-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="770c4-124">NOTES</span></span>

## <span data-ttu-id="770c4-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="770c4-125">RELATED LINKS</span></span>
