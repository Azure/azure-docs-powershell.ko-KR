---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzActivityLogAlert.md
ms.openlocfilehash: a69297afe49bb7cda0abc95cf97b371e04cac0ce
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101964411"
---
# <span data-ttu-id="540d6-101">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="540d6-101">Remove-AzActivityLogAlert</span></span>

## <span data-ttu-id="540d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="540d6-102">SYNOPSIS</span></span>
<span data-ttu-id="540d6-103">활동 로그 경고를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-103">Removes an activity log alert.</span></span>

## <span data-ttu-id="540d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="540d6-104">SYNTAX</span></span>

### <span data-ttu-id="540d6-105">RemoveByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="540d6-105">RemoveByNameAndResourceGroup</span></span>
```
Remove-AzActivityLogAlert -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540d6-106">RemoveByInputObject</span><span class="sxs-lookup"><span data-stu-id="540d6-106">RemoveByInputObject</span></span>
```
Remove-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="540d6-107">RemoveByResourceId</span><span class="sxs-lookup"><span data-stu-id="540d6-107">RemoveByResourceId</span></span>
```
Remove-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="540d6-108">설명</span><span class="sxs-lookup"><span data-stu-id="540d6-108">DESCRIPTION</span></span>
<span data-ttu-id="540d6-109">**Remove-AzActivityLogAlert** cmdlet은 활동 로그 경고를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-109">The **Remove-AzActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="540d6-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 실제로 리소스를 패치하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>
<span data-ttu-id="540d6-111">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 만들거나 수정하거나 제거하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-111">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="540d6-112">예제</span><span class="sxs-lookup"><span data-stu-id="540d6-112">EXAMPLES</span></span>

### <span data-ttu-id="540d6-113">예제 1: 활동 로그 경고 제거</span><span class="sxs-lookup"><span data-stu-id="540d6-113">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="540d6-114">이름 및 리소스 그룹 이름을 입력으로 사용하여 활동 로그 경고를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-114">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="540d6-115">예제 2: PSActivityLogAlertResource를 입력으로 사용하여 활동 로그 경고 제거</span><span class="sxs-lookup"><span data-stu-id="540d6-115">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="540d6-116">PSActivityLogAlertResource를 입력으로 사용하여 활동 로그 경고를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-116">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="540d6-117">예제 3: ResourceId 매개 변수를 사용하여 ActivityLogAlert 제거</span><span class="sxs-lookup"><span data-stu-id="540d6-117">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Remove-AzActivityLogAlert
```

<span data-ttu-id="540d6-118">이 명령은 파이프에서 ResourceId 매개 변수를 사용하여 ActivityLogAlert를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-118">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="540d6-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="540d6-119">PARAMETERS</span></span>

### <span data-ttu-id="540d6-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="540d6-120">-DefaultProfile</span></span>
<span data-ttu-id="540d6-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="540d6-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="540d6-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="540d6-122">-InputObject</span></span>
<span data-ttu-id="540d6-123">필요한 이름 및 리소스 그룹 이름 속성을 추출하기 위해 호출의 InputObject 태그 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-123">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: RemoveByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="540d6-124">-Name</span><span class="sxs-lookup"><span data-stu-id="540d6-124">-Name</span></span>
<span data-ttu-id="540d6-125">활동 로그 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540d6-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="540d6-126">-ResourceGroupName</span></span>
<span data-ttu-id="540d6-127">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-127">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540d6-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="540d6-128">-ResourceId</span></span>
<span data-ttu-id="540d6-129">호출의 ResourceId 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="540d6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="540d6-130">-Confirm</span></span>
<span data-ttu-id="540d6-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="540d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="540d6-132">-WhatIf</span></span>
<span data-ttu-id="540d6-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="540d6-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="540d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="540d6-135">CommonParameters</span></span>
<span data-ttu-id="540d6-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="540d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="540d6-137">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="540d6-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="540d6-138">입력</span><span class="sxs-lookup"><span data-stu-id="540d6-138">INPUTS</span></span>

### <span data-ttu-id="540d6-139">System.String</span><span class="sxs-lookup"><span data-stu-id="540d6-139">System.String</span></span>

### <span data-ttu-id="540d6-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="540d6-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="540d6-141">출력</span><span class="sxs-lookup"><span data-stu-id="540d6-141">OUTPUTS</span></span>

### <span data-ttu-id="540d6-142">Microsoft.Azure.AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="540d6-142">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="540d6-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="540d6-143">NOTES</span></span>

## <span data-ttu-id="540d6-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="540d6-144">RELATED LINKS</span></span>

[<span data-ttu-id="540d6-145">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="540d6-145">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)

[<span data-ttu-id="540d6-146">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="540d6-146">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)

[<span data-ttu-id="540d6-147">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="540d6-147">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="540d6-148">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="540d6-148">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="540d6-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="540d6-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="540d6-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="540d6-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

