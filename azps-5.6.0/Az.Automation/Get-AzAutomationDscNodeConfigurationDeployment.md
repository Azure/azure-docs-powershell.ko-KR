---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: f5cbb59ffbd5b79087e9f338788dde9d1176f4d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101995731"
---
# <span data-ttu-id="e4751-101">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e4751-101">Get-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="e4751-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4751-102">SYNOPSIS</span></span>
<span data-ttu-id="e4751-103">Automation에서 DSC 노드 구성 배포를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-103">Gets DSC Node configuration deployments in Automation.</span></span>

## <span data-ttu-id="e4751-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4751-104">SYNTAX</span></span>

### <span data-ttu-id="e4751-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="e4751-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment [-Status <String>] [-StartTime <DateTimeOffset>]
 [-EndTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4751-106">ByJobId</span><span class="sxs-lookup"><span data-stu-id="e4751-106">ByJobId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4751-107">설명</span><span class="sxs-lookup"><span data-stu-id="e4751-107">DESCRIPTION</span></span>
<span data-ttu-id="e4751-108">**Get-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 APS 원하는 상태 구성(DSC) 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="e4751-109">예제</span><span class="sxs-lookup"><span data-stu-id="e4751-109">EXAMPLES</span></span>

### <span data-ttu-id="e4751-110">예제 1: 노드 구성 배포하기</span><span class="sxs-lookup"><span data-stu-id="e4751-110">Example 1: Get a node configuration deployment</span></span>
```
PS C:\> $deployment = Get-AzAutomationDscNodeConfigurationDeployment `
                         -JobId 35b14eb4-52b7-4a1d-ad62-8e9f84adc657 `
                         -AutomationAccountName "Contoso01"  `
                         -ResourceGroupName "ResourceGroup01" `
            
ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : Running
NodeStatus            : {System.Collections.Generic.Dictionary`2[System.String,System.String], System.Collections.Generic.Dictionary`2[System.String,System.String]}
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000

PS C:\> $deployment | Select -expand nodeStatus

Key        Value
---        -----
WebServer  Pending
WebServer2 Pending
WebServer3 Compliant
```

<span data-ttu-id="e4751-111">위의 명령은 "Config01.Node1"이라는 DSC 노드 구성을 주어진 2차원 노드 이름 배열에 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="e4751-112">배포는 단계적 방식으로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-112">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="e4751-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4751-113">PARAMETERS</span></span>

### <span data-ttu-id="e4751-114">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="e4751-114">-AutomationAccountName</span></span>
<span data-ttu-id="e4751-115">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-115">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4751-116">-DefaultProfile</span></span>
<span data-ttu-id="e4751-117">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4751-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4751-118">-EndTime</span><span class="sxs-lookup"><span data-stu-id="e4751-118">-EndTime</span></span>
<span data-ttu-id="e4751-119">종료 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-119">End time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-120">-JobId</span><span class="sxs-lookup"><span data-stu-id="e4751-120">-JobId</span></span>
<span data-ttu-id="e4751-121">기존 배포 작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-121">Specifies the Job id of an existing deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4751-122">-ResourceGroupName</span></span>
<span data-ttu-id="e4751-123">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-123">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-124">-StartTime</span><span class="sxs-lookup"><span data-stu-id="e4751-124">-StartTime</span></span>
<span data-ttu-id="e4751-125">시작 시간 필터입니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-125">Start time filter.</span></span>

```yaml
Type: System.Nullable`1[System.DateTimeOffset]
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-126">-Status</span><span class="sxs-lookup"><span data-stu-id="e4751-126">-Status</span></span>
<span data-ttu-id="e4751-127">작업 필터의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-127">Status of the Job filter.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases:
Accepted values: Completed, Failed, Queued, Starting, Resuming, Running, Stopped, Stopping, Suspended, Suspending, Activating

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e4751-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4751-128">CommonParameters</span></span>
<span data-ttu-id="e4751-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4751-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4751-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e4751-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4751-131">입력</span><span class="sxs-lookup"><span data-stu-id="e4751-131">INPUTS</span></span>

### <span data-ttu-id="e4751-132">System.Guid</span><span class="sxs-lookup"><span data-stu-id="e4751-132">System.Guid</span></span>

### <span data-ttu-id="e4751-133">System.String</span><span class="sxs-lookup"><span data-stu-id="e4751-133">System.String</span></span>

## <span data-ttu-id="e4751-134">출력</span><span class="sxs-lookup"><span data-stu-id="e4751-134">OUTPUTS</span></span>

### <span data-ttu-id="e4751-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e4751-135">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="e4751-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4751-136">NOTES</span></span>

## <span data-ttu-id="e4751-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4751-137">RELATED LINKS</span></span>

[<span data-ttu-id="e4751-138">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="e4751-138">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="e4751-139">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4751-139">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="e4751-140">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e4751-140">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e4751-141">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="e4751-141">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="e4751-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="e4751-142">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
