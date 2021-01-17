---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373717"
---
# <span data-ttu-id="38068-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="38068-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="38068-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38068-102">SYNOPSIS</span></span>
<span data-ttu-id="38068-103">Azure Automation 소프트웨어 업데이트 구성 머신 실행 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="38068-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="38068-104">구문</span><span class="sxs-lookup"><span data-stu-id="38068-104">SYNTAX</span></span>

### <span data-ttu-id="38068-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="38068-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="38068-106">ById</span><span class="sxs-lookup"><span data-stu-id="38068-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38068-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="38068-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="38068-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="38068-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="38068-109">설명</span><span class="sxs-lookup"><span data-stu-id="38068-109">DESCRIPTION</span></span>
<span data-ttu-id="38068-110">이 cmdlet은 컴퓨터 실행 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="38068-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="38068-111">각 소프트웨어 업데이트 실행은 각 소프트웨어 업데이트 구성 대상 머신에 대해 머신 실행을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="38068-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="38068-112">특정 머신 실행을 얻습니다. ID 매개 변수를 전달합니다.</span><span class="sxs-lookup"><span data-stu-id="38068-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="38068-113">모든 컴퓨터 실행, 특정 컴퓨터에 대한 모든 실행, 해당 매개 변수를 전달하여 특정 상태의 모든 실행을 나열할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38068-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="38068-114">예제</span><span class="sxs-lookup"><span data-stu-id="38068-114">EXAMPLES</span></span>

### <span data-ttu-id="38068-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="38068-115">Example 1</span></span>
<span data-ttu-id="38068-116">이 예제에서는 지정된 Azure 가상 머신에 대해 실패한 모든 컴퓨터 실행을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="38068-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


```powershell
PS C:\> $targetComputer = "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm"
PS C:\> Get-AzAutomationSoftwareUpdateMachineRun -ResourceGroupName "mygroup" `
                                                      -AutomationAccountName "myaccount" `
                                                      -TargetComputer $targetComputer `
                                                      -Status Failed

MachineRunId          : 0033d6d6-828d-4712-adab-293cc4fc8809
TargetComputer        : /subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/myvm
TargetComputerType    : AzureVirtualMachines
SoftwareUpdateRunId   : 46568d26-0182-49b2-8bfd-af3455780397
OperatingSystem       : Windows
Status                : Failed
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : 0033d6d6-828d-4712-adab-293cc4fc8809
CreationTime          : 5/17/2018 2:06:44 AM +00:00
LastModifiedTime      : 5/17/2018 2:08:49 AM +00:00
```

## <span data-ttu-id="38068-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="38068-117">PARAMETERS</span></span>

### <span data-ttu-id="38068-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="38068-118">-AutomationAccountName</span></span>
<span data-ttu-id="38068-119">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-119">The automation account name.</span></span>

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

### <span data-ttu-id="38068-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38068-120">-DefaultProfile</span></span>
<span data-ttu-id="38068-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="38068-122">-Id</span><span class="sxs-lookup"><span data-stu-id="38068-122">-Id</span></span>
<span data-ttu-id="38068-123">소프트웨어 업데이트 컴퓨터 실행의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-123">Id of the software update machine run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: ById
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38068-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38068-124">-ResourceGroupName</span></span>
<span data-ttu-id="38068-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-125">The resource group name.</span></span>

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

### <span data-ttu-id="38068-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="38068-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="38068-127">소프트웨어 업데이트가 실행됩니다.</span><span class="sxs-lookup"><span data-stu-id="38068-127">The software update run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun
Parameter Sets: BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38068-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="38068-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="38068-129">소프트웨어 업데이트 실행의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-129">Id of the software update run.</span></span>

```yaml
Type: System.Guid
Parameter Sets: BySucrId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38068-130">-Status</span><span class="sxs-lookup"><span data-stu-id="38068-130">-Status</span></span>
<span data-ttu-id="38068-131">컴퓨터 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-131">Status of the machine run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus]
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded, FailedToStart

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38068-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="38068-132">-TargetComputer</span></span>
<span data-ttu-id="38068-133">컴퓨터 실행을 위한 대상 컴퓨터입니다.</span><span class="sxs-lookup"><span data-stu-id="38068-133">target computer for the machine run.</span></span>
<span data-ttu-id="38068-134">az가 아닌 컴퓨터 이름 또는 Azure VM 리소스 ID일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="38068-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByAll, BySucrId, BySucr
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="38068-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38068-135">CommonParameters</span></span>
<span data-ttu-id="38068-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="38068-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38068-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="38068-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38068-138">입력</span><span class="sxs-lookup"><span data-stu-id="38068-138">INPUTS</span></span>

### <span data-ttu-id="38068-139">System.Guid</span><span class="sxs-lookup"><span data-stu-id="38068-139">System.Guid</span></span>

### <span data-ttu-id="38068-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="38068-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="38068-141">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="38068-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="38068-142">System.String</span><span class="sxs-lookup"><span data-stu-id="38068-142">System.String</span></span>

## <span data-ttu-id="38068-143">출력</span><span class="sxs-lookup"><span data-stu-id="38068-143">OUTPUTS</span></span>

### <span data-ttu-id="38068-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="38068-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="38068-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="38068-145">NOTES</span></span>

## <span data-ttu-id="38068-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38068-146">RELATED LINKS</span></span>
