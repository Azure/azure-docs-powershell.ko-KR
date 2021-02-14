---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRule.md
ms.openlocfilehash: cdde294c3af4684146d265e2024f6948660312bb
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203441"
---
# <span data-ttu-id="4abf8-101">New-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="4abf8-101">New-AzDataCollectionRule</span></span>

## <span data-ttu-id="4abf8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4abf8-102">SYNOPSIS</span></span>
<span data-ttu-id="4abf8-103">데이터 수집 규칙을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-103">Create a data collection rule.</span></span>

## <span data-ttu-id="4abf8-104">구문</span><span class="sxs-lookup"><span data-stu-id="4abf8-104">SYNTAX</span></span>

### <span data-ttu-id="4abf8-105">ByFile(기본값)</span><span class="sxs-lookup"><span data-stu-id="4abf8-105">ByFile (Default)</span></span>
```
New-AzDataCollectionRule
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

## <span data-ttu-id="4abf8-106">설명</span><span class="sxs-lookup"><span data-stu-id="4abf8-106">DESCRIPTION</span></span>
<span data-ttu-id="4abf8-107">**New-AzDataCollectionRule** cmdlet은 데이터 컬렉션 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-107">The **New-AzDataCollectionRule** cmdlet creates a data collection rule.</span></span>

<span data-ttu-id="4abf8-108">DCR(데이터 수집 규칙)은 Azure Monitor로 들어오는 데이터를 정의하고 해당 데이터를 보내거나 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-108">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="4abf8-109">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="4abf8-109">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

<span data-ttu-id="4abf8-110">-RuleFile 매개 변수를 사용 설정하기 위해 dataSources, destinations, dataFlows의 세 가지 속성을 포함하는 json 파일을 생성합니다(예제 #1).</span><span class="sxs-lookup"><span data-stu-id="4abf8-110">To use the -RuleFile parameter, construct a json file containing three properties: dataSources, destinations, dataFlows (see Example #1)</span></span>

<span data-ttu-id="4abf8-111">여기에서는 해당 세부 [정보를 찾을 수 있습니다.](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create)</span><span class="sxs-lookup"><span data-stu-id="4abf8-111">You may find here the [schema detail](https://docs.microsoft.com/en-us/rest/api/monitor/datacollectionrules/create).</span></span>

<span data-ttu-id="4abf8-112">cmdlet을 통해 직렬화된 DCR의 출력도 ConvertTo-Json 있습니다(예제 #2 참조).</span><span class="sxs-lookup"><span data-stu-id="4abf8-112">The output of a DCR serialized with the cmdlet ConvertTo-Json is also supported (see Example #2).</span></span>

## <span data-ttu-id="4abf8-113">예제</span><span class="sxs-lookup"><span data-stu-id="4abf8-113">EXAMPLES</span></span>

### <span data-ttu-id="4abf8-114">예제 1: 데이터 수집 규칙 만들기, Rest API에서 JSON</span><span class="sxs-lookup"><span data-stu-id="4abf8-114">Example 1: Create data collection rule, JSON from Rest API</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx1' -RuleFile 'C:\samples\dcrEx1.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx1
Name              : newDcrEx1
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx1.json
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

<span data-ttu-id="4abf8-115">이 명령은 현재 구독에 대한 데이터 수집 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-115">This command creates a data collection rules for the current subscription.</span></span>

### <span data-ttu-id="4abf8-116">예제 2: PSDataCollectionRuleResource에서 JSON 데이터 수집 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="4abf8-116">Example 2: Create data collection rule, JSON from PSDataCollectionRuleResource</span></span>
```powershell
PS C:\>New-AzDataCollectionRule -Location 'East US 2 EUAP' -ResourceGroupName 'testdcr'
                                -RuleName 'newDcrEx2' -RuleFile 'C:\samples\dcrEx2.json'
                                -Description 'Dcr description'
                                -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : Dcr description
DataSources       : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDataSources
Destinations      : Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleDestinations
DataFlows         : {Microsoft.Azure.Commands.Insights.OutputClasses.PSDataFlow}
ProvisioningState : Succeeded
Etag              : "{etag}"
Id                : /subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcrEx2
Name              : newDcrEx2
Type              : Microsoft.Insights/dataCollectionRules
Location          : East US 2 EUAP
Tags              : {[tag2, value2], [tag1, value1]}

# Note: Content of C:\samples\dcrEx2.json
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

<span data-ttu-id="4abf8-117">이 명령은 현재 구독에 대한 데이터 수집 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-117">This command creates a data collection rules for the current subscription.</span></span>

## <span data-ttu-id="4abf8-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4abf8-118">PARAMETERS</span></span>

### <span data-ttu-id="4abf8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4abf8-119">-DefaultProfile</span></span>
<span data-ttu-id="4abf8-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4abf8-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="4abf8-121">-Location</span><span class="sxs-lookup"><span data-stu-id="4abf8-121">-Location</span></span>
<span data-ttu-id="4abf8-122">리소스 위치</span><span class="sxs-lookup"><span data-stu-id="4abf8-122">The resource location</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4abf8-123">-ResourceGroupName</span></span>
<span data-ttu-id="4abf8-124">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="4abf8-124">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-125">-RuleName</span><span class="sxs-lookup"><span data-stu-id="4abf8-125">-RuleName</span></span>
<span data-ttu-id="4abf8-126">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="4abf8-126">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-127">-RuleFile</span><span class="sxs-lookup"><span data-stu-id="4abf8-127">-RuleFile</span></span>
<span data-ttu-id="4abf8-128">JSON 파일 경로</span><span class="sxs-lookup"><span data-stu-id="4abf8-128">The JSON file path</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-129">-Description</span><span class="sxs-lookup"><span data-stu-id="4abf8-129">-Description</span></span>
<span data-ttu-id="4abf8-130">리소스 설명</span><span class="sxs-lookup"><span data-stu-id="4abf8-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="4abf8-131">-Tag</span></span>
<span data-ttu-id="4abf8-132">리소스 태그</span><span class="sxs-lookup"><span data-stu-id="4abf8-132">The resource tags</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: ByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4abf8-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="4abf8-133">-Confirm</span></span>
<span data-ttu-id="4abf8-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4abf8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4abf8-135">-WhatIf</span></span>
<span data-ttu-id="4abf8-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="4abf8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4abf8-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4abf8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4abf8-138">CommonParameters</span></span>
<span data-ttu-id="4abf8-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4abf8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4abf8-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4abf8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4abf8-141">입력</span><span class="sxs-lookup"><span data-stu-id="4abf8-141">INPUTS</span></span>

### <span data-ttu-id="4abf8-142">System.String</span><span class="sxs-lookup"><span data-stu-id="4abf8-142">System.String</span></span>

## <span data-ttu-id="4abf8-143">출력</span><span class="sxs-lookup"><span data-stu-id="4abf8-143">OUTPUTS</span></span>

### <span data-ttu-id="4abf8-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="4abf8-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="4abf8-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4abf8-145">NOTES</span></span>

## <span data-ttu-id="4abf8-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4abf8-146">RELATED LINKS</span></span>

<span data-ttu-id="4abf8-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="4abf8-147">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>