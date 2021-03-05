---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/powershell/module/az.monitor/disable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Disable-AzActivityLogAlert.md
ms.openlocfilehash: 0f8e532e1bda9555c12cdf0770a5c2c986e8eac7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980235"
---
# <span data-ttu-id="12862-101">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12862-101">Disable-AzActivityLogAlert</span></span>

## <span data-ttu-id="12862-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="12862-102">SYNOPSIS</span></span>
<span data-ttu-id="12862-103">활동 로그 경고를 사용하지 않도록 설정하고 해당 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-103">Disables an activity log alert and sets its tags.</span></span>

## <span data-ttu-id="12862-104">구문</span><span class="sxs-lookup"><span data-stu-id="12862-104">SYNTAX</span></span>

### <span data-ttu-id="12862-105">DisableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="12862-105">DisableByNameAndResourceGroup</span></span>
```
Disable-AzActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12862-106">DisableByInputObject</span><span class="sxs-lookup"><span data-stu-id="12862-106">DisableByInputObject</span></span>
```
Disable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="12862-107">DisableByResourceId</span><span class="sxs-lookup"><span data-stu-id="12862-107">DisableByResourceId</span></span>
```
Disable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="12862-108">설명</span><span class="sxs-lookup"><span data-stu-id="12862-108">DESCRIPTION</span></span>
<span data-ttu-id="12862-109">**Disable-AzActivityLogAlert** cmdlet은 비활성화 및 활동 로그 경고를 해제하고 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12862-109">The **Disable-AzActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="12862-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 실제로 리소스를 패치하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="12862-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="12862-111">예제</span><span class="sxs-lookup"><span data-stu-id="12862-111">EXAMPLES</span></span>

### <span data-ttu-id="12862-112">예제 1: 활동 로그 경고 사용 안 하여</span><span class="sxs-lookup"><span data-stu-id="12862-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="12862-113">이 명령은 리소스 그룹 Default-ActivityLogsAlerts에서 alert1이라는 활동 로그 경고를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>
<span data-ttu-id="12862-114">이 명령은 alert1이라는 활동 로그 경고의 태그 속성을 변경하고 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="12862-115">예제 2: PSActivityLogAlertResource 개체를 입력으로 사용하여 활동 로그 경고 비활성화</span><span class="sxs-lookup"><span data-stu-id="12862-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="12862-116">이 명령은 alert1이라는 활동 로그 경고를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="12862-117">이를 위해 PSActivityLogAlertResource 개체를 입력 인수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="12862-118">예제 3: ResourceId 매개 변수를 사용하여 ActivityLogAlert 사용 안</span><span class="sxs-lookup"><span data-stu-id="12862-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Disable-AzActivityLogAlert
```

<span data-ttu-id="12862-119">이 명령은 파이프의 ResourceId 매개 변수를 사용하여 ActivityLogAlert를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="12862-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="12862-120">PARAMETERS</span></span>

### <span data-ttu-id="12862-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="12862-121">-DefaultProfile</span></span>
<span data-ttu-id="12862-122">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="12862-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="12862-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="12862-123">-InputObject</span></span>
<span data-ttu-id="12862-124">필요한 이름, 리소스 그룹 이름 및 선택적 태그 속성을 추출하기 위해 호출의 InputObject 태그 속성을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-124">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: DisableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="12862-125">-Name</span><span class="sxs-lookup"><span data-stu-id="12862-125">-Name</span></span>
<span data-ttu-id="12862-126">활동 로그 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12862-126">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12862-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="12862-127">-ResourceGroupName</span></span>
<span data-ttu-id="12862-128">경고 리소스가 존재할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="12862-128">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12862-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="12862-129">-ResourceId</span></span>
<span data-ttu-id="12862-130">호출의 ResourceId 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-130">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: DisableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="12862-131">-확인</span><span class="sxs-lookup"><span data-stu-id="12862-131">-Confirm</span></span>
<span data-ttu-id="12862-132">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="12862-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="12862-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="12862-133">-WhatIf</span></span>
<span data-ttu-id="12862-134">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="12862-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="12862-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="12862-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="12862-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="12862-136">CommonParameters</span></span>
<span data-ttu-id="12862-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="12862-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="12862-138">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="12862-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="12862-139">입력</span><span class="sxs-lookup"><span data-stu-id="12862-139">INPUTS</span></span>

### <span data-ttu-id="12862-140">System.String</span><span class="sxs-lookup"><span data-stu-id="12862-140">System.String</span></span>

### <span data-ttu-id="12862-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="12862-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="12862-142">출력</span><span class="sxs-lookup"><span data-stu-id="12862-142">OUTPUTS</span></span>

### <span data-ttu-id="12862-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="12862-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="12862-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="12862-144">NOTES</span></span>

## <span data-ttu-id="12862-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="12862-145">RELATED LINKS</span></span>

[<span data-ttu-id="12862-146">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12862-146">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="12862-147">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12862-147">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="12862-148">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12862-148">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="12862-149">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="12862-149">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="12862-150">New-AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="12862-150">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="12862-151">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="12862-151">Enable-AzActivityLogAlert</span></span>](./Enable-AzActivityLogAlert.md)
