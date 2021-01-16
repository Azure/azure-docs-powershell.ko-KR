---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 3e5ec84dd3560c07fbf68c6f566b4691c1f6e512
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344318"
---
# <span data-ttu-id="5963a-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5963a-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="5963a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5963a-102">SYNOPSIS</span></span>
<span data-ttu-id="5963a-103">Automation에서 DSC 노드 구성 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="5963a-104">현재 배포 작업만 중지하지만 이미 할당된 노드 구성의 할당을 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="5963a-105">구문</span><span class="sxs-lookup"><span data-stu-id="5963a-105">SYNTAX</span></span>

### <span data-ttu-id="5963a-106">ByJobId(기본값)</span><span class="sxs-lookup"><span data-stu-id="5963a-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="5963a-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="5963a-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5963a-108">설명</span><span class="sxs-lookup"><span data-stu-id="5963a-108">DESCRIPTION</span></span>
<span data-ttu-id="5963a-109">**Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 DSC(필요한 상태 구성) 노드 구성의 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="5963a-110">할당될 노드가 남아 있는 경우 노드 그룹에 대한 노드 구성 할당을 중지하지만 이미 할당된 노드의 할당을 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="5963a-111">예약된 작업을 등록을 등록하지 않은 경우 [JobScheduleId와 함께 Unregister-AzAutomationScheduledRunbook을](./Unregister-AzAutomationScheduledRunbook.md) 사용하여 기존 예약된 작업의 예약을 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="5963a-112">예제</span><span class="sxs-lookup"><span data-stu-id="5963a-112">EXAMPLES</span></span>

### <span data-ttu-id="5963a-113">예제 1: Automation에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="5963a-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="5963a-114">위의 명령은 jobId가 전달된 DSC 노드 구성 배포 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="5963a-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5963a-115">PARAMETERS</span></span>

### <span data-ttu-id="5963a-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="5963a-116">-AutomationAccountName</span></span>
<span data-ttu-id="5963a-117">이 cmdlet이 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="5963a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5963a-118">-DefaultProfile</span></span>
<span data-ttu-id="5963a-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5963a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5963a-120">-Force</span><span class="sxs-lookup"><span data-stu-id="5963a-120">-Force</span></span>
<span data-ttu-id="5963a-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="5963a-121">ps_force</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByJobId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5963a-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="5963a-122">-InputObject</span></span>
<span data-ttu-id="5963a-123">파이핑에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="5963a-123">Input object for Piping</span></span>

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

### <span data-ttu-id="5963a-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="5963a-124">-JobId</span></span>
<span data-ttu-id="5963a-125">기존 배포 작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="5963a-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5963a-126">-PassThru</span></span>
<span data-ttu-id="5963a-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5963a-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5963a-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5963a-129">-ResourceGroupName</span></span>
<span data-ttu-id="5963a-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="5963a-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5963a-131">-Confirm</span></span>
<span data-ttu-id="5963a-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5963a-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5963a-133">-WhatIf</span></span>
<span data-ttu-id="5963a-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5963a-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5963a-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5963a-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5963a-136">CommonParameters</span></span>
<span data-ttu-id="5963a-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5963a-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5963a-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5963a-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5963a-139">입력</span><span class="sxs-lookup"><span data-stu-id="5963a-139">INPUTS</span></span>

### <span data-ttu-id="5963a-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="5963a-140">System.Guid</span></span>

### <span data-ttu-id="5963a-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5963a-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="5963a-142">System.String</span><span class="sxs-lookup"><span data-stu-id="5963a-142">System.String</span></span>

## <span data-ttu-id="5963a-143">출력</span><span class="sxs-lookup"><span data-stu-id="5963a-143">OUTPUTS</span></span>

### <span data-ttu-id="5963a-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5963a-144">System.Boolean</span></span>

## <span data-ttu-id="5963a-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5963a-145">NOTES</span></span>

## <span data-ttu-id="5963a-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5963a-146">RELATED LINKS</span></span>

[<span data-ttu-id="5963a-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="5963a-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="5963a-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="5963a-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="5963a-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5963a-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5963a-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="5963a-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="5963a-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="5963a-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)