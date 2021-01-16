---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98366955"
---
# <span data-ttu-id="0da49-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0da49-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="0da49-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0da49-102">SYNOPSIS</span></span>
<span data-ttu-id="0da49-103">새 CosmosDB Sql UniqueKey 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0da49-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="0da49-104">구문</span><span class="sxs-lookup"><span data-stu-id="0da49-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0da49-105">설명</span><span class="sxs-lookup"><span data-stu-id="0da49-105">DESCRIPTION</span></span>
<span data-ttu-id="0da49-106">**New-AzCosmosDBSqlUniqueKey** cmdlet은 PSUniqueKey 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0da49-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="0da49-107">예제</span><span class="sxs-lookup"><span data-stu-id="0da49-107">EXAMPLES</span></span>

### <span data-ttu-id="0da49-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="0da49-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="0da49-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0da49-109">PARAMETERS</span></span>

### <span data-ttu-id="0da49-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0da49-110">-DefaultProfile</span></span>
<span data-ttu-id="0da49-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0da49-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0da49-112">-Path</span><span class="sxs-lookup"><span data-stu-id="0da49-112">-Path</span></span>
<span data-ttu-id="0da49-113">경로 값의 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="0da49-113">Array of string of path values</span></span>

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

### <span data-ttu-id="0da49-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0da49-114">CommonParameters</span></span>
<span data-ttu-id="0da49-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0da49-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0da49-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0da49-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0da49-117">입력</span><span class="sxs-lookup"><span data-stu-id="0da49-117">INPUTS</span></span>

### <span data-ttu-id="0da49-118">없음</span><span class="sxs-lookup"><span data-stu-id="0da49-118">None</span></span>

## <span data-ttu-id="0da49-119">출력</span><span class="sxs-lookup"><span data-stu-id="0da49-119">OUTPUTS</span></span>

### <span data-ttu-id="0da49-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="0da49-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="0da49-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0da49-121">NOTES</span></span>

## <span data-ttu-id="0da49-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0da49-122">RELATED LINKS</span></span>
