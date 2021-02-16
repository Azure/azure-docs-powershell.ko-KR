---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100198961"
---
# <span data-ttu-id="edb26-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="edb26-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="edb26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="edb26-102">SYNOPSIS</span></span>
<span data-ttu-id="edb26-103">PSSqlConflictResolutionPolicy 형식의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="edb26-104">Set-AzCosmosDBSqlContainer에 대한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="edb26-105">구문</span><span class="sxs-lookup"><span data-stu-id="edb26-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="edb26-106">설명</span><span class="sxs-lookup"><span data-stu-id="edb26-106">DESCRIPTION</span></span>
<span data-ttu-id="edb26-107">Sql API의 ConflictResolutionPolicy에 해당하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="edb26-108">예제</span><span class="sxs-lookup"><span data-stu-id="edb26-108">EXAMPLES</span></span>

### <span data-ttu-id="edb26-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="edb26-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="edb26-110">{{ 여기에 예제 설명 추가 }}</span><span class="sxs-lookup"><span data-stu-id="edb26-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="edb26-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="edb26-111">PARAMETERS</span></span>

### <span data-ttu-id="edb26-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="edb26-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="edb26-113">형식이 사용자 지정일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="edb26-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="edb26-114">-DefaultProfile</span></span>
<span data-ttu-id="edb26-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="edb26-116">-Path</span><span class="sxs-lookup"><span data-stu-id="edb26-116">-Path</span></span>
<span data-ttu-id="edb26-117">형식이 LastWriterWins일 때 제공될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="edb26-118">-Type</span><span class="sxs-lookup"><span data-stu-id="edb26-118">-Type</span></span>
<span data-ttu-id="edb26-119">LastWriterWins, Custom, Manual 값을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="edb26-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="edb26-120">CommonParameters</span></span>
<span data-ttu-id="edb26-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="edb26-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="edb26-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="edb26-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="edb26-123">입력</span><span class="sxs-lookup"><span data-stu-id="edb26-123">INPUTS</span></span>

### <span data-ttu-id="edb26-124">없음</span><span class="sxs-lookup"><span data-stu-id="edb26-124">None</span></span>

## <span data-ttu-id="edb26-125">출력</span><span class="sxs-lookup"><span data-stu-id="edb26-125">OUTPUTS</span></span>

### <span data-ttu-id="edb26-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="edb26-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="edb26-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="edb26-127">NOTES</span></span>

## <span data-ttu-id="edb26-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="edb26-128">RELATED LINKS</span></span>
