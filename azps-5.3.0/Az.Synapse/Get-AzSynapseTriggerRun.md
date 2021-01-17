---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 0d6d3bb99062177e1d75c4ab496562782cf142c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98383727"
---
# <span data-ttu-id="89b21-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="89b21-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="89b21-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89b21-102">SYNOPSIS</span></span>
<span data-ttu-id="89b21-103">트리거 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="89b21-104">구문</span><span class="sxs-lookup"><span data-stu-id="89b21-104">SYNTAX</span></span>

### <span data-ttu-id="89b21-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="89b21-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="89b21-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="89b21-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89b21-107">설명</span><span class="sxs-lookup"><span data-stu-id="89b21-107">DESCRIPTION</span></span>
<span data-ttu-id="89b21-108">**Get-AzSynapseTriggerRun** 명령은 지정된 시간 프레임에서 지정된 트리거에 대한 트리거 실행에 대한 자세한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="89b21-109">예제</span><span class="sxs-lookup"><span data-stu-id="89b21-109">EXAMPLES</span></span>

### <span data-ttu-id="89b21-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="89b21-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="89b21-111">이 명령은 "2018-09-01T21:00" 및 "2019-09-01T21:00" 사이에서 시작된 작업 영역 ContosoWorkspace의 ContosoTrigger에 대한 실행에 대한 정보를 보여 주며,</span><span class="sxs-lookup"><span data-stu-id="89b21-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="89b21-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="89b21-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="89b21-113">이 명령은 파이프라인을 통해 "2018-09-01T21:00" 및 "2019-09-01T21:00" 사이에서 시작된 작업 영역 ContosoWorkspace의 ContosoTrigger에 대한 실행에 대한 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="89b21-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="89b21-114">PARAMETERS</span></span>

### <span data-ttu-id="89b21-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89b21-115">-DefaultProfile</span></span>
<span data-ttu-id="89b21-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="89b21-117">-Name</span><span class="sxs-lookup"><span data-stu-id="89b21-117">-Name</span></span>
<span data-ttu-id="89b21-118">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-118">The trigger name.</span></span>

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

### <span data-ttu-id="89b21-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="89b21-119">-RunStartedAfter</span></span>
<span data-ttu-id="89b21-120">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 그 이후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="89b21-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="89b21-121">-RunStartedBefore</span></span>
<span data-ttu-id="89b21-122">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 이전 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="89b21-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="89b21-123">-WorkspaceName</span></span>
<span data-ttu-id="89b21-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="89b21-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="89b21-125">-WorkspaceObject</span></span>
<span data-ttu-id="89b21-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="89b21-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89b21-127">CommonParameters</span></span>
<span data-ttu-id="89b21-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="89b21-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89b21-129">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="89b21-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89b21-130">입력</span><span class="sxs-lookup"><span data-stu-id="89b21-130">INPUTS</span></span>

### <span data-ttu-id="89b21-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="89b21-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="89b21-132">출력</span><span class="sxs-lookup"><span data-stu-id="89b21-132">OUTPUTS</span></span>

### <span data-ttu-id="89b21-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="89b21-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="89b21-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="89b21-134">NOTES</span></span>

## <span data-ttu-id="89b21-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89b21-135">RELATED LINKS</span></span>
