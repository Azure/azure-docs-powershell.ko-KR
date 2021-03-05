---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A70F4C03-E842-45D5-9323-DC5B14B569F1
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azautoscalehistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleHistory.md
ms.openlocfilehash: c88cd3bbf132ccb7b8913b15dcc66f58ea2d2db3
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980107"
---
# <span data-ttu-id="13afc-101">Get-AzAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="13afc-101">Get-AzAutoscaleHistory</span></span>

## <span data-ttu-id="13afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="13afc-102">SYNOPSIS</span></span>
<span data-ttu-id="13afc-103">자동 조정 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-103">Gets the Autoscale history.</span></span>

## <span data-ttu-id="13afc-104">구문</span><span class="sxs-lookup"><span data-stu-id="13afc-104">SYNTAX</span></span>

```
Get-AzAutoscaleHistory [-ResourceId <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-Status <String>]
 [-Caller <String>] [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="13afc-105">설명</span><span class="sxs-lookup"><span data-stu-id="13afc-105">DESCRIPTION</span></span>
<span data-ttu-id="13afc-106">**Get-AzAutoscaleHistory** cmdlet은 자동 크기 조정 설정과 관련된 이벤트의 기록을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-106">The **Get-AzAutoscaleHistory** cmdlet gets the history of events related to an Autoscale setting.</span></span>

## <span data-ttu-id="13afc-107">예제</span><span class="sxs-lookup"><span data-stu-id="13afc-107">EXAMPLES</span></span>

### <span data-ttu-id="13afc-108">예제 1: 구독과 연결된 모든 이벤트 얻기</span><span class="sxs-lookup"><span data-stu-id="13afc-108">Example 1: Get all events associated with a subscription</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -DetailedOutput
```

<span data-ttu-id="13afc-109">이 명령은 현재 구독과 연결된 모든 자동 조정 관련 이벤트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-109">This command gets all of the Autoscale-related events associated with the current subscription.</span></span>

### <span data-ttu-id="13afc-110">예제 2: 특정 리소스에 대한 GetAutoscaleHistory</span><span class="sxs-lookup"><span data-stu-id="13afc-110">Example 2: GetAutoscaleHistory for a particular resource</span></span>
```
PS C:\>Get-AzAutoscaleHistory -StartTime 2015-02-09T18:35:00 -EndTime 2015-02-09T18:40:00 -ResourceId "/subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft.insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
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

<span data-ttu-id="13afc-111">이 명령은 리소스의 ID(기본적으로 ResourceUri)에서 식별된 특정 리소스와 연결된 모든 자동 조정 관련 이벤트를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-111">This command gets all Autoscale-related events associated with a particular resource identified by the resource's ID (essentially, the ResourceUri).</span></span>

## <span data-ttu-id="13afc-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="13afc-112">PARAMETERS</span></span>

### <span data-ttu-id="13afc-113">-Caller</span><span class="sxs-lookup"><span data-stu-id="13afc-113">-Caller</span></span>
<span data-ttu-id="13afc-114">호출자 지정.</span><span class="sxs-lookup"><span data-stu-id="13afc-114">Specifies a caller.</span></span>

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

### <span data-ttu-id="13afc-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="13afc-115">-DefaultProfile</span></span>
<span data-ttu-id="13afc-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="13afc-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="13afc-117">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="13afc-117">-DetailedOutput</span></span>
<span data-ttu-id="13afc-118">이 작업에 자세한 출력이 포함되어 있는 경우를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-118">Indicates that this operation included detailed output.</span></span>
<span data-ttu-id="13afc-119">이 매개 변수를 지정하지 않으면 출력이 요약됩니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-119">If you do not specify this parameter, the output is summarized.</span></span>

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

### <span data-ttu-id="13afc-120">-EndTime</span><span class="sxs-lookup"><span data-stu-id="13afc-120">-EndTime</span></span>
<span data-ttu-id="13afc-121">로컬 시간으로 쿼리의 종료 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-121">Specifies the end time of the query in local time.</span></span>
<span data-ttu-id="13afc-122">기본값은 현재 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-122">The default is the current time.</span></span>

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

### <span data-ttu-id="13afc-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="13afc-123">-ResourceId</span></span>
<span data-ttu-id="13afc-124">자동 조정 설정이 연결된 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-124">Specifies the resource ID to which the autoscale setting is associated.</span></span>

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

### <span data-ttu-id="13afc-125">-StartTime</span><span class="sxs-lookup"><span data-stu-id="13afc-125">-StartTime</span></span>
<span data-ttu-id="13afc-126">로컬 시간으로 쿼리의 시작 시간을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-126">Specifies the start time of the query in local time.</span></span>
<span data-ttu-id="13afc-127">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-127">This parameter is optional.</span></span>
<span data-ttu-id="13afc-128">기본값은 현재 로컬 시간에서 1시간을 씩 입니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-128">The default is the current local time minus one hour.</span></span>

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

### <span data-ttu-id="13afc-129">-Status</span><span class="sxs-lookup"><span data-stu-id="13afc-129">-Status</span></span>
<span data-ttu-id="13afc-130">상태로 필터를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-130">Specifies a filter by status.</span></span>
<span data-ttu-id="13afc-131">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-131">This parameter is optional.</span></span>
<span data-ttu-id="13afc-132">오류는 빈 문자열입니다(예: 필터 없음)</span><span class="sxs-lookup"><span data-stu-id="13afc-132">The fault is an empty string (i.e. no filter)</span></span>

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

### <span data-ttu-id="13afc-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="13afc-133">CommonParameters</span></span>
<span data-ttu-id="13afc-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="13afc-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="13afc-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="13afc-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="13afc-136">입력</span><span class="sxs-lookup"><span data-stu-id="13afc-136">INPUTS</span></span>

### <span data-ttu-id="13afc-137">System.String</span><span class="sxs-lookup"><span data-stu-id="13afc-137">System.String</span></span>

### <span data-ttu-id="13afc-138">System.Nullable'1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="13afc-138">System.Nullable\`1[[System.DateTime, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="13afc-139">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="13afc-139">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="13afc-140">출력</span><span class="sxs-lookup"><span data-stu-id="13afc-140">OUTPUTS</span></span>

### <span data-ttu-id="13afc-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span><span class="sxs-lookup"><span data-stu-id="13afc-141">Microsoft.Azure.Commands.Insights.OutputClasses.PSEventData</span></span>

## <span data-ttu-id="13afc-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="13afc-142">NOTES</span></span>

## <span data-ttu-id="13afc-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="13afc-143">RELATED LINKS</span></span>

[<span data-ttu-id="13afc-144">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="13afc-144">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="13afc-145">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="13afc-145">Get-AzAutoscaleSetting</span></span>](./Get-AzAutoscaleSetting.md)

[<span data-ttu-id="13afc-146">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="13afc-146">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


