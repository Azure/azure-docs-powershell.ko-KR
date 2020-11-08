---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042090"
---
# <span data-ttu-id="7304b-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="7304b-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="7304b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7304b-102">SYNOPSIS</span></span>
<span data-ttu-id="7304b-103">새 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="7304b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7304b-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7304b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7304b-105">DESCRIPTION</span></span>
<span data-ttu-id="7304b-106">**AzCosmosDBCassandraColumn** 는 새 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="7304b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7304b-107">EXAMPLES</span></span>

### <span data-ttu-id="7304b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7304b-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="7304b-109">변수</span><span class="sxs-lookup"><span data-stu-id="7304b-109">PARAMETERS</span></span>

### <span data-ttu-id="7304b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7304b-110">-DefaultProfile</span></span>
<span data-ttu-id="7304b-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7304b-112">-이름</span><span class="sxs-lookup"><span data-stu-id="7304b-112">-Name</span></span>
<span data-ttu-id="7304b-113">Cassandra 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="7304b-114">-Type</span><span class="sxs-lookup"><span data-stu-id="7304b-114">-Type</span></span>
<span data-ttu-id="7304b-115">Cassandra 열의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="7304b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7304b-116">CommonParameters</span></span>
<span data-ttu-id="7304b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7304b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7304b-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="7304b-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7304b-119">입력</span><span class="sxs-lookup"><span data-stu-id="7304b-119">INPUTS</span></span>

### <span data-ttu-id="7304b-120">않아야</span><span class="sxs-lookup"><span data-stu-id="7304b-120">None</span></span>

## <span data-ttu-id="7304b-121">출력</span><span class="sxs-lookup"><span data-stu-id="7304b-121">OUTPUTS</span></span>

### <span data-ttu-id="7304b-122">CosmosDB 열에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="7304b-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="7304b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="7304b-123">NOTES</span></span>

## <span data-ttu-id="7304b-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7304b-124">RELATED LINKS</span></span>