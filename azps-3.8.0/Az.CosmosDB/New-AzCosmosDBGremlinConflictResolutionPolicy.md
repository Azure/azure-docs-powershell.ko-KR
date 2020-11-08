---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbgremlinconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBGremlinConflictResolutionPolicy.md
ms.openlocfilehash: 4662368f89f77c331619472feefe16736c40ef55
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94042086"
---
# <span data-ttu-id="9376e-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="9376e-101">New-AzCosmosDBGremlinConflictResolutionPolicy</span></span>

## <span data-ttu-id="9376e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9376e-102">SYNOPSIS</span></span>
<span data-ttu-id="9376e-103">PSConflictResolutionPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-103">Creates a new object of type PSConflictResolutionPolicy.</span></span> <span data-ttu-id="9376e-104">Set-AzCosmosDBGremlinGraph에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-104">It can be passed as a parameter value for Set-AzCosmosDBGremlinGraph.</span></span>

## <span data-ttu-id="9376e-105">구문과</span><span class="sxs-lookup"><span data-stu-id="9376e-105">SYNTAX</span></span>

```
New-AzCosmosDBGremlinConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9376e-106">설명은</span><span class="sxs-lookup"><span data-stu-id="9376e-106">DESCRIPTION</span></span>
<span data-ttu-id="9376e-107">Gremlin API의 ConflictResolutionPolicy에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-107">Object corresponding to Gremlin API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="9376e-108">예제의</span><span class="sxs-lookup"><span data-stu-id="9376e-108">EXAMPLES</span></span>

### <span data-ttu-id="9376e-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="9376e-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBGremlinConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

## <span data-ttu-id="9376e-110">변수</span><span class="sxs-lookup"><span data-stu-id="9376e-110">PARAMETERS</span></span>

### <span data-ttu-id="9376e-111">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="9376e-111">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="9376e-112">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-112">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="9376e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9376e-113">-DefaultProfile</span></span>
<span data-ttu-id="9376e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9376e-115">-Path</span><span class="sxs-lookup"><span data-stu-id="9376e-115">-Path</span></span>
<span data-ttu-id="9376e-116">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-116">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="9376e-117">-Type</span><span class="sxs-lookup"><span data-stu-id="9376e-117">-Type</span></span>
<span data-ttu-id="9376e-118">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-118">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="9376e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9376e-119">CommonParameters</span></span>
<span data-ttu-id="9376e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9376e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9376e-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9376e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9376e-122">입력</span><span class="sxs-lookup"><span data-stu-id="9376e-122">INPUTS</span></span>

### <span data-ttu-id="9376e-123">않아야</span><span class="sxs-lookup"><span data-stu-id="9376e-123">None</span></span>

## <span data-ttu-id="9376e-124">출력</span><span class="sxs-lookup"><span data-stu-id="9376e-124">OUTPUTS</span></span>

### <span data-ttu-id="9376e-125">CosmosDB. PSConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="9376e-125">Microsoft.Azure.Commands.CosmosDB.Models.PSConflictResolutionPolicy</span></span>

## <span data-ttu-id="9376e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="9376e-126">NOTES</span></span>

## <span data-ttu-id="9376e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9376e-127">RELATED LINKS</span></span>
