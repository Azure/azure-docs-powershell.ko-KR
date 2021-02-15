---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKeyPolicy.md
ms.openlocfilehash: bf91d1948b4040a35ee77f2a1111861a03076783
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100196764"
---
# <span data-ttu-id="6f7ea-101">New-AzCosmosDBSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6f7ea-101">New-AzCosmosDBSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="6f7ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6f7ea-102">SYNOPSIS</span></span>
<span data-ttu-id="6f7ea-103">새 CosmosDB SqlUniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-103">Creates a new CosmosDB SqlUniqueKeyPolicy object.</span></span>

## <span data-ttu-id="6f7ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="6f7ea-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6f7ea-105">설명</span><span class="sxs-lookup"><span data-stu-id="6f7ea-105">DESCRIPTION</span></span>
<span data-ttu-id="6f7ea-106">**New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet은 PSSqlUniqueKeyPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-106">The **New-AzCosmosDBSqlUniqueKeyPolicy** cmdlet creates a new object of type PSSqlUniqueKeyPolicy.</span></span>

## <span data-ttu-id="6f7ea-107">예제</span><span class="sxs-lookup"><span data-stu-id="6f7ea-107">EXAMPLES</span></span>

### <span data-ttu-id="6f7ea-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6f7ea-108">Example 1</span></span>
```powershell
PS C:\>New-AzCosmosDBSqlUniqueKeyPolicy -UniqueKey {psUniqueKey1, psUniqueKey2}

UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="6f7ea-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6f7ea-109">PARAMETERS</span></span>

### <span data-ttu-id="6f7ea-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6f7ea-110">-DefaultProfile</span></span>
<span data-ttu-id="6f7ea-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6f7ea-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="6f7ea-112">-UniqueKey</span></span>
<span data-ttu-id="6f7ea-113">데이터베이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-113">Database name.</span></span>

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

### <span data-ttu-id="6f7ea-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6f7ea-114">CommonParameters</span></span>
<span data-ttu-id="6f7ea-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6f7ea-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6f7ea-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6f7ea-117">입력</span><span class="sxs-lookup"><span data-stu-id="6f7ea-117">INPUTS</span></span>

### <span data-ttu-id="6f7ea-118">없음</span><span class="sxs-lookup"><span data-stu-id="6f7ea-118">None</span></span>

## <span data-ttu-id="6f7ea-119">출력</span><span class="sxs-lookup"><span data-stu-id="6f7ea-119">OUTPUTS</span></span>

### <span data-ttu-id="6f7ea-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="6f7ea-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKeyPolicy</span></span>

## <span data-ttu-id="6f7ea-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6f7ea-121">NOTES</span></span>

## <span data-ttu-id="6f7ea-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6f7ea-122">RELATED LINKS</span></span>
