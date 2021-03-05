---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 3a19e0c60b5a32e1d1083b1afba55a8bf3045fe9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101983611"
---
# <span data-ttu-id="79bbe-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="79bbe-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="79bbe-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79bbe-102">SYNOPSIS</span></span>
<span data-ttu-id="79bbe-103">새 CosmosDB Cassandra Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="79bbe-104">구문</span><span class="sxs-lookup"><span data-stu-id="79bbe-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="79bbe-105">설명</span><span class="sxs-lookup"><span data-stu-id="79bbe-105">DESCRIPTION</span></span>
<span data-ttu-id="79bbe-106">**New-AzCosmosDBCassandraSchema는** 새로운 CosmosDB Cassandra Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="79bbe-107">예제</span><span class="sxs-lookup"><span data-stu-id="79bbe-107">EXAMPLES</span></span>

### <span data-ttu-id="79bbe-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79bbe-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="79bbe-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="79bbe-109">PARAMETERS</span></span>

### <span data-ttu-id="79bbe-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="79bbe-110">-ClusterKey</span></span>
<span data-ttu-id="79bbe-111">PSClusterKey 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-111">Array of PSClusterKey objects.</span></span>

```yaml
Type: PSClusterKey[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bbe-112">-Column</span><span class="sxs-lookup"><span data-stu-id="79bbe-112">-Column</span></span>
<span data-ttu-id="79bbe-113">PSColumn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-113">PSColumn object.</span></span>

```yaml
Type: PSColumn[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bbe-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79bbe-114">-DefaultProfile</span></span>
<span data-ttu-id="79bbe-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79bbe-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="79bbe-116">-PartitionKey</span></span>
<span data-ttu-id="79bbe-117">파티션 키를 포함하는 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-117">Array of strings containing Partition Keys.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79bbe-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79bbe-118">CommonParameters</span></span>
<span data-ttu-id="79bbe-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="79bbe-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79bbe-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="79bbe-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79bbe-121">입력</span><span class="sxs-lookup"><span data-stu-id="79bbe-121">INPUTS</span></span>

### <span data-ttu-id="79bbe-122">없음</span><span class="sxs-lookup"><span data-stu-id="79bbe-122">None</span></span>

## <span data-ttu-id="79bbe-123">출력</span><span class="sxs-lookup"><span data-stu-id="79bbe-123">OUTPUTS</span></span>

### <span data-ttu-id="79bbe-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="79bbe-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="79bbe-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="79bbe-125">NOTES</span></span>

## <span data-ttu-id="79bbe-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79bbe-126">RELATED LINKS</span></span>
