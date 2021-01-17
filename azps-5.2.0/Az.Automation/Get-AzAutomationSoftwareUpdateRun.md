---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/get-azautomationsoftwareupdaterun
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Get-AzAutomationSoftwareUpdateRun.md
ms.openlocfilehash: d93820d12a2f61714c58341f835bef8cba832b84
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98373710"
---
# <span data-ttu-id="8ca84-101">Get-AzAutomationSoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8ca84-101">Get-AzAutomationSoftwareUpdateRun</span></span>

## <span data-ttu-id="8ca84-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8ca84-102">SYNOPSIS</span></span>
<span data-ttu-id="8ca84-103">Azure Automation 소프트웨어 업데이트 실행 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-103">Gets a list of azure automation software update runs.</span></span>

## <span data-ttu-id="8ca84-104">구문</span><span class="sxs-lookup"><span data-stu-id="8ca84-104">SYNTAX</span></span>

### <span data-ttu-id="8ca84-105">ByAll(기본값)</span><span class="sxs-lookup"><span data-stu-id="8ca84-105">ByAll (Default)</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>]
 [-StartTime <DateTimeOffset>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ca84-106">ById</span><span class="sxs-lookup"><span data-stu-id="8ca84-106">ById</span></span>
```
Get-AzAutomationSoftwareUpdateRun -Id <Guid> [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="8ca84-107">BySucName</span><span class="sxs-lookup"><span data-stu-id="8ca84-107">BySucName</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfigurationName <String>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8ca84-108">BySuc</span><span class="sxs-lookup"><span data-stu-id="8ca84-108">BySuc</span></span>
```
Get-AzAutomationSoftwareUpdateRun [-SoftwareUpdateConfiguration <SoftwareUpdateConfiguration>]
 [-OperatingSystem <OperatingSystemType>] [-Status <SoftwareUpdateRunStatus>] [-StartTime <DateTimeOffset>]
 [-ResourceGroupName] <String> [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8ca84-109">설명</span><span class="sxs-lookup"><span data-stu-id="8ca84-109">DESCRIPTION</span></span>
<span data-ttu-id="8ca84-110">Get-AzAutomationSoftwareUpdateRun cmdlet은 소프트웨어 업데이트 실행 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-110">The Get-AzAutomationSoftwareUpdateRun cmdlet returns a list of software update runs.</span></span> <span data-ttu-id="8ca84-111">소프트웨어 업데이트 구성에는 연결된 일정이 적용되어 여러 번 트리거될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-111">Since a software update configuration has an associated schedule, it can be triggered multiple times.</span></span> <span data-ttu-id="8ca84-112">일정이 트리거될 때마다 업데이트 실행이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-112">Each time a schedule is triggered will result in an update run created.</span></span> <span data-ttu-id="8ca84-113">업데이트 실행은 모든 컴퓨터 실행의 결과 집계입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-113">Update run is an aggregate of the result of all machine runs.</span></span> <span data-ttu-id="8ca84-114">SoftwareUpdateConfigurationName 매개 변수를 전달하여 특정 소프트웨어 업데이트 구성에 대한 실행을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-114">You can get runs for specific software update configuration by passing the SoftwareUpdateConfigurationName parameter.</span></span> <span data-ttu-id="8ca84-115">특정 실행을 얻습니다. 이름 매개 변수를 전달해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-115">To get a specific runs, you need to pass the name parameter.</span></span> <span data-ttu-id="8ca84-116">특정 상태의 실행을 나열하거나, 특정 운영 체제를 대상으로 실행하거나, 적절한 매개 변수를 전달하여 특정 시간 후에 시작된 실행을 나열할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-116">You can also list runs with specific status, runs targeting specific operating system, or runs started after specific time by passing the appropriate parameter.</span></span>

## <span data-ttu-id="8ca84-117">예제</span><span class="sxs-lookup"><span data-stu-id="8ca84-117">EXAMPLES</span></span>

### <span data-ttu-id="8ca84-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="8ca84-118">Example 1</span></span>
<span data-ttu-id="8ca84-119">이 예제에서는 특정 소프트웨어 업데이트 구성에 의해 트리거되는 모든 업데이트 실행을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-119">This example list all update runs triggered by a specific software update configuration.</span></span>

```powershell
PS C:\> Get-AzAutomationSoftwareUpdateRun -ResourceGroupName "mygroup" `
                                               -AutomationAccountName "myaccount" `
                                               -SoftwareUpdateConfigurationName "MyUpdateConfiguration"

RunId                           : ec9ce57f-da18-44be-b33b-651a0f93cb52
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 11:37:42 PM +00:00
EndTime                         : 5/22/2018 11:38:31 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ec9ce57f-da18-44be-b33b-651a0f93cb52
CreationTime                    : 5/22/2018 11:37:42 PM +00:00
LastModifiedTime                : 5/22/2018 11:38:54 PM +00:00
Description                     :

RunId                           : ac9396c7-a837-43d4-be97-fbfe46c80baa
SoftwareUpdateConfigurationName : MyUpdateConfiguration
ConfiguredDuration              : 02:00:00
OperatingSystem                 : Windows
StartTime                       : 5/22/2018 10:00:47 PM +00:00
EndTime                         : 5/22/2018 10:02:20 PM +00:00
ComputerCount                   : 2
FailedCount                     : 0
ResourceGroupName               : mygroup
AutomationAccountName           : myaccount
Name                            : ac9396c7-a837-43d4-be97-fbfe46c80baa
CreationTime                    : 5/22/2018 10:00:47 PM +00:00
LastModifiedTime                : 5/22/2018 10:02:58 PM +00:00
```

## <span data-ttu-id="8ca84-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8ca84-120">PARAMETERS</span></span>

### <span data-ttu-id="8ca84-121">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8ca84-121">-AutomationAccountName</span></span>
<span data-ttu-id="8ca84-122">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-122">The automation account name.</span></span>

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

### <span data-ttu-id="8ca84-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8ca84-123">-DefaultProfile</span></span>
<span data-ttu-id="8ca84-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8ca84-125">-Id</span><span class="sxs-lookup"><span data-stu-id="8ca84-125">-Id</span></span>
<span data-ttu-id="8ca84-126">소프트웨어 업데이트 구성 실행의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-126">Id of the software update configuration run.</span></span>

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

### <span data-ttu-id="8ca84-127">-OperatingSystem</span><span class="sxs-lookup"><span data-stu-id="8ca84-127">-OperatingSystem</span></span>
<span data-ttu-id="8ca84-128">실행의 운영 체제입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-128">The operating system of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: Windows, Linux

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca84-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8ca84-129">-ResourceGroupName</span></span>
<span data-ttu-id="8ca84-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-130">The resource group name.</span></span>

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

### <span data-ttu-id="8ca84-131">-SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca84-131">-SoftwareUpdateConfiguration</span></span>
<span data-ttu-id="8ca84-132">소프트웨어 업데이트 구성이 실행을 트리거했습니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-132">The software update configuration triggered the run.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration
Parameter Sets: BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca84-133">-SoftwareUpdateConfigurationName</span><span class="sxs-lookup"><span data-stu-id="8ca84-133">-SoftwareUpdateConfigurationName</span></span>
<span data-ttu-id="8ca84-134">실행을 트리거한 소프트웨어 업데이트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-134">Name of the software update configuration triggered the run.</span></span>

```yaml
Type: System.String
Parameter Sets: BySucName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca84-135">-StartTime</span><span class="sxs-lookup"><span data-stu-id="8ca84-135">-StartTime</span></span>
<span data-ttu-id="8ca84-136">실행의 최소 시작 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-136">Minimum start time of the run.</span></span>

```yaml
Type: System.DateTimeOffset
Parameter Sets: ByAll, BySucName, BySuc
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca84-137">-Status</span><span class="sxs-lookup"><span data-stu-id="8ca84-137">-Status</span></span>
<span data-ttu-id="8ca84-138">실행의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-138">Status of the run.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus]
Parameter Sets: ByAll, BySucName, BySuc
Aliases:
Accepted values: NotStarted, InProgress, Succeeded, Failed, MaintenanceWindowExceeded

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8ca84-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8ca84-139">CommonParameters</span></span>
<span data-ttu-id="8ca84-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8ca84-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8ca84-141">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8ca84-141">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8ca84-142">입력</span><span class="sxs-lookup"><span data-stu-id="8ca84-142">INPUTS</span></span>

### <span data-ttu-id="8ca84-143">System.Guid</span><span class="sxs-lookup"><span data-stu-id="8ca84-143">System.Guid</span></span>

### <span data-ttu-id="8ca84-144">System.String</span><span class="sxs-lookup"><span data-stu-id="8ca84-144">System.String</span></span>

### <span data-ttu-id="8ca84-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8ca84-145">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

### <span data-ttu-id="8ca84-146">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8ca84-146">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.OperatingSystemType, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8ca84-147">System.Nullable'1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="8ca84-147">System.Nullable\`1[[Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRunStatus, Microsoft.Azure.PowerShell.Cmdlets.Automation, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="8ca84-148">System.DateTimeOffset</span><span class="sxs-lookup"><span data-stu-id="8ca84-148">System.DateTimeOffset</span></span>

## <span data-ttu-id="8ca84-149">출력</span><span class="sxs-lookup"><span data-stu-id="8ca84-149">OUTPUTS</span></span>

### <span data-ttu-id="8ca84-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span><span class="sxs-lookup"><span data-stu-id="8ca84-150">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateRun</span></span>

## <span data-ttu-id="8ca84-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8ca84-151">NOTES</span></span>

## <span data-ttu-id="8ca84-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8ca84-152">RELATED LINKS</span></span>
