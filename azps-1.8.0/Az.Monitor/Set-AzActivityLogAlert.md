---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 7436F31F-9DCB-4365-BA6D-41BDB5D7FCB6
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzActivityLogAlert.md
ms.openlocfilehash: 6c7b867add359edec8379f20e630c9aca5fed00e
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402884"
---
# <span data-ttu-id="96e13-101">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-101">Set-AzActivityLogAlert</span></span>

## <span data-ttu-id="96e13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="96e13-102">SYNOPSIS</span></span>
<span data-ttu-id="96e13-103">새 활동 로그 경고를 생성하거나 기존 활동 로그 경고를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-103">Creates a new or sets an existing activity log alert.</span></span>

## <span data-ttu-id="96e13-104">구문</span><span class="sxs-lookup"><span data-stu-id="96e13-104">SYNTAX</span></span>

### <span data-ttu-id="96e13-105">SetByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="96e13-105">SetByNameAndResourceGroup</span></span>
```
Set-AzActivityLogAlert -Location <String> -Name <String> -ResourceGroupName <String>
 -Scope <System.Collections.Generic.List`1[System.String]>
 -Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>
 -Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e13-106">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="96e13-106">SetByResourceId</span></span>
```
Set-AzActivityLogAlert [-Location <String>] [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-DisableAlert] [-Description <String>]
 [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="96e13-107">SetByInputObject</span><span class="sxs-lookup"><span data-stu-id="96e13-107">SetByInputObject</span></span>
```
Set-AzActivityLogAlert [-Scope <System.Collections.Generic.List`1[System.String]>]
 [-Condition <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]>]
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]>]
 [-Description <String>] [-Tag <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="96e13-108">설명</span><span class="sxs-lookup"><span data-stu-id="96e13-108">DESCRIPTION</span></span>
<span data-ttu-id="96e13-109">**Set-AzActivityLogAlert** cmdlet은 새 활동을 생성하거나 기존 활동 로그 경고를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-109">The **Set-AzActivityLogAlert** cmdlet creates a new or sets an existing activity log alert.</span></span>
<span data-ttu-id="96e13-110">태그, 조건 및 작업의 경우 개체를 미리 만들어 이 호출의 매개 변수로 콤마로 구분해야 합니다(아래 예제 참조).</span><span class="sxs-lookup"><span data-stu-id="96e13-110">For tags, conditions, and actions the objects must be created in advance and passed as parameters in this call as a comma separated (see the example below).</span></span>
<span data-ttu-id="96e13-111">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 실제로 리소스를 만들고 수정하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating/modifying the resource.</span></span>
<span data-ttu-id="96e13-112">**참고:** 이 cmdlet 및 관련 cmdlet은 더 이상 사용이 불가능한(2017년 11월) **Add-AzLogAlertRule을 대체합니다.**</span><span class="sxs-lookup"><span data-stu-id="96e13-112">**NOTE**: This cmdlet and its related ones replaces the deprecated (November 2017) **Add-AzLogAlertRule**.</span></span>

## <span data-ttu-id="96e13-113">예제</span><span class="sxs-lookup"><span data-stu-id="96e13-113">EXAMPLES</span></span>

### <span data-ttu-id="96e13-114">예제 1: 활동 로그 경고 만들기</span><span class="sxs-lookup"><span data-stu-id="96e13-114">Example 1: Create an Activity Log Alert</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2
```

<span data-ttu-id="96e13-115">처음 네 개의 명령은 리프 조건 및 작업 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-115">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="96e13-116">마지막 명령은 조건 및 작업 그룹을 사용하여 활동 로그 경고를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-116">The final command creates an Activity Log Alert using the condition and the action group.</span></span>

### <span data-ttu-id="96e13-117">예제 2: 활동 로그 경고를 사용할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-117">Example 2: Create an Activity Log Alert disabled</span></span>
```
PS C:\>$location = 'Global'
PS C:\>$alertName = 'myAlert'
PS C:\>$resourceGroupName = 'theResourceGroupName'
PS C:\>$condition1 = New-AzActivityLogAlertCondition -Field 'field1' -Equals 'equals1'
PS C:\>$condition2 = New-AzActivityLogAlertCondition -Field 'field2' -Equals 'equals2'
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
PS C:\>Set-AzActivityLogAlert -Location $location -Name $alertName -ResourceGroupName $resourceGroupName -Scope 'scope1','scope2' -Action $actionGrp1 -Condition $condition1, $condition2 -DisableAlert
```

<span data-ttu-id="96e13-118">처음 네 개의 명령은 리프 조건 및 작업 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-118">The first four commands create leaf condition and action group.</span></span>
<span data-ttu-id="96e13-119">마지막 명령은 조건 및 작업 그룹을 사용하여 활동 로그 경고를 생성하지만 비활성화된 경고를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-119">The final command creates an Activity Log Alert using the condition and the action group, but it creates the alert disabled.</span></span>

### <span data-ttu-id="96e13-120">예제 3: 파이프 또는 InputObject 매개 변수의 값을 사용하여 활동 로그 경고 설정</span><span class="sxs-lookup"><span data-stu-id="96e13-120">Example 3: Set an activity log alert based using a value from the pipe or the InputObject parameter</span></span>
```
PS C:\>Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName | Set-AzActivityLogAlert
PS C:\>$alert = Get-AzActivityLogAlert -Name $alertName -ResourceGroupName $resourceGroupName
PS C:\>$alert.Description = 'Changing the description'
PS C:\>$alert.Enabled = $false
PS C:\>Set-AzActivityLogAlert -InputObject $alert
```

<span data-ttu-id="96e13-121">첫 번째 명령은 nop와 유사하며, 이미 포함된 동일한 값으로 경고를 설정하고 나머지 명령은 경고 규칙을 검색하고 설명을 변경하고 비활성화한 다음 InputObject 매개 변수를 사용하여 이러한 변경 내용을 유지</span><span class="sxs-lookup"><span data-stu-id="96e13-121">The first command is similar to a nop, it sets the alert with the same values it already contained The rest of the commands retrieve the alert rule, change the description and disable it, then use the InputObject parameter to persist those changes</span></span>

### <span data-ttu-id="96e13-122">예제 4: 파이프의 ResourceId 값을 사용하여 활동 로그 경고 설정</span><span class="sxs-lookup"><span data-stu-id="96e13-122">Example 4: Set an activity log alert based using the ResourceId value from the pipe</span></span>
```
PS C:\>Find-AzResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Set-AzActivityLogAlert -DisableAlert
```

<span data-ttu-id="96e13-123">주어진 로그 경고 규칙이 있는 경우 이 명령은 해당 규칙을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-123">If the given log alert rule exists this command disables it.</span></span>

## <span data-ttu-id="96e13-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="96e13-124">PARAMETERS</span></span>

### <span data-ttu-id="96e13-125">-Action</span><span class="sxs-lookup"><span data-stu-id="96e13-125">-Action</span></span>
<span data-ttu-id="96e13-126">활동 로그 경고에 대한 작업 그룹 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-126">The list of action groups for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-127">-Condition</span><span class="sxs-lookup"><span data-stu-id="96e13-127">-Condition</span></span>
<span data-ttu-id="96e13-128">활동 로그 경고에 대한 조건 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-128">The list of conditions for the activity log alert.</span></span>
<span data-ttu-id="96e13-129">**참고:** 조건 목록에 필드가 "범주"와 같은 조건이 하나 이상 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-129">**NOTE**: In the list of conditions there must be at least one with the Field equal to "Category".</span></span> <span data-ttu-id="96e13-130">이 조건이 없는 경우 백에는 400(BadRequest)으로 응답합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-130">The backend responds with 400 (BadRequest) if this condition is not present.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="96e13-131">-DefaultProfile</span></span>
<span data-ttu-id="96e13-132">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="96e13-132">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="96e13-133">-Description</span><span class="sxs-lookup"><span data-stu-id="96e13-133">-Description</span></span>
<span data-ttu-id="96e13-134">경고 리소스에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-134">The description of the alert resource.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-135">-DisableAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-135">-DisableAlert</span></span>
<span data-ttu-id="96e13-136">사용자가 비활성화된 활동 로그 경고를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-136">Allows the user to create a disabled the activity log alert.</span></span> <span data-ttu-id="96e13-137">제공되지 않은 경우 경고가 사용하도록 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-137">If not given, the alerts are created enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="96e13-138">-InputObject</span></span>
<span data-ttu-id="96e13-139">호출의 InputObject 태그 속성을 설정하여 필요한 이름 및 리소스 그룹 이름 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-139">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: SetByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-140">-Location</span><span class="sxs-lookup"><span data-stu-id="96e13-140">-Location</span></span>
<span data-ttu-id="96e13-141">활동 로그 경고가 있는 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-141">The location where the activity log alert will exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-142">-Name</span><span class="sxs-lookup"><span data-stu-id="96e13-142">-Name</span></span>
<span data-ttu-id="96e13-143">활동 로그 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-143">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-144">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="96e13-144">-ResourceGroupName</span></span>
<span data-ttu-id="96e13-145">경고 리소스가 존재할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-145">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-146">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="96e13-146">-ResourceId</span></span>
<span data-ttu-id="96e13-147">호출의 ResourceId 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-147">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-148">-Scope</span><span class="sxs-lookup"><span data-stu-id="96e13-148">-Scope</span></span>
<span data-ttu-id="96e13-149">활동 로그 경고에 대한 범위 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-149">The list of scopes for the activity log alert.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="96e13-150">-Tag</span></span>
<span data-ttu-id="96e13-151">활동 로그 경고 리소스의 태그 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-151">Sets the tags property of the activity log alert resource.</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByNameAndResourceGroup, SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: SetByInputObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="96e13-152">-Confirm</span><span class="sxs-lookup"><span data-stu-id="96e13-152">-Confirm</span></span>
<span data-ttu-id="96e13-153">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="96e13-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="96e13-154">-WhatIf</span></span>
<span data-ttu-id="96e13-155">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="96e13-155">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="96e13-156">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="96e13-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="96e13-157">CommonParameters</span></span>
<span data-ttu-id="96e13-158">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="96e13-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="96e13-159">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="96e13-159">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="96e13-160">입력</span><span class="sxs-lookup"><span data-stu-id="96e13-160">INPUTS</span></span>

### <span data-ttu-id="96e13-161">System.String</span><span class="sxs-lookup"><span data-stu-id="96e13-161">System.String</span></span>

### <span data-ttu-id="96e13-162">System.Collections.Generic.List'1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96e13-162">System.Collections.Generic.List\`1[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96e13-163">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="96e13-163">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertLeafCondition, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="96e13-164">System.Collections.Generic.List'1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="96e13-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup, Microsoft.Azure.PowerShell.Cmdlets.Monitor, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="96e13-165">System.Collections.Generic.Dictionary'2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="96e13-165">System.Collections.Generic.Dictionary\`2[[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e],[System.String, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="96e13-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="96e13-166">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="96e13-167">출력</span><span class="sxs-lookup"><span data-stu-id="96e13-167">OUTPUTS</span></span>

### <span data-ttu-id="96e13-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="96e13-168">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="96e13-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="96e13-169">NOTES</span></span>

## <span data-ttu-id="96e13-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="96e13-170">RELATED LINKS</span></span>

[<span data-ttu-id="96e13-171">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-171">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="96e13-172">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-172">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="96e13-173">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-173">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="96e13-174">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="96e13-174">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="96e13-175">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="96e13-175">New-AzActionGroup</span></span>](./New-AzActionGroup.md)
