---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204184"
---
# <span data-ttu-id="55f1f-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="55f1f-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="55f1f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55f1f-102">SYNOPSIS</span></span>
<span data-ttu-id="55f1f-103">트리거 실행에 대 한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="55f1f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="55f1f-104">SYNTAX</span></span>

### <span data-ttu-id="55f1f-105">GetByName (기본값)</span><span class="sxs-lookup"><span data-stu-id="55f1f-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="55f1f-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="55f1f-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="55f1f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="55f1f-107">DESCRIPTION</span></span>
<span data-ttu-id="55f1f-108">**AzSynapseTriggerRun** 명령은 지정 된 시간에 지정한 트리거에 대 한 트리거 실행에 대 한 자세한 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="55f1f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="55f1f-109">EXAMPLES</span></span>

### <span data-ttu-id="55f1f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="55f1f-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="55f1f-111">이 명령은 "2018-09-01T21:00" 및 "2019-09-01T21:00" 간에 시작 된 작업 영역 ContosoWorkspace의 ContosoTrigger에 대 한 연속 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="55f1f-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="55f1f-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="55f1f-113">이 명령은 "2018-09-01T21:00" 및 "2019-09-01T21:00"에서 파이프라인을 통해 시작 된 작업 영역 ContosoWorkspace의 ContosoTrigger에 대 한 연속 정보를 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="55f1f-114">변수</span><span class="sxs-lookup"><span data-stu-id="55f1f-114">PARAMETERS</span></span>

### <span data-ttu-id="55f1f-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55f1f-115">-DefaultProfile</span></span>
<span data-ttu-id="55f1f-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-117">-이름</span><span class="sxs-lookup"><span data-stu-id="55f1f-117">-Name</span></span>
<span data-ttu-id="55f1f-118">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-118">The trigger name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: TriggerName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="55f1f-119">-RunStartedAfter</span></span>
<span data-ttu-id="55f1f-120">' ISO 8601 ' 형식으로 실행 이벤트가 업데이트 된 시간 또는 이후</span><span class="sxs-lookup"><span data-stu-id="55f1f-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="55f1f-121">-RunStartedBefore</span></span>
<span data-ttu-id="55f1f-122">' ISO 8601 ' 형식으로 실행 이벤트를 업데이트 한 날짜 또는 그 이전의 시간</span><span class="sxs-lookup"><span data-stu-id="55f1f-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="55f1f-123">-WorkspaceName</span></span>
<span data-ttu-id="55f1f-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-124">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="55f1f-125">-WorkspaceObject</span></span>
<span data-ttu-id="55f1f-126">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-126">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="55f1f-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55f1f-127">CommonParameters</span></span>
<span data-ttu-id="55f1f-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="55f1f-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55f1f-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="55f1f-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55f1f-130">입력</span><span class="sxs-lookup"><span data-stu-id="55f1f-130">INPUTS</span></span>

### <span data-ttu-id="55f1f-131">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="55f1f-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="55f1f-132">출력</span><span class="sxs-lookup"><span data-stu-id="55f1f-132">OUTPUTS</span></span>

### <span data-ttu-id="55f1f-133">Synapse. PSTriggerRun/.</span><span class="sxs-lookup"><span data-stu-id="55f1f-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="55f1f-134">상속자</span><span class="sxs-lookup"><span data-stu-id="55f1f-134">NOTES</span></span>

## <span data-ttu-id="55f1f-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55f1f-135">RELATED LINKS</span></span>
