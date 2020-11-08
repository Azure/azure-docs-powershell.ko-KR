---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandraclusterkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraClusterKey.md
ms.openlocfilehash: f58ba883cd724137d45632cabd293f0c7cdbefbd
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056473"
---
# <span data-ttu-id="96672-101">New-AzCosmosDBCassandraClusterKey</span><span class="sxs-lookup"><span data-stu-id="96672-101">New-AzCosmosDBCassandraClusterKey</span></span>

## <span data-ttu-id="96672-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96672-102">SYNOPSIS</span></span>
<span data-ttu-id="96672-103">새 CosmosDB Cassandra Cluster 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96672-103">Creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="96672-104">구문과</span><span class="sxs-lookup"><span data-stu-id="96672-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="96672-105">설명은</span><span class="sxs-lookup"><span data-stu-id="96672-105">DESCRIPTION</span></span>
<span data-ttu-id="96672-106">**AzCosmosDBCassandraClusterKey** 는 새 CosmosDB Cassandra Cluster 키를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96672-106">The **New-AzCosmosDBCassandraClusterKey** creates a new CosmosDB Cassandra Cluster Key.</span></span>

## <span data-ttu-id="96672-107">예제의</span><span class="sxs-lookup"><span data-stu-id="96672-107">EXAMPLES</span></span>

### <span data-ttu-id="96672-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="96672-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraClusterKey -Name <String> -OrderBy <String>

Name   OrderBy
----   -------
{name}  Asc
```

## <span data-ttu-id="96672-109">변수</span><span class="sxs-lookup"><span data-stu-id="96672-109">PARAMETERS</span></span>

### <span data-ttu-id="96672-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96672-110">-DefaultProfile</span></span>
<span data-ttu-id="96672-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="96672-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="96672-112">-이름</span><span class="sxs-lookup"><span data-stu-id="96672-112">-Name</span></span>
<span data-ttu-id="96672-113">Cassandra 클러스터 키의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96672-113">Name of Cassandra Cluster Key.</span></span>

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

### <span data-ttu-id="96672-114">-OrderBy</span><span class="sxs-lookup"><span data-stu-id="96672-114">-OrderBy</span></span>
<span data-ttu-id="96672-115">Cassandra 클러스터 키의 순서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="96672-115">Ordering of Cassandra Cluster key.</span></span>
<span data-ttu-id="96672-116">사용할 수 있는 값은 다음과 같습니다. ' Asc ', ' Desc '</span><span class="sxs-lookup"><span data-stu-id="96672-116">Possible values include: 'Asc', 'Desc'</span></span>

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

### <span data-ttu-id="96672-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96672-117">CommonParameters</span></span>
<span data-ttu-id="96672-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="96672-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96672-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="96672-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96672-120">입력</span><span class="sxs-lookup"><span data-stu-id="96672-120">INPUTS</span></span>

### <span data-ttu-id="96672-121">않아야</span><span class="sxs-lookup"><span data-stu-id="96672-121">None</span></span>

## <span data-ttu-id="96672-122">출력</span><span class="sxs-lookup"><span data-stu-id="96672-122">OUTPUTS</span></span>

### <span data-ttu-id="96672-123">CosmosDB를. PSClusterKey</span><span class="sxs-lookup"><span data-stu-id="96672-123">Microsoft.Azure.Commands.CosmosDB.Models.PSClusterKey</span></span>

## <span data-ttu-id="96672-124">상속자</span><span class="sxs-lookup"><span data-stu-id="96672-124">NOTES</span></span>

## <span data-ttu-id="96672-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96672-125">RELATED LINKS</span></span>
