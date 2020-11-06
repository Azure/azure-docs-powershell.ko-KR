---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 11A521DF-E77C-4D6F-A2D9-1C2CF8972F57
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmLogAlertRule.md
ms.openlocfilehash: 38644018ac9ae19d1c413123ca071f564d336fa7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537192"
---
# <span data-ttu-id="89570-101">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="89570-101">Add-AzureRmLogAlertRule</span></span>

## <span data-ttu-id="89570-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="89570-102">SYNOPSIS</span></span>
<span data-ttu-id="89570-103">로그 알림 규칙을 추가 하거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="89570-103">Adds or replaces a log alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="89570-104">구문과</span><span class="sxs-lookup"><span data-stu-id="89570-104">SYNTAX</span></span>

```
Add-AzureRmLogAlertRule [-TargetResourceGroup <String>] [-TargetResourceId <String>] [-Level <String>]
 -OperationName <String> [-TargetResourceProvider <String>] [-Status <String>] [-SubStatus <String>]
 -Location <String> [-Description <String>] [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="89570-105">설명은</span><span class="sxs-lookup"><span data-stu-id="89570-105">DESCRIPTION</span></span>
<span data-ttu-id="89570-106">**Add-AzureRmLogAlertRule** cmdlet은 이벤트 경고 규칙을 추가 하거나 바꿉니다.</span><span class="sxs-lookup"><span data-stu-id="89570-106">The **Add-AzureRmLogAlertRule** cmdlet adds or replaces an event alert rule.</span></span>
<span data-ttu-id="89570-107">추가 된 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89570-107">The added rule is associated with a resource group and has a name.</span></span>

<span data-ttu-id="89570-108">이전 릴리스에서 발표 된 것 처럼 **AzureRMLogAlertRule cmdlet은 이후 릴리스에서 더 이상 사용 되지 않습니다.**</span><span class="sxs-lookup"><span data-stu-id="89570-108">As announced in previous releases: **Add-AzureRMLogAlertRule cmdlet will be deprecated in a future release.**</span></span> <span data-ttu-id="89570-109">이 cmdlet을 사용 하는 첫 번째 2017 년 10 월 이후이 기능은 활동 로그 알림으로 전환 되는 데 영향을 주지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89570-109">After October 1st 2017 using this cmdlet will no longer have any effect as this functionality is being transitioned to Activity Log Alerts.</span></span> <span data-ttu-id="89570-110">**_https://aka.ms/migratemealerts_** 자세한 내용은을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="89570-110">Please see **_https://aka.ms/migratemealerts_** for more information.</span></span>

## <span data-ttu-id="89570-111">예제의</span><span class="sxs-lookup"><span data-stu-id="89570-111">EXAMPLES</span></span>

### <span data-ttu-id="89570-112">예제 1: 로그 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="89570-112">Example 1: Add a log alert rule</span></span>
```
PS C:\>Add-AzureRmLogAlertRule -Name "logRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -OperationName "Create" -TargetResourceId "/subscriptions/abbfb07c-6c93-40be-bc9b-4f0deba32f4c/resourceGroups/Default-Web-EastUS/providers/microsoft.web/sites/misitiooeltuyo" -Description "My log rule"
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="89570-113">이 명령은 이벤트 기반 알림 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-113">This command adds or updates an event-based alert rule.</span></span>

## <span data-ttu-id="89570-114">변수</span><span class="sxs-lookup"><span data-stu-id="89570-114">PARAMETERS</span></span>

### <span data-ttu-id="89570-115">-작업</span><span class="sxs-lookup"><span data-stu-id="89570-115">-Actions</span></span>
<span data-ttu-id="89570-116">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-116">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-117">-설명</span><span class="sxs-lookup"><span data-stu-id="89570-117">-Description</span></span>
<span data-ttu-id="89570-118">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-118">Specifies a description of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="89570-119">-DisableRule</span></span>
<span data-ttu-id="89570-120">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="89570-120">Disables a rule.</span></span>
<span data-ttu-id="89570-121">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="89570-121">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="89570-122">수준</span><span class="sxs-lookup"><span data-stu-id="89570-122">-Level</span></span>
<span data-ttu-id="89570-123">규칙이 모니터링 하는 이벤트 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-123">Specifies the level of the event the rule is monitoring.</span></span>
<span data-ttu-id="89570-124">이벤트 기반 규칙에 대해서만이 매개 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-124">Specify this parameter only for event-based rules.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-125">-위치</span><span class="sxs-lookup"><span data-stu-id="89570-125">-Location</span></span>
<span data-ttu-id="89570-126">규칙의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-126">Specifies the location for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-127">-이름</span><span class="sxs-lookup"><span data-stu-id="89570-127">-Name</span></span>
<span data-ttu-id="89570-128">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-128">Specifies the name of the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-129">-OperationName</span><span class="sxs-lookup"><span data-stu-id="89570-129">-OperationName</span></span>
<span data-ttu-id="89570-130">작업의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-130">Specifies the name of the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-131">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89570-131">-ResourceGroup</span></span>
<span data-ttu-id="89570-132">규칙에 대 한 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-132">Specifies the name of the resource group for the rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-133">-상태</span><span class="sxs-lookup"><span data-stu-id="89570-133">-Status</span></span>
<span data-ttu-id="89570-134">상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-134">Specifies the status.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-135">-하위 상태</span><span class="sxs-lookup"><span data-stu-id="89570-135">-SubStatus</span></span>
<span data-ttu-id="89570-136">하위 상태를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-136">Specifies the substatus.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-137">-TargetResourceGroup</span><span class="sxs-lookup"><span data-stu-id="89570-137">-TargetResourceGroup</span></span>
<span data-ttu-id="89570-138">규칙이 모니터링 하는 리소스의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-138">Specifies the resource group of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-139">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="89570-139">-TargetResourceId</span></span>
<span data-ttu-id="89570-140">규칙이 모니터링 하는 리소스의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-140">Specifies the ID of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-141">-TargetResourceProvider</span><span class="sxs-lookup"><span data-stu-id="89570-141">-TargetResourceProvider</span></span>
<span data-ttu-id="89570-142">규칙이 모니터링 하는 리소스의 리소스 공급자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-142">Specifies the resource provider of the resource the rule is monitoring.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="89570-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="89570-143">-DefaultProfile</span></span>
<span data-ttu-id="89570-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="89570-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="89570-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="89570-145">CommonParameters</span></span>
<span data-ttu-id="89570-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="89570-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="89570-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="89570-148">입력</span><span class="sxs-lookup"><span data-stu-id="89570-148">INPUTS</span></span>

## <span data-ttu-id="89570-149">출력</span><span class="sxs-lookup"><span data-stu-id="89570-149">OUTPUTS</span></span>

### <span data-ttu-id="89570-150">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="89570-150">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="89570-151">상속자</span><span class="sxs-lookup"><span data-stu-id="89570-151">NOTES</span></span>

## <span data-ttu-id="89570-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="89570-152">RELATED LINKS</span></span>

[<span data-ttu-id="89570-153">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="89570-153">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="89570-154">추가-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="89570-154">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="89570-155">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="89570-155">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="89570-156">새로운 AzureRmAlertRuleEmail</span><span class="sxs-lookup"><span data-stu-id="89570-156">New-AzureRmAlertRuleEmail</span></span>](./New-AzureRmAlertRuleEmail.md)

[<span data-ttu-id="89570-157">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="89570-157">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


