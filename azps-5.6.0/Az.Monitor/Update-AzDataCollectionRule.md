---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/update-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Update-AzDataCollectionRule.md
ms.openlocfilehash: 2e4aba9a2572b5612070d860dcbe20cda2366a02
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994126"
---
# <span data-ttu-id="bd110-101">Update-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="bd110-101">Update-AzDataCollectionRule</span></span>

## <span data-ttu-id="bd110-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd110-102">SYNOPSIS</span></span>
<span data-ttu-id="bd110-103">데이터 수집 규칙 태그 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-103">Updates a data collection rule tags property.</span></span>

## <span data-ttu-id="bd110-104">구문</span><span class="sxs-lookup"><span data-stu-id="bd110-104">SYNTAX</span></span>

### <span data-ttu-id="bd110-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="bd110-105">ByName (Default)</span></span>
```
Update-AzDataCollectionRule 
      -ResourceGroupName <string> 
      -RuleName <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="bd110-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="bd110-106">ByResourceId</span></span>
```
Update-AzDataCollectionRule 
      -RuleId <string> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>] 
      [-WhatIf] 
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="bd110-107">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="bd110-107">ByInputObject</span></span>
```
Update-AzDataCollectionRule 
      -InputObject <PSDataCollectionRuleResource> 
      [-Tag <hashtable>] 
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="bd110-108">설명</span><span class="sxs-lookup"><span data-stu-id="bd110-108">DESCRIPTION</span></span>
<span data-ttu-id="bd110-109">**Update-AzDataCollectionRule** cmdlet은 데이터 수집 규칙 Tags 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-109">The **Update-AzDataCollectionRule** cmdlet updates a data collection rule Tags property.</span></span>

<span data-ttu-id="bd110-110">DCR(데이터 수집 규칙)은 Azure Monitor로 오는 데이터를 정의하고 해당 데이터를 보내거나 저장해야 하는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="bd110-111">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="bd110-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="bd110-112">예제</span><span class="sxs-lookup"><span data-stu-id="bd110-112">EXAMPLES</span></span>

### <span data-ttu-id="bd110-113">예제 1: 데이터 수집 규칙 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd110-113">Example 1: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleName 'newDcr'
                                   -ResourceGroupName 'testdcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="bd110-114">이 명령은 주어진 데이터 수집 규칙에 대한 태그 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-114">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="bd110-115">예제 2: 데이터 수집 규칙 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd110-115">Example 2: Update data collection rule tags</span></span>
```
PS C:\>Update-AzDataCollectionRule -RuleId '/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/newDcr'
                                   -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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
```

<span data-ttu-id="bd110-116">이 명령은 주어진 데이터 수집 규칙에 대한 태그 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-116">This command updates the tags property for the given data collection rule.</span></span>

### <span data-ttu-id="bd110-117">예제 3: 데이터 수집 규칙 태그 업데이트</span><span class="sxs-lookup"><span data-stu-id="bd110-117">Example 3: Update data collection rule tags</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName "testdcr" -Name "newDcr"
PS C:\>$dcr | Update-AzDataCollectionRule -Tag @{"tag1"="value1"; "tag2"="value2"}

Description       : 
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

<span data-ttu-id="bd110-118">이 명령은 주어진 데이터 수집 규칙에 대한 태그 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-118">This command updates the tags property for the given data collection rule.</span></span>

## <span data-ttu-id="bd110-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="bd110-119">PARAMETERS</span></span>

### <span data-ttu-id="bd110-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd110-120">-DefaultProfile</span></span>
<span data-ttu-id="bd110-121">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="bd110-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="bd110-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bd110-122">-ResourceGroupName</span></span>
<span data-ttu-id="bd110-123">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="bd110-123">The resource group name</span></span>

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

### <span data-ttu-id="bd110-124">-RuleName</span><span class="sxs-lookup"><span data-stu-id="bd110-124">-RuleName</span></span>
<span data-ttu-id="bd110-125">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="bd110-125">The resource name</span></span>

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

### <span data-ttu-id="bd110-126">-RuleId</span><span class="sxs-lookup"><span data-stu-id="bd110-126">-RuleId</span></span>
<span data-ttu-id="bd110-127">데이터 수집 규칙의 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="bd110-127">The resource ID of the data collection rule</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="bd110-128">-InputObject</span><span class="sxs-lookup"><span data-stu-id="bd110-128">-InputObject</span></span>
<span data-ttu-id="bd110-129">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="bd110-129">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="bd110-130">-Tag</span><span class="sxs-lookup"><span data-stu-id="bd110-130">-Tag</span></span>
<span data-ttu-id="bd110-131">데이터 수집 규칙의 태그 속성</span><span class="sxs-lookup"><span data-stu-id="bd110-131">The tags property of the data collection rule</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: Falose
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd110-132">-확인</span><span class="sxs-lookup"><span data-stu-id="bd110-132">-Confirm</span></span>
<span data-ttu-id="bd110-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bd110-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bd110-134">-WhatIf</span></span>
<span data-ttu-id="bd110-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bd110-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bd110-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd110-137">CommonParameters</span></span>
<span data-ttu-id="bd110-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="bd110-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd110-139">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="bd110-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd110-140">입력</span><span class="sxs-lookup"><span data-stu-id="bd110-140">INPUTS</span></span>

### <span data-ttu-id="bd110-141">System.String</span><span class="sxs-lookup"><span data-stu-id="bd110-141">System.String</span></span>

## <span data-ttu-id="bd110-142">출력</span><span class="sxs-lookup"><span data-stu-id="bd110-142">OUTPUTS</span></span>

### <span data-ttu-id="bd110-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="bd110-143">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="bd110-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="bd110-144">NOTES</span></span>

## <span data-ttu-id="bd110-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd110-145">RELATED LINKS</span></span>

<span data-ttu-id="bd110-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="bd110-146">[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Remove-AzDataCollectionRule](./Remove-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)</span></span>