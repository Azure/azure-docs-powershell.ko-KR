---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348909"
---
# <span data-ttu-id="a75e9-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a75e9-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="a75e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a75e9-102">SYNOPSIS</span></span>
<span data-ttu-id="a75e9-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a75e9-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="a75e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="a75e9-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a75e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="a75e9-105">DESCRIPTION</span></span>
<span data-ttu-id="a75e9-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet은 PSUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a75e9-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="a75e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="a75e9-107">EXAMPLES</span></span>

### <span data-ttu-id="a75e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a75e9-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="a75e9-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a75e9-109">PARAMETERS</span></span>

### <span data-ttu-id="a75e9-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a75e9-110">-DefaultProfile</span></span>
<span data-ttu-id="a75e9-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a75e9-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a75e9-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="a75e9-112">-UniqueKey</span></span>
<span data-ttu-id="a75e9-113">PSUniqueKey 형식의 개체 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="a75e9-113">Array of objects of type PSUniqueKey.</span></span>

```yaml
Type: PSSqlUniqueKey[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a75e9-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a75e9-114">CommonParameters</span></span>
<span data-ttu-id="a75e9-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a75e9-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a75e9-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a75e9-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a75e9-117">입력</span><span class="sxs-lookup"><span data-stu-id="a75e9-117">INPUTS</span></span>

### <span data-ttu-id="a75e9-118">없음</span><span class="sxs-lookup"><span data-stu-id="a75e9-118">None</span></span>

## <span data-ttu-id="a75e9-119">출력</span><span class="sxs-lookup"><span data-stu-id="a75e9-119">OUTPUTS</span></span>

### <span data-ttu-id="a75e9-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="a75e9-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="a75e9-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a75e9-121">NOTES</span></span>

## <span data-ttu-id="a75e9-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a75e9-122">RELATED LINKS</span></span>