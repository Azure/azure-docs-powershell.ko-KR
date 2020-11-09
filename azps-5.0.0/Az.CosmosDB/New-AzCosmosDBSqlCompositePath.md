---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlcompositepath
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlCompositePath.md
ms.openlocfilehash: ff78ad82c89b774f034fe6f1d4499db7868d43c7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94307022"
---
# <span data-ttu-id="2b5e7-101">New-AzCosmosDBSqlCompositePath</span><span class="sxs-lookup"><span data-stu-id="2b5e7-101">New-AzCosmosDBSqlCompositePath</span></span>

## <span data-ttu-id="2b5e7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b5e7-102">SYNOPSIS</span></span>
<span data-ttu-id="2b5e7-103">PSCompositePath 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-103">Creates a new object of type PSCompositePath.</span></span> <span data-ttu-id="2b5e7-104">Set-AzCosmosDBSqlContainer에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="2b5e7-105">구문과</span><span class="sxs-lookup"><span data-stu-id="2b5e7-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlCompositePath [-Path <String>] [-Order <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2b5e7-106">설명은</span><span class="sxs-lookup"><span data-stu-id="2b5e7-106">DESCRIPTION</span></span>
<span data-ttu-id="2b5e7-107">Sql API의 CompositePath에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-107">Object corresponding to Sql API's CompositePath.</span></span>

## <span data-ttu-id="2b5e7-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2b5e7-108">EXAMPLES</span></span>

### <span data-ttu-id="2b5e7-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="2b5e7-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlCompositePath -Path "/abc" -Order Ascending

Path Order
---- -----
/abc Ascending
```

## <span data-ttu-id="2b5e7-110">변수</span><span class="sxs-lookup"><span data-stu-id="2b5e7-110">PARAMETERS</span></span>

### <span data-ttu-id="2b5e7-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b5e7-111">-DefaultProfile</span></span>
<span data-ttu-id="2b5e7-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b5e7-113">-주문</span><span class="sxs-lookup"><span data-stu-id="2b5e7-113">-Order</span></span>
<span data-ttu-id="2b5e7-114">복합 경로의 정렬 순서를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-114">Gets or sets sort order for composite paths.</span></span>
<span data-ttu-id="2b5e7-115">사용할 수 있는 값은 다음과 같습니다. ' 오름차순 ', ' 내림차순 '</span><span class="sxs-lookup"><span data-stu-id="2b5e7-115">Possible values include: 'Ascending', 'Descending'</span></span>

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

### <span data-ttu-id="2b5e7-116">-Path</span><span class="sxs-lookup"><span data-stu-id="2b5e7-116">-Path</span></span>
<span data-ttu-id="2b5e7-117">인덱싱 동작이 적용 되는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-117">The path for which the indexing behavior applies to.</span></span>
<span data-ttu-id="2b5e7-118">일반적으로 인덱스 경로는 와일드 카드 (/path/\*)를 사용 하 여 root로 시작 하 고 끝납니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-118">Index paths typically start with root and end with wildcard (/path/\*)</span></span>

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

### <span data-ttu-id="2b5e7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b5e7-119">CommonParameters</span></span>
<span data-ttu-id="2b5e7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b5e7-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b5e7-122">입력</span><span class="sxs-lookup"><span data-stu-id="2b5e7-122">INPUTS</span></span>

### <span data-ttu-id="2b5e7-123">않아야</span><span class="sxs-lookup"><span data-stu-id="2b5e7-123">None</span></span>

## <span data-ttu-id="2b5e7-124">출력</span><span class="sxs-lookup"><span data-stu-id="2b5e7-124">OUTPUTS</span></span>

### <span data-ttu-id="2b5e7-125">CosmosDB. PSCompositePath/.</span><span class="sxs-lookup"><span data-stu-id="2b5e7-125">Microsoft.Azure.Commands.CosmosDB.Models.PSCompositePath</span></span>

## <span data-ttu-id="2b5e7-126">상속자</span><span class="sxs-lookup"><span data-stu-id="2b5e7-126">NOTES</span></span>

## <span data-ttu-id="2b5e7-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b5e7-127">RELATED LINKS</span></span>
