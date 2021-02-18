---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201020"
---
# <span data-ttu-id="6294a-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6294a-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6294a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6294a-102">SYNOPSIS</span></span>
<span data-ttu-id="6294a-103">예약된 Azure Automation 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="6294a-104">구문</span><span class="sxs-lookup"><span data-stu-id="6294a-104">SYNTAX</span></span>

### <span data-ttu-id="6294a-105">Windows(기본값)</span><span class="sxs-lookup"><span data-stu-id="6294a-105">Windows (Default)</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedUpdateClassification <WindowsUpdateClasses[]>]
 [-ExcludedKbNumber <String[]>] [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="6294a-106">Linux</span><span class="sxs-lookup"><span data-stu-id="6294a-106">Linux</span></span>
```
New-AzAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-RebootOnly]
 [-AzureVMResourceId <String[]>] [-PreTaskRunbookName <String>] [-PostTaskRunbookName <String>]
 [-PreTaskRunbookParameter <Hashtable>] [-PostTaskRunbookParameter <Hashtable>] [-NonAzureComputer <String[]>]
 [-AzureQuery <AzureQueryProperties[]>] [-NonAzureQuery <NonAzureQueryProperties[]>] [-Duration <TimeSpan>]
 [-RebootSetting <RebootSetting>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6294a-107">설명</span><span class="sxs-lookup"><span data-stu-id="6294a-107">DESCRIPTION</span></span>
<span data-ttu-id="6294a-108">일정에 따라 실행되는 소프트웨어 업데이트 구성을 만들어 컴퓨터 목록을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="6294a-109">컴퓨터에는 Azure 가상 머신 또는 비 az 컴퓨터가 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="6294a-110">예제</span><span class="sxs-lookup"><span data-stu-id="6294a-110">EXAMPLES</span></span>

### <span data-ttu-id="6294a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="6294a-111">Example 1</span></span>
<span data-ttu-id="6294a-112">매주 토요일 9시에 한 번씩 두 개의 Windows Azure 가상 머신에 중요 업데이트를 설치하는 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="6294a-113">업데이트 기간은 이 예제에서 2시간으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceId $targetMachines `
                                                 -IncludedUpdateClassification Critical `
                                                 -Duration $duration

UpdateConfiguration   : Microsoft.Azure.Commands.Automation.Model.UpdateManagement.UpdateConfiguration
ScheduleConfiguration : Microsoft.Azure.Commands.Automation.Model.Schedule
ProvisioningState     : Provisioning
ErrorInfo             :
ResourceGroupName     : mygroup
AutomationAccountName : myaccount
Name                  : MyWeeklySchedule
CreationTime          : 9/14/2018 3:53:27 AM +00:00
LastModifiedTime      : 9/14/2018 3:53:27 AM +00:00
Description           :
```

## <span data-ttu-id="6294a-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6294a-114">PARAMETERS</span></span>

### <span data-ttu-id="6294a-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="6294a-115">-AutomationAccountName</span></span>
<span data-ttu-id="6294a-116">자동화 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-116">The automation account name.</span></span>

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

### <span data-ttu-id="6294a-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="6294a-117">-AzureQuery</span></span>
<span data-ttu-id="6294a-118">동적 그룹 Azure 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-118">Dynamic group azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.AzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="6294a-119">-AzureVMResourceId</span></span>
<span data-ttu-id="6294a-120">Azure 가상 머신에 대한 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-120">Resource Ids for azure virtual machines.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6294a-121">-DefaultProfile</span></span>
<span data-ttu-id="6294a-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-123">-Duration</span><span class="sxs-lookup"><span data-stu-id="6294a-123">-Duration</span></span>
<span data-ttu-id="6294a-124">업데이트의 최대 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-124">Maximum duration for the update.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="6294a-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="6294a-126">제외된 업데이트의 KB 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-126">KB numbers of excluded updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="6294a-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="6294a-128">제외된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="6294a-128">Excluded Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="6294a-129">-IncludedKbNumber</span></span>
<span data-ttu-id="6294a-130">포함된 업데이트의 KB 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-130">KB numbers of included updates.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Windows
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="6294a-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="6294a-132">포함된 Linux 패키지 분류.</span><span class="sxs-lookup"><span data-stu-id="6294a-132">Included Linux package classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]
Parameter Sets: Linux
Aliases:
Accepted values: Unclassified, Critical, Security, Other

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="6294a-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="6294a-134">포함된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="6294a-134">Included Linux package masks.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Linux
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="6294a-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="6294a-136">포함된 Windows 업데이트 분류.</span><span class="sxs-lookup"><span data-stu-id="6294a-136">Included Windows Update classifications.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]
Parameter Sets: Windows
Aliases:
Accepted values: Unclassified, Critical, Security, UpdateRollup, FeaturePack, ServicePack, Definition, Tools, Updates

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="6294a-137">-Linux</span></span>
<span data-ttu-id="6294a-138">Linux 운영 체제 컴퓨터를 대상으로 하는 소프트웨어 업데이트 구성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Linux
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-139">-NonAzureComputer</span><span class="sxs-lookup"><span data-stu-id="6294a-139">-NonAzureComputer</span></span>
<span data-ttu-id="6294a-140">Az가 아닌 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-140">Non-Az computer names.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="6294a-141">-NonAzureQuery</span></span>
<span data-ttu-id="6294a-142">동적 그룹 비 Azure 쿼리</span><span class="sxs-lookup"><span data-stu-id="6294a-142">Dynamic group non Azure query.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.NonAzureQueryProperties[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="6294a-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="6294a-144">작업을 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-144">Post task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="6294a-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="6294a-146">작업 매개 변수를 게시합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-146">Post task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="6294a-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="6294a-148">사전 작업.</span><span class="sxs-lookup"><span data-stu-id="6294a-148">Pre task.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="6294a-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="6294a-150">사전 태스크 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-150">Pre task parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="6294a-151">-RebootOnly</span></span>
<span data-ttu-id="6294a-152">소프트웨어 업데이트 구성이 컴퓨터를 다시부팅하는 것만 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="6294a-153">-RebootSetting</span></span>
<span data-ttu-id="6294a-154">다시부팅 설정입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-154">Reboot Setting.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.UpdateManagement.RebootSetting
Parameter Sets: (All)
Aliases:
Accepted values: IfRequired, Never, Always, RebootOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6294a-155">-ResourceGroupName</span></span>
<span data-ttu-id="6294a-156">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-156">The resource group name.</span></span>

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

### <span data-ttu-id="6294a-157">-Schedule</span><span class="sxs-lookup"><span data-stu-id="6294a-157">-Schedule</span></span>
<span data-ttu-id="6294a-158">소프트웨어 업데이트 구성에 사용되는 일정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-158">Schedule object used for software update configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Automation.Model.Schedule
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="6294a-159">-Windows</span></span>
<span data-ttu-id="6294a-160">Windows 운영 체제 컴퓨터를 대상으로 하는 소프트웨어 업데이트 구성을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Windows
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-161">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6294a-161">-Confirm</span></span>
<span data-ttu-id="6294a-162">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-162">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6294a-163">-WhatIf</span></span>
<span data-ttu-id="6294a-164">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6294a-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6294a-165">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-165">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6294a-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6294a-166">CommonParameters</span></span>
<span data-ttu-id="6294a-167">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6294a-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6294a-168">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6294a-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6294a-169">입력</span><span class="sxs-lookup"><span data-stu-id="6294a-169">INPUTS</span></span>

### <span data-ttu-id="6294a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span><span class="sxs-lookup"><span data-stu-id="6294a-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="6294a-171">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="6294a-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="6294a-172">System.String[]</span><span class="sxs-lookup"><span data-stu-id="6294a-172">System.String[]</span></span>

### <span data-ttu-id="6294a-173">System.TimeSpan</span><span class="sxs-lookup"><span data-stu-id="6294a-173">System.TimeSpan</span></span>

### <span data-ttu-id="6294a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span><span class="sxs-lookup"><span data-stu-id="6294a-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="6294a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span><span class="sxs-lookup"><span data-stu-id="6294a-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="6294a-176">System.String</span><span class="sxs-lookup"><span data-stu-id="6294a-176">System.String</span></span>

## <span data-ttu-id="6294a-177">출력</span><span class="sxs-lookup"><span data-stu-id="6294a-177">OUTPUTS</span></span>

### <span data-ttu-id="6294a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="6294a-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="6294a-179">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6294a-179">NOTES</span></span>

## <span data-ttu-id="6294a-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6294a-180">RELATED LINKS</span></span>
