---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleHistory.md
ms.openlocfilehash: 6afe0a9ce4882b0d04c07db351bf841f6d12b9c7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703857"
---
# <span data-ttu-id="1933c-101">Get-AzureRmAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1933c-101">Get-AzureRmAutoscaleHistory</span></span>

## <span data-ttu-id="1933c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1933c-102">SYNOPSIS</span></span>
<span data-ttu-id="1933c-103">자동 크기 조정 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-103">Gets the Autoscale history.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1933c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1933c-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>]
 [-Status <String>] [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1933c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1933c-105">DESCRIPTION</span></span>
<span data-ttu-id="1933c-106">**AzureRmAutoscaleHistory** Cmdlet은 자동 크기 조정 설정과 관련 된 이벤트 기록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-106">The **Get-AzureRmAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="1933c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1933c-107">EXAMPLES</span></span>

### <span data-ttu-id="1933c-108">예제 1: 구독과 연결 된 모든 이벤트 가져오기</span><span class="sxs-lookup"><span data-stu-id="1933c-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="1933c-109">이 명령은 현재 구독과 연결 된 자동 크기 조정 관련 이벤트를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="1933c-110">예제 2: 특정 리소스에 대 한 GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="1933c-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzureRmAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
Authorization        : 
Caller               : Microsoft.Insights/autoscaleSettings
Claims               :  http://schemas.xmlsoap.org/ws/2005/05/identity/claims/spn: Microsoft.Insights/autoscaleSettings
CorrelationId        : ac5b03ca-05d4-4811-9c27-0314a145f785
Description          : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93-40be-bf3b-4f0deb
                       a10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm'
                       from 1 instances count to 2 instances count. 
EventDataId          : c554f7ed-514c-449c-9338-13e15b4b56a3
EventName            : AutoscaleAction
EventSource          : microsoft.insights/autoscalesettings
EventTimestamp       : 2/10/2015 2:38:19 AM
HttpRequest          : 
Id                   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS/events/c554f7ed-514c-4
                       49c-9338-13e15b4b56a3/ticks/635591326997519815
Level                : Informational
OperationId          : ac5b03ca-05d4-4811-9c27-0314a145f785
OperationName        : ScaleUp
Properties           : 
Description    : The autoscale engine attempting to scale resource '/subscriptions/a93fb07c-6c93
                       -40be-bf3b-4f0deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/De
                       faultServerFarm' from 1 instances count to 2 instances count. 
ResourceName   : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-
                       EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
OldInstancesCount: 1
NewInstancesCount: 2
ActiveAutoscaleProfile: {
                         "Name": "No scheduled times",
                         "Capacity": {
                           "Minimum": "1",
                           "Maximum": "3",
                           "Default": "1"
                         },
                         "Rules": [
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 14.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT5M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "CpuPercentage",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT45M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 4.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT2H"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT10M",
                               "TimeAggregation": "Average",
                               "Operator": "LessThanOrEqual",
                               "Threshold": 50.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Decrease",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           },
                           {
                             "MetricTrigger": {
                               "Name": "BytesReceived",
                               "Namespace": "",
                               "Resource": "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-
                       Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm",
                               "ResourceLocation": "East US",
                               "TimeGrain": "PT1M",
                               "Statistic": "Average",
                               "TimeWindow": "PT5M",
                               "TimeAggregation": "Average",
                               "Operator": "GreaterThanOrEqual",
                               "Threshold": 100.0, 
                               "Source": "WebsiteDedicated:eastuswebspace:DefaultServerFarm"
                             },
                             "ScaleAction": {
                               "Direction": "Increase",
                               "Type": "ChangeCount",
                               "Value": "1",
                               "Cooldown": "PT10M"
                             }
                           }
                         ] 
                       }
ResourceGroupName    : Default-Web-EastUS
ResourceProviderName : microsoft.insights
ResourceId           : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/
                       microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Status               : Succeeded
SubmissionTimestamp  : 2/10/2015 2:38:19 AM
SubscriptionId       : b93fb07a-6f93-30be-bf3e-4f0deca15f4f
SubStatus            :
```

<span data-ttu-id="1933c-111">이 명령은 리소스 ID (본질적으로 ResourceUri)로 식별 되는 특정 리소스와 관련 된 자동 크기 조정 관련 이벤트를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="1933c-112">변수</span><span class="sxs-lookup"><span data-stu-id="1933c-112">PARAMETERS</span></span>

### <span data-ttu-id="1933c-113">-발신자</span><span class="sxs-lookup"><span data-stu-id="1933c-113">-Caller</span></span>
<span data-ttu-id="1933c-114">발신자를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="1933c-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1933c-115">-DefaultProfile</span></span>
<span data-ttu-id="1933c-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1933c-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1933c-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="1933c-117">-DetailedOutput</span></span>
<span data-ttu-id="1933c-118">이 작업에 자세한 출력이 포함 됨을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="1933c-119">이 매개 변수를 지정 하지 않으면 출력이 요약 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="1933c-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="1933c-120">-EndTime</span></span>
<span data-ttu-id="1933c-121">현지 시간으로 쿼리의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="1933c-122">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-122">The default is the current time.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1933c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="1933c-123">-ResourceId</span></span>
<span data-ttu-id="1933c-124">자동 크기 조정 설정이 연결 되는 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="1933c-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="1933c-125">-StartTime</span></span>
<span data-ttu-id="1933c-126">현지 시간으로 쿼리의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="1933c-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-127">This parameter is optional.</span></span>
<span data-ttu-id="1933c-128">기본값은 현재 현지 시간이 1 시간을 뺀 값입니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-128">The default is the current local time minus one hour.</span></span>

```yaml
Type: System.Nullable`1[System.DateTime]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="1933c-129">-상태</span><span class="sxs-lookup"><span data-stu-id="1933c-129">-Status</span></span>
<span data-ttu-id="1933c-130">상태별 필터를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-130">Specifies a filter by status.</span></span>
<span data-ttu-id="1933c-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-131">This parameter is optional.</span></span>
<span data-ttu-id="1933c-132">오류는 빈 문자열입니다 (즉, 필터 없음).</span><span class="sxs-lookup"><span data-stu-id="1933c-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="1933c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1933c-133">CommonParameters</span></span>
<span data-ttu-id="1933c-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1933c-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1933c-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1933c-136">입력</span><span class="sxs-lookup"><span data-stu-id="1933c-136">INPUTS</span></span>

### <span data-ttu-id="1933c-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="1933c-137">System.String</span></span>

### <span data-ttu-id="1933c-138">시스템 Null 허용 ' 1 [[System. DateTime, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="1933c-138">System.Nullable\`1[[System.DateTime, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="1933c-139">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="1933c-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="1933c-140">출력</span><span class="sxs-lookup"><span data-stu-id="1933c-140">OUTPUTS</span></span>

### <span data-ttu-id="1933c-141">PSEventData를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="1933c-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="1933c-142">상속자</span><span class="sxs-lookup"><span data-stu-id="1933c-142">NOTES</span></span>

## <span data-ttu-id="1933c-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1933c-143">RELATED LINKS</span></span>

[<span data-ttu-id="1933c-144">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1933c-144">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1933c-145">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1933c-145">Get-AzureRmAutoscaleSetting</span></span>](./Get-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="1933c-146">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="1933c-146">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


