---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/get-azsynapsetriggerrun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseTriggerRun.md
ms.openlocfilehash: 284974cc2d4cb98519b82c5c5a50e40d323dc354
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101977947"
---
# <span data-ttu-id="34c18-101">Get-AzSynapseTriggerRun</span><span class="sxs-lookup"><span data-stu-id="34c18-101">Get-AzSynapseTriggerRun</span></span>

## <span data-ttu-id="34c18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34c18-102">SYNOPSIS</span></span>
<span data-ttu-id="34c18-103">트리거 실행에 대한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-103">Returns information about trigger runs.</span></span>

## <span data-ttu-id="34c18-104">구문</span><span class="sxs-lookup"><span data-stu-id="34c18-104">SYNTAX</span></span>

### <span data-ttu-id="34c18-105">GetByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="34c18-105">GetByName (Default)</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceName <String> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="34c18-106">GetByObject</span><span class="sxs-lookup"><span data-stu-id="34c18-106">GetByObject</span></span>
```
Get-AzSynapseTriggerRun -WorkspaceObject <PSSynapseWorkspace> -Name <String> -RunStartedAfter <DateTimeOffset>
 -RunStartedBefore <DateTimeOffset> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="34c18-107">설명</span><span class="sxs-lookup"><span data-stu-id="34c18-107">DESCRIPTION</span></span>
<span data-ttu-id="34c18-108">**Get-AzSynapseTriggerRun** 명령은 지정된 기간에 지정된 트리거에 대한 트리거 실행에 대한 자세한 정보를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-108">The **Get-AzSynapseTriggerRun** command returns detailed information about trigger runs for the specified trigger in the given timeframe.</span></span>

## <span data-ttu-id="34c18-109">예제</span><span class="sxs-lookup"><span data-stu-id="34c18-109">EXAMPLES</span></span>

### <span data-ttu-id="34c18-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="34c18-110">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseTriggerRun -WorkspaceName ContosoWorkspace -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="34c18-111">이 명령은 "2018-09-01T21:00"과 "2019-09-01T21:00"으로 시작된 작업 영역 ContosoWorkspace에서 ContosoTrigger에 대한 실행에 대한 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-111">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00".</span></span>

### <span data-ttu-id="34c18-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="34c18-112">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseTriggerRun -Name ContosoTrigger -RunStartedAfter [DateTimeOffset]"2018-09-01T21:00" -RunStartedBefore [DateTimeOffset]"2019-09-01T21:00"
```

<span data-ttu-id="34c18-113">이 명령은 파이프라인을 통해 "2018-09-01T21:00"과 "2019-09-01T21:00"으로 시작된 작업 영역 ContosoWorkspace에서 ContosoTrigger에 대한 실행에 대한 정보를 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-113">This command shows information about runs for ContosoTrigger in the workspace ContosoWorkspace that started between "2018-09-01T21:00" and "2019-09-01T21:00" through pipeline.</span></span>

## <span data-ttu-id="34c18-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="34c18-114">PARAMETERS</span></span>

### <span data-ttu-id="34c18-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34c18-115">-DefaultProfile</span></span>
<span data-ttu-id="34c18-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34c18-117">-Name</span><span class="sxs-lookup"><span data-stu-id="34c18-117">-Name</span></span>
<span data-ttu-id="34c18-118">트리거 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-118">The trigger name.</span></span>

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

### <span data-ttu-id="34c18-119">-RunStartedAfter</span><span class="sxs-lookup"><span data-stu-id="34c18-119">-RunStartedAfter</span></span>
<span data-ttu-id="34c18-120">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 그 후의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-120">The time at or after which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="34c18-121">-RunStartedBefore</span><span class="sxs-lookup"><span data-stu-id="34c18-121">-RunStartedBefore</span></span>
<span data-ttu-id="34c18-122">실행 이벤트가 'ISO 8601' 형식으로 업데이트된 시간 또는 이전의 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-122">The time at or before which the run event was updated in 'ISO 8601' format.</span></span>

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

### <span data-ttu-id="34c18-123">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="34c18-123">-WorkspaceName</span></span>
<span data-ttu-id="34c18-124">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-124">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="34c18-125">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="34c18-125">-WorkspaceObject</span></span>
<span data-ttu-id="34c18-126">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-126">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="34c18-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34c18-127">CommonParameters</span></span>
<span data-ttu-id="34c18-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34c18-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34c18-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="34c18-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34c18-130">입력</span><span class="sxs-lookup"><span data-stu-id="34c18-130">INPUTS</span></span>

### <span data-ttu-id="34c18-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="34c18-131">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="34c18-132">출력</span><span class="sxs-lookup"><span data-stu-id="34c18-132">OUTPUTS</span></span>

### <span data-ttu-id="34c18-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span><span class="sxs-lookup"><span data-stu-id="34c18-133">Microsoft.Azure.Commands.Synapse.Models.PSTriggerRun</span></span>

## <span data-ttu-id="34c18-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34c18-134">NOTES</span></span>

## <span data-ttu-id="34c18-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34c18-135">RELATED LINKS</span></span>
