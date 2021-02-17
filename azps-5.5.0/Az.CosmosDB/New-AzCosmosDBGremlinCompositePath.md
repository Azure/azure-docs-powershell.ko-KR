---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlincompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinCompositePath.md
ms.openlocfilehash: 612f4623c7944c3c3d930ece44d4c2ae938e1a68
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196844"
---
# <span data-ttu-id="50d99-101">New-AzCosmosDBGremlinCompositePath</span><span class="sxs-lookup"><span data-stu-id="50d99-101">New-AzCosmosDBGremlinCompositePath</span></span>

## <span data-ttu-id="50d99-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50d99-102">SYNOPSIS</span></span>
<span data-ttu-id="50d99-103">PSCompositePath 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="50d99-104">Set-AzCosmosDBGremlinGraph에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="50d99-105">구문</span><span class="sxs-lookup"><span data-stu-id="50d99-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinCompositePath [-Path <String>] [-Order <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="50d99-106">설명</span><span class="sxs-lookup"><span data-stu-id="50d99-106">DESCRIPTION</span></span>
<span data-ttu-id="50d99-107">Gremlin API의 CompositePath에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-107">Object corresponding to Gremlin API's CompositePath.</span></span>

## <span data-ttu-id="50d99-108">예제</span><span class="sxs-lookup"><span data-stu-id="50d99-108">EXAMPLES</span></span>

### <span data-ttu-id="50d99-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="50d99-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="50d99-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="50d99-110">PARAMETERS</span></span>

### <span data-ttu-id="50d99-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50d99-111">-DefaultProfile</span></span>
<span data-ttu-id="50d99-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="50d99-113">-Order</span><span class="sxs-lookup"><span data-stu-id="50d99-113">-Order</span></span>
<span data-ttu-id="50d99-114">복합 경로에 대한 정렬 순서를 얻거나 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="50d99-115">가능한 값은 '오차', '내선'입니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-115">Possible values include: 'Ascending', 'Descending'</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d99-116">-Path</span><span class="sxs-lookup"><span data-stu-id="50d99-116">-Path</span></span>
<span data-ttu-id="50d99-117">인덱싱 동작이 적용되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="50d99-118">인덱스 경로는 일반적으로 루트로 시작하고 와일드카드(/path/\*)로 끝날 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="50d99-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50d99-119">CommonParameters</span></span>
<span data-ttu-id="50d99-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="50d99-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50d99-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="50d99-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50d99-122">입력</span><span class="sxs-lookup"><span data-stu-id="50d99-122">INPUTS</span></span>

### <span data-ttu-id="50d99-123">없음</span><span class="sxs-lookup"><span data-stu-id="50d99-123">None</span></span>

## <span data-ttu-id="50d99-124">출력</span><span class="sxs-lookup"><span data-stu-id="50d99-124">OUTPUTS</span></span>

### <span data-ttu-id="50d99-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span><span class="sxs-lookup"><span data-stu-id="50d99-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="50d99-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="50d99-126">NOTES</span></span>

## <span data-ttu-id="50d99-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="50d99-127">RELATED LINKS</span></span>
