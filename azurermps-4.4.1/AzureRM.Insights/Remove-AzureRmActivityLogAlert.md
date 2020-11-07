---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: C7EC21C7-1C7E-49B2-9B33-486532FCDAEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Remove-AzureRmActivityLogAlert.md
ms.openlocfilehash: adff43beed709db91b2f22bd1072728d3e7a0425
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711892"
---
# <span data-ttu-id="2afcc-101">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2afcc-101">Remove-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="2afcc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2afcc-102">SYNOPSIS</span></span>
<span data-ttu-id="2afcc-103">활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-103">Removes an activity log alert.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2afcc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2afcc-104">SYNTAX</span></span>

### <span data-ttu-id="2afcc-105">활동 로그 제거 경고의 기본 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2afcc-105">Default parameters for remove an activity log alert</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afcc-106">파이프에서 값을 가져오는 활동 로그 알림을 제거 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2afcc-106">Parameters to remove an activity log alerts taking value from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -InputObject <PSActivityLogAlertResource>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2afcc-107">파이프에서 ResourceId 값을 가져오는 활동 로그 알림을 제거 하는 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2afcc-107">Parameters to remove an activity log alerts taking the value of ResourceId from the pipe</span></span>
```
Remove-AzureRmActivityLogAlert -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2afcc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2afcc-108">DESCRIPTION</span></span>
<span data-ttu-id="2afcc-109">**AzureRmActivityLogAlert** cmdlet은 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-109">The **Remove-AzureRmActivityLogAlert** cmdlet removes an activity log alert.</span></span>
<span data-ttu-id="2afcc-110">이 cmdlet은 ShouldProcess 패턴을 구현 합니다 (예: 리소스를 실제로 패치 하기 전에 사용자에 게 확인을 요청할 수 있음).</span><span class="sxs-lookup"><span data-stu-id="2afcc-110">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually patching the resource.</span></span>

## <span data-ttu-id="2afcc-111">예제의</span><span class="sxs-lookup"><span data-stu-id="2afcc-111">EXAMPLES</span></span>

### <span data-ttu-id="2afcc-112">예제 1: 활동 로그 알림 제거</span><span class="sxs-lookup"><span data-stu-id="2afcc-112">Example 1: Remove an activity log alert</span></span>
```
PS C:\>Remove-AzureRmActivityLogAlert -ResourceGroup "Default-Web-CentralUS" -Name "myalert"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
2c6c159b-0e73-4a01-a67b-c32c1a0008a3                                                                                 OK
```

<span data-ttu-id="2afcc-113">이름 및 리소스 그룹 이름을 입력으로 사용 하 여 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-113">Removes an activity log alert using name and resource group name as inputs.</span></span>

### <span data-ttu-id="2afcc-114">예제 2: PSActivityLogAlertResource를 입력으로 사용 하 여 활동 로그 알림 제거</span><span class="sxs-lookup"><span data-stu-id="2afcc-114">Example 2: Remove an activity log alert using a PSActivityLogAlertResource as input</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroup "Default-activityLogAlerts" -Name "alert1" | Remove-AzureRmActivityLogAlert 
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
5c371547-80b0-4185-9b95-700b129de9d4                                                                                 OK
```

<span data-ttu-id="2afcc-115">PSActivityLogAlertResource를 입력으로 사용 하 여 활동 로그 알림을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-115">Removes an activity log alert using a PSActivityLogAlertResource as input.</span></span>

### <span data-ttu-id="2afcc-116">예제 3: ResourceId 매개 변수를 사용 하 여 ActivityLogAlert 제거</span><span class="sxs-lookup"><span data-stu-id="2afcc-116">Example 3: Remove the ActivityLogAlert using the ResourceId parameter</span></span>
```
PS C:\>Find-AzureRmResource -ResourceGroupEquals "myResourceGroup" -ResourceNameEquals "myLogAlert" | Remove-AzureRmActivityLogAlert
```

<span data-ttu-id="2afcc-117">이 명령은 파이프의 ResourceId 매개 변수를 사용 하 여 ActivityLogAlert를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-117">This command removes the ActivityLogAlert using the ResourceId parameter from the pipe.</span></span>

## <span data-ttu-id="2afcc-118">변수</span><span class="sxs-lookup"><span data-stu-id="2afcc-118">PARAMETERS</span></span>

### <span data-ttu-id="2afcc-119">-이름</span><span class="sxs-lookup"><span data-stu-id="2afcc-119">-Name</span></span>
<span data-ttu-id="2afcc-120">활동 로그 알림의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afcc-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2afcc-121">-ResourceGroupName</span></span>
<span data-ttu-id="2afcc-122">경고 리소스가 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-122">The name of the resource group where the alert resource exists.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for remove an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afcc-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2afcc-123">-InputObject</span></span>
<span data-ttu-id="2afcc-124">필요한 이름을 추출 하는 호출의 InputObject tags 속성 및 리소스 그룹 이름 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-124">Sets the InputObject tags property of the call to extract the required name, and resource group name properties.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource
Parameter Sets: Parameters to remove an activity log alerts taking value from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2afcc-125">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="2afcc-125">-ResourceId</span></span>
<span data-ttu-id="2afcc-126">필요한 이름, 리소스 그룹 이름 속성을 추출 하는 호출의 ResourceId 태그 속성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-126">Sets the ResourceId tags property of the call to extract the required name, resource group name properties.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters to remove an activity log alerts taking the value of ResourceId from the pipe
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2afcc-127">-확인</span><span class="sxs-lookup"><span data-stu-id="2afcc-127">-Confirm</span></span>
<span data-ttu-id="2afcc-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2afcc-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2afcc-129">-DefaultProfile</span></span>
<span data-ttu-id="2afcc-130">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2afcc-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2afcc-131">-WhatIf</span></span>
<span data-ttu-id="2afcc-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="2afcc-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2afcc-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2afcc-134">CommonParameters</span></span>
<span data-ttu-id="2afcc-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2afcc-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2afcc-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2afcc-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2afcc-137">입력</span><span class="sxs-lookup"><span data-stu-id="2afcc-137">INPUTS</span></span>

## <span data-ttu-id="2afcc-138">출력</span><span class="sxs-lookup"><span data-stu-id="2afcc-138">OUTPUTS</span></span>

### <span data-ttu-id="2afcc-139">Microsoft Azure AzureOperationResponse</span><span class="sxs-lookup"><span data-stu-id="2afcc-139">Microsoft.Azure.AzureOperationResponse</span></span>

## <span data-ttu-id="2afcc-140">상속자</span><span class="sxs-lookup"><span data-stu-id="2afcc-140">NOTES</span></span>

## <span data-ttu-id="2afcc-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2afcc-141">RELATED LINKS</span></span>

[<span data-ttu-id="2afcc-142">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2afcc-142">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2afcc-143">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2afcc-143">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2afcc-144">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2afcc-144">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2afcc-145">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2afcc-145">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="2afcc-146">새로운 AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="2afcc-146">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="2afcc-147">새로운 AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="2afcc-147">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

