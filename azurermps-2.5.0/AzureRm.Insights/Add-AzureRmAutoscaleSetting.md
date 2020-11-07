---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermautoscalesetting
schema: 2.0.0
ms.openlocfilehash: 8025c68c7fcaf2e7757cc81718636785bd62a19b
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93883090"
---
# <span data-ttu-id="289ec-101">Add-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-101">Add-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="289ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="289ec-102">SYNOPSIS</span></span>
<span data-ttu-id="289ec-103">자동 크기 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-103">Creates an Autoscale setting.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="289ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="289ec-104">SYNTAX</span></span>

### <span data-ttu-id="289ec-105">UpdateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-105">UpdateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -InputObject <PSAutoscaleSetting> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="289ec-106">CreateAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-106">CreateAutoscaleSetting</span></span>
```
Add-AzureRmAutoscaleSetting -Location <String> -Name <String> -ResourceGroupName <String> [-DisableSetting]
 [-AutoscaleProfile <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile]>]
 -TargetResourceId <String>
 [-Notification <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="289ec-107">설명은</span><span class="sxs-lookup"><span data-stu-id="289ec-107">DESCRIPTION</span></span>
<span data-ttu-id="289ec-108">**AzureRmAutoscaleSetting** Cmdlet은 자동 크기 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-108">The **Add-AzureRmAutoscaleSetting** cmdlet creates an Autoscale setting.</span></span>
<span data-ttu-id="289ec-109">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-109">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="289ec-110">예제의</span><span class="sxs-lookup"><span data-stu-id="289ec-110">EXAMPLES</span></span>

### <span data-ttu-id="289ec-111">예제 1: 자동 크기 조정 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="289ec-111">Example 1: Create an Autoscale setting</span></span>
```
PS C:\>$Rule1 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:05:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "1" 

PS C:\> $Rule2 = New-AzureRmAutoscaleRule -MetricName "Requests" -MetricResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/mywebsite" -Operator GreaterThan -MetricStatistic Average -Threshold 10 -TimeGrain 00:01:00 -ScaleActionCooldown 00:10:00 -ScaleActionDirection Increase -ScaleActionScaleType ChangeCount -ScaleActionValue "2"

PS C:\> $Profile1 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -StartTimeWindow 2015-03-05T14:00:00 -EndTimeWindow 2015-03-05T14:30:00 -TimeWindowTimeZone GMT -Rules $Rule1, $Rule2 -Name "adios"

PS C:\> $Profile2 = New-AzureRmAutoscaleProfile -DefaultCapacity "1" -MaximumCapacity "10" -MinimumCapacity "1" -Rules $Rule1, $Rule2 -Name "SecondProfileName" -RecurrenceFrequency Minute -ScheduleDays "1", "2", "3" -ScheduleHours 5, 10, 15 -ScheduleMinutes 15, 30, 45 -ScheduleTimeZone GMT

PS C:\> Add-AzureRmAutoscaleSetting -Location "East US" -Name "MySetting" -ResourceGroupName "Default-Web-EastUS" -TargetResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm" -AutoscaleProfiles $Profile1, $Profile2
```

<span data-ttu-id="289ec-112">첫 번째 두 명령은 두 가지 자동 크기 조정 규칙 (1 $Rule $Rule 2)을 만들기 위해 New-AzureRmAutoscaleRule를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-112">The first two commands use New-AzureRmAutoscaleRule to create two Autoscale rules, $Rule1 and $Rule2.</span></span>
<span data-ttu-id="289ec-113">세 번째와 네 번째 명령은 New-AzureRmAutoscaleProfile를 사용 하 여 자동 크기 조정 프로필을 만들고 $Profile 1 및 $Profile 2를 $Rule 1 및 $Rule 2를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-113">The third and fourth commands use New-AzureRmAutoscaleProfile to create Autoscale profiles, $Profile1 and $Profile2, using $Rule1 and $Rule2.</span></span>
<span data-ttu-id="289ec-114">마지막 명령은 $Profile 1 및 $Profile 2의 프로필을 사용 하 여 자동 크기 조정 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-114">The final command creates an Autoscale setting using the profiles in $Profile1 and $Profile2.</span></span>

## <span data-ttu-id="289ec-115">변수</span><span class="sxs-lookup"><span data-stu-id="289ec-115">PARAMETERS</span></span>

### <span data-ttu-id="289ec-116">-AutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="289ec-116">-AutoscaleProfile</span></span>
<span data-ttu-id="289ec-117">자동 크기 조정 설정에 추가할 프로필 목록을 지정 하거나 프로필을 추가 하지 $Null 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-117">Specifies a list of profiles to add to the Autoscale setting, or $Null to add no profile.</span></span>

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

### <span data-ttu-id="289ec-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="289ec-118">-DefaultProfile</span></span>
<span data-ttu-id="289ec-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="289ec-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="289ec-120">-DisableSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-120">-DisableSetting</span></span>
<span data-ttu-id="289ec-121">기존 자동 크기 조정 설정을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-121">Disables an existing Autoscale setting.</span></span>

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

### <span data-ttu-id="289ec-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="289ec-122">-InputObject</span></span>
<span data-ttu-id="289ec-123">AutoscaleSetting의 완벽 한 사양</span><span class="sxs-lookup"><span data-stu-id="289ec-123">The complete spec of an AutoscaleSetting</span></span>

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

### <span data-ttu-id="289ec-124">-위치</span><span class="sxs-lookup"><span data-stu-id="289ec-124">-Location</span></span>
<span data-ttu-id="289ec-125">자동 크기 조정 설정의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-125">Specifies the location of the Autoscale setting.</span></span>

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

### <span data-ttu-id="289ec-126">-이름</span><span class="sxs-lookup"><span data-stu-id="289ec-126">-Name</span></span>
<span data-ttu-id="289ec-127">만들 자동 크기 조정 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-127">Specifies the name of the Autoscale setting to create.</span></span>

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

### <span data-ttu-id="289ec-128">-알림</span><span class="sxs-lookup"><span data-stu-id="289ec-128">-Notification</span></span>
<span data-ttu-id="289ec-129">쉼표로 구분 된 알림의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-129">Specifies a list of comma-separated notifications.</span></span>

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

### <span data-ttu-id="289ec-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="289ec-130">-ResourceGroupName</span></span>
<span data-ttu-id="289ec-131">자동 크기 조정 설정과 연결 된 리소스에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-131">Specifies the name of the resource group for the resource associated with the Autoscale setting.</span></span>

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

### <span data-ttu-id="289ec-132">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="289ec-132">-TargetResourceId</span></span>
<span data-ttu-id="289ec-133">크기를 조정 하는 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-133">Specifies the ID of the resource to autoscale.</span></span>

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

### <span data-ttu-id="289ec-134">-확인</span><span class="sxs-lookup"><span data-stu-id="289ec-134">-Confirm</span></span>
<span data-ttu-id="289ec-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="289ec-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="289ec-136">-WhatIf</span></span>
<span data-ttu-id="289ec-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-137">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="289ec-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="289ec-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="289ec-139">CommonParameters</span></span>
<span data-ttu-id="289ec-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="289ec-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="289ec-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="289ec-142">입력</span><span class="sxs-lookup"><span data-stu-id="289ec-142">INPUTS</span></span>

### <span data-ttu-id="289ec-143">PSAutoscaleSetting를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

### <span data-ttu-id="289ec-144">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="289ec-144">System.String</span></span>

### <span data-ttu-id="289ec-145">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="289ec-145">System.Management.Automation.SwitchParameter</span></span>

### <span data-ttu-id="289ec-146">System.webserver. List ' 1 [[AutoscaleProfile, Microsoft azure. 5.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-146">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleProfile, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="289ec-147">System.webserver. List ' 1 [[AutoscaleNotification, Microsoft azure. 5.1.0.0, Version =, Culture = 중립, PublicKeyToken = null]]을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-147">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.AutoscaleNotification, Microsoft.Azure.Commands.Insights, Version=5.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="289ec-148">출력</span><span class="sxs-lookup"><span data-stu-id="289ec-148">OUTPUTS</span></span>

### <span data-ttu-id="289ec-149">PSAddAutoscaleSettingOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="289ec-149">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAutoscaleSettingOperationResponse</span></span>

## <span data-ttu-id="289ec-150">상속자</span><span class="sxs-lookup"><span data-stu-id="289ec-150">NOTES</span></span>

## <span data-ttu-id="289ec-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="289ec-151">RELATED LINKS</span></span>

[<span data-ttu-id="289ec-152">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-152">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="289ec-153">새로운 AzureRmAutoscaleProfile</span><span class="sxs-lookup"><span data-stu-id="289ec-153">New-AzureRmAutoscaleProfile</span></span>](./New-AzureRmAutoscaleProfile.md)

[<span data-ttu-id="289ec-154">새로운 AzureRmAutoscaleRule</span><span class="sxs-lookup"><span data-stu-id="289ec-154">New-AzureRmAutoscaleRule</span></span>](./New-AzureRmAutoscaleRule.md)

[<span data-ttu-id="289ec-155">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="289ec-155">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


