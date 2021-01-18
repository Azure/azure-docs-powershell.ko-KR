---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqluniquekey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlUniqueKey.md
ms.openlocfilehash: e3c96cfd4051a186e0584d810088bc06a57ad862
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493680"
---
# <span data-ttu-id="845fd-101">New-AzCosmosDBSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="845fd-101">New-AzCosmosDBSqlUniqueKey</span></span>

## <span data-ttu-id="845fd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="845fd-102">SYNOPSIS</span></span>
<span data-ttu-id="845fd-103">새 CosmosDB Sql UniqueKey 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="845fd-103">Creates a new CosmosDB Sql UniqueKey object.</span></span>

## <span data-ttu-id="845fd-104">구문</span><span class="sxs-lookup"><span data-stu-id="845fd-104">SYNTAX</span></span>

```
New-AzCosmosDBSqlUniqueKey -Path <String[]> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="845fd-105">설명</span><span class="sxs-lookup"><span data-stu-id="845fd-105">DESCRIPTION</span></span>
<span data-ttu-id="845fd-106">**New-AzCosmosDBSqlUniqueKey** cmdlet은 PSUniqueKey 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="845fd-106">The **New-AzCosmosDBSqlUniqueKey** cmdlet creates a new object of type PSUniqueKey.</span></span>

## <span data-ttu-id="845fd-107">예제</span><span class="sxs-lookup"><span data-stu-id="845fd-107">EXAMPLES</span></span>

### <span data-ttu-id="845fd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="845fd-108">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlUniqueKey -Path {path}

Path
----
{path}
```

## <span data-ttu-id="845fd-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="845fd-109">PARAMETERS</span></span>

### <span data-ttu-id="845fd-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="845fd-110">-DefaultProfile</span></span>
<span data-ttu-id="845fd-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="845fd-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="845fd-112">-Path</span><span class="sxs-lookup"><span data-stu-id="845fd-112">-Path</span></span>
<span data-ttu-id="845fd-113">경로 값의 문자열 배열</span><span class="sxs-lookup"><span data-stu-id="845fd-113">Array of string of path values</span></span>

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

### <span data-ttu-id="845fd-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="845fd-114">CommonParameters</span></span>
<span data-ttu-id="845fd-115">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="845fd-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="845fd-116">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="845fd-116">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="845fd-117">입력</span><span class="sxs-lookup"><span data-stu-id="845fd-117">INPUTS</span></span>

### <span data-ttu-id="845fd-118">없음</span><span class="sxs-lookup"><span data-stu-id="845fd-118">None</span></span>

## <span data-ttu-id="845fd-119">출력</span><span class="sxs-lookup"><span data-stu-id="845fd-119">OUTPUTS</span></span>

### <span data-ttu-id="845fd-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span><span class="sxs-lookup"><span data-stu-id="845fd-120">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlUniqueKey</span></span>

## <span data-ttu-id="845fd-121">참고 사항</span><span class="sxs-lookup"><span data-stu-id="845fd-121">NOTES</span></span>

## <span data-ttu-id="845fd-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="845fd-122">RELATED LINKS</span></span>
