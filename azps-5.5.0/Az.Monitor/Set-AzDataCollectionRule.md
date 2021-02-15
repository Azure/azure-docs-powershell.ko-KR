---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/set-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Set-AzDataCollectionRule.md
ms.openlocfilehash: 864b3c8abe2411316edf155c49757c1082a863a6
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190089"
---
# <span data-ttu-id="fb6d6-101">Set-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="fb6d6-101">Set-AzDataCollectionRule</span></span>

## <span data-ttu-id="fb6d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb6d6-102">SYNOPSIS</span></span>
<span data-ttu-id="fb6d6-103">데이터 수집 규칙을 업데이트(전체 대체)합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-103">Updates (full replacement) a data collection rule.</span></span>

## <span data-ttu-id="fb6d6-104">구문</span><span class="sxs-lookup"><span data-stu-id="fb6d6-104">SYNTAX</span></span>

### <span data-ttu-id="fb6d6-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fb6d6-105">ByName (Default)</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -ResourceGroupName <string>
   -RuleName <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="fb6d6-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="fb6d6-106">ByResourceId</span></span>
```
Set-AzDataCollectionRule 
   -Location <string>
   -RuleId <string>
   -RuleFile <string>
   [-Description <string>]
   [-Tag <hashtable>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="fb6d6-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="fb6d6-107">ByInputObject</span></span>
```
Set-AzDataCollectionRule 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="fb6d6-108">설명</span><span class="sxs-lookup"><span data-stu-id="fb6d6-108">DESCRIPTION</span></span>
<span data-ttu-id="fb6d6-109">**Set-AzDataCollectionRule** cmdlet은 기존 데이터 수집 규칙을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-109">The **Set-AzDataCollectionRule** cmdlet replaces an existing data collection rule.</span></span>

<span data-ttu-id="fb6d6-110">DCR(데이터 수집 규칙)은 Azure Monitor로 들어오는 데이터를 정의하고 해당 데이터를 보내거나 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="fb6d6-111">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="fb6d6-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="fb6d6-112">-RuleFile 매개 변수를 사용하세요. dataSources, destinations, dataFlows의 세 가지 속성을 포함하는 json 파일을 생성합니다(예제 #1).</span><span class="sxs-lookup"><span data-stu-id="fb6d6-112">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1).</span></span>

<span data-ttu-id="fb6d6-113">여기에서는 해당 세부 [정보를 찾을 수 있습니다.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="fb6d6-113">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="fb6d6-114">cmdlet을 통해 직렬화된 DCR의 출력도 ConvertTo-Json(예제 #2).</span><span class="sxs-lookup"><span data-stu-id="fb6d6-114">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (Example #2).</span></span>

## <span data-ttu-id="fb6d6-115">예제</span><span class="sxs-lookup"><span data-stu-id="fb6d6-115">EXAMPLES</span></span>

### <span data-ttu-id="fb6d6-116">예제 1: 데이터 수집 규칙 업데이트, Rest API에서 JSON</span><span class="sxs-lookup"><span data-stu-id="fb6d6-116">Example 1: Update data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -ResourceGroupName 'testdcr' 
                                -RuleName 'newDcr' 
                                -RuleFile 'C:\samples\dcr1.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr1.json
{
  "properties": {
    "dataSources": {
      "performanceCounters": [
        {
          "streams": [
            "Microsoft-InsightsMetrics"
          ],
          "scheduledTransferPeriod": "PT1M",
          "samplingFrequencyInSeconds": 10,
          "counterSpecifiers": [
            "\\Processor Information(_Total)\\% Processor Time"
          ],
          "name": "perfCounter01"
        }
      ]
    },
    "destinations": {
      "azureMonitorMetrics": {
        "name": "azureMonitorMetrics-default"
      }
    },
    "dataFlows": [
      {
        "streams": [
          "Microsoft-InsightsMetrics"
        ],
        "destinations": [
          "azureMonitorMetrics-default"
        ]
      }
    ]
  }
}
```

<span data-ttu-id="fb6d6-117">이 명령은 현재 구독에 대한 기존 데이터 수집 규칙을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-117">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="fb6d6-118">예제 2: 데이터 수집 규칙 업데이트, PSDataCollectionRuleResource에서 JSON</span><span class="sxs-lookup"><span data-stu-id="fb6d6-118">Example 2: Update data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>Set-AzDataCollectionRule -Location 'East US 2 EUAP'
                                -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr' 
                                -RuleFile 'C:\samples\dcr2.json'
                                -Description 'Updated Description'

Description       : Updated Description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcr2.json
{
  "DataSources": {
    "PerformanceCounters": [
      {
        "Streams": [
          "Microsoft-InsightsMetrics"
        ],
        "ScheduledTransferPeriod": "PT1M",
        "SamplingFrequencyInSeconds": 10,
        "CounterSpecifiers": [
          "\\Processor Information(_Total)\\% Processor Time"
        ],
        "Name": "perfCounter01"
      }
    ]
  },
  "Destinations": {
    "AzureMonitorMetrics": {
      "Name": "azureMonitorMetrics-default"
    }
  },
  "DataFlows": [
    {
      "Streams": [
        "Microsoft-InsightsMetrics"
      ],
      "Destinations": [
        "azureMonitorMetrics-default"
      ]
    }
  ]
}
```

<span data-ttu-id="fb6d6-119">이 명령은 현재 구독에 대한 기존 데이터 수집 규칙을 대체합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-119">This command replaces an existing data collection rules for the current subscription.</span></span>

### <span data-ttu-id="fb6d6-120">예제 3: 개체에서 데이터 수집 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="fb6d6-120">Example 3: Update data collection rule from object</span></span>
```powershell
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr.Description = 'This is a test'
PS C:\>$dcr | Set-AzDataCollectionRule

Description       : This is a test
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : {provState}
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr
Name              : newDcr
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}
```

## <span data-ttu-id="fb6d6-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fb6d6-121">PARAMETERS</span></span>

### <span data-ttu-id="fb6d6-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb6d6-122">-DefaultProfile</span></span>
<span data-ttu-id="fb6d6-123">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb6d6-123">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb6d6-124">-Location</span><span class="sxs-lookup"><span data-stu-id="fb6d6-124">-Location</span></span>
<span data-ttu-id="fb6d6-125">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="fb6d6-125">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-126">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="fb6d6-126">-RuleFile</span></span>
<span data-ttu-id="fb6d6-127">JSON 파일 경로</span><span class="sxs-lookup"><span data-stu-id="fb6d6-127">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fb6d6-128">-ResourceGroupName</span></span>
<span data-ttu-id="fb6d6-129">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="fb6d6-129">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-130">-RuleName</span><span class="sxs-lookup"><span data-stu-id="fb6d6-130">-RuleName</span></span>
<span data-ttu-id="fb6d6-131">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="fb6d6-131">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-132">-RuleId</span><span class="sxs-lookup"><span data-stu-id="fb6d6-132">-RuleId</span></span>
<span data-ttu-id="fb6d6-133">리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fb6d6-133">The resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-134">-Description</span><span class="sxs-lookup"><span data-stu-id="fb6d6-134">-Description</span></span>
<span data-ttu-id="fb6d6-135">리소스 설명</span><span class="sxs-lookup"><span data-stu-id="fb6d6-135">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-136">-Tag</span><span class="sxs-lookup"><span data-stu-id="fb6d6-136">-Tag</span></span>
<span data-ttu-id="fb6d6-137">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="fb6d6-137">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-138">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fb6d6-138">-InputObject</span></span>
<span data-ttu-id="fb6d6-139">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="fb6d6-139">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-140">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fb6d6-140">-Confirm</span></span>
<span data-ttu-id="fb6d6-141">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-141">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-142">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fb6d6-142">-WhatIf</span></span>
<span data-ttu-id="fb6d6-143">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fb6d6-143">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fb6d6-144">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-144">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb6d6-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb6d6-145">CommonParameters</span></span>
<span data-ttu-id="fb6d6-146">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb6d6-147">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fb6d6-147">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb6d6-148">입력</span><span class="sxs-lookup"><span data-stu-id="fb6d6-148">INPUTS</span></span>

### <span data-ttu-id="fb6d6-149">System.String</span><span class="sxs-lookup"><span data-stu-id="fb6d6-149">System.String</span></span>

## <span data-ttu-id="fb6d6-150">출력</span><span class="sxs-lookup"><span data-stu-id="fb6d6-150">OUTPUTS</span></span>

### <span data-ttu-id="fb6d6-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="fb6d6-151">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="fb6d6-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fb6d6-152">NOTES</span></span>

## <span data-ttu-id="fb6d6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb6d6-153">RELATED LINKS</span></span>

<span data-ttu-id="fb6d6-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="fb6d6-154">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>