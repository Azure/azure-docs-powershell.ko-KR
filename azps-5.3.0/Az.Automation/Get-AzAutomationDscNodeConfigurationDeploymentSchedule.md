---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationdscnodeconfigurationdeploymentschedule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md
ms.openlocfilehash: bc98d8ed8773e49eab594a4d715bef3f93862e83
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494338"
---
# <span data-ttu-id="67236-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="67236-101">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="67236-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67236-102">SYNOPSIS</span></span>
<span data-ttu-id="67236-103">Automation에서 DSC 노드 구성 배포 작업 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67236-103">Gets a DSC Node configuration deployment job schedule in Automation.</span></span>

## <span data-ttu-id="67236-104">구문</span><span class="sxs-lookup"><span data-stu-id="67236-104">SYNTAX</span></span>

### <span data-ttu-id="67236-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="67236-105">ByAll (Default)</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="67236-106">ByJobScheduleId</span><span class="sxs-lookup"><span data-stu-id="67236-106">ByJobScheduleId</span></span>
```
Get-AzAutomationDscNodeConfigurationDeploymentSchedule -JobScheduleId <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="67236-107">설명</span><span class="sxs-lookup"><span data-stu-id="67236-107">DESCRIPTION</span></span>
<span data-ttu-id="67236-108">**Get-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 APS DSC(필요한 상태 구성) 노드 구성을 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-108">The **Get-AzAutomationDscNodeConfigurationDeployment** cmdlet deploys an APS Desired State Configuration (DSC) node configuration in Azure Automation.</span></span>

## <span data-ttu-id="67236-109">예제</span><span class="sxs-lookup"><span data-stu-id="67236-109">EXAMPLES</span></span>

### <span data-ttu-id="67236-110">예제 1: 모든 배포 일정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="67236-110">Example 1: Get all the deployment schedules</span></span>
```
PS C:\> Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
            -AutomationAccountName "Contoso01"  `
            -ResourceGroupName "ResourceGroup01"

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : e347dfc4-62fe-4ed6-adfb-55518c57b558
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSchedule
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
```

### <span data-ttu-id="67236-111">예제 2: 배포 일정 얻기</span><span class="sxs-lookup"><span data-stu-id="67236-111">Example 2: Get a deployment schedule</span></span>
```
PS C:\> $js= Get-AzAutomationDscNodeConfigurationDeploymentSchedule `
                 -AutomationAccountName "Contoso01" `
                 -ResourceGroupName "ResourceGroup01" `
                 -JobScheduleId 2b1d7738-093d-4ff7-b87b-e4b2321319e5

PS C:\> $js

ResourceGroupName     : ResourceGroup01
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
JobSchedule           : Microsoft.Azure.Commands.Automation.Model.JobSche
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1

PS C:\> $js.JobSchedule

ResourceGroupName     : ResourceGroup01
RunOn                 :
AutomationAccountName : Contoso01
JobScheduleId         : 2b1d7738-093d-4ff7-b87b-e4b2321319e5
RunbookName           : Deploy-NodeConfigurationToAutomationDscNodesV1
ScheduleName          : TestScheduleName
Parameters            : {AutomationAccountName, NodeConfigurationName, ResourceGroupName, ListOfNodeNames}
HybridWorker          :
```

<span data-ttu-id="67236-112">위의 명령은 "Config01.Node1"이라는 DSC 노드 구성을 주어진 노드 이름의 2차원 배열에 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-112">The above command deploys the DSC node configuration named "Config01.Node1" to the given two-dimensional array of Node Names.</span></span> <span data-ttu-id="67236-113">배포는 단계적 방식으로 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-113">The deployment happens in a staged manner.</span></span>

## <span data-ttu-id="67236-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="67236-114">PARAMETERS</span></span>

### <span data-ttu-id="67236-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="67236-115">-AutomationAccountName</span></span>
<span data-ttu-id="67236-116">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-116">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles.</span></span>

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

### <span data-ttu-id="67236-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67236-117">-DefaultProfile</span></span>
<span data-ttu-id="67236-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="67236-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="67236-119">-JobScheduleId</span><span class="sxs-lookup"><span data-stu-id="67236-119">-JobScheduleId</span></span>
<span data-ttu-id="67236-120">기존 예약된 배포 작업의 작업 일정 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-120">Specifies the Job Schedule id of an existing scheduled deployment job.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ByJobScheduleId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="67236-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="67236-121">-ResourceGroupName</span></span>
<span data-ttu-id="67236-122">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-122">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="67236-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67236-123">CommonParameters</span></span>
<span data-ttu-id="67236-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="67236-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67236-125">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="67236-125">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67236-126">입력</span><span class="sxs-lookup"><span data-stu-id="67236-126">INPUTS</span></span>

### <span data-ttu-id="67236-127">System.Guid</span><span class="sxs-lookup"><span data-stu-id="67236-127">System.Guid</span></span>

### <span data-ttu-id="67236-128">System.String</span><span class="sxs-lookup"><span data-stu-id="67236-128">System.String</span></span>

## <span data-ttu-id="67236-129">출력</span><span class="sxs-lookup"><span data-stu-id="67236-129">OUTPUTS</span></span>

### <span data-ttu-id="67236-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="67236-130">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeploymentSchedule</span></span>

## <span data-ttu-id="67236-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="67236-131">NOTES</span></span>

## <span data-ttu-id="67236-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="67236-132">RELATED LINKS</span></span>

[<span data-ttu-id="67236-133">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="67236-133">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="67236-134">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="67236-134">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="67236-135">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="67236-135">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="67236-136">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="67236-136">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>](./Stop-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="67236-137">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="67236-137">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)
