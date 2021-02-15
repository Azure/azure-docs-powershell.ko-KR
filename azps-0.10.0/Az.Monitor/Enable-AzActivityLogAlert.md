---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 89a2d96b79fa771b18e085978c85c7a98da4e9b5
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100398770"
---
# <span data-ttu-id="ddaab-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ddaab-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="ddaab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ddaab-102">SYNOPSIS</span></span>
<span data-ttu-id="ddaab-103">활동 로그 경고를 설정하고 해당 태그를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="ddaab-104">구문</span><span class="sxs-lookup"><span data-stu-id="ddaab-104">SYNTAX</span></span>

### <span data-ttu-id="ddaab-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ddaab-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddaab-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="ddaab-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ddaab-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="ddaab-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ddaab-108">설명</span><span class="sxs-lookup"><span data-stu-id="ddaab-108">DESCRIPTION</span></span>
<span data-ttu-id="ddaab-109">**Enable-AzActivityLogAlert** cmdlet을 사용하면 활동 로그 경고를 사용하도록 설정하고 해당 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="ddaab-110">이 cmdlet은 ShouldProcess 패턴을 구현합니다. 즉, 리소스를 실제로 패치하기 전에 사용자로부터 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="ddaab-111">예제</span><span class="sxs-lookup"><span data-stu-id="ddaab-111">EXAMPLES</span></span>

### <span data-ttu-id="ddaab-112">예제 1: 활동 로그 경고 사용</span><span class="sxs-lookup"><span data-stu-id="ddaab-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="ddaab-113">이 명령은 리소스 그룹 Default-ActivityLogsAlerts에서 alert1이라는 활동 로그 경고를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="ddaab-114">예제 2: PSActivityLogAlertResource 개체를 입력으로 사용하여 활동 로그 경고 사용</span><span class="sxs-lookup"><span data-stu-id="ddaab-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="ddaab-115">이 명령은 alert1이라는 활동 로그 경고를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="ddaab-116">이를 위해 PSActivityLogAlertResource 개체를 입력 인수로 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="ddaab-117">예제 3: ResourceId 매개 변수를 사용하여 ActivityLogAlert 사용</span><span class="sxs-lookup"><span data-stu-id="ddaab-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="ddaab-118">이 명령은 파이프의 ResourceId 매개 변수를 사용하여 ActivityLogAlert를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="ddaab-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ddaab-119">PARAMETERS</span></span>

### <span data-ttu-id="ddaab-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ddaab-120">-DefaultProfile</span></span>
<span data-ttu-id="ddaab-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ddaab-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ddaab-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="ddaab-122">-InputObject</span></span>
<span data-ttu-id="ddaab-123">호출의 InputObject 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 및 선택적 태그 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: EnableByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaab-124">-Name</span><span class="sxs-lookup"><span data-stu-id="ddaab-124">-Name</span></span>
<span data-ttu-id="ddaab-125">활동 로그 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-125">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaab-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ddaab-126">-ResourceGroupName</span></span>
<span data-ttu-id="ddaab-127">경고 리소스가 존재할 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-127">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByNameAndResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaab-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="ddaab-128">-ResourceId</span></span>
<span data-ttu-id="ddaab-129">호출의 ResourceId 태그 속성을 설정하여 필요한 이름, 리소스 그룹 이름 속성을 추출합니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: EnableByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ddaab-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ddaab-130">-Confirm</span></span>
<span data-ttu-id="ddaab-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ddaab-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ddaab-132">-WhatIf</span></span>
<span data-ttu-id="ddaab-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ddaab-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ddaab-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ddaab-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ddaab-135">CommonParameters</span></span>
<span data-ttu-id="ddaab-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ddaab-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ddaab-137">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ddaab-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ddaab-138">입력</span><span class="sxs-lookup"><span data-stu-id="ddaab-138">INPUTS</span></span>

### <span data-ttu-id="ddaab-139">System.String</span><span class="sxs-lookup"><span data-stu-id="ddaab-139">System.String</span></span>

### <span data-ttu-id="ddaab-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="ddaab-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="ddaab-141">출력</span><span class="sxs-lookup"><span data-stu-id="ddaab-141">OUTPUTS</span></span>

### <span data-ttu-id="ddaab-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="ddaab-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="ddaab-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ddaab-143">NOTES</span></span>

## <span data-ttu-id="ddaab-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ddaab-144">RELATED LINKS</span></span>

[<span data-ttu-id="ddaab-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ddaab-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="ddaab-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ddaab-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="ddaab-147">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ddaab-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="ddaab-148">New-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="ddaab-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="ddaab-149">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="ddaab-149">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
