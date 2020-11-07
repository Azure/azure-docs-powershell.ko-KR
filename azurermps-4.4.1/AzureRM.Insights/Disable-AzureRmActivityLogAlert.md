---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: B5F2388E-0136-4F8A-8577-67CE2A45671E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Disable-AzureRmActivityLogAlert.md
ms.openlocfilehash: cf920fe8fbe235a2c003bebc0cdecf1a480926ba
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711547"
---
# <span data-ttu-id="9aee5-101">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9aee5-101">Disable-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="9aee5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9aee5-102">SYNOPSIS</span></span>
<span data-ttu-id="9aee5-103">활동 로그 알림을 비활성화 하 고 해당 태그를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-103">Disables an activity log alert and sets its tags.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9aee5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9aee5-104">SYNTAX</span></span>

### <span data-ttu-id="9aee5-105">활동 로그 사용 안 함 경고에 대 한 기본 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9aee5-105">Default parameters for disable an activity log alert</span></span>
```
Disable-AzureRmActivityLogAlert -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee5-106">파이프에서 값을 가져오는 활동 로그 알림을 사용 하지 않도록 설정 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9aee5-106">Parameters to disable an activity log alerts taking value from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9aee5-107">파이프에서 ResourceId 값을 가져오는 활동 로그 알림을 사용 하지 않도록 설정 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="9aee5-107">Parameters to disable an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Disable-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9aee5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="9aee5-108">DESCRIPTION</span></span>
<span data-ttu-id="9aee5-109">AzureRmActivityLogAlert cmdlet을 **사용 하지** 않도록 설정 하 고 활동 로그 알림을 설정 하 고 해당 태그 설정을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-109">The **Disable-AzureRmActivityLogAlert** cmdlet disables and activity log alert and allows setting its tags.</span></span>
<span data-ttu-id="9aee5-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 패치 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="9aee5-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="9aee5-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9aee5-111">EXAMPLES</span></span>

### <span data-ttu-id="9aee5-112">예제 1: 활동 로그 알림 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9aee5-112">Example 1: Disable an activity log alert</span></span>
```
PS C:\>Disable-AzureRmActivityLogAlert -Name "alert1" -ResourceGroupName "Default-ActivityLogsAlerts"
```

<span data-ttu-id="9aee5-113">이 명령은 리소스 그룹 기본값-ActivityLogsAlerts에서 alert1 이라는 활동 로그 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-113">This command disables the activity log alert called alert1 in the resource group Default-ActivityLogsAlerts.</span></span>

<span data-ttu-id="9aee5-114">이 명령은 alert1 이라는 활동 로그 알림의 tags 속성을 변경 하 고 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-114">This command changes the tags property of the activity log alert called alert1 and disables it.</span></span>

### <span data-ttu-id="9aee5-115">예제 2: PSActivityLogAlertResource 개체를 입력으로 사용 하 여 활동 로그 알림 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9aee5-115">Example 2: Disable an activity log alert using a PSActivityLogAlertResource object as input</span></span>
```
PS C:\>$obj = Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1"
PS C:\>Disable-AzureRmActivityLogAlert -InputObject $obj
```

<span data-ttu-id="9aee5-116">이 명령은 alert1 이라는 활동 로그 알림을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-116">This command disables an activity log alert called alert1.</span></span> <span data-ttu-id="9aee5-117">이를 위해 PSActivityLogAlertResource 개체를 입력 인수로 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-117">For this it uses a PSActivityLogAlertResource object as input argument.</span></span>

### <span data-ttu-id="9aee5-118">예제 3: ResourceId 매개 변수를 사용 하 여 ActivityLogAlert 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="9aee5-118">Example 3: Disable the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Disable-AzureRmActivityLogAlert
```

<span data-ttu-id="9aee5-119">이 명령은 파이프의 ResourceId 매개 변수를 사용 하 여 ActivityLogAlert를 비활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-119">This command disables the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="9aee5-120">변수</span><span class="sxs-lookup"><span data-stu-id="9aee5-120">PARAMETERS</span></span>

### <span data-ttu-id="9aee5-121">-이름</span><span class="sxs-lookup"><span data-stu-id="9aee5-121">-Name</span></span>
<span data-ttu-id="9aee5-122">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-122">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee5-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9aee5-123">-ResourceGroupName</span></span>
<span data-ttu-id="9aee5-124">알림 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-124">The name of the resource group where the alert resource is going to exist.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for disable an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee5-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9aee5-125">-InputObject</span></span>
<span data-ttu-id="9aee5-126">필요한 이름, 리소스 그룹 이름 및 선택적 태그 속성을 추출 하는 호출의 InputObject tags 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-126">Sets the InputObject tags property of the call to extract the required name, resource group name, and the optional tag properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to disable an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee5-127">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9aee5-127">-ResourceId</span></span>
<span data-ttu-id="9aee5-128">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-128">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to disable an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="9aee5-129">-확인</span><span class="sxs-lookup"><span data-stu-id="9aee5-129">-Confirm</span></span>
<span data-ttu-id="9aee5-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9aee5-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9aee5-131">-DefaultProfile</span></span>
<span data-ttu-id="9aee5-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9aee5-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9aee5-133">-WhatIf</span></span>
<span data-ttu-id="9aee5-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9aee5-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9aee5-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9aee5-136">CommonParameters</span></span>
<span data-ttu-id="9aee5-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9aee5-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9aee5-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9aee5-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9aee5-139">입력</span><span class="sxs-lookup"><span data-stu-id="9aee5-139">INPUTS</span></span>

## <span data-ttu-id="9aee5-140">출력</span><span class="sxs-lookup"><span data-stu-id="9aee5-140">OUTPUTS</span></span>

### <span data-ttu-id="9aee5-141">Microsoft Azure. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="9aee5-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="9aee5-142">상속자</span><span class="sxs-lookup"><span data-stu-id="9aee5-142">NOTES</span></span>

## <span data-ttu-id="9aee5-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9aee5-143">RELATED LINKS</span></span>

[<span data-ttu-id="9aee5-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9aee5-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9aee5-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9aee5-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9aee5-146">제거-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9aee5-146">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="9aee5-147">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="9aee5-147">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="9aee5-148">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="9aee5-148">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

[<span data-ttu-id="9aee5-149">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="9aee5-149">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)
