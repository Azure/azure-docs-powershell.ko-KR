---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348945"
---
# <span data-ttu-id="a4971-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a4971-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="a4971-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4971-102">SYNOPSIS</span></span>
<span data-ttu-id="a4971-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4971-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="a4971-104">구문</span><span class="sxs-lookup"><span data-stu-id="a4971-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a4971-105">설명</span><span class="sxs-lookup"><span data-stu-id="a4971-105">DESCRIPTION</span></span>
<span data-ttu-id="a4971-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet은 PSUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a4971-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="a4971-107">예제</span><span class="sxs-lookup"><span data-stu-id="a4971-107">EXAMPLES</span></span>

### <span data-ttu-id="a4971-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4971-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="a4971-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a4971-109">PARAMETERS</span></span>

### <span data-ttu-id="a4971-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4971-110">-DefaultProfile</span></span>
<span data-ttu-id="a4971-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4971-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a4971-112">-Path</span><span class="sxs-lookup"><span data-stu-id="a4971-112">-Path</span></span>
<span data-ttu-id="a4971-113">경로 값의 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="a4971-113">Array of string of path values</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a4971-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4971-114">CommonParameters</span></span>
<span data-ttu-id="a4971-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a4971-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4971-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a4971-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4971-117">입력</span><span class="sxs-lookup"><span data-stu-id="a4971-117">INPUTS</span></span>

### <span data-ttu-id="a4971-118">없음</span><span class="sxs-lookup"><span data-stu-id="a4971-118">None</span></span>

## <span data-ttu-id="a4971-119">출력</span><span class="sxs-lookup"><span data-stu-id="a4971-119">OUTPUTS</span></span>

### <span data-ttu-id="a4971-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="a4971-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="a4971-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a4971-121">NOTES</span></span>

## <span data-ttu-id="a4971-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4971-122">RELATED LINKS</span></span>