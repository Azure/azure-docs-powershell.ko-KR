---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 54f7a1cb17413fe9d6703dbd0e909555e0c3926a
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957440"
---
# <span data-ttu-id="b6a9a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b6a9a-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="b6a9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6a9a-102">SYNOPSIS</span></span>
<span data-ttu-id="b6a9a-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9a-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="b6a9a-104">구문</span><span class="sxs-lookup"><span data-stu-id="b6a9a-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b6a9a-105">설명</span><span class="sxs-lookup"><span data-stu-id="b6a9a-105">DESCRIPTION</span></span>
<span data-ttu-id="b6a9a-106">**New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet은 PSUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9a-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="b6a9a-107">예제</span><span class="sxs-lookup"><span data-stu-id="b6a9a-107">EXAMPLES</span></span>

### <span data-ttu-id="b6a9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b6a9a-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="b6a9a-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="b6a9a-109">PARAMETERS</span></span>

### <span data-ttu-id="b6a9a-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b6a9a-110">-DefaultProfile</span></span>
<span data-ttu-id="b6a9a-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9a-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b6a9a-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="b6a9a-112">-UniqueKey</span></span>
<span data-ttu-id="b6a9a-113">PSUniqueKey 형식의 개체 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9a-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="b6a9a-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6a9a-114">CommonParameters</span></span>
<span data-ttu-id="b6a9a-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b6a9a-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6a9a-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="b6a9a-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6a9a-117">입력</span><span class="sxs-lookup"><span data-stu-id="b6a9a-117">INPUTS</span></span>

### <span data-ttu-id="b6a9a-118">없음</span><span class="sxs-lookup"><span data-stu-id="b6a9a-118">None</span></span>

## <span data-ttu-id="b6a9a-119">출력</span><span class="sxs-lookup"><span data-stu-id="b6a9a-119">OUTPUTS</span></span>

### <span data-ttu-id="b6a9a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="b6a9a-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="b6a9a-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b6a9a-121">NOTES</span></span>

## <span data-ttu-id="b6a9a-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b6a9a-122">RELATED LINKS</span></span>
