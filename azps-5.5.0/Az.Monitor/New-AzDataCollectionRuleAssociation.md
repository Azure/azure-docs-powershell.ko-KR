---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: bdfc576c64b56d11ecf30f32e34f80b0ef6de866
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203426"
---
# <span data-ttu-id="f75ea-101">New-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="f75ea-101">New-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="f75ea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f75ea-102">SYNOPSIS</span></span>
<span data-ttu-id="f75ea-103">데이터 수집 규칙 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="f75ea-103">Create data collection rule association.</span></span>

## <span data-ttu-id="f75ea-104">구문</span><span class="sxs-lookup"><span data-stu-id="f75ea-104">SYNTAX</span></span>

### <span data-ttu-id="f75ea-105">ByDataCollectionRuleId(기본값)</span><span class="sxs-lookup"><span data-stu-id="f75ea-105">ByDataCollectionRuleId (Default)</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -RuleId <string>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="f75ea-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="f75ea-106">ByInputObject</span></span>
```
New-AzDataCollectionRuleAssociation
   -TargetResourceId <string>
   -AssociationName <string>
   -InputObject <PSDataCollectionRuleResource>
   [-Description <string>]
   [-DefaultProfile <IAzureContextContainer>]  
   [-WhatIf]   
   [-Confirm]   
   [<CommonParameters>]
```


## <span data-ttu-id="f75ea-107">설명</span><span class="sxs-lookup"><span data-stu-id="f75ea-107">DESCRIPTION</span></span>
<span data-ttu-id="f75ea-108">**New-AzDataCollectionRuleAssociation** cmdlet은 DCRA(데이터 수집 규칙 연결)를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-108">The **New-AzDataCollectionRuleAssociation** cmdlet creates a data collection rules association (DCRA).</span></span>

<span data-ttu-id="f75ea-109">가상 머신에 DCR을 적용하기 위해 가상 머신에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="f75ea-109">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="f75ea-110">가상 머신은 여러 DCRS에 연결될 수 있으며 DCR에는 여러 가상 머신이 연결되어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-110">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="f75ea-111">이렇게 하면 각각 특정 요구 사항과 일치하는 DCRs 집합을 정의하고 해당 요구 사항이 적용되는 가상 머신에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-111">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="f75ea-112">DCRA 문서를 사용하여 ["Azure Monitor 에이전트에 대한](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 데이터 수집 구성"은 다음과 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-112">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="f75ea-113">예제</span><span class="sxs-lookup"><span data-stu-id="f75ea-113">EXAMPLES</span></span>

### <span data-ttu-id="f75ea-114">예제 1: 데이터 수집 규칙 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="f75ea-114">Example 1: Create data collection rule association</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssoc" -RuleId $dcr.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssoc
Name                 : dcrAssoc
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="f75ea-115">이 명령은 주어진 규칙 및 대상 리소스 ID에 대한 데이터 수집 규칙 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-115">This command creates a data collection rule association for given rule and target resource ID.</span></span>

### <span data-ttu-id="f75ea-116">예제 2: DCR 개체에서 데이터 수집 규칙 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="f75ea-116">Example 2: Create data collection rule association from a DCR object</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$vmId = '/subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}'
PS C:\>$dcr | New-AzDataCollectionRuleAssociation -TargetResourceId $vmId -AssociationName "dcrAssocInput"

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Insights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{resourcegroup}/providers/Microsoft.Compute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/dcrAssocInput
Name                 : dcrAssocInput
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="f75ea-117">이 명령은 주어진 규칙 및 대상 리소스 ID에 대한 데이터 수집 규칙 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-117">This command creates a data collection rule association for given rule and target resource ID.</span></span>

## <span data-ttu-id="f75ea-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f75ea-118">PARAMETERS</span></span>

### <span data-ttu-id="f75ea-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f75ea-119">-DefaultProfile</span></span>
<span data-ttu-id="f75ea-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f75ea-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f75ea-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="f75ea-121">-TargetResourceId</span></span>
<span data-ttu-id="f75ea-122">연결되는 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="f75ea-122">The resource ID to associate</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75ea-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="f75ea-123">-AssociationName</span></span>
<span data-ttu-id="f75ea-124">리소스 이름</span><span class="sxs-lookup"><span data-stu-id="f75ea-124">The resource name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75ea-125">-RuleId</span><span class="sxs-lookup"><span data-stu-id="f75ea-125">-RuleId</span></span>
<span data-ttu-id="f75ea-126">데이터 수집 규칙 ID</span><span class="sxs-lookup"><span data-stu-id="f75ea-126">The data collection rule ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByDataCollectionRuleId
Aliases: DataCollectionRuleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75ea-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f75ea-127">-InputObject</span></span>
<span data-ttu-id="f75ea-128">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="f75ea-128">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: System.String
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="f75ea-129">-Description</span><span class="sxs-lookup"><span data-stu-id="f75ea-129">-Description</span></span>
<span data-ttu-id="f75ea-130">리소스 설명</span><span class="sxs-lookup"><span data-stu-id="f75ea-130">The resource description</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f75ea-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f75ea-131">-Confirm</span></span>
<span data-ttu-id="f75ea-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f75ea-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f75ea-133">-WhatIf</span></span>
<span data-ttu-id="f75ea-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f75ea-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f75ea-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f75ea-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f75ea-136">CommonParameters</span></span>
<span data-ttu-id="f75ea-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f75ea-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f75ea-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f75ea-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f75ea-139">입력</span><span class="sxs-lookup"><span data-stu-id="f75ea-139">INPUTS</span></span>

### <span data-ttu-id="f75ea-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f75ea-140">System.String</span></span>

## <span data-ttu-id="f75ea-141">출력</span><span class="sxs-lookup"><span data-stu-id="f75ea-141">OUTPUTS</span></span>

### <span data-ttu-id="f75ea-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="f75ea-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="f75ea-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f75ea-143">NOTES</span></span>

## <span data-ttu-id="f75ea-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f75ea-144">RELATED LINKS</span></span>

<span data-ttu-id="f75ea-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md) 
 [Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="f75ea-145">[Set-AzDataCollectionRuleAssociation](./Set-AzDataCollectionRuleAssociation.md)
[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[Get-AzDataCollectionRuleAssociation](./Get-AzDataCollectionRuleAssociation.md)</span></span>
