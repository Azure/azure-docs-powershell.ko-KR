---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: a086705465aea30480a4f41f6981a47d8fcc612c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101991447"
---
# <span data-ttu-id="14ffd-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="14ffd-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="14ffd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14ffd-102">SYNOPSIS</span></span>
<span data-ttu-id="14ffd-103">새 CosmosDB MongoDB 인덱스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="14ffd-104">구문</span><span class="sxs-lookup"><span data-stu-id="14ffd-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="14ffd-105">설명</span><span class="sxs-lookup"><span data-stu-id="14ffd-105">DESCRIPTION</span></span>
<span data-ttu-id="14ffd-106">**New-AzCosmosDBMongoDBIndex는** 새로운 CosmosDB MongoDB 인덱스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="14ffd-107">예제</span><span class="sxs-lookup"><span data-stu-id="14ffd-107">EXAMPLES</span></span>

### <span data-ttu-id="14ffd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="14ffd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="14ffd-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="14ffd-109">PARAMETERS</span></span>

### <span data-ttu-id="14ffd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14ffd-110">-DefaultProfile</span></span>
<span data-ttu-id="14ffd-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="14ffd-112">-Key</span><span class="sxs-lookup"><span data-stu-id="14ffd-112">-Key</span></span>
<span data-ttu-id="14ffd-113">문자열로 키 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="14ffd-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="14ffd-114">-TtlInSeconds</span></span>
<span data-ttu-id="14ffd-115">인덱스가 만료된 후의 초 수입니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-115">Number of seconds after which the index expires.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="14ffd-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="14ffd-116">-Unique</span></span>
<span data-ttu-id="14ffd-117">인덱스가 고유하거나 아닌지 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="14ffd-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14ffd-118">CommonParameters</span></span>
<span data-ttu-id="14ffd-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="14ffd-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14ffd-120">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="14ffd-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14ffd-121">입력</span><span class="sxs-lookup"><span data-stu-id="14ffd-121">INPUTS</span></span>

### <span data-ttu-id="14ffd-122">없음</span><span class="sxs-lookup"><span data-stu-id="14ffd-122">None</span></span>

## <span data-ttu-id="14ffd-123">출력</span><span class="sxs-lookup"><span data-stu-id="14ffd-123">OUTPUTS</span></span>

### <span data-ttu-id="14ffd-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="14ffd-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="14ffd-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="14ffd-125">NOTES</span></span>

## <span data-ttu-id="14ffd-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="14ffd-126">RELATED LINKS</span></span>
