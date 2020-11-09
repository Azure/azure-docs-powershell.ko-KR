---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinuniquekeypolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinUniqueKeyPolicy.md
ms.openlocfilehash: 275019b1eaf4854c4fd9e5be84791368fe09efba
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307061"
---
# <span data-ttu-id="69533-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span><span class="sxs-lookup"><span data-stu-id="69533-101">New-AzCosmosDBGremlinUniqueKeyPolicy</span></span>

## <span data-ttu-id="69533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69533-102">SYNOPSIS</span></span>
<span data-ttu-id="69533-103">새 CosmosDB UniqueKeyPolicy 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69533-103">Creates a new CosmosDB UniqueKeyPolicy object.</span></span>

## <span data-ttu-id="69533-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69533-104">SYNTAX</span></span>

```
New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey <PSSqlUniqueKey[]> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69533-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69533-105">DESCRIPTION</span></span>
<span data-ttu-id="69533-106">**AzCosmosDBGremlinUniqueKeyPolicy** Cmdlet은 PSUniqueKeyPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="69533-106">The **New-AzCosmosDBGremlinUniqueKeyPolicy** cmdlet creates a new object of type PSUniqueKeyPolicy.</span></span>

## <span data-ttu-id="69533-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69533-107">EXAMPLES</span></span>

### <span data-ttu-id="69533-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="69533-108">Example 1</span></span>
```powershell
PS C:\> $uk = New-AzCosmosDBGremlinUniqueKey -Path "abc"

 New-AzCosmosDBGremlinUniqueKeyPolicy -UniqueKey $uk,$uk
 
 UniqueKey
---------
{Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey, Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey}
```

## <span data-ttu-id="69533-109">변수</span><span class="sxs-lookup"><span data-stu-id="69533-109">PARAMETERS</span></span>

### <span data-ttu-id="69533-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69533-110">-DefaultProfile</span></span>
<span data-ttu-id="69533-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69533-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="69533-112">-UniqueKey</span><span class="sxs-lookup"><span data-stu-id="69533-112">-UniqueKey</span></span>
<span data-ttu-id="69533-113">PSUniqueKey 형식의 개체 배열입니다.</span><span class="sxs-lookup"><span data-stu-id="69533-113">Array of objects of type PSUniqueKey.</span></span>

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

### <span data-ttu-id="69533-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69533-114">CommonParameters</span></span>
<span data-ttu-id="69533-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69533-116">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="69533-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69533-117">입력</span><span class="sxs-lookup"><span data-stu-id="69533-117">INPUTS</span></span>

### <span data-ttu-id="69533-118">않아야</span><span class="sxs-lookup"><span data-stu-id="69533-118">None</span></span>

## <span data-ttu-id="69533-119">출력</span><span class="sxs-lookup"><span data-stu-id="69533-119">OUTPUTS</span></span>

### <span data-ttu-id="69533-120">CosmosDB. PSUniqueKeyPolicy/.</span><span class="sxs-lookup"><span data-stu-id="69533-120">Microsoft.Azure.Commands.CosmosDB.Models.PSUniqueKeyPolicy</span></span>

## <span data-ttu-id="69533-121">상속자</span><span class="sxs-lookup"><span data-stu-id="69533-121">NOTES</span></span>

## <span data-ttu-id="69533-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69533-122">RELATED LINKS</span></span>
