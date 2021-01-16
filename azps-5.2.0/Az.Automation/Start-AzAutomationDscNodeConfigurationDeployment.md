---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 41605bbdd37ae29f420581f9ad916a1cc87150be
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325688"
---
# <span data-ttu-id="c0e72-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c0e72-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="c0e72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0e72-102">SYNOPSIS</span></span>
<span data-ttu-id="c0e72-103">Automation에서 DSC 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="c0e72-104">구문</span><span class="sxs-lookup"><span data-stu-id="c0e72-104">SYNTAX</span></span>

### <span data-ttu-id="c0e72-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="c0e72-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0e72-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="c0e72-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c0e72-107">설명</span><span class="sxs-lookup"><span data-stu-id="c0e72-107">DESCRIPTION</span></span>
<span data-ttu-id="c0e72-108">**Start-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 DSC(필요한 상태 구성) 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="c0e72-109">예제</span><span class="sxs-lookup"><span data-stu-id="c0e72-109">EXAMPLES</span></span>

### <span data-ttu-id="c0e72-110">예제 1: Automation에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="c0e72-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Yes

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 35b14eb4-52b7-4a1d-ad62-8e9f84adc657
Job                   : Microsoft.Azure.Commands.Automation.Model.Job
JobStatus             : New
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           :
JobScheduleId         : 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="c0e72-111">위의 명령은 "Config01.Node1"이라는 DSC 노드 구성을 주어진 노드 이름의 2차원 배열에 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c0e72-112">배포는 단계적 방식으로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="c0e72-113">예제 2: Automation에서 Azure DSC 노드 구성 배포 예약</span><span class="sxs-lookup"><span data-stu-id="c0e72-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzAutomationDscNodeConfigurationDeployment `
            -NodeConfigurationName "Config01.Node1" `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01" `
            -NodeName $nodes `
            -Schedule $sched

Starting a node configuration deployment.
Starting a node configuration deployment. It will override any existing node configurations assigned to the node.
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): Y

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobId                 : 00000000-0000-0000-0000-000000000000
Job                   :
JobStatus             :
NodeStatus            :
NodeConfigurationName : Config01.Node1
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
```

<span data-ttu-id="c0e72-114">위의 명령은 "Config01.Node1"이라는 DSC 노드 구성을 주어진 2차원 노드 배열에 배포하는 작업을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="c0e72-115">배포는 준비된 방식으로 수행되고 일정에 따라 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="c0e72-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c0e72-116">PARAMETERS</span></span>

### <span data-ttu-id="c0e72-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="c0e72-117">-AutomationAccountName</span></span>
<span data-ttu-id="c0e72-118">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="c0e72-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0e72-119">-DefaultProfile</span></span>
<span data-ttu-id="c0e72-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c0e72-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c0e72-121">-Force</span><span class="sxs-lookup"><span data-stu-id="c0e72-121">-Force</span></span>
<span data-ttu-id="c0e72-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="c0e72-122">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0e72-123">-InputObject</span></span>
<span data-ttu-id="c0e72-124">파이핑에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c0e72-124">Input object for Piping</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="c0e72-125">-NodeConfigurationName</span></span>
<span data-ttu-id="c0e72-126">이 cmdlet이 배포하는 DSC 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="c0e72-127">-NodeName</span></span>
<span data-ttu-id="c0e72-128">노드 구성을 배포할 노드의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: System.String[][]
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0e72-129">-ResourceGroupName</span></span>
<span data-ttu-id="c0e72-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="c0e72-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="c0e72-131">-Schedule</span></span>
<span data-ttu-id="c0e72-132">배포 작업을 예약하는 Automation Schedule 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: ByAll
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c0e72-133">-Confirm</span></span>
<span data-ttu-id="c0e72-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0e72-135">-WhatIf</span></span>
<span data-ttu-id="c0e72-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c0e72-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0e72-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-137">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0e72-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0e72-138">CommonParameters</span></span>
<span data-ttu-id="c0e72-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c0e72-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0e72-140">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c0e72-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0e72-141">입력</span><span class="sxs-lookup"><span data-stu-id="c0e72-141">INPUTS</span></span>

### <span data-ttu-id="c0e72-142">System.String</span><span class="sxs-lookup"><span data-stu-id="c0e72-142">System.String</span></span>

### <span data-ttu-id="c0e72-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c0e72-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c0e72-144">출력</span><span class="sxs-lookup"><span data-stu-id="c0e72-144">OUTPUTS</span></span>

### <span data-ttu-id="c0e72-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c0e72-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="c0e72-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c0e72-146">NOTES</span></span>

## <span data-ttu-id="c0e72-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0e72-147">RELATED LINKS</span></span>

[<span data-ttu-id="c0e72-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="c0e72-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="c0e72-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="c0e72-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="c0e72-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c0e72-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c0e72-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="c0e72-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="c0e72-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="c0e72-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="c0e72-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="c0e72-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
