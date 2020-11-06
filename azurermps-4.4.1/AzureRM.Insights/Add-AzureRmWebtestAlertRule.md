---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: 52b3d39aef4c117fe8b26bb35f1bf50143e5fec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537183"
---
# <span data-ttu-id="6aed3-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="6aed3-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="6aed3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aed3-102">SYNOPSIS</span></span>
<span data-ttu-id="6aed3-103">Webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aed3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6aed3-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroup <String> -Name <String>
 [-Actions <System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6aed3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6aed3-105">DESCRIPTION</span></span>
<span data-ttu-id="6aed3-106">**AzureRmWebtestAlertRule** cmdlet은 메트릭, 이벤트 또는 webtest 유형의 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="6aed3-107">추가한 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-107">The added rule is associated to a resource group and has a name.</span></span>

## <span data-ttu-id="6aed3-108">예제의</span><span class="sxs-lookup"><span data-stu-id="6aed3-108">EXAMPLES</span></span>

### <span data-ttu-id="6aed3-109">예제 1: webtest 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="6aed3-109">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="6aed3-110">이 명령은 webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-110">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="6aed3-111">변수</span><span class="sxs-lookup"><span data-stu-id="6aed3-111">PARAMETERS</span></span>

### <span data-ttu-id="6aed3-112">-작업</span><span class="sxs-lookup"><span data-stu-id="6aed3-112">-Actions</span></span>
<span data-ttu-id="6aed3-113">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-113">Specifies a comma-separated list of actions.</span></span>

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

### <span data-ttu-id="6aed3-114">-설명</span><span class="sxs-lookup"><span data-stu-id="6aed3-114">-Description</span></span>
<span data-ttu-id="6aed3-115">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-115">Specifies a description of the rule.</span></span>

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

### <span data-ttu-id="6aed3-116">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="6aed3-116">-DisableRule</span></span>
<span data-ttu-id="6aed3-117">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-117">Disables the rule.</span></span>
<span data-ttu-id="6aed3-118">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-118">If you do not specify this parameter, the rule is enabled.</span></span>

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

### <span data-ttu-id="6aed3-119">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="6aed3-119">-FailedLocationCount</span></span>
<span data-ttu-id="6aed3-120">Webtest 규칙의 실패 한 위치 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-120">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="6aed3-121">이는 다른 유형의 규칙에 있는 임계값과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-121">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aed3-122">-위치</span><span class="sxs-lookup"><span data-stu-id="6aed3-122">-Location</span></span>
<span data-ttu-id="6aed3-123">규칙이 정의 된 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-123">Specifies the location where the rule is defined.</span></span>

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

### <span data-ttu-id="6aed3-124">-MetricName</span><span class="sxs-lookup"><span data-stu-id="6aed3-124">-MetricName</span></span>
<span data-ttu-id="6aed3-125">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-125">Specifies the name of the metric.</span></span>

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

### <span data-ttu-id="6aed3-126">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="6aed3-126">-MetricNamespace</span></span>
<span data-ttu-id="6aed3-127">규칙에 대 한 메트릭 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-127">Specifies the metric namespace for rule.</span></span>

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

### <span data-ttu-id="6aed3-128">-이름</span><span class="sxs-lookup"><span data-stu-id="6aed3-128">-Name</span></span>
<span data-ttu-id="6aed3-129">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-129">Specifies the name of the rule.</span></span>

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

### <span data-ttu-id="6aed3-130">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="6aed3-130">-ResourceGroup</span></span>
<span data-ttu-id="6aed3-131">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-131">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="6aed3-132">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="6aed3-132">-TargetResourceUri</span></span>
<span data-ttu-id="6aed3-133">Webtest의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-133">Specifies the resource ID of the webtest.</span></span>

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

### <span data-ttu-id="6aed3-134">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="6aed3-134">-WindowSize</span></span>
<span data-ttu-id="6aed3-135">해당 데이터를 계산 하는 규칙의 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-135">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: System.TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6aed3-136">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aed3-136">-DefaultProfile</span></span>
<span data-ttu-id="6aed3-137">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-137">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aed3-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aed3-138">CommonParameters</span></span>
<span data-ttu-id="6aed3-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aed3-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aed3-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aed3-141">입력</span><span class="sxs-lookup"><span data-stu-id="6aed3-141">INPUTS</span></span>

## <span data-ttu-id="6aed3-142">출력</span><span class="sxs-lookup"><span data-stu-id="6aed3-142">OUTPUTS</span></span>

### <span data-ttu-id="6aed3-143">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aed3-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="6aed3-144">상속자</span><span class="sxs-lookup"><span data-stu-id="6aed3-144">NOTES</span></span>

## <span data-ttu-id="6aed3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aed3-145">RELATED LINKS</span></span>

[<span data-ttu-id="6aed3-146">추가-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="6aed3-146">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="6aed3-147">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="6aed3-147">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="6aed3-148">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="6aed3-148">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="6aed3-149">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="6aed3-149">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


