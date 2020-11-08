---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/enable-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Enable-AzActivityLogAlert.md
ms.openlocfilehash: 6e3414efd21b1dd333f91e24333cda05ea650600
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213493"
---
# <span data-ttu-id="a98cb-101">Enable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a98cb-101">Enable-AzActivityLogAlert</span></span>

## <span data-ttu-id="a98cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a98cb-102">SYNOPSIS</span></span>
<span data-ttu-id="a98cb-103">활동 로그 알림을 사용 하 고 해당 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-103">Enables an activity log alert and sets its Tags.</span></span>

## <span data-ttu-id="a98cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a98cb-104">SYNTAX</span></span>

### <span data-ttu-id="a98cb-105">EnableByNameAndResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a98cb-105">EnableByNameAndResourceGroup</span></span>
```
Enable-AzActivityLogAlert -Name <String> -ResourceGroupName <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a98cb-106">EnableByInputObject</span><span class="sxs-lookup"><span data-stu-id="a98cb-106">EnableByInputObject</span></span>
```
Enable-AzActivityLogAlert -InputObject <PSActivityLogAlertResource> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a98cb-107">EnableByResourceId</span><span class="sxs-lookup"><span data-stu-id="a98cb-107">EnableByResourceId</span></span>
```
Enable-AzActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a98cb-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a98cb-108">DESCRIPTION</span></span>
<span data-ttu-id="a98cb-109">**AzActivityLogAlert** cmdlet을 사용 하면 활동 로그 알림을 사용 하도록 설정 하 고 해당 태그를 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-109">The **Enable-AzActivityLogAlert** cmdlet allows enabling an activity log alert and setting its tags.</span></span>
<span data-ttu-id="a98cb-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 패치 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="a98cb-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="a98cb-111">예제의</span><span class="sxs-lookup"><span data-stu-id="a98cb-111">EXAMPLES</span></span>

### <span data-ttu-id="a98cb-112">예제 1: 활동 로그 알림 활성화</span><span class="sxs-lookup"><span data-stu-id="a98cb-112">Example 1: Enable an activity log alert</span></span>
```
PS C:\>Enable-AzActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="a98cb-113">이 명령은 리소스 그룹 기본값-ActivityLogsAlerts에서 alert1 이라는 활동 로그 알림을 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-113">This command enables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

### <span data-ttu-id="a98cb-114">예제 2: PSActivityLogAlertResource 개체를 입력으로 사용 하 여 활동 로그 알림 설정</span><span class="sxs-lookup"><span data-stu-id="a98cb-114">Example 2: Enable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Enable-AzActivityLogAlert -InputObject $obj
```

<span data-ttu-id="a98cb-115">이 명령을 사용 하면 alert1 이라는 활동 로그 알림을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-115">This command enables an activity log alert called alert1.</span></span> <span data-ttu-id="a98cb-116">이를 위해 PSActivityLogAlertResource 개체를 입력 인수로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-116">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="a98cb-117">예제 3: ResourceId 매개 변수를 사용 하 여 ActivityLogAlert 사용</span><span class="sxs-lookup"><span data-stu-id="a98cb-117">Example 3: Enable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Get-AzResource -ResourceGroupName "myResourceGroup" -Name "myLogAlert" | Enable-AzActivityLogAlert
```

<span data-ttu-id="a98cb-118">이 명령은 파이프의 ResourceId 매개 변수를 사용 하 여 ActivityLogAlert을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-118">This command enables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="a98cb-119">변수</span><span class="sxs-lookup"><span data-stu-id="a98cb-119">PARAMETERS</span></span>

### <span data-ttu-id="a98cb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a98cb-120">-DefaultProfile</span></span>
<span data-ttu-id="a98cb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a98cb-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a98cb-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a98cb-122">-InputObject</span></span>
<span data-ttu-id="a98cb-123">필요한 이름, 리소스 그룹 이름 및 선택적 태그 속성을 추출 하는 호출의 InputObject tags 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-123">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tags properties.</span></span>

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

### <span data-ttu-id="a98cb-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a98cb-124">-Name</span></span>
<span data-ttu-id="a98cb-125">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-125">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="a98cb-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a98cb-126">-ResourceGroupName</span></span>
<span data-ttu-id="a98cb-127">알림 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-127">The name of the resource group where the alert resource is going to exist.</span></span>

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

### <span data-ttu-id="a98cb-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a98cb-128">-ResourceId</span></span>
<span data-ttu-id="a98cb-129">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-129">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

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

### <span data-ttu-id="a98cb-130">-확인</span><span class="sxs-lookup"><span data-stu-id="a98cb-130">-Confirm</span></span>
<span data-ttu-id="a98cb-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a98cb-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a98cb-132">-WhatIf</span></span>
<span data-ttu-id="a98cb-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a98cb-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a98cb-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a98cb-135">CommonParameters</span></span>
<span data-ttu-id="a98cb-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a98cb-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a98cb-137">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a98cb-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a98cb-138">입력</span><span class="sxs-lookup"><span data-stu-id="a98cb-138">INPUTS</span></span>

### <span data-ttu-id="a98cb-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a98cb-139">System.String</span></span>

### <span data-ttu-id="a98cb-140">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a98cb-140">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a98cb-141">출력</span><span class="sxs-lookup"><span data-stu-id="a98cb-141">OUTPUTS</span></span>

### <span data-ttu-id="a98cb-142">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="a98cb-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="a98cb-143">상속자</span><span class="sxs-lookup"><span data-stu-id="a98cb-143">NOTES</span></span>

## <span data-ttu-id="a98cb-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a98cb-144">RELATED LINKS</span></span>

[<span data-ttu-id="a98cb-145">Set-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a98cb-145">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="a98cb-146">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a98cb-146">Get-AzActivityLogAlert</span></span>](./Get-AzActivityLogAlert.md)

[<span data-ttu-id="a98cb-147">제거-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a98cb-147">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="a98cb-148">새로운 AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="a98cb-148">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="a98cb-149">새로운 AzActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="a98cb-149">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

[<span data-ttu-id="a98cb-150">Disable-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="a98cb-150">Disable-AzActivityLogAlert</span></span>](./Disable-AzActivityLogAlert.md)
