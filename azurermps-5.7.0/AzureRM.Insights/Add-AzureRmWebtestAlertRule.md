---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: FBAE5F75-1E28-4F1C-A9ED-20075FFD4AC7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/add-azurermwebtestalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Add-AzureRmWebtestAlertRule.md
ms.openlocfilehash: da395b66cb4d63593c097f214701365370e06b75
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529813"
---
# <span data-ttu-id="c712a-101">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="c712a-101">Add-AzureRmWebtestAlertRule</span></span>

## <span data-ttu-id="c712a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c712a-102">SYNOPSIS</span></span>
<span data-ttu-id="c712a-103">Webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-103">Adds or updates a webtest alert rule.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c712a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c712a-104">SYNTAX</span></span>

```
Add-AzureRmWebtestAlertRule -MetricName <String> -TargetResourceUri <String> -WindowSize <TimeSpan>
 -FailedLocationCount <Int32> [-MetricNamespace <String>] -Location <String> [-Description <String>]
 [-DisableRule] -ResourceGroupName <String> -Name <String>
 [-Action <System.Collections.Generic.List`1[Microsoft.Azure.Management.Insights.Models.RuleAction]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c712a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c712a-105">DESCRIPTION</span></span>
<span data-ttu-id="c712a-106">**AzureRmWebtestAlertRule** cmdlet은 메트릭, 이벤트 또는 webtest 유형의 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-106">The **Add-AzureRmWebtestAlertRule** cmdlet adds or updates an alert rule of either metric, event, or webtest type.</span></span>
<span data-ttu-id="c712a-107">추가한 규칙이 리소스 그룹과 연결 되어 있으며 이름이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-107">The added rule is associated to a resource group and has a name.</span></span>
<span data-ttu-id="c712a-108">이 cmdlet은 ShouldProcess 패턴을 구현 합니다. 즉, 리소스를 실제로 생성, 수정 또는 제거 하기 전에 사용자에 게 확인을 요청할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-108">This cmdlet implements the ShouldProcess pattern, i.e. it might request confirmation from the user before actually creating, modifying, or removing the resource.</span></span>

## <span data-ttu-id="c712a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c712a-109">EXAMPLES</span></span>

### <span data-ttu-id="c712a-110">예제 1: webtest 알림 규칙 추가</span><span class="sxs-lookup"><span data-stu-id="c712a-110">Example 1: Add a webtest alert rule</span></span>
```
PS C:\>Add-AzureRmWebtestAlertRule -Name "webtestRule" -Location "East US" -ResourceGroup "Default-Web-EastUS" -WindowSize 00:05:00 -MetricName "metric" -TargetResourceUri ":/subscriptions/b67f7fec-69fc-4974-9099-a26bd6ffeda3/resourcegroups/Default-Web-WestUS/providers/microsoft.insights/webtests/leowebtestr1-webtestr1" -Description "Nice Webtest rule" -Failed 3
RequestId                                                                                                    StatusCode
---------                                                                                                    ----------
9a5bc388-c7ac-4dc6-aa70-f4bc29c2c712                                                                                 OK
```

<span data-ttu-id="c712a-111">이 명령은 webtest 경고 규칙을 추가 하거나 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-111">This command adds or updates a webtest alert rule.</span></span>

## <span data-ttu-id="c712a-112">변수</span><span class="sxs-lookup"><span data-stu-id="c712a-112">PARAMETERS</span></span>

### <span data-ttu-id="c712a-113">-작업</span><span class="sxs-lookup"><span data-stu-id="c712a-113">-Action</span></span>
<span data-ttu-id="c712a-114">쉼표로 구분 된 작업 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-114">Specifies a comma-separated list of actions.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Management.Monitor.Management.Models.RuleAction]
Parameter Sets: (All)
Aliases: Actions

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c712a-115">-DefaultProfile</span></span>
<span data-ttu-id="c712a-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="c712a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-117">-설명</span><span class="sxs-lookup"><span data-stu-id="c712a-117">-Description</span></span>
<span data-ttu-id="c712a-118">규칙에 대 한 설명을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-118">Specifies a description of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-119">-DisableRule</span><span class="sxs-lookup"><span data-stu-id="c712a-119">-DisableRule</span></span>
<span data-ttu-id="c712a-120">규칙을 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-120">Disables the rule.</span></span>
<span data-ttu-id="c712a-121">이 매개 변수를 지정 하지 않으면 규칙을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-121">If you do not specify this parameter, the rule is enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-122">-FailedLocationCount</span><span class="sxs-lookup"><span data-stu-id="c712a-122">-FailedLocationCount</span></span>
<span data-ttu-id="c712a-123">Webtest 규칙의 실패 한 위치 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-123">Specifies the failed location count for the webtest rules.</span></span>
<span data-ttu-id="c712a-124">이는 다른 유형의 규칙에 있는 임계값과 유사 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-124">This is similar to the threshold in the other types of rules.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-125">-위치</span><span class="sxs-lookup"><span data-stu-id="c712a-125">-Location</span></span>
<span data-ttu-id="c712a-126">규칙이 정의 된 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-126">Specifies the location where the rule is defined.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-127">-MetricName</span><span class="sxs-lookup"><span data-stu-id="c712a-127">-MetricName</span></span>
<span data-ttu-id="c712a-128">메트릭의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-128">Specifies the name of the metric.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-129">-MetricNamespace</span><span class="sxs-lookup"><span data-stu-id="c712a-129">-MetricNamespace</span></span>
<span data-ttu-id="c712a-130">규칙에 대 한 메트릭 네임 스페이스를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-130">Specifies the metric namespace for rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-131">-이름</span><span class="sxs-lookup"><span data-stu-id="c712a-131">-Name</span></span>
<span data-ttu-id="c712a-132">규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-132">Specifies the name of the rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c712a-133">-ResourceGroupName</span></span>
<span data-ttu-id="c712a-134">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-134">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-135">-TargetResourceUri</span><span class="sxs-lookup"><span data-stu-id="c712a-135">-TargetResourceUri</span></span>
<span data-ttu-id="c712a-136">Webtest의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-136">Specifies the resource ID of the webtest.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-137">-WindowSize</span><span class="sxs-lookup"><span data-stu-id="c712a-137">-WindowSize</span></span>
<span data-ttu-id="c712a-138">해당 데이터를 계산 하는 규칙의 시간 창 크기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-138">Specifies the time window size for the rule to compute its data.</span></span>

```yaml
Type: TimeSpan
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c712a-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c712a-139">CommonParameters</span></span>
<span data-ttu-id="c712a-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c712a-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c712a-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c712a-142">입력</span><span class="sxs-lookup"><span data-stu-id="c712a-142">INPUTS</span></span>

### <span data-ttu-id="c712a-143">않아야</span><span class="sxs-lookup"><span data-stu-id="c712a-143">None</span></span>
<span data-ttu-id="c712a-144">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-144">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="c712a-145">출력</span><span class="sxs-lookup"><span data-stu-id="c712a-145">OUTPUTS</span></span>

### <span data-ttu-id="c712a-146">PSAddAlertRuleOperationResponse를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="c712a-146">Microsoft.Azure.Commands.Insights.OutputClasses.PSAddAlertRuleOperationResponse</span></span>

## <span data-ttu-id="c712a-147">상속자</span><span class="sxs-lookup"><span data-stu-id="c712a-147">NOTES</span></span>

## <span data-ttu-id="c712a-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c712a-148">RELATED LINKS</span></span>

[<span data-ttu-id="c712a-149">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c712a-149">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c712a-150">추가-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="c712a-150">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="c712a-151">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="c712a-151">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="c712a-152">새로운 AzureRmAlertRuleWebhook</span><span class="sxs-lookup"><span data-stu-id="c712a-152">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


