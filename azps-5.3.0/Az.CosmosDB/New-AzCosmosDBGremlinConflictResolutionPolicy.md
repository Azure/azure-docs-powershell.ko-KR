---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495800"
---
# <span data-ttu-id="b7279-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7279-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="b7279-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7279-102">SYNOPSIS</span></span>
<span data-ttu-id="b7279-103">PSConflictResolutionPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="b7279-104">Set-AzCosmosDBGremlinGraph에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="b7279-105">구문</span><span class="sxs-lookup"><span data-stu-id="b7279-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b7279-106">설명</span><span class="sxs-lookup"><span data-stu-id="b7279-106">DESCRIPTION</span></span>
<span data-ttu-id="b7279-107">Gremlin API의 ConflictResolutionPolicy에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="b7279-108">예제</span><span class="sxs-lookup"><span data-stu-id="b7279-108">EXAMPLES</span></span>

### <span data-ttu-id="b7279-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7279-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="b7279-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b7279-110">PARAMETERS</span></span>

### <span data-ttu-id="b7279-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="b7279-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="b7279-112">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="b7279-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7279-113">-DefaultProfile</span></span>
<span data-ttu-id="b7279-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7279-115">-Path</span><span class="sxs-lookup"><span data-stu-id="b7279-115">-Path</span></span>
<span data-ttu-id="b7279-116">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="b7279-117">-Type</span><span class="sxs-lookup"><span data-stu-id="b7279-117">-Type</span></span>
<span data-ttu-id="b7279-118">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b7279-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7279-119">CommonParameters</span></span>
<span data-ttu-id="b7279-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b7279-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7279-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b7279-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7279-122">입력</span><span class="sxs-lookup"><span data-stu-id="b7279-122">INPUTS</span></span>

### <span data-ttu-id="b7279-123">없음</span><span class="sxs-lookup"><span data-stu-id="b7279-123">None</span></span>

## <span data-ttu-id="b7279-124">출력</span><span class="sxs-lookup"><span data-stu-id="b7279-124">OUTPUTS</span></span>

### <span data-ttu-id="b7279-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="b7279-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="b7279-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b7279-126">NOTES</span></span>

## <span data-ttu-id="b7279-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7279-127">RELATED LINKS</span></span>
