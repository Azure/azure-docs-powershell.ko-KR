---
external help file: Microsoft.Azure.PowerShell.Cmdlets.CosmosDB.dll-Help.xml
Module Name: Az.CosmosDB
online version: https://docs.microsoft.com/en-us/powershell/module/az.cosmosdb/new-azcosmosdbsqlconflictresolutionpolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/CosmosDB/CosmosDB/help/New-AzCosmosDBSqlConflictResolutionPolicy.md
ms.openlocfilehash: b11142be65935522a73d3a068be0ee329994e2ee
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212377"
---
# <span data-ttu-id="3cc10-101">New-AzCosmosDBSqlConflictResolutionPolicy</span><span class="sxs-lookup"><span data-stu-id="3cc10-101">New-AzCosmosDBSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="3cc10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3cc10-102">SYNOPSIS</span></span>
<span data-ttu-id="3cc10-103">PSSqlConflictResolutionPolicy 유형의 새 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-103">Creates a new object of type PSSqlConflictResolutionPolicy.</span></span> <span data-ttu-id="3cc10-104">Set-AzCosmosDBSqlContainer에 대 한 매개 변수 값으로 전달할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-104">It can be passed as a parameter value for Set-AzCosmosDBSqlContainer.</span></span>

## <span data-ttu-id="3cc10-105">구문과</span><span class="sxs-lookup"><span data-stu-id="3cc10-105">SYNTAX</span></span>

```
New-AzCosmosDBSqlConflictResolutionPolicy -Type <String> [-Path <String>]
 [-ConflictResolutionProcedure <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3cc10-106">설명은</span><span class="sxs-lookup"><span data-stu-id="3cc10-106">DESCRIPTION</span></span>
<span data-ttu-id="3cc10-107">Sql API의 ConflictResolutionPolicy에 해당 하는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-107">Object corresponding to Sql API's ConflictResolutionPolicy.</span></span>

## <span data-ttu-id="3cc10-108">예제의</span><span class="sxs-lookup"><span data-stu-id="3cc10-108">EXAMPLES</span></span>

### <span data-ttu-id="3cc10-109">예제 1</span><span class="sxs-lookup"><span data-stu-id="3cc10-109">Example 1</span></span>
```powershell
PS C:\> New-AzCosmosDBSqlConflictResolutionPolicy -Type LastWriterWins -Path "/myPath"

Mode           ConflictResolutionPath ConflictResolutionProcedure
----           ---------------------- ---------------------------
LastWriterWins /myPath
```

<span data-ttu-id="3cc10-110">{{여기에 예제 설명 추가}}</span><span class="sxs-lookup"><span data-stu-id="3cc10-110">{{ Add example description here }}</span></span>

## <span data-ttu-id="3cc10-111">변수</span><span class="sxs-lookup"><span data-stu-id="3cc10-111">PARAMETERS</span></span>

### <span data-ttu-id="3cc10-112">-ConflictResolutionProcedure</span><span class="sxs-lookup"><span data-stu-id="3cc10-112">-ConflictResolutionProcedure</span></span>
<span data-ttu-id="3cc10-113">형식이 사용자 지정 일 때 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-113">To be provided when the type is custom.</span></span>

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

### <span data-ttu-id="3cc10-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3cc10-114">-DefaultProfile</span></span>
<span data-ttu-id="3cc10-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3cc10-116">-Path</span><span class="sxs-lookup"><span data-stu-id="3cc10-116">-Path</span></span>
<span data-ttu-id="3cc10-117">형식이 Last만들려는 경우 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-117">To be provided when the type is LastWriterWins.</span></span>

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

### <span data-ttu-id="3cc10-118">-Type</span><span class="sxs-lookup"><span data-stu-id="3cc10-118">-Type</span></span>
<span data-ttu-id="3cc10-119">값은 Last승 Wins, Custom, Manual 중에서 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-119">Can have the values: LastWriterWins, Custom, Manual.</span></span>

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

### <span data-ttu-id="3cc10-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3cc10-120">CommonParameters</span></span>
<span data-ttu-id="3cc10-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3cc10-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3cc10-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3cc10-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3cc10-123">입력</span><span class="sxs-lookup"><span data-stu-id="3cc10-123">INPUTS</span></span>

### <span data-ttu-id="3cc10-124">않아야</span><span class="sxs-lookup"><span data-stu-id="3cc10-124">None</span></span>

## <span data-ttu-id="3cc10-125">출력</span><span class="sxs-lookup"><span data-stu-id="3cc10-125">OUTPUTS</span></span>

### <span data-ttu-id="3cc10-126">CosmosDB. PSSqlConflictResolutionPolicy/.</span><span class="sxs-lookup"><span data-stu-id="3cc10-126">Microsoft.Azure.Commands.CosmosDB.Models.PSSqlConflictResolutionPolicy</span></span>

## <span data-ttu-id="3cc10-127">상속자</span><span class="sxs-lookup"><span data-stu-id="3cc10-127">NOTES</span></span>

## <span data-ttu-id="3cc10-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3cc10-128">RELATED LINKS</span></span>
