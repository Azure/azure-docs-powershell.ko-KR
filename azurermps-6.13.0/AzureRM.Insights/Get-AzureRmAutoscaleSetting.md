---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 989CE245-FD1D-4E1D-90A2-2D7DA3975D0B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermautoscalesetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAutoscaleSetting.md
ms.openlocfilehash: 6bf59522b09d9a8a5c301860ab175eef8f7537b8
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534335"
---
# <span data-ttu-id="78944-101">Get-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78944-101">Get-AzureRmAutoscaleSetting</span></span>

## <span data-ttu-id="78944-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78944-102">SYNOPSIS</span></span>
<span data-ttu-id="78944-103">자동 크기 조정 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78944-103">Gets Autoscale settings.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78944-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78944-104">SYNTAX</span></span>

```
Get-AzureRmAutoscaleSetting -ResourceGroupName <String> [-Name <String>] [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="78944-105">설명은</span><span class="sxs-lookup"><span data-stu-id="78944-105">DESCRIPTION</span></span>
<span data-ttu-id="78944-106">**AzureRmAutoscaleSetting** cmdlet은 리소스 그룹과 연결 된 자동 크기 조정 설정이 나 지정 된 크기 자동 조정 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78944-106">The **Get-AzureRmAutoscaleSetting** cmdlet gets all Autoscale settings associated with a resource group or a specified Autoscale setting.</span></span>

## <span data-ttu-id="78944-107">예제의</span><span class="sxs-lookup"><span data-stu-id="78944-107">EXAMPLES</span></span>

### <span data-ttu-id="78944-108">예제 1: 크기 자동 조정 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="78944-108">Example 1: Get Autoscale settings</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroup "Default-Web-EastUS" -DetailedOutput
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

<span data-ttu-id="78944-109">이 명령은 리소스 그룹 Default-웹에 할당 된 자동 크기 조정 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="78944-109">This command gets the Autoscale settings assigned to the resource group Default-Web-EastUS.</span></span>

### <span data-ttu-id="78944-110">예제 2: 이름 자동 크기 조정 설정 가져오기</span><span class="sxs-lookup"><span data-stu-id="78944-110">Example 2: Get an Autoscale setting by name</span></span>
```
PS C:\>Get-AzureRmAutoscaleSetting -ResourceGroupName "Default-Web-EastUS" -Name "DefaultServerFarm-Default-Web-EastUS" -DetailedOutput
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

<span data-ttu-id="78944-111">이 명령은 DefaultServerFarm 이라는 자동 크기 조정 설정을 가져옵니다-기본값-웹용-e \ t.</span><span class="sxs-lookup"><span data-stu-id="78944-111">This command gets the Autoscale setting named DefaultServerFarm-Default-Web-EastUS.</span></span>

## <span data-ttu-id="78944-112">변수</span><span class="sxs-lookup"><span data-stu-id="78944-112">PARAMETERS</span></span>

### <span data-ttu-id="78944-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78944-113">-DefaultProfile</span></span>
<span data-ttu-id="78944-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="78944-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="78944-115">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="78944-115">-DetailedOutput</span></span>
<span data-ttu-id="78944-116">이 작업에서 출력에 전체 세부 정보를 표시 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="78944-116">Indicates that this operation displays full details in the output.</span></span>

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

### <span data-ttu-id="78944-117">-이름</span><span class="sxs-lookup"><span data-stu-id="78944-117">-Name</span></span>
<span data-ttu-id="78944-118">가져올 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78944-118">Specifies the name of the setting to get.</span></span>

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

### <span data-ttu-id="78944-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78944-119">-ResourceGroupName</span></span>
<span data-ttu-id="78944-120">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="78944-120">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="78944-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78944-121">CommonParameters</span></span>
<span data-ttu-id="78944-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78944-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78944-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78944-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78944-124">입력</span><span class="sxs-lookup"><span data-stu-id="78944-124">INPUTS</span></span>

### <span data-ttu-id="78944-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78944-125">System.String</span></span>

### <span data-ttu-id="78944-126">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="78944-126">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="78944-127">출력</span><span class="sxs-lookup"><span data-stu-id="78944-127">OUTPUTS</span></span>

### <span data-ttu-id="78944-128">PSAutoscaleSetting를 통해 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="78944-128">Microsoft.Azure.Commands.Insights.OutputClasses.PSAutoscaleSetting</span></span>

## <span data-ttu-id="78944-129">상속자</span><span class="sxs-lookup"><span data-stu-id="78944-129">NOTES</span></span>

## <span data-ttu-id="78944-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78944-130">RELATED LINKS</span></span>

[<span data-ttu-id="78944-131">추가-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78944-131">Add-AzureRmAutoscaleSetting</span></span>](./Add-AzureRmAutoscaleSetting.md)

[<span data-ttu-id="78944-132">제거-AzureRmAutoscaleSetting</span><span class="sxs-lookup"><span data-stu-id="78944-132">Remove-AzureRmAutoscaleSetting</span></span>](./Remove-AzureRmAutoscaleSetting.md)


