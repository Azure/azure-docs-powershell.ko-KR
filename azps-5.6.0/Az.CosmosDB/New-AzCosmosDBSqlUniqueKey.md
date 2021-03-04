---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: b172c5e22c26cba8d88d188198868da720d611d4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990327"
---
# <span data-ttu-id="f5420-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="f5420-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="f5420-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5420-102">SYNOPSIS</span></span>
<span data-ttu-id="f5420-103">새 CosmosDB Sql UniqueKey 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5420-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="f5420-104">구문</span><span class="sxs-lookup"><span data-stu-id="f5420-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5420-105">설명</span><span class="sxs-lookup"><span data-stu-id="f5420-105">DESCRIPTION</span></span>
<span data-ttu-id="f5420-106">**New-AzCosmosDBSqlUniqueKey** cmdlet은 PSUniqueKey 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f5420-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="f5420-107">예제</span><span class="sxs-lookup"><span data-stu-id="f5420-107">EXAMPLES</span></span>

### <span data-ttu-id="f5420-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5420-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="f5420-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f5420-109">PARAMETERS</span></span>

### <span data-ttu-id="f5420-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5420-110">-DefaultProfile</span></span>
<span data-ttu-id="f5420-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5420-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f5420-112">-Path</span><span class="sxs-lookup"><span data-stu-id="f5420-112">-Path</span></span>
<span data-ttu-id="f5420-113">경로 값의 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="f5420-113">Array of string of path values</span></span>

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

### <span data-ttu-id="f5420-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5420-114">CommonParameters</span></span>
<span data-ttu-id="f5420-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f5420-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5420-116">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f5420-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5420-117">입력</span><span class="sxs-lookup"><span data-stu-id="f5420-117">INPUTS</span></span>

### <span data-ttu-id="f5420-118">없음</span><span class="sxs-lookup"><span data-stu-id="f5420-118">None</span></span>

## <span data-ttu-id="f5420-119">출력</span><span class="sxs-lookup"><span data-stu-id="f5420-119">OUTPUTS</span></span>

### <span data-ttu-id="f5420-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="f5420-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="f5420-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f5420-121">NOTES</span></span>

## <span data-ttu-id="f5420-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5420-122">RELATED LINKS</span></span>
