---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Set-AzureRmActivityLogAlert.md
ms.openlocfilehash: 77d8792bf7499f2634ae525396568a9a21432f6b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703368"
---
# <span data-ttu-id="1108e-101">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-101">Set-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="1108e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1108e-102">SYNOPSIS</span></span>
<span data-ttu-id="1108e-103">기존 활동 로그 알림을 새로 만들거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-103">Creates a new or sets an existing activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1108e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1108e-104">SYNTAX</span></span>

### <span data-ttu-id="1108e-105">활동 로그 설정 알림에 대 한 기본 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1108e-105">Default parameters for set activity log alert</span></span>
```
Set-AzureRmActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1108e-106">파이프에서 ResourceId 값을 가져오는 활동 로그 알림을 설정 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1108e-106">Parameters to set an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="1108e-107">파이프에서 값을 가져오는 활동 로그 알림을 설정 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1108e-107">Parameters to set an activity log alerts taking value from the pipe</span></span>
```
Set-AzureRmActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="1108e-108">설명은</span><span class="sxs-lookup"><span data-stu-id="1108e-108">DESCRIPTION</span></span>
<span data-ttu-id="1108e-109">**AzureRmActivityLogAlert** cmdlet은 새 작업을 만들거나 기존 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-109">The **Set-AzureRmActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="1108e-110">태그, 조건, 작업의 경우 개체를 미리 생성 하 고 쉼표로 구분 된이 호출에 매개 변수로 전달 해야 합니다 (아래 예제 참조).</span><span class="sxs-lookup"><span data-stu-id="1108e-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="1108e-111">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 만들거나 수정 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="1108e-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>

## <span data-ttu-id="1108e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="1108e-112">EXAMPLES</span></span>

### <span data-ttu-id="1108e-113">예제 1: 활동 로그 알림 만들기</span><span class="sxs-lookup"><span data-stu-id="1108e-113">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="1108e-114">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-114">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="1108e-115">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-115">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="1108e-116">예제 2: 활동 로그 알림 만들기 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="1108e-116">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzureRmActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzureRmActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzureRmActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="1108e-117">처음 4 개의 명령은 리프 조건과 작업 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-117">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="1108e-118">마지막 명령은 조건과 작업 그룹을 사용 하 여 활동 로그 알림을 만들지만 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-118">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="1108e-119">예제 3: 파이프 또는 InputObject 매개 변수의 값을 사용 하 여 활동 로그 알림을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-119">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzureRmActivityLogAlert
PS C:\>$alert = Get-AzureRmActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzureRmActivityLogAlert -InputObject $alert
```

<span data-ttu-id="1108e-120">첫 번째 명령은 nop과 비슷하지만 경고 규칙을 검색 하 고, 설명을 변경 하 고, 사용 하지 않도록 설정한 다음 InputObject 매개 변수를 사용 하 여 해당 변경 내용을 유지 하는 것과 동일한 값으로 경고를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-120">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="1108e-121">예제 4: 파이프의 ResourceId 값을 사용 하 여 활동 로그 알림 설정</span><span class="sxs-lookup"><span data-stu-id="1108e-121">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzureRmActivityLogAlert -DisableAlert
```

<span data-ttu-id="1108e-122">지정 된 로그 알림 규칙이 있으면이 명령을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-122">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="1108e-123">변수</span><span class="sxs-lookup"><span data-stu-id="1108e-123">PARAMETERS</span></span>

### <span data-ttu-id="1108e-124">-위치</span><span class="sxs-lookup"><span data-stu-id="1108e-124">-Location</span></span>
<span data-ttu-id="1108e-125">활동 로그 경고가 존재 하는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-125">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-126">-이름</span><span class="sxs-lookup"><span data-stu-id="1108e-126">-Name</span></span>
<span data-ttu-id="1108e-127">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-127">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1108e-128">-ResourceGroupName</span></span>
<span data-ttu-id="1108e-129">알림 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-129">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-130">-범위</span><span class="sxs-lookup"><span data-stu-id="1108e-130">-Scope</span></span>
<span data-ttu-id="1108e-131">활동 로그 알림의 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-131">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-132">-조건</span><span class="sxs-lookup"><span data-stu-id="1108e-132">-Condition</span></span>
<span data-ttu-id="1108e-133">활동 로그 알림에 대 한 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-133">The list of conditions for the activity log alert.</span></span>

<span data-ttu-id="1108e-134">**참고** : 조건 목록에 "Category"와 같은 필드에 적어도 1이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-134">**NOTE** : In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="1108e-135">이 조건이 없는 경우 백 엔드는 400 (BadRequest)로 응답 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-135">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-136">-작업</span><span class="sxs-lookup"><span data-stu-id="1108e-136">-Action</span></span>
<span data-ttu-id="1108e-137">활동 로그 알림에 대 한 작업 그룹의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-137">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Default parameters for set activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-138">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-138">-DisableAlert</span></span>
<span data-ttu-id="1108e-139">사용 하지 않도록 설정 된 활동 로그 알림을 사용자가 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-139">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="1108e-140">지정 하지 않으면 경고가 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-140">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-141">-설명</span><span class="sxs-lookup"><span data-stu-id="1108e-141">-Description</span></span>
<span data-ttu-id="1108e-142">알림 리소스에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-142">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-143">태그</span><span class="sxs-lookup"><span data-stu-id="1108e-143">-Tag</span></span>
<span data-ttu-id="1108e-144">활동 로그 알림 리소스의 tags 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-144">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Default parameters for set activity log alert, Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-145">-InputObject</span><span class="sxs-lookup"><span data-stu-id="1108e-145">-InputObject</span></span>
<span data-ttu-id="1108e-146">필요한 이름을 추출 하는 호출의 InputObject tags 속성 및 리소스 그룹 이름 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-146">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to set an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-147">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1108e-147">-ResourceId</span></span>
<span data-ttu-id="1108e-148">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-148">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to set an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1108e-149">-확인</span><span class="sxs-lookup"><span data-stu-id="1108e-149">-Confirm</span></span>
<span data-ttu-id="1108e-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="1108e-151">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1108e-151">-DefaultProfile</span></span>
<span data-ttu-id="1108e-152">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-152">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1108e-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="1108e-153">-WhatIf</span></span>
<span data-ttu-id="1108e-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-154">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="1108e-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="1108e-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1108e-156">CommonParameters</span></span>
<span data-ttu-id="1108e-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1108e-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1108e-158">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1108e-158">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1108e-159">입력</span><span class="sxs-lookup"><span data-stu-id="1108e-159">INPUTS</span></span>

## <span data-ttu-id="1108e-160">출력</span><span class="sxs-lookup"><span data-stu-id="1108e-160">OUTPUTS</span></span>

### <span data-ttu-id="1108e-161">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="1108e-161">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="1108e-162">상속자</span><span class="sxs-lookup"><span data-stu-id="1108e-162">NOTES</span></span>

## <span data-ttu-id="1108e-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1108e-163">RELATED LINKS</span></span>

[<span data-ttu-id="1108e-164">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-164">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1108e-165">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-165">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1108e-166">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-166">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1108e-167">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="1108e-167">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="1108e-168">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="1108e-168">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="1108e-169">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="1108e-169">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)
