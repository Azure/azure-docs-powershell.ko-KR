---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbmongodbindex
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBMongoDBIndex.md
ms.openlocfilehash: c88e1567a7784f89eadd112d7a985b1f2f286a40
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98346226"
---
# <span data-ttu-id="e51d2-101">New-AzCosmosDBMongoDBIndex</span><span class="sxs-lookup"><span data-stu-id="e51d2-101">New-AzCosmosDBMongoDBIndex</span></span>

## <span data-ttu-id="e51d2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e51d2-102">SYNOPSIS</span></span>
<span data-ttu-id="e51d2-103">새 CosmosDB MongoDB 인덱스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-103">Creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="e51d2-104">구문</span><span class="sxs-lookup"><span data-stu-id="e51d2-104">SYNTAX</span></span>

```
New-AzCosmosDBMongoDBIndex [-TtlInSeconds <Int32>] [-Unique <Boolean>] [-Key <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e51d2-105">설명</span><span class="sxs-lookup"><span data-stu-id="e51d2-105">DESCRIPTION</span></span>
<span data-ttu-id="e51d2-106">**New-AzCosmosDBMongoDBIndex는** 새 CosmosDB MongoDB 인덱스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-106">The **New-AzCosmosDBMongoDBIndex** creates a new CosmosDB MongoDB Index.</span></span>

## <span data-ttu-id="e51d2-107">예제</span><span class="sxs-lookup"><span data-stu-id="e51d2-107">EXAMPLES</span></span>

### <span data-ttu-id="e51d2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e51d2-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBMongoDBIndex -TtlInSeconds {val} -Unique 1 -Key "key1"
Key                                                       Options
---                                                       -------
Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexKeys Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndexOptions
```

## <span data-ttu-id="e51d2-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e51d2-109">PARAMETERS</span></span>

### <span data-ttu-id="e51d2-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e51d2-110">-DefaultProfile</span></span>
<span data-ttu-id="e51d2-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e51d2-112">-Key</span><span class="sxs-lookup"><span data-stu-id="e51d2-112">-Key</span></span>
<span data-ttu-id="e51d2-113">문자열로 사용할 키 값의 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-113">Array of key values as strings.</span></span>

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

### <span data-ttu-id="e51d2-114">-TtlInSeconds</span><span class="sxs-lookup"><span data-stu-id="e51d2-114">-TtlInSeconds</span></span>
<span data-ttu-id="e51d2-115">인덱스가 만료된 후의 시간(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-115">Number of seconds after which the index expires.</span></span>

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

### <span data-ttu-id="e51d2-116">-Unique</span><span class="sxs-lookup"><span data-stu-id="e51d2-116">-Unique</span></span>
<span data-ttu-id="e51d2-117">인덱스가 고유하거나 그렇지 않은지 나타내는 Bool입니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-117">Bool to indicate if the index is unique or not.</span></span>

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

### <span data-ttu-id="e51d2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e51d2-118">CommonParameters</span></span>
<span data-ttu-id="e51d2-119">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e51d2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e51d2-120">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e51d2-120">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e51d2-121">입력</span><span class="sxs-lookup"><span data-stu-id="e51d2-121">INPUTS</span></span>

### <span data-ttu-id="e51d2-122">없음</span><span class="sxs-lookup"><span data-stu-id="e51d2-122">None</span></span>

## <span data-ttu-id="e51d2-123">출력</span><span class="sxs-lookup"><span data-stu-id="e51d2-123">OUTPUTS</span></span>

### <span data-ttu-id="e51d2-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span><span class="sxs-lookup"><span data-stu-id="e51d2-124">Microsoft.Azure.Commands.CosmosDB.Models.PSMongoIndex</span></span>

## <span data-ttu-id="e51d2-125">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e51d2-125">NOTES</span></span>

## <span data-ttu-id="e51d2-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e51d2-126">RELATED LINKS</span></span>
