---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/new-azautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/New-AzAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: d54acf3ad4e47c173b8ec4ef2fd37145c6dbf198
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044958"
---
# <span data-ttu-id="ff3e9-101">New-AzAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="ff3e9-101">New-AzAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="ff3e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ff3e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ff3e9-103">예약 된 azure 자동화 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-103">Creates a scheduled azure automation software update configuration.</span></span>

## <span data-ttu-id="ff3e9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ff3e9-104">SYNTAX</span></span>

### <span data-ttu-id="ff3e9-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="ff3e9-105">Windows (Default)</span></span>
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

### <span data-ttu-id="ff3e9-106">Linux</span><span class="sxs-lookup"><span data-stu-id="ff3e9-106">Linux</span></span>
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

## <span data-ttu-id="ff3e9-107">설명은</span><span class="sxs-lookup"><span data-stu-id="ff3e9-107">DESCRIPTION</span></span>
<span data-ttu-id="ff3e9-108">컴퓨터 목록을 업데이트 하기 위해 일정에 따라 실행 되는 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="ff3e9-109">컴퓨터에는 azure 가상 컴퓨터와 비 az 컴퓨터가 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-109">Computers include both azure virtual machines or non-az computers.</span></span>

## <span data-ttu-id="ff3e9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="ff3e9-110">EXAMPLES</span></span>

### <span data-ttu-id="ff3e9-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="ff3e9-111">Example 1</span></span>
<span data-ttu-id="ff3e9-112">소프트웨어 업데이트 구성을 만들어 매주 토요일 9PM에 두 개의 Windows azure 가상 컴퓨터에 중요 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="ff3e9-113">이 예제에서는 업데이트 기간이 2 시간으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-113">Update duration is set to 2 hours in this example.</span></span>

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

## <span data-ttu-id="ff3e9-114">변수</span><span class="sxs-lookup"><span data-stu-id="ff3e9-114">PARAMETERS</span></span>

### <span data-ttu-id="ff3e9-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="ff3e9-115">-AutomationAccountName</span></span>
<span data-ttu-id="ff3e9-116">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-116">The automation account name.</span></span>

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

### <span data-ttu-id="ff3e9-117">-AzureQuery</span><span class="sxs-lookup"><span data-stu-id="ff3e9-117">-AzureQuery</span></span>
<span data-ttu-id="ff3e9-118">동적 그룹 azure 쿼리.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-118">Dynamic group azure query.</span></span>

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

### <span data-ttu-id="ff3e9-119">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="ff3e9-119">-AzureVMResourceId</span></span>
<span data-ttu-id="ff3e9-120">Azure 가상 컴퓨터의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-120">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="ff3e9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ff3e9-121">-DefaultProfile</span></span>
<span data-ttu-id="ff3e9-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ff3e9-123">-기간</span><span class="sxs-lookup"><span data-stu-id="ff3e9-123">-Duration</span></span>
<span data-ttu-id="ff3e9-124">업데이트의 최대 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-124">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="ff3e9-125">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="ff3e9-125">-ExcludedKbNumber</span></span>
<span data-ttu-id="ff3e9-126">제외 된 업데이트의 KB 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-126">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="ff3e9-127">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="ff3e9-127">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="ff3e9-128">제외 된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-128">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="ff3e9-129">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="ff3e9-129">-IncludedKbNumber</span></span>
<span data-ttu-id="ff3e9-130">포함 된 업데이트의 KB 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-130">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="ff3e9-131">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="ff3e9-131">-IncludedPackageClassification</span></span>
<span data-ttu-id="ff3e9-132">포함 된 Linux 패키지 분류.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-132">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="ff3e9-133">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="ff3e9-133">-IncludedPackageNameMask</span></span>
<span data-ttu-id="ff3e9-134">포함 된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-134">Included Linux package masks.</span></span>

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

### <span data-ttu-id="ff3e9-135">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="ff3e9-135">-IncludedUpdateClassification</span></span>
<span data-ttu-id="ff3e9-136">포함 된 Windows 업데이트 분류.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-136">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="ff3e9-137">-Linux</span><span class="sxs-lookup"><span data-stu-id="ff3e9-137">-Linux</span></span>
<span data-ttu-id="ff3e9-138">소프트웨어 업데이트 구성이 Linux 운영 체제 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-138">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="ff3e9-139">-Azure컴퓨터</span><span class="sxs-lookup"><span data-stu-id="ff3e9-139">-NonAzureComputer</span></span>
<span data-ttu-id="ff3e9-140">비 Az 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-140">Non-Az computer names.</span></span>

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

### <span data-ttu-id="ff3e9-141">-NonAzureQuery</span><span class="sxs-lookup"><span data-stu-id="ff3e9-141">-NonAzureQuery</span></span>
<span data-ttu-id="ff3e9-142">Azure가 아닌 동적 그룹 쿼리입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-142">Dynamic group non Azure query.</span></span>

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

### <span data-ttu-id="ff3e9-143">-PostTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="ff3e9-143">-PostTaskRunbookName</span></span>
<span data-ttu-id="ff3e9-144">작업을 게시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-144">Post task.</span></span>

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

### <span data-ttu-id="ff3e9-145">-PostTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="ff3e9-145">-PostTaskRunbookParameter</span></span>
<span data-ttu-id="ff3e9-146">게시 작업 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-146">Post task parameter.</span></span>

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

### <span data-ttu-id="ff3e9-147">-PreTaskRunbookName</span><span class="sxs-lookup"><span data-stu-id="ff3e9-147">-PreTaskRunbookName</span></span>
<span data-ttu-id="ff3e9-148">사전 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-148">Pre task.</span></span>

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

### <span data-ttu-id="ff3e9-149">-PreTaskRunbookParameter</span><span class="sxs-lookup"><span data-stu-id="ff3e9-149">-PreTaskRunbookParameter</span></span>
<span data-ttu-id="ff3e9-150">Pre 작업 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-150">Pre task parameter.</span></span>

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

### <span data-ttu-id="ff3e9-151">-RebootOnly</span><span class="sxs-lookup"><span data-stu-id="ff3e9-151">-RebootOnly</span></span>
<span data-ttu-id="ff3e9-152">소프트웨어 업데이트 구성에서 컴퓨터만 다시 부팅 한다는 것을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-152">Indicates that the software update configuration will Only Reboot the machines.</span></span>

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

### <span data-ttu-id="ff3e9-153">-RebootSetting</span><span class="sxs-lookup"><span data-stu-id="ff3e9-153">-RebootSetting</span></span>
<span data-ttu-id="ff3e9-154">다시 부팅 설정.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-154">Reboot Setting.</span></span>

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

### <span data-ttu-id="ff3e9-155">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ff3e9-155">-ResourceGroupName</span></span>
<span data-ttu-id="ff3e9-156">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-156">The resource group name.</span></span>

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

### <span data-ttu-id="ff3e9-157">-일정</span><span class="sxs-lookup"><span data-stu-id="ff3e9-157">-Schedule</span></span>
<span data-ttu-id="ff3e9-158">소프트웨어 업데이트 구성에 사용 되는 일정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-158">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="ff3e9-159">-Windows</span><span class="sxs-lookup"><span data-stu-id="ff3e9-159">-Windows</span></span>
<span data-ttu-id="ff3e9-160">소프트웨어 업데이트 구성이 windows 운영 체제 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-160">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="ff3e9-161">-확인</span><span class="sxs-lookup"><span data-stu-id="ff3e9-161">-Confirm</span></span>
<span data-ttu-id="ff3e9-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ff3e9-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ff3e9-163">-WhatIf</span></span>
<span data-ttu-id="ff3e9-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ff3e9-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ff3e9-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ff3e9-166">CommonParameters</span></span>
<span data-ttu-id="ff3e9-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ff3e9-168">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ff3e9-168">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ff3e9-169">입력</span><span class="sxs-lookup"><span data-stu-id="ff3e9-169">INPUTS</span></span>

### <span data-ttu-id="ff3e9-170">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="ff3e9-170">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="ff3e9-171">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="ff3e9-171">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="ff3e9-172">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="ff3e9-172">System.String[]</span></span>

### <span data-ttu-id="ff3e9-173">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="ff3e9-173">System.TimeSpan</span></span>

### <span data-ttu-id="ff3e9-174">UpdateManagement. WindowsUpdateClasses []/. \*</span><span class="sxs-lookup"><span data-stu-id="ff3e9-174">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="ff3e9-175">UpdateManagement. LinuxPackageClasses []/. \*</span><span class="sxs-lookup"><span data-stu-id="ff3e9-175">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="ff3e9-176">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="ff3e9-176">System.String</span></span>

## <span data-ttu-id="ff3e9-177">출력</span><span class="sxs-lookup"><span data-stu-id="ff3e9-177">OUTPUTS</span></span>

### <span data-ttu-id="ff3e9-178">UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="ff3e9-178">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="ff3e9-179">상속자</span><span class="sxs-lookup"><span data-stu-id="ff3e9-179">NOTES</span></span>

## <span data-ttu-id="ff3e9-180">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ff3e9-180">RELATED LINKS</span></span>
