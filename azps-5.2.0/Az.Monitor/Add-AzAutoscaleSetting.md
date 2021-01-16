---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/add-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Add-AzAutoscaleSetting.md
ms.openlocfilehash: b2f7410f45a5b60a768d22fe7e66b7d8c1e4ad94
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98357204"
---
# <span data-ttu-id="e18ff-101">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-101">Add-AzAutoscaleSetting</span></span>

## <span data-ttu-id="e18ff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e18ff-102">SYNOPSIS</span></span>
<span data-ttu-id="e18ff-103">자동 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-103">Creates an Autoscale setting.</span></span>

## <span data-ttu-id="e18ff-104">구문</span><span class="sxs-lookup"><span data-stu-id="e18ff-104">SYNTAX</span></span>

### <span data-ttu-id="e18ff-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-105">UpdateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e18ff-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-106">CreateAutoscaleSetting</span></span>
```
Add-AzAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e18ff-107">설명</span><span class="sxs-lookup"><span data-stu-id="e18ff-107">DESCRIPTION</span></span>
<span data-ttu-id="e18ff-108">**Add-AzAutoscaleSetting** cmdlet은 자동 크기 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-108">The **Add-AzAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="e18ff-109">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="e18ff-110">예제</span><span class="sxs-lookup"><span data-stu-id="e18ff-110">EXAMPLES</span></span>

### <span data-ttu-id="e18ff-111">예제 1: 자동 조정 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="e18ff-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rule $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rule $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDay "1", "2", "3" -ScheduleHour 5, 10, 15 -ScheduleMinute 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfile $Profile1, $Profile2
```

<span data-ttu-id="e18ff-112">처음 두 명령은 [New-AzAutoscaleRule을](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) 사용하여 두 개의 자동 조정 규칙인 $Rule 1 및 $Rule 2를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-112">The first two commands use [New-AzAutoscaleRule](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalerule) to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="e18ff-113">세 번째 및 네 번째 명령은 [New-AzAutoscaleProfile을](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) 사용하여 $Rule 1 및 $Profile 2를 사용하여 $Profile 1 및 $Profile 2 자동 조정 프로필을 $Rule.</span><span class="sxs-lookup"><span data-stu-id="e18ff-113">The third and fourth commands use [New-AzAutoscaleProfile](https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscaleprofile) to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="e18ff-114">마지막 명령은 $Profile 1 및 $Profile 2의 프로필을 사용하여 자동 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="e18ff-115">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e18ff-115">PARAMETERS</span></span>

### <span data-ttu-id="e18ff-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e18ff-116">-AutoscaleProfile</span></span>
<span data-ttu-id="e18ff-117">자동 조정 설정에 추가할 프로필 목록을 지정하거나 프로필을 $Null 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e18ff-118">-DefaultProfile</span></span>
<span data-ttu-id="e18ff-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e18ff-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e18ff-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-120">-DisableSetting</span></span>
<span data-ttu-id="e18ff-121">기존 자동 조정 설정을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="e18ff-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e18ff-122">-InputObject</span></span>
<span data-ttu-id="e18ff-123">AutoscaleSetting의 전체 사양</span><span class="sxs-lookup"><span data-stu-id="e18ff-123">The complete spec of an AutoscaleSetting</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting
Parameter Sets: UpdateAutoscaleSetting
Aliases: SettingSpec

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-124">-Location</span><span class="sxs-lookup"><span data-stu-id="e18ff-124">-Location</span></span>
<span data-ttu-id="e18ff-125">자동 조정 설정의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-125">Specifies the location of the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-126">-Name</span><span class="sxs-lookup"><span data-stu-id="e18ff-126">-Name</span></span>
<span data-ttu-id="e18ff-127">만들 자동 조정 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-127">Specifies the name of the Autoscale setting to create.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-128">-Notification</span><span class="sxs-lookup"><span data-stu-id="e18ff-128">-Notification</span></span>
<span data-ttu-id="e18ff-129">콤마로 구분된 알림 목록을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-129">Specifies a list of comma-separated notifications.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e18ff-130">-ResourceGroupName</span></span>
<span data-ttu-id="e18ff-131">자동 조정 설정과 연결된 리소스에 대한 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="e18ff-132">-TargetResourceId</span></span>
<span data-ttu-id="e18ff-133">자동 조정에 사용할 리소스의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-133">Specifies the ID of the resource to autoscale.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateAutoscaleSetting
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e18ff-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e18ff-134">-Confirm</span></span>
<span data-ttu-id="e18ff-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e18ff-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e18ff-136">-WhatIf</span></span>
<span data-ttu-id="e18ff-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e18ff-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e18ff-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e18ff-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e18ff-139">CommonParameters</span></span>
<span data-ttu-id="e18ff-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e18ff-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e18ff-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e18ff-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e18ff-142">입력</span><span class="sxs-lookup"><span data-stu-id="e18ff-142">INPUTS</span></span>

### <span data-ttu-id="e18ff-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="e18ff-144">System.String</span><span class="sxs-lookup"><span data-stu-id="e18ff-144">System.String</span></span>

### <span data-ttu-id="e18ff-145">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="e18ff-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="e18ff-146">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e18ff-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="e18ff-147">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="e18ff-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="e18ff-148">출력</span><span class="sxs-lookup"><span data-stu-id="e18ff-148">OUTPUTS</span></span>

### <span data-ttu-id="e18ff-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span><span class="sxs-lookup"><span data-stu-id="e18ff-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="e18ff-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e18ff-150">NOTES</span></span>

## <span data-ttu-id="e18ff-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e18ff-151">RELATED LINKS</span></span>

[<span data-ttu-id="e18ff-152">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-152">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="e18ff-153">New-AzAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="e18ff-153">New-AzAutoscaleProfile</span></span>](./New-AzAutoscaleProfile.md)

[<span data-ttu-id="e18ff-154">New-AzAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="e18ff-154">New-AzAutoscaleRule</span></span>](./New-AzAutoscaleRule.md)

[<span data-ttu-id="e18ff-155">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="e18ff-155">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


