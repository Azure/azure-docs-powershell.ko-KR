---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbcassandracolumn
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBCassandraColumn.md
ms.openlocfilehash: 634a6a8e1e6b921703603ee7f2bfd345aa64608c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102010768"
---
# <span data-ttu-id="81176-101">New-AzCosmosDBCassandraColumn</span><span class="sxs-lookup"><span data-stu-id="81176-101">New-AzCosmosDBCassandraColumn</span></span>

## <span data-ttu-id="81176-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81176-102">SYNOPSIS</span></span>
<span data-ttu-id="81176-103">새 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81176-103">Creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="81176-104">구문</span><span class="sxs-lookup"><span data-stu-id="81176-104">SYNTAX</span></span>

```
New-AzCosmosDBCassandraColumn -Name <String> -Type <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="81176-105">설명</span><span class="sxs-lookup"><span data-stu-id="81176-105">DESCRIPTION</span></span>
<span data-ttu-id="81176-106">**New-AzCosmosDBCassandraColumn은** 새로운 CosmosDB Cassandra 열을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="81176-106">The **New-AzCosmosDBCassandraColumn** creates a new CosmosDB Cassandra Column.</span></span>

## <span data-ttu-id="81176-107">예제</span><span class="sxs-lookup"><span data-stu-id="81176-107">EXAMPLES</span></span>

### <span data-ttu-id="81176-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="81176-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBCassandraColumn -Name "name" -Type int

Name Type
---- ----
name int
```

## <span data-ttu-id="81176-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="81176-109">PARAMETERS</span></span>

### <span data-ttu-id="81176-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="81176-110">-DefaultProfile</span></span>
<span data-ttu-id="81176-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="81176-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="81176-112">-Name</span><span class="sxs-lookup"><span data-stu-id="81176-112">-Name</span></span>
<span data-ttu-id="81176-113">Cassandra 열의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="81176-113">Name of Cassandra Column.</span></span>

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

### <span data-ttu-id="81176-114">-Type</span><span class="sxs-lookup"><span data-stu-id="81176-114">-Type</span></span>
<span data-ttu-id="81176-115">Cassandra 열의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="81176-115">Type of Cassandra Column.</span></span>

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

### <span data-ttu-id="81176-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81176-116">CommonParameters</span></span>
<span data-ttu-id="81176-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="81176-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81176-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="81176-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81176-119">입력</span><span class="sxs-lookup"><span data-stu-id="81176-119">INPUTS</span></span>

### <span data-ttu-id="81176-120">없음</span><span class="sxs-lookup"><span data-stu-id="81176-120">None</span></span>

## <span data-ttu-id="81176-121">출력</span><span class="sxs-lookup"><span data-stu-id="81176-121">OUTPUTS</span></span>

### <span data-ttu-id="81176-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span><span class="sxs-lookup"><span data-stu-id="81176-122">Microsoft.Azure.Commands.CosmosDB.Models.PSColumn</span></span>

## <span data-ttu-id="81176-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="81176-123">NOTES</span></span>

## <span data-ttu-id="81176-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81176-124">RELATED LINKS</span></span>
