---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 32CF9BF7-519F-4B5D-9F2B-3CC556A77A48
online version: https://docs.microsoft.com/powershell/module/az.automation/stop-azautomationdscnodeconfigurationdeployment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Stop-AzAutomationDscNodeConfigurationDeployment.md
ms.openlocfilehash: 726423dfcfef07142002cd40b29b6e4d26f91137
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978912"
---
# <span data-ttu-id="cd46b-101">Stop-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="cd46b-101">Stop-AzAutomationDscNodeConfigurationDeployment</span></span>

## <span data-ttu-id="cd46b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd46b-102">SYNOPSIS</span></span>
<span data-ttu-id="cd46b-103">Automation에서 DSC 노드 구성 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-103">Stops a DSC Node configuration deployment in Automation.</span></span> <span data-ttu-id="cd46b-104">현재 배포 작업만 중지하지만 이미 할당된 노드 구성을 할당하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-104">It only stops the current deployment job but does not unassign already assigned node configurations.</span></span>

## <span data-ttu-id="cd46b-105">구문</span><span class="sxs-lookup"><span data-stu-id="cd46b-105">SYNTAX</span></span>

### <span data-ttu-id="cd46b-106">ByJobId(기본값)</span><span class="sxs-lookup"><span data-stu-id="cd46b-106">ByJobId (Default)</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment -JobId <Guid> [-Force] [-PassThru]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="cd46b-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="cd46b-107">ByInputObject</span></span>
```
Stop-AzAutomationDscNodeConfigurationDeployment [-PassThru] -InputObject <NodeConfigurationDeployment>
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="cd46b-108">설명</span><span class="sxs-lookup"><span data-stu-id="cd46b-108">DESCRIPTION</span></span>
<span data-ttu-id="cd46b-109">**Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet은 Azure Automation에서 원하는 상태 구성(DSC) 노드 구성의 배포를 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-109">The **Stop-AzAutomationDscNodeConfigurationDeployment** cmdlet stops a deployment of a Desired State Configuration (DSC) node configuration in Azure Automation.</span></span> <span data-ttu-id="cd46b-110">할당될 노드가 남아 있는 경우 노드 구성의 할당을 중지하지만 이미 할당된 노드의 할당을 제거하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-110">It stops assignment of node configuration to groups of nodes, if any are remaining to be assigned, but does not unassign already assigned nodes.</span></span> <span data-ttu-id="cd46b-111">예약된 작업을 등록을 등록하지 않은 경우 JobScheduleId와 함께 [Unregister-AzAutomationScheduledRunbook을](./Unregister-AzAutomationScheduledRunbook.md) 사용하여 기존 예약된 작업의 예약을 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-111">To unregister a scheduled job, please use the [Unregister-AzAutomationScheduledRunbook](./Unregister-AzAutomationScheduledRunbook.md) with the JobScheduleId to unassign an existing scheduled job.</span></span>

## <span data-ttu-id="cd46b-112">예제</span><span class="sxs-lookup"><span data-stu-id="cd46b-112">EXAMPLES</span></span>

### <span data-ttu-id="cd46b-113">예제 1: Automation에서 Azure DSC 노드 구성 배포</span><span class="sxs-lookup"><span data-stu-id="cd46b-113">Example 1: Deploy an Azure DSC node configuration in Automation</span></span>
```
PS C:\> Stop-AzAutomationDscNodeConfigurationDeployment -AutomationAccountName "Contoso01" -ResourceGroupName "ResourceGroup01" -JobId 00000000-0000-0000-0000-000000000000
```

<span data-ttu-id="cd46b-114">위의 명령은 jobId가 전달된 DSC 노드 구성 배포 작업을 중지합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-114">The above command stops the DSC node configuration deployment job with the jobId passed in.</span></span>

## <span data-ttu-id="cd46b-115">매개 변수</span><span class="sxs-lookup"><span data-stu-id="cd46b-115">PARAMETERS</span></span>

### <span data-ttu-id="cd46b-116">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="cd46b-116">-AutomationAccountName</span></span>
<span data-ttu-id="cd46b-117">이 cmdlet에서 컴파일하는 DSC 구성을 포함하는 Automation 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-117">Specifies the name of the Automation account that contains the DSC configuration that this cmdlet compiles</span></span>

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

### <span data-ttu-id="cd46b-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd46b-118">-DefaultProfile</span></span>
<span data-ttu-id="cd46b-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="cd46b-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd46b-120">-Force</span><span class="sxs-lookup"><span data-stu-id="cd46b-120">-Force</span></span>
<span data-ttu-id="cd46b-121">ps_force</span><span class="sxs-lookup"><span data-stu-id="cd46b-121">ps_force</span></span>

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

### <span data-ttu-id="cd46b-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="cd46b-122">-InputObject</span></span>
<span data-ttu-id="cd46b-123">Piping에 대한 입력 개체</span><span class="sxs-lookup"><span data-stu-id="cd46b-123">Input object for Piping</span></span>

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

### <span data-ttu-id="cd46b-124">-JobId</span><span class="sxs-lookup"><span data-stu-id="cd46b-124">-JobId</span></span>
<span data-ttu-id="cd46b-125">기존 배포 작업의 작업 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-125">Specifies the Job id of an existing deployment job.</span></span>

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

### <span data-ttu-id="cd46b-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="cd46b-126">-PassThru</span></span>
<span data-ttu-id="cd46b-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-127">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="cd46b-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="cd46b-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="cd46b-129">-ResourceGroupName</span></span>
<span data-ttu-id="cd46b-130">이 cmdlet이 구성을 컴파일하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-130">Specifies the name of a resource group in which this cmdlet compiles a configuration.</span></span>

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

### <span data-ttu-id="cd46b-131">-확인</span><span class="sxs-lookup"><span data-stu-id="cd46b-131">-Confirm</span></span>
<span data-ttu-id="cd46b-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="cd46b-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="cd46b-133">-WhatIf</span></span>
<span data-ttu-id="cd46b-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="cd46b-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="cd46b-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd46b-136">CommonParameters</span></span>
<span data-ttu-id="cd46b-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="cd46b-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd46b-138">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="cd46b-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd46b-139">입력</span><span class="sxs-lookup"><span data-stu-id="cd46b-139">INPUTS</span></span>

### <span data-ttu-id="cd46b-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="cd46b-140">System.Guid</span></span>

### <span data-ttu-id="cd46b-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="cd46b-141">Microsoft.Azure.Commands.Automation.Model.NodeConfigurationDeployment</span></span>

### <span data-ttu-id="cd46b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="cd46b-142">System.String</span></span>

## <span data-ttu-id="cd46b-143">출력</span><span class="sxs-lookup"><span data-stu-id="cd46b-143">OUTPUTS</span></span>

### <span data-ttu-id="cd46b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="cd46b-144">System.Boolean</span></span>

## <span data-ttu-id="cd46b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="cd46b-145">NOTES</span></span>

## <span data-ttu-id="cd46b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="cd46b-146">RELATED LINKS</span></span>

[<span data-ttu-id="cd46b-147">Start-AzAutomationDscCompilationJob</span><span class="sxs-lookup"><span data-stu-id="cd46b-147">Start-AzAutomationDscCompilationJob</span></span>](./Start-AzAutomationDscCompilationJob.md)

[<span data-ttu-id="cd46b-148">Import-AzAutomationDscNodeConfiguration</span><span class="sxs-lookup"><span data-stu-id="cd46b-148">Import-AzAutomationDscNodeConfiguration</span></span>](./Import-AzAutomationDscNodeConfiguration.md)

[<span data-ttu-id="cd46b-149">Start-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="cd46b-149">Start-AzAutomationDscNodeConfigurationDeployment</span></span>](./Start-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="cd46b-150">Get-AzAutomationDscNodeConfigurationDeployment</span><span class="sxs-lookup"><span data-stu-id="cd46b-150">Get-AzAutomationDscNodeConfigurationDeployment</span></span>](./Get-AzAutomationDscNodeConfigurationDeployment.md)

[<span data-ttu-id="cd46b-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span><span class="sxs-lookup"><span data-stu-id="cd46b-151">Get-AzAutomationDscNodeConfigurationDeploymentSchedule</span></span>](./Get-AzAutomationDscNodeConfigurationDeploymentSchedule.md)
