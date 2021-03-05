---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/powershell/module/az.monitor/get-azautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzAutoscaleSetting.md
ms.openlocfilehash: 5e493bed4dafb7c0b91465d9a9dff684cfcffcb9
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101980096"
---
# <span data-ttu-id="fdcf1-101">Get-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fdcf1-101">Get-AzAutoscaleSetting</span></span>

## <span data-ttu-id="fdcf1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fdcf1-102">SYNOPSIS</span></span>
<span data-ttu-id="fdcf1-103">자동 조정 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-103">Gets Autoscale settings.</span></span>

## <span data-ttu-id="fdcf1-104">구문</span><span class="sxs-lookup"><span data-stu-id="fdcf1-104">SYNTAX</span></span>

```
Get-AzAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fdcf1-105">설명</span><span class="sxs-lookup"><span data-stu-id="fdcf1-105">DESCRIPTION</span></span>
<span data-ttu-id="fdcf1-106">**Get-AzAutoscaleSetting** cmdlet은 리소스 그룹 또는 지정된 자동 크기 조정 설정과 연결된 모든 자동 크기 조정 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-106">The **Get-AzAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="fdcf1-107">예제</span><span class="sxs-lookup"><span data-stu-id="fdcf1-107">EXAMPLES</span></span>

### <span data-ttu-id="fdcf1-108">예제 1: 자동 조정 설정 사용</span><span class="sxs-lookup"><span data-stu-id="fdcf1-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction        : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction  : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1

MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
                                                TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
                                                Direction  : Increase
Type       : ChangeCount
Value      : 1
             TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="fdcf1-109">이 명령은 리소스 그룹에 할당된 자동 조정 설정을 Default-Web-EastUS로 이동합니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="fdcf1-110">예제 2: 이름에 따라 자동 조정 설정 사용</span><span class="sxs-lookup"><span data-stu-id="fdcf1-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
resourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/providers/microsoft. 
             insights/autoscalesettings/DefaultServerFarm-Default-Web-EastUS
Location   : East US
Name       : DefaultServerFarm-Default-Web-EastUS
Properties : 
Enabled    : True
Profiles   : 
Capacity   : 
Default    : 1
Minimum    : 3
Maximum    : 1
FixedDate     : 
Name          : No scheduled times
Recurrence    : 
Rules         : 
MetricTrigger : 
MetricName         : CpuPercentage
MetricResourceId   : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 14
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 00:05:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : CpuPercentage
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 4
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:45:00
ScaleAction    : 
Cooldown   : 02:00:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : LessThanOrEqual
Statistic          : Average
Threshold          : 50
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:10:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Decrease
Type       : ChangeCount
Value      : 1
MetricTrigger  : 
MetricName         : BytesReceived
MetricResourceId  : /subscriptions/a93fb07c-6c93-40be-bf3b-4f0deba10f4
             b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm
Operator           : GreaterThanOrEqual
Statistic          : Average
Threshold          : 100
TimeAggregation    : Average
TimeGrain          : 00:01:00
TimeWindow         : 00:05:00
ScaleAction    : 
Cooldown   : 00:10:00
Direction  : Increase
Type       : ChangeCount
Value      : 1
TargetResourceId : /subscriptions/b93fb07a-6f93-30be-bf3e-4f0deca15f4f/resourceGroups/Default-Web-EastUS/
             providers/microsoft.web/serverFarms/DefaultServerFarm
Tags       : {[$type, Microsoft.WindowsAzure.Management.Common.Storage.CasePreservedDictionary, 
             Microsoft.WindowsAzure.Management.Common.Storage], [hidden-link:/subscriptions/a93fb07c-6c93-40be-bf3b-4f0
             deba10f4b/resourceGroups/Default-Web-EastUS/providers/microsoft.web/serverFarms/DefaultServerFarm, 
             Resource]}
```

<span data-ttu-id="fdcf1-111">이 명령은 DefaultServerFarm-Default-Web-EastUS라는 자동 조정 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="fdcf1-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="fdcf1-112">PARAMETERS</span></span>

### <span data-ttu-id="fdcf1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fdcf1-113">-DefaultProfile</span></span>
<span data-ttu-id="fdcf1-114">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fdcf1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fdcf1-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="fdcf1-115">-DetailedOutput</span></span>
<span data-ttu-id="fdcf1-116">이 작업은 출력에 전체 세부 정보를 표시하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-116">Indicates that this operation displays full details in the output.</span></span>

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

### <span data-ttu-id="fdcf1-117">-Name</span><span class="sxs-lookup"><span data-stu-id="fdcf1-117">-Name</span></span>
<span data-ttu-id="fdcf1-118">얻을 설정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-118">Specifies the name of the setting to get.</span></span>

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

### <span data-ttu-id="fdcf1-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fdcf1-119">-ResourceGroupName</span></span>
<span data-ttu-id="fdcf1-120">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-120">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fdcf1-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fdcf1-121">CommonParameters</span></span>
<span data-ttu-id="fdcf1-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fdcf1-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fdcf1-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="fdcf1-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fdcf1-124">입력</span><span class="sxs-lookup"><span data-stu-id="fdcf1-124">INPUTS</span></span>

### <span data-ttu-id="fdcf1-125">System.String</span><span class="sxs-lookup"><span data-stu-id="fdcf1-125">System.String</span></span>

### <span data-ttu-id="fdcf1-126">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="fdcf1-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="fdcf1-127">출력</span><span class="sxs-lookup"><span data-stu-id="fdcf1-127">OUTPUTS</span></span>

### <span data-ttu-id="fdcf1-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fdcf1-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="fdcf1-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fdcf1-129">NOTES</span></span>

## <span data-ttu-id="fdcf1-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fdcf1-130">RELATED LINKS</span></span>

[<span data-ttu-id="fdcf1-131">Add-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fdcf1-131">Add-AzAutoscaleSetting</span></span>](./Add-AzAutoscaleSetting.md)

[<span data-ttu-id="fdcf1-132">Remove-AzAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="fdcf1-132">Remove-AzAutoscaleSetting</span></span>](./Remove-AzAutoscaleSetting.md)


