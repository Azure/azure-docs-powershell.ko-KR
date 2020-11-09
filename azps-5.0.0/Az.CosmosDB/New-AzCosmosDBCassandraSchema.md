---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraschema
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraSchema.md
ms.openlocfilehash: 997f9e0751eb616fdc9e64f73d66b3f15b7ed756
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307127"
---
# <span data-ttu-id="6c510-101">New-AzCosmosDBCassandraSchema</span><span class="sxs-lookup"><span data-stu-id="6c510-101">New-AzCosmosDBCassandraSchema</span></span>

## <span data-ttu-id="6c510-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c510-102">SYNOPSIS</span></span>
<span data-ttu-id="6c510-103">새 CosmosDB Cassandra 스키마를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-103">Creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="6c510-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6c510-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraSchema [-Column <PSColumn[]>] [-PartitionKey <String[]>] [-ClusterKey <PSClusterKey[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c510-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6c510-105">DESCRIPTION</span></span>
<span data-ttu-id="6c510-106">**AzCosmosDBCassandraSchema** 는 새 CosmosDB Cassandra 스키마를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-106">The **New-AzCosmosDBCassandraSchema** creates a new CosmosDB Cassandra Schema.</span></span>

## <span data-ttu-id="6c510-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6c510-107">EXAMPLES</span></span>

### <span data-ttu-id="6c510-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6c510-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraSchema -Column {PSColumn[]} -PartitionKey <String[]> -ClusterKey {PSClusterKey[]}

Columns PartitionKeys ClusterKeys
------- ------------- -----------
{column1}     {a}     {clusterkey1}
```

## <span data-ttu-id="6c510-109">변수</span><span class="sxs-lookup"><span data-stu-id="6c510-109">PARAMETERS</span></span>

### <span data-ttu-id="6c510-110">-ClusterKey</span><span class="sxs-lookup"><span data-stu-id="6c510-110">-ClusterKey</span></span>
<span data-ttu-id="6c510-111">PSClusterKey 개체의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-111">Array of PSClusterKey objects.</span></span>

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

### <span data-ttu-id="6c510-112">-열</span><span class="sxs-lookup"><span data-stu-id="6c510-112">-Column</span></span>
<span data-ttu-id="6c510-113">PSColumn 개체</span><span class="sxs-lookup"><span data-stu-id="6c510-113">PSColumn object.</span></span>

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

### <span data-ttu-id="6c510-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c510-114">-DefaultProfile</span></span>
<span data-ttu-id="6c510-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6c510-116">-PartitionKey</span><span class="sxs-lookup"><span data-stu-id="6c510-116">-PartitionKey</span></span>
<span data-ttu-id="6c510-117">파티션 키를 포함 하는 문자열의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-117">Array of strings containing Partition Keys.</span></span>

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

### <span data-ttu-id="6c510-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c510-118">CommonParameters</span></span>
<span data-ttu-id="6c510-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6c510-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c510-120">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6c510-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c510-121">입력</span><span class="sxs-lookup"><span data-stu-id="6c510-121">INPUTS</span></span>

### <span data-ttu-id="6c510-122">않아야</span><span class="sxs-lookup"><span data-stu-id="6c510-122">None</span></span>

## <span data-ttu-id="6c510-123">출력</span><span class="sxs-lookup"><span data-stu-id="6c510-123">OUTPUTS</span></span>

### <span data-ttu-id="6c510-124">CosmosDB. PSCassandraSchema/.</span><span class="sxs-lookup"><span data-stu-id="6c510-124">Microsoft.Azure.Commands.CosmosDB.Models.PSCassandraSchema</span></span>

## <span data-ttu-id="6c510-125">상속자</span><span class="sxs-lookup"><span data-stu-id="6c510-125">NOTES</span></span>

## <span data-ttu-id="6c510-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6c510-126">RELATED LINKS</span></span>
