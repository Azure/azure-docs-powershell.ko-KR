---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKey.md
ms.openlocfilehash: a51075274c20d0beeb9e73c26ec72f5f69fdf388
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307070"
---
# <span data-ttu-id="dc993-101">New-AzCosmosDBGremlinUniqueKey</span><span class="sxs-lookup"><span data-stu-id="dc993-101">New-AzCosmosDBGremlinUniqueKey</span></span>

## <span data-ttu-id="dc993-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc993-102">SYNOPSIS</span></span>
<span data-ttu-id="dc993-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc993-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="dc993-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc993-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc993-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dc993-105">DESCRIPTION</span></span>
<span data-ttu-id="dc993-106">**AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet은 PSUniqueKeyPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc993-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="dc993-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dc993-107">EXAMPLES</span></span>

### <span data-ttu-id="dc993-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc993-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinUniqueKey -Path "abc"
UniqueKeys
----------
{Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey}
```

## <span data-ttu-id="dc993-109">변수</span><span class="sxs-lookup"><span data-stu-id="dc993-109">PARAMETERS</span></span>

### <span data-ttu-id="dc993-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc993-110">-DefaultProfile</span></span>
<span data-ttu-id="dc993-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc993-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc993-112">-Path</span><span class="sxs-lookup"><span data-stu-id="dc993-112">-Path</span></span>
<span data-ttu-id="dc993-113">경로 값 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="dc993-113">Array of string of path values</span></span>

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

### <span data-ttu-id="dc993-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc993-114">CommonParameters</span></span>
<span data-ttu-id="dc993-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc993-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc993-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dc993-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc993-117">입력</span><span class="sxs-lookup"><span data-stu-id="dc993-117">INPUTS</span></span>

### <span data-ttu-id="dc993-118">않아야</span><span class="sxs-lookup"><span data-stu-id="dc993-118">None</span></span>

## <span data-ttu-id="dc993-119">출력</span><span class="sxs-lookup"><span data-stu-id="dc993-119">OUTPUTS</span></span>

### <span data-ttu-id="dc993-120">CosmosDB. PSUniqueKey/.</span><span class="sxs-lookup"><span data-stu-id="dc993-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKey</span></span>

## <span data-ttu-id="dc993-121">상속자</span><span class="sxs-lookup"><span data-stu-id="dc993-121">NOTES</span></span>

## <span data-ttu-id="dc993-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc993-122">RELATED LINKS</span></span>
