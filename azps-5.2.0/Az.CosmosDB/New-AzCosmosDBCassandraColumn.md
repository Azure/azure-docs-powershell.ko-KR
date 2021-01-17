---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 31563c11a1df418d0f53c1eeb80e8bc02691188c
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98332318"
---
# <span data-ttu-id="2a11d-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="2a11d-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="2a11d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2a11d-102">SYNOPSIS</span></span>
<span data-ttu-id="2a11d-103">새 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="2a11d-104">구문</span><span class="sxs-lookup"><span data-stu-id="2a11d-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2a11d-105">설명</span><span class="sxs-lookup"><span data-stu-id="2a11d-105">DESCRIPTION</span></span>
<span data-ttu-id="2a11d-106">**New-AzCosmosDBCassandraColumn은** 새 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="2a11d-107">예제</span><span class="sxs-lookup"><span data-stu-id="2a11d-107">EXAMPLES</span></span>

### <span data-ttu-id="2a11d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="2a11d-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="2a11d-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2a11d-109">PARAMETERS</span></span>

### <span data-ttu-id="2a11d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2a11d-110">-DefaultProfile</span></span>
<span data-ttu-id="2a11d-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2a11d-112">-Name</span><span class="sxs-lookup"><span data-stu-id="2a11d-112">-Name</span></span>
<span data-ttu-id="2a11d-113">Cassandra 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="2a11d-114">-Type</span><span class="sxs-lookup"><span data-stu-id="2a11d-114">-Type</span></span>
<span data-ttu-id="2a11d-115">Cassandra 열의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="2a11d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2a11d-116">CommonParameters</span></span>
<span data-ttu-id="2a11d-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2a11d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2a11d-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2a11d-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2a11d-119">입력</span><span class="sxs-lookup"><span data-stu-id="2a11d-119">INPUTS</span></span>

### <span data-ttu-id="2a11d-120">없음</span><span class="sxs-lookup"><span data-stu-id="2a11d-120">None</span></span>

## <span data-ttu-id="2a11d-121">출력</span><span class="sxs-lookup"><span data-stu-id="2a11d-121">OUTPUTS</span></span>

### <span data-ttu-id="2a11d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="2a11d-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="2a11d-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2a11d-123">NOTES</span></span>

## <span data-ttu-id="2a11d-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2a11d-124">RELATED LINKS</span></span>
