---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdatemachinerun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateMachineRun.md
ms.openlocfilehash: 19c0321b1c915519b7c3617b52810da18e534521
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94049219"
---
# <span data-ttu-id="337d8-101">Get-AzAutomationSoftwareUpdateMachineRun</span><span class="sxs-lookup"><span data-stu-id="337d8-101">Get-AzAutomationSoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="337d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="337d8-102">SYNOPSIS</span></span>
<span data-ttu-id="337d8-103">Azure automation 소프트웨어 업데이트 구성 컴퓨터 실행 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-103">Gets a list of azure automation software update configuration machine runs.</span></span>

## <span data-ttu-id="337d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="337d8-104">SYNTAX</span></span>

### <span data-ttu-id="337d8-105">ByAll (기본값)</span><span class="sxs-lookup"><span data-stu-id="337d8-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="337d8-106">ById</span><span class="sxs-lookup"><span data-stu-id="337d8-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun -Id <Guid> [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="337d8-107">BySucrId</span><span class="sxs-lookup"><span data-stu-id="337d8-107">BySucrId</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRunId <Guid>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="337d8-108">BySucr</span><span class="sxs-lookup"><span data-stu-id="337d8-108">BySucr</span></span>
```
Get-AzAutomationSoftwareUpdateMachineRun [-SoftwareUpdateRun <SoftwareUpdateRun>]
 [-Status <SoftwareUpdateMachineRunStatus>] [-TargetComputer <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="337d8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="337d8-109">DESCRIPTION</span></span>
<span data-ttu-id="337d8-110">이 cmdlet은 컴퓨터 실행 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-110">This cmdlet returns a list of machine runs.</span></span> <span data-ttu-id="337d8-111">각 소프트웨어 업데이트 실행은 소프트웨어 업데이트 구성 대상 컴퓨터 각각에 대해 컴퓨터 실행을 트리거합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-111">Each software update run will trigger a machine run for each of the software update configuration target machine.</span></span> <span data-ttu-id="337d8-112">특정 컴퓨터 실행을 얻으려면 Id 매개 변수를 전달 합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-112">To get a specific machine run, pass the Id parameter.</span></span> <span data-ttu-id="337d8-113">모든 컴퓨터 실행을 나열할 수 있으며, 특정 컴퓨터에 대해 모두 실행 되며, 해당 매개 변수를 전달 하 여 모든 작업을 특정 상태로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-113">You can list all the machine runs, all runs for a specific computer, all runs with specific status by passing the corresponding parameters.</span></span>

## <span data-ttu-id="337d8-114">예제의</span><span class="sxs-lookup"><span data-stu-id="337d8-114">EXAMPLES</span></span>

### <span data-ttu-id="337d8-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="337d8-115">Example 1</span></span>
<span data-ttu-id="337d8-116">이 예제에서는 지정 된 azure 가상 컴퓨터에 대해 실패 한 모든 시스템 실행을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-116">This example returns all failed machine runs for the specified azure virtual machine.</span></span>


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

## <span data-ttu-id="337d8-117">변수</span><span class="sxs-lookup"><span data-stu-id="337d8-117">PARAMETERS</span></span>

### <span data-ttu-id="337d8-118">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="337d8-118">-AutomationAccountName</span></span>
<span data-ttu-id="337d8-119">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-119">The automation account name.</span></span>

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

### <span data-ttu-id="337d8-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="337d8-120">-DefaultProfile</span></span>
<span data-ttu-id="337d8-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="337d8-122">-Id</span><span class="sxs-lookup"><span data-stu-id="337d8-122">-Id</span></span>
<span data-ttu-id="337d8-123">소프트웨어 업데이트 컴퓨터 실행의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-123">Id of the software update machine run.</span></span>

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

### <span data-ttu-id="337d8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="337d8-124">-ResourceGroupName</span></span>
<span data-ttu-id="337d8-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-125">The resource group name.</span></span>

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

### <span data-ttu-id="337d8-126">-SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="337d8-126">-SoftwareUpdateRun</span></span>
<span data-ttu-id="337d8-127">소프트웨어 업데이트가 실행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-127">The software update run.</span></span>

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

### <span data-ttu-id="337d8-128">-SoftwareUpdateRunId</span><span class="sxs-lookup"><span data-stu-id="337d8-128">-SoftwareUpdateRunId</span></span>
<span data-ttu-id="337d8-129">소프트웨어 업데이트 실행의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-129">Id of the software update run.</span></span>

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

### <span data-ttu-id="337d8-130">-상태</span><span class="sxs-lookup"><span data-stu-id="337d8-130">-Status</span></span>
<span data-ttu-id="337d8-131">컴퓨터 실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-131">Status of the machine run.</span></span>

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

### <span data-ttu-id="337d8-132">-TargetComputer</span><span class="sxs-lookup"><span data-stu-id="337d8-132">-TargetComputer</span></span>
<span data-ttu-id="337d8-133">컴퓨터 실행을 위한 대상 컴퓨터.</span><span class="sxs-lookup"><span data-stu-id="337d8-133">target computer for the machine run.</span></span>
<span data-ttu-id="337d8-134">Az가 아닌 컴퓨터 이름 또는 azure VM 리소스 id 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-134">Can be either a non-az computer name or an azure VM resource id.</span></span>

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

### <span data-ttu-id="337d8-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="337d8-135">CommonParameters</span></span>
<span data-ttu-id="337d8-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="337d8-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="337d8-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="337d8-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="337d8-138">입력</span><span class="sxs-lookup"><span data-stu-id="337d8-138">INPUTS</span></span>

### <span data-ttu-id="337d8-139">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="337d8-139">System.Guid</span></span>

### <span data-ttu-id="337d8-140">UpdateManagement. SoftwareUpdateRun에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="337d8-140">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

### <span data-ttu-id="337d8-141">시스템 Null 허용 ' 1 [[UpdateManagement]. SoftwareUpdateMachineRunStatus, Microsoft azure. PowerShell. t i = 1.0.0.0, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="337d8-141">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="337d8-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="337d8-142">System.String</span></span>

## <span data-ttu-id="337d8-143">출력</span><span class="sxs-lookup"><span data-stu-id="337d8-143">OUTPUTS</span></span>

### <span data-ttu-id="337d8-144">UpdateManagement. SoftwareUpdateMachineRun에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="337d8-144">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateMachineRun</span></span>

## <span data-ttu-id="337d8-145">상속자</span><span class="sxs-lookup"><span data-stu-id="337d8-145">NOTES</span></span>

## <span data-ttu-id="337d8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="337d8-146">RELATED LINKS</span></span>
