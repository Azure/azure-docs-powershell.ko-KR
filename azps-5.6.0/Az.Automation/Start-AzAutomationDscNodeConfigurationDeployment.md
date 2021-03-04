---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/start-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Start-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 477b8f5853d9a5dbe3dd030e7419316825088807
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101957712"
---
# <span data-ttu-id="7560a-101">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7560a-101">Start-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="7560a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7560a-102">SYNOPSIS</span></span>
<span data-ttu-id="7560a-103">Automation에서 DSC 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-103">Deploys a DSC Node configuration in Automation.</span></span>

## <span data-ttu-id="7560a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7560a-104">SYNTAX</span></span>

### <span data-ttu-id="7560a-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="7560a-105">ByAll (Default)</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="7560a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="7560a-106">ByInputObject</span></span>
```
Start-AzAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String> [-NodeName] <String[][]>
 -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7560a-107">설명</span><span class="sxs-lookup"><span data-stu-id="7560a-107">DESCRIPTION</span></span>
<span data-ttu-id="7560a-108">**Start-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 원하는 상태 구성(DSC) 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-108">The **Start-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="7560a-109">예제</span><span class="sxs-lookup"><span data-stu-id="7560a-109">EXAMPLES</span></span>

### <span data-ttu-id="7560a-110">예제 1: Automation에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="7560a-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
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

<span data-ttu-id="7560a-111">위의 명령은 "Config01.Node1"이라는 DSC 노드 구성을 주어진 2차원 노드 이름 배열에 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="7560a-112">배포는 단계적 방식으로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="7560a-113">예제 2: Automation에서 Azure DSC 노드 구성 배포 예약</span><span class="sxs-lookup"><span data-stu-id="7560a-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
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

<span data-ttu-id="7560a-114">위의 명령은 주어진 2차원 노드 이름 배열에 "Config01.Node1"이라는 DSC 노드 구성 배포를 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="7560a-115">배포는 준비된 방식으로 수행되고 일정에 따라 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="7560a-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7560a-116">PARAMETERS</span></span>

### <span data-ttu-id="7560a-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="7560a-117">-AutomationAccountName</span></span>
<span data-ttu-id="7560a-118">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="7560a-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7560a-119">-DefaultProfile</span></span>
<span data-ttu-id="7560a-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7560a-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7560a-121">-Force</span><span class="sxs-lookup"><span data-stu-id="7560a-121">-Force</span></span>
<span data-ttu-id="7560a-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="7560a-122">ps_force</span></span>

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

### <span data-ttu-id="7560a-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="7560a-123">-InputObject</span></span>
<span data-ttu-id="7560a-124">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="7560a-124">Input object for Piping</span></span>

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

### <span data-ttu-id="7560a-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7560a-125">-NodeConfigurationName</span></span>
<span data-ttu-id="7560a-126">이 cmdlet이 배포하는 DSC 노드 구성의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

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

### <span data-ttu-id="7560a-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="7560a-127">-NodeName</span></span>
<span data-ttu-id="7560a-128">노드 구성이 배포될 노드의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

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

### <span data-ttu-id="7560a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7560a-129">-ResourceGroupName</span></span>
<span data-ttu-id="7560a-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="7560a-131">-Schedule</span><span class="sxs-lookup"><span data-stu-id="7560a-131">-Schedule</span></span>
<span data-ttu-id="7560a-132">Automation Schedule 개체를 통해 배포 작업을 예약합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-132">Automation Schedule object to schedule the deployment job.</span></span>

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

### <span data-ttu-id="7560a-133">-확인</span><span class="sxs-lookup"><span data-stu-id="7560a-133">-Confirm</span></span>
<span data-ttu-id="7560a-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7560a-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7560a-135">-WhatIf</span></span>
<span data-ttu-id="7560a-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7560a-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7560a-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7560a-138">CommonParameters</span></span>
<span data-ttu-id="7560a-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7560a-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7560a-140">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7560a-140">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7560a-141">입력</span><span class="sxs-lookup"><span data-stu-id="7560a-141">INPUTS</span></span>

### <span data-ttu-id="7560a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="7560a-142">System.String</span></span>

### <span data-ttu-id="7560a-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7560a-143">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="7560a-144">출력</span><span class="sxs-lookup"><span data-stu-id="7560a-144">OUTPUTS</span></span>

### <span data-ttu-id="7560a-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7560a-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="7560a-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7560a-146">NOTES</span></span>

## <span data-ttu-id="7560a-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7560a-147">RELATED LINKS</span></span>

[<span data-ttu-id="7560a-148">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="7560a-148">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="7560a-149">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="7560a-149">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="7560a-150">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7560a-150">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7560a-151">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="7560a-151">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="7560a-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="7560a-152">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="7560a-153">New-AzAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="7560a-153">New-AzAutomationSchedule</span></span>](./New-AzAutomationSchedule.md)
