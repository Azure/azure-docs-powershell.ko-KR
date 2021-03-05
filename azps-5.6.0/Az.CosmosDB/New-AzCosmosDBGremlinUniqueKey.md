---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: b2984ffc8b2c268f5298d88e9dc64e0729798e97
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101998788"
---
# <span data-ttu-id="0c7f5-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0c7f5-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="0c7f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0c7f5-102">SYNOPSIS</span></span>
<span data-ttu-id="0c7f5-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="0c7f5-104">구문</span><span class="sxs-lookup"><span data-stu-id="0c7f5-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0c7f5-105">설명</span><span class="sxs-lookup"><span data-stu-id="0c7f5-105">DESCRIPTION</span></span>
<span data-ttu-id="0c7f5-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet은 PSUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="0c7f5-107">예제</span><span class="sxs-lookup"><span data-stu-id="0c7f5-107">EXAMPLES</span></span>

### <span data-ttu-id="0c7f5-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0c7f5-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="0c7f5-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="0c7f5-109">PARAMETERS</span></span>

### <span data-ttu-id="0c7f5-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0c7f5-110">-DefaultProfile</span></span>
<span data-ttu-id="0c7f5-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0c7f5-112">-Path</span><span class="sxs-lookup"><span data-stu-id="0c7f5-112">-Path</span></span>
<span data-ttu-id="0c7f5-113">경로 값의 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="0c7f5-113">Array of string of path values</span></span>

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

### <span data-ttu-id="0c7f5-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0c7f5-114">CommonParameters</span></span>
<span data-ttu-id="0c7f5-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0c7f5-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0c7f5-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="0c7f5-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0c7f5-117">입력</span><span class="sxs-lookup"><span data-stu-id="0c7f5-117">INPUTS</span></span>

### <span data-ttu-id="0c7f5-118">없음</span><span class="sxs-lookup"><span data-stu-id="0c7f5-118">None</span></span>

## <span data-ttu-id="0c7f5-119">출력</span><span class="sxs-lookup"><span data-stu-id="0c7f5-119">OUTPUTS</span></span>

### <span data-ttu-id="0c7f5-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0c7f5-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="0c7f5-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0c7f5-121">NOTES</span></span>

## <span data-ttu-id="0c7f5-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0c7f5-122">RELATED LINKS</span></span>
