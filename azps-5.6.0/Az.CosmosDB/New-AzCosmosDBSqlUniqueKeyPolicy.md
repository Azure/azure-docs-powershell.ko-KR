---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: 6ef9e9b4fe2332af22bb8bdab1334096860f53ff
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101986860"
---
# <span data-ttu-id="e3b1d-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b1d-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="e3b1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e3b1d-102">SYNOPSIS</span></span>
<span data-ttu-id="e3b1d-103">새 CosmosDB SqlUniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="e3b1d-104">구문</span><span class="sxs-lookup"><span data-stu-id="e3b1d-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e3b1d-105">설명</span><span class="sxs-lookup"><span data-stu-id="e3b1d-105">DESCRIPTION</span></span>
<span data-ttu-id="e3b1d-106">**New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet은 PSSqlUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="e3b1d-107">예제</span><span class="sxs-lookup"><span data-stu-id="e3b1d-107">EXAMPLES</span></span>

### <span data-ttu-id="e3b1d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e3b1d-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="e3b1d-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e3b1d-109">PARAMETERS</span></span>

### <span data-ttu-id="e3b1d-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e3b1d-110">-DefaultProfile</span></span>
<span data-ttu-id="e3b1d-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e3b1d-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="e3b1d-112">-UniqueKey</span></span>
<span data-ttu-id="e3b1d-113">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-113">Database name.</span></span>

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

### <span data-ttu-id="e3b1d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e3b1d-114">CommonParameters</span></span>
<span data-ttu-id="e3b1d-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e3b1d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e3b1d-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e3b1d-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e3b1d-117">입력</span><span class="sxs-lookup"><span data-stu-id="e3b1d-117">INPUTS</span></span>

### <span data-ttu-id="e3b1d-118">없음</span><span class="sxs-lookup"><span data-stu-id="e3b1d-118">None</span></span>

## <span data-ttu-id="e3b1d-119">출력</span><span class="sxs-lookup"><span data-stu-id="e3b1d-119">OUTPUTS</span></span>

### <span data-ttu-id="e3b1d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="e3b1d-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="e3b1d-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e3b1d-121">NOTES</span></span>

## <span data-ttu-id="e3b1d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e3b1d-122">RELATED LINKS</span></span>
