---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRule.md
ms.openlocfilehash: 8826dfdf8fe0152035319c576210088bcd5521e3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180193"
---
# <span data-ttu-id="ce032-101">Get-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="ce032-101">Get-AzDataCollectionRule</span></span>

## <span data-ttu-id="ce032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ce032-102">SYNOPSIS</span></span>
<span data-ttu-id="ce032-103">데이터 수집 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-103">Gets data collection rule(s).</span></span>

## <span data-ttu-id="ce032-104">구문</span><span class="sxs-lookup"><span data-stu-id="ce032-104">SYNTAX</span></span>

### <span data-ttu-id="ce032-105">BySubscription(기본값)</span><span class="sxs-lookup"><span data-stu-id="ce032-105">BySubscription (Default)</span></span>
```
Get-AzDataCollectionRule
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ce032-106">ByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="ce032-106">ByResourceGroup</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ce032-107">ByName</span><span class="sxs-lookup"><span data-stu-id="ce032-107">ByName</span></span>
```
Get-AzDataCollectionRule
   -ResourceGroupName <string>
   -RuleName <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="ce032-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="ce032-108">ByResourceId</span></span>
```
Get-AzDataCollectionRule
   -RuleId <string>
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="ce032-109">설명</span><span class="sxs-lookup"><span data-stu-id="ce032-109">DESCRIPTION</span></span>
<span data-ttu-id="ce032-110">**Get-AzDataCollectionRule** cmdlet은 하나 이상의 데이터 수집 규칙을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-110">The **Get-AzDataCollectionRule** cmdlet gets one or more data collection rules.</span></span>

<span data-ttu-id="ce032-111">DCR(데이터 수집 규칙)은 Azure Monitor로 들어오는 데이터를 정의하고 해당 데이터를 보내거나 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-111">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="ce032-112">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="ce032-112">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="ce032-113">예제</span><span class="sxs-lookup"><span data-stu-id="ce032-113">EXAMPLES</span></span>

### <span data-ttu-id="ce032-114">예제 1: 구독 ID로 데이터 수집 규칙 확인</span><span class="sxs-lookup"><span data-stu-id="ce032-114">Example 1: Get data collection rules by subscription ID</span></span>
```
PS C:\>Get-AzDataCollectionRule

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="ce032-115">이 명령은 현재 구독에 대한 모든 데이터 수집 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-115">This command lists all the data collection rules for the current subscription.</span></span>

### <span data-ttu-id="ce032-116">예제 2: 주어진 리소스 그룹에 대한 데이터 수집 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="ce032-116">Example 2: Get data collection rules for the given resource group</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="ce032-117">이 명령은 주어진 리소스 그룹에 대한 데이터 수집 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-117">This command lists data collection rules for the given resource group.</span></span>

### <span data-ttu-id="ce032-118">예제 3: 데이터 수집 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="ce032-118">Example 3: Get a data collection rule</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroup "testgroup" -RuleName "testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="ce032-119">이 명령은 데이터 수집 규칙 하나(단일 요소가 있는 목록)를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-119">This command lists one (a list with a single element) data collection rule.</span></span>

### <span data-ttu-id="ce032-120">예제 4: 규칙 ID로 데이터 수집 규칙 얻기</span><span class="sxs-lookup"><span data-stu-id="ce032-120">Example 4: Get a data collection rule by Rule ID</span></span>
```
PS C:\>Get-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr"

Description       : DCR description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testgroup/providers/Microsoft.Insights/dataCollectionRules/testDcr
Name              : testDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

<span data-ttu-id="ce032-121">이 명령은 데이터 수집 규칙 하나(단일 요소가 있는 목록)를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-121">This command lists one (a list with a single element) data collection rule.</span></span>

## <span data-ttu-id="ce032-122">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ce032-122">PARAMETERS</span></span>

### <span data-ttu-id="ce032-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ce032-123">-DefaultProfile</span></span>
<span data-ttu-id="ce032-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ce032-124">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ce032-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ce032-125">-ResourceGroupName</span></span>
<span data-ttu-id="ce032-126">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="ce032-126">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce032-127">-RuleName</span><span class="sxs-lookup"><span data-stu-id="ce032-127">-RuleName</span></span>
<span data-ttu-id="ce032-128">리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-128">The name of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce032-129">-RuleId</span><span class="sxs-lookup"><span data-stu-id="ce032-129">-RuleId</span></span>
<span data-ttu-id="ce032-130">리소스의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-130">The ID of the resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ce032-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ce032-131">CommonParameters</span></span>
<span data-ttu-id="ce032-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ce032-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ce032-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ce032-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ce032-134">입력</span><span class="sxs-lookup"><span data-stu-id="ce032-134">INPUTS</span></span>

### <span data-ttu-id="ce032-135">System.String</span><span class="sxs-lookup"><span data-stu-id="ce032-135">System.String</span></span>

## <span data-ttu-id="ce032-136">출력</span><span class="sxs-lookup"><span data-stu-id="ce032-136">OUTPUTS</span></span>

### <span data-ttu-id="ce032-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="ce032-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="ce032-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ce032-138">NOTES</span></span>

## <span data-ttu-id="ce032-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ce032-139">RELATED LINKS</span></span>

<span data-ttu-id="ce032-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="ce032-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>
