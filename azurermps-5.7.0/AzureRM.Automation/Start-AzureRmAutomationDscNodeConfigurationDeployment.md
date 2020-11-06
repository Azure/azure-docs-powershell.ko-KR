---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/start-azurermautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/Start-AzureRmAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 61018e7713f2e19da646b69d75c89699da86a0c0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529035"
---
# <span data-ttu-id="5dfbb-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5dfbb-101">Start-AzureRmAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5dfbb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5dfbb-102">SYNOPSIS</span></span>
<span data-ttu-id="5dfbb-103">자동화에서 DSC 노드 구성을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-103">Deploys a DSC Node configuration in Automation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5dfbb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5dfbb-104">SYNTAX</span></span>

### <span data-ttu-id="5dfbb-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="5dfbb-105">ByAll (Default)</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> [-Schedule <Schedule>] [-Force] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5dfbb-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5dfbb-106">ByInputObject</span></span>
```
Start-AzureRmAutomationDscNodeConfigurationDeployment [-NodeConfigurationName] <String>
 [-NodeName] <String[][]> -InputObject <NodeConfigurationDeployment> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5dfbb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5dfbb-107">DESCRIPTION</span></span>
<span data-ttu-id="5dfbb-108">AzureRmAutomationDscNodeConfigurationDeployment cmdlet은 Azure Automation의 DSC (원하는 상태 구성) 노드 구성을 **실행** 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-108">The **Start-AzureRmAutomationDscNodeConfigurationDeployment** cmdlet deployes a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="5dfbb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5dfbb-109">EXAMPLES</span></span>

### <span data-ttu-id="5dfbb-110">예제 1: 자동화에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="5dfbb-110">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="5dfbb-111">위의 명령은 노드 이름의 지정 된 2 차원 배열에 "Config01" 라는 DSC 노드 구성을 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-111">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="5dfbb-112">구축은 미리 준비 된 방식으로 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-112">The deployment happens in a staged manner.</span></span>

### <span data-ttu-id="5dfbb-113">예제 2: 자동화에서 Azure DSC 노드 구성 배포 예약</span><span class="sxs-lookup"><span data-stu-id="5dfbb-113">Example 2: Schedule an Azure DSC node configuration deployment in Automation</span></span>
```
PS C:\> $sched = New-AzureRmAutomationSchedule -AutomationAccountName "Contoso01" `
            -ResourceGroupName "ResourceGroup01" `
            -Name "TestSchedule" `
            -StartTime "23:00" `
            -OneTime
PS C:\> $pilot = @("WebServerPilot1", "WebServerPilot2")
PS C:\> $prod = @("WebServerProd1", "WebServerProd2")
PS C:\> $nodes = @($pilot, $prod)
PS C:\> Start-AzureRmAutomationDscNodeConfigurationDeployment `
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

<span data-ttu-id="5dfbb-114">위의 명령은 노드 이름의 지정 된 2 차원 배열에 "Config01" 이라는 DSC 노드 구성의 배포를 예약 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-114">The above command schedules a deployment of a DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="5dfbb-115">구축은 미리 준비 된 방식으로 진행 되며 일정에 따라 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-115">The deployment happens in a staged manner and will be executed based on the schedule.</span></span>

## <span data-ttu-id="5dfbb-116">변수</span><span class="sxs-lookup"><span data-stu-id="5dfbb-116">PARAMETERS</span></span>

### <span data-ttu-id="5dfbb-117">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5dfbb-117">-AutomationAccountName</span></span>
<span data-ttu-id="5dfbb-118">이 cmdlet이 컴파일하는 DSC 구성을 포함 하는 Automation 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-118">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5dfbb-119">-DefaultProfile</span></span>
<span data-ttu-id="5dfbb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5dfbb-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5dfbb-121">-Force</span></span>
<span data-ttu-id="5dfbb-122">ps_force</span><span class="sxs-lookup"><span data-stu-id="5dfbb-122">ps_force</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5dfbb-123">-InputObject</span></span>
<span data-ttu-id="5dfbb-124">파이핑에 대 한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="5dfbb-124">Input object for Piping</span></span>

```yaml
Type: NodeConfigurationDeployment
Parameter Sets: ByInputObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-125">-NodeConfigurationName</span><span class="sxs-lookup"><span data-stu-id="5dfbb-125">-NodeConfigurationName</span></span>
<span data-ttu-id="5dfbb-126">이 cmdlet이 배포 하는 DSC 노드 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-126">Specifies the name of the DSC node configuration that this cmdlet deploys.</span></span>

```yaml
Type: String
Parameter Sets: ByAll
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByInputObject
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-127">-NodeName</span><span class="sxs-lookup"><span data-stu-id="5dfbb-127">-NodeName</span></span>
<span data-ttu-id="5dfbb-128">노드 구성을 배포할 노드의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-128">Specifies the names of the nodes to which the Node Configuration would be deployed to.</span></span>

```yaml
Type: String[][]
Parameter Sets: (All)
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5dfbb-129">-ResourceGroupName</span></span>
<span data-ttu-id="5dfbb-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-131">-일정</span><span class="sxs-lookup"><span data-stu-id="5dfbb-131">-Schedule</span></span>
<span data-ttu-id="5dfbb-132">배포 작업을 예약 하는 자동화 일정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-132">Automation Schedule object to schedule the deployment job.</span></span>

```yaml
Type: Schedule
Parameter Sets: ByAll
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-133">-확인</span><span class="sxs-lookup"><span data-stu-id="5dfbb-133">-Confirm</span></span>
<span data-ttu-id="5dfbb-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-134">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5dfbb-135">-WhatIf</span></span>
<span data-ttu-id="5dfbb-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-136">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5dfbb-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-137">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5dfbb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5dfbb-138">CommonParameters</span></span>
<span data-ttu-id="5dfbb-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5dfbb-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5dfbb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5dfbb-141">입력</span><span class="sxs-lookup"><span data-stu-id="5dfbb-141">INPUTS</span></span>

### <span data-ttu-id="5dfbb-142">않아야</span><span class="sxs-lookup"><span data-stu-id="5dfbb-142">None</span></span>
<span data-ttu-id="5dfbb-143">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-143">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="5dfbb-144">출력</span><span class="sxs-lookup"><span data-stu-id="5dfbb-144">OUTPUTS</span></span>

### <span data-ttu-id="5dfbb-145">NodeConfigurationDeployment를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="5dfbb-145">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

## <span data-ttu-id="5dfbb-146">상속자</span><span class="sxs-lookup"><span data-stu-id="5dfbb-146">NOTES</span></span>

## <span data-ttu-id="5dfbb-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5dfbb-147">RELATED LINKS</span></span>

[<span data-ttu-id="5dfbb-148">시작-AzureRmAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5dfbb-148">Start-AzureRmAutomationDscCompilationJob</span></span>](./Start-AzureRmAutomationDscCompilationJob.md)

[<span data-ttu-id="5dfbb-149">가져오기-AzureRmAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5dfbb-149">Import-AzureRmAutomationDscNodeConfiguration</span></span>](./Import-AzureRmAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5dfbb-150">중지-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5dfbb-150">Stop-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5dfbb-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5dfbb-151">Get-AzureRmAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5dfbb-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5dfbb-152">Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzureRmAutomationDscNodeConfigurationDeploymentSchedule.md)

[<span data-ttu-id="5dfbb-153">새로운 AzureRmAutomationSchedule</span><span class="sxs-lookup"><span data-stu-id="5dfbb-153">New-AzureRmAutomationSchedule</span></span>](./New-AzureRmAutomationSchedule.md)
