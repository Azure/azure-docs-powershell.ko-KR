---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100177297"
---
# <span data-ttu-id="f908c-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f908c-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="f908c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f908c-102">SYNOPSIS</span></span>
<span data-ttu-id="f908c-103">새 CosmosDB Cassandra Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f908c-104">구문</span><span class="sxs-lookup"><span data-stu-id="f908c-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f908c-105">설명</span><span class="sxs-lookup"><span data-stu-id="f908c-105">DESCRIPTION</span></span>
<span data-ttu-id="f908c-106">**New-AzCosmosDBCassandraSchema는** 새 CosmosDB Cassandra Schema를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="f908c-107">예제</span><span class="sxs-lookup"><span data-stu-id="f908c-107">EXAMPLES</span></span>

### <span data-ttu-id="f908c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f908c-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="f908c-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f908c-109">PARAMETERS</span></span>

### <span data-ttu-id="f908c-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="f908c-110">-ClusterKey</span></span>
<span data-ttu-id="f908c-111">PSClusterKey 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="f908c-112">-Column</span><span class="sxs-lookup"><span data-stu-id="f908c-112">-Column</span></span>
<span data-ttu-id="f908c-113">PSColumn 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-113">PSColumn object.</span></span>

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

### <span data-ttu-id="f908c-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f908c-114">-DefaultProfile</span></span>
<span data-ttu-id="f908c-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f908c-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="f908c-116">-PartitionKey</span></span>
<span data-ttu-id="f908c-117">파티션 키를 포함하는 문자열 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="f908c-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f908c-118">CommonParameters</span></span>
<span data-ttu-id="f908c-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f908c-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f908c-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f908c-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f908c-121">입력</span><span class="sxs-lookup"><span data-stu-id="f908c-121">INPUTS</span></span>

### <span data-ttu-id="f908c-122">없음</span><span class="sxs-lookup"><span data-stu-id="f908c-122">None</span></span>

## <span data-ttu-id="f908c-123">출력</span><span class="sxs-lookup"><span data-stu-id="f908c-123">OUTPUTS</span></span>

### <span data-ttu-id="f908c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="f908c-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="f908c-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f908c-125">NOTES</span></span>

## <span data-ttu-id="f908c-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f908c-126">RELATED LINKS</span></span>
