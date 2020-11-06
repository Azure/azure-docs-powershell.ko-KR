---
external help file: Microsoft.Azure.Commands.ResourceManager.Automation.dll-Help.xml
Module Name: AzureRM.Automation
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.automation/new-azurermautomationsoftwareupdateconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Automation/Commands.Automation/help/New-AzureRmAutomationSoftwareUpdateConfiguration.md
ms.openlocfilehash: f66d22e8ca07812ab76c482c29018f2a639d84f1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531489"
---
# <span data-ttu-id="8cf23-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span><span class="sxs-lookup"><span data-stu-id="8cf23-101">New-AzureRmAutomationSoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8cf23-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8cf23-102">SYNOPSIS</span></span>
<span data-ttu-id="8cf23-103">예약 된 azure 자동화 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-103">Creates a scheduled azure automation software update configuration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8cf23-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8cf23-104">SYNTAX</span></span>

### <span data-ttu-id="8cf23-105">Windows (기본값)</span><span class="sxs-lookup"><span data-stu-id="8cf23-105">Windows (Default)</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Windows]
 [-AzureVMResourceId <String[]>] [-NonAzureComputer <String[]>] [-Duration <TimeSpan>]
 [-IncludedUpdateClassification <WindowsUpdateClasses[]>] [-ExcludedKbNumber <String[]>]
 [-IncludedKbNumber <String[]>] [-ResourceGroupName] <String> [-AutomationAccountName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8cf23-106">Linux</span><span class="sxs-lookup"><span data-stu-id="8cf23-106">Linux</span></span>
```
New-AzureRmAutomationSoftwareUpdateConfiguration -Schedule <Schedule> [-Linux] [-AzureVMResourceId <String[]>]
 [-NonAzureComputer <String[]>] [-Duration <TimeSpan>] [-IncludedPackageClassification <LinuxPackageClasses[]>]
 [-ExcludedPackageNameMask <String[]>] [-IncludedPackageNameMask <String[]>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8cf23-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8cf23-107">DESCRIPTION</span></span>
<span data-ttu-id="8cf23-108">컴퓨터 목록을 업데이트 하기 위해 일정에 따라 실행 되는 소프트웨어 업데이트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-108">Creates a software update configuration that runs on a schedule to update a list of computers.</span></span> <span data-ttu-id="8cf23-109">컴퓨터에는 azure virtual machines 또는 비 azure 컴퓨터가 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-109">Computers include both azure virtual machines or non-azure computers.</span></span>

## <span data-ttu-id="8cf23-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8cf23-110">EXAMPLES</span></span>

### <span data-ttu-id="8cf23-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8cf23-111">Example 1</span></span>
<span data-ttu-id="8cf23-112">소프트웨어 업데이트 구성을 만들어 매주 토요일 9PM에 두 개의 Windows azure 가상 컴퓨터에 중요 업데이트를 설치 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-112">Creates a software update configuration to install critical updates on two Windows azure virtual machines once every Saturday 9PM.</span></span> <span data-ttu-id="8cf23-113">이 예제에서는 업데이트 기간이 2 시간으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-113">Update duration is set to 2 hours in this example.</span></span>

```powershell
PS C:\> $startTime = [DateTimeOffset]"2018-09-13T21:00"
PS C:\> $targetMachines = @( `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-01", `
    "/subscriptions/22e2445a-0984-4fa5-86a4-0280d76c4b2c/resourceGroups/compute/providers/Microsoft.Compute/virtualMachines/vm-w-02"
    )
PS C:\> $duration = New-TimeSpan -Hours 2
PS C:\> $schedule = New-AzureRmAutomationSchedule -ResourceGroupName "mygroup" `
                                                  -AutomationAccountName "myaccount" `
                                                  -Name MyWeeklySchedule `
                                                  -StartTime $startTime `
                                                  -DaysOfWeek Saturday `
                                                  -WeekInterval 1 `
                                                  -ForUpdateConfiguration

New-AzureRmAutomationSoftwareUpdateConfiguration -ResourceGroupName "mygroup" `
                                                 -AutomationAccountName "myaccount" `
                                                 -Schedule $schedule `
                                                 -Windows `
                                                 -AzureVMResourceIds $targetMachines `
                                                 -IncludedUpdateClassifications Critical `
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

## <span data-ttu-id="8cf23-114">변수</span><span class="sxs-lookup"><span data-stu-id="8cf23-114">PARAMETERS</span></span>

### <span data-ttu-id="8cf23-115">-AutomationAccountName</span><span class="sxs-lookup"><span data-stu-id="8cf23-115">-AutomationAccountName</span></span>
<span data-ttu-id="8cf23-116">Automation 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-116">The automation account name.</span></span>

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

### <span data-ttu-id="8cf23-117">-AzureVMResourceId</span><span class="sxs-lookup"><span data-stu-id="8cf23-117">-AzureVMResourceId</span></span>
<span data-ttu-id="8cf23-118">Azure 가상 컴퓨터의 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-118">Resource Ids for azure virtual machines.</span></span>

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

### <span data-ttu-id="8cf23-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8cf23-119">-DefaultProfile</span></span>
<span data-ttu-id="8cf23-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf23-121">-기간</span><span class="sxs-lookup"><span data-stu-id="8cf23-121">-Duration</span></span>
<span data-ttu-id="8cf23-122">업데이트의 최대 기간입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-122">Maximum duration for the update.</span></span>

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

### <span data-ttu-id="8cf23-123">-ExcludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="8cf23-123">-ExcludedKbNumber</span></span>
<span data-ttu-id="8cf23-124">제외 된 업데이트의 KB 번호입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-124">KB numbers of excluded updates.</span></span>

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

### <span data-ttu-id="8cf23-125">-ExcludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="8cf23-125">-ExcludedPackageNameMask</span></span>
<span data-ttu-id="8cf23-126">제외 된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="8cf23-126">Excluded Linux package masks.</span></span>

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

### <span data-ttu-id="8cf23-127">-IncludedKbNumber</span><span class="sxs-lookup"><span data-stu-id="8cf23-127">-IncludedKbNumber</span></span>
<span data-ttu-id="8cf23-128">포함 된 업데이트의 KB 개수입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-128">KB numbers of included updates.</span></span>

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

### <span data-ttu-id="8cf23-129">-IncludedPackageClassification</span><span class="sxs-lookup"><span data-stu-id="8cf23-129">-IncludedPackageClassification</span></span>
<span data-ttu-id="8cf23-130">포함 된 Linux 패키지 분류.</span><span class="sxs-lookup"><span data-stu-id="8cf23-130">Included Linux package classifications.</span></span>

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

### <span data-ttu-id="8cf23-131">-IncludedPackageNameMask</span><span class="sxs-lookup"><span data-stu-id="8cf23-131">-IncludedPackageNameMask</span></span>
<span data-ttu-id="8cf23-132">포함 된 Linux 패키지 마스크.</span><span class="sxs-lookup"><span data-stu-id="8cf23-132">Included Linux package masks.</span></span>

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

### <span data-ttu-id="8cf23-133">-IncludedUpdateClassification</span><span class="sxs-lookup"><span data-stu-id="8cf23-133">-IncludedUpdateClassification</span></span>
<span data-ttu-id="8cf23-134">포함 된 Windows 업데이트 분류.</span><span class="sxs-lookup"><span data-stu-id="8cf23-134">Included Windows Update classifications.</span></span>

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

### <span data-ttu-id="8cf23-135">-Linux</span><span class="sxs-lookup"><span data-stu-id="8cf23-135">-Linux</span></span>
<span data-ttu-id="8cf23-136">소프트웨어 업데이트 구성이 Linux 운영 체제 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-136">Indicates that the software update configuration targeting Linux operating system machines.</span></span>

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

### <span data-ttu-id="8cf23-137">-Azure컴퓨터</span><span class="sxs-lookup"><span data-stu-id="8cf23-137">-NonAzureComputer</span></span>
<span data-ttu-id="8cf23-138">비 Azure 컴퓨터 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-138">Non-Azure computer names.</span></span>

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

### <span data-ttu-id="8cf23-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8cf23-139">-ResourceGroupName</span></span>
<span data-ttu-id="8cf23-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-140">The resource group name.</span></span>

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

### <span data-ttu-id="8cf23-141">-일정</span><span class="sxs-lookup"><span data-stu-id="8cf23-141">-Schedule</span></span>
<span data-ttu-id="8cf23-142">소프트웨어 업데이트 구성에 사용 되는 일정 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-142">Schedule object used for software update configuration.</span></span>

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

### <span data-ttu-id="8cf23-143">-Windows</span><span class="sxs-lookup"><span data-stu-id="8cf23-143">-Windows</span></span>
<span data-ttu-id="8cf23-144">소프트웨어 업데이트 구성이 windows 운영 체제 컴퓨터를 대상으로 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-144">Indicates that the software update configuration targeting windows operating system machines.</span></span>

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

### <span data-ttu-id="8cf23-145">-확인</span><span class="sxs-lookup"><span data-stu-id="8cf23-145">-Confirm</span></span>
<span data-ttu-id="8cf23-146">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-146">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf23-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8cf23-147">-WhatIf</span></span>
<span data-ttu-id="8cf23-148">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-148">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8cf23-149">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-149">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8cf23-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8cf23-150">CommonParameters</span></span>
<span data-ttu-id="8cf23-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8cf23-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8cf23-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8cf23-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8cf23-153">입력</span><span class="sxs-lookup"><span data-stu-id="8cf23-153">INPUTS</span></span>

### <span data-ttu-id="8cf23-154">Microsoft Azure. 명령. 일정</span><span class="sxs-lookup"><span data-stu-id="8cf23-154">Microsoft.Azure.Commands.Automation.Model.Schedule</span></span>

### <span data-ttu-id="8cf23-155">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8cf23-155">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="8cf23-156">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="8cf23-156">System.String[]</span></span>

### <span data-ttu-id="8cf23-157">System. TimeSpan</span><span class="sxs-lookup"><span data-stu-id="8cf23-157">System.TimeSpan</span></span>

### <span data-ttu-id="8cf23-158">UpdateManagement. WindowsUpdateClasses []/. \*</span><span class="sxs-lookup"><span data-stu-id="8cf23-158">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.WindowsUpdateClasses[]</span></span>

### <span data-ttu-id="8cf23-159">UpdateManagement. LinuxPackageClasses []/. \*</span><span class="sxs-lookup"><span data-stu-id="8cf23-159">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.LinuxPackageClasses[]</span></span>

### <span data-ttu-id="8cf23-160">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8cf23-160">System.String</span></span>

## <span data-ttu-id="8cf23-161">출력</span><span class="sxs-lookup"><span data-stu-id="8cf23-161">OUTPUTS</span></span>

### <span data-ttu-id="8cf23-162">UpdateManagement. SoftwareUpdateConfiguration에 대 한 자동.</span><span class="sxs-lookup"><span data-stu-id="8cf23-162">Microsoft.Azure.Commands.Automation.Model.UpdateManagement.SoftwareUpdateConfiguration</span></span>

## <span data-ttu-id="8cf23-163">상속자</span><span class="sxs-lookup"><span data-stu-id="8cf23-163">NOTES</span></span>

## <span data-ttu-id="8cf23-164">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8cf23-164">RELATED LINKS</span></span>
