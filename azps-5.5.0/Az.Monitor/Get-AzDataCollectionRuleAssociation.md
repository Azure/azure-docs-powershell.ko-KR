---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 144e67a2e58aeaa7fe7aa424ddc79bfca4aaa538
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180188"
---
# <span data-ttu-id="85ab1-101">Get-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="85ab1-101">Get-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="85ab1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ab1-102">SYNOPSIS</span></span>
<span data-ttu-id="85ab1-103">데이터 수집 규칙 연결(s)을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-103">Gets data collection rule association(s).</span></span>

## <span data-ttu-id="85ab1-104">구문</span><span class="sxs-lookup"><span data-stu-id="85ab1-104">SYNTAX</span></span>

### <span data-ttu-id="85ab1-105">ByAssociatedResource(기본값)</span><span class="sxs-lookup"><span data-stu-id="85ab1-105">ByAssociatedResource (Default)</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="85ab1-106">ByName</span><span class="sxs-lookup"><span data-stu-id="85ab1-106">ByName</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -TargetResourceId <string> 
   -AssociationName <string> 
   [-DefaultProfile <IAzureContextContainer>] 
   [<CommonParameters>]
```

### <span data-ttu-id="85ab1-107">ByRule</span><span class="sxs-lookup"><span data-stu-id="85ab1-107">ByRule</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

### <span data-ttu-id="85ab1-108">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="85ab1-108">ByInputObject</span></span>
```
Get-AzDataCollectionRuleAssociation 
   -InputObject <PSDataCollectionRuleResource> 
   [-DefaultProfile <IAzureContextContainer>]
   [<CommonParameters>]
```

## <span data-ttu-id="85ab1-109">설명</span><span class="sxs-lookup"><span data-stu-id="85ab1-109">DESCRIPTION</span></span>
<span data-ttu-id="85ab1-110">**Get-AzDataCollectionRuleAssociation** cmdlet은 DCRA(데이터 수집 규칙 연결)를 하나 이상 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-110">The **Get-AzDataCollectionRuleAssociation** cmdlet gets one or more data collection rules associations (DCRA).</span></span>

<span data-ttu-id="85ab1-111">가상 머신에 DCR을 적용하기 위해 가상 머신에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="85ab1-111">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="85ab1-112">가상 머신은 여러 DCRS에 연결될 수 있으며 DCR에는 여러 가상 머신이 연결되어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-112">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="85ab1-113">이렇게 하면 각각 특정 요구 사항과 일치하는 DCRs 집합을 정의하고 해당 요구 사항이 적용되는 가상 머신에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-113">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="85ab1-114">DCRA 문서를 사용하여 ["Azure Monitor 에이전트에 대한](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 데이터 수집 구성"은 다음과 있습니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-114">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="85ab1-115">예제</span><span class="sxs-lookup"><span data-stu-id="85ab1-115">EXAMPLES</span></span>

### <span data-ttu-id="85ab1-116">예제 1: 대상 리소스 ID(연결된 가상 머신)에 따라 데이터 수집 규칙 연결 얻기</span><span class="sxs-lookup"><span data-stu-id="85ab1-116">Example 1: Get data collection rules associations by target resource ID (associated virtual machine)</span></span>
```
PS C:\>$vm = Get-AzVM -ResourceGroupName $rg -Name $vmName
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="85ab1-117">이 명령은 주어진 대상 리소스 ID(가상 머신)에 대한 모든 데이터 수집 규칙을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-117">This command lists all the data collection rules for the given target resource ID (virtual machine).</span></span>

### <span data-ttu-id="85ab1-118">예제 2: DCR(규칙에 따라 데이터 수집 규칙 연결)</span><span class="sxs-lookup"><span data-stu-id="85ab1-118">Example 2: Get data collection rules associations by rule (DCR)</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -ResourceGroup $rg -RuleName $dcrName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="85ab1-119">이 명령은 주어진 리소스 그룹 및 규칙(DCR)에 대한 데이터 수집 규칙 연결 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-119">This command lists data collection rules associations for the given resource group and rule (DCR).</span></span>

### <span data-ttu-id="85ab1-120">예제 3: 입력 개체로 데이터 수집 규칙 연결(PSDataCollectionRuleResource)</span><span class="sxs-lookup"><span data-stu-id="85ab1-120">Example 3: Get data collection rule associations by input object (PSDataCollectionRuleResource)</span></span>
```
PS C:\>$dcr = Get-AzDataCollectionRule -ResourceGroupName $rg -RuleName $dcrName
PS C:\>$dcr | Get-AzDataCollectionRuleAssociation

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="85ab1-121">이 명령은 주어진 입력 개체에 대한 데이터 수집 규칙 연결 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-121">This command lists data collection rules associations for the given input object.</span></span>

### <span data-ttu-id="85ab1-122">예제 4: 대상 리소스 ID(연결된 가상 머신) 및 연결 이름으로 데이터 수집 규칙 연결</span><span class="sxs-lookup"><span data-stu-id="85ab1-122">Example 4: Get a data collection rule association by target resource ID (associated virtual machine) and association name</span></span>
```
PS C:\>Get-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName

Description          :
DataCollectionRuleId : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.I
                       nsights/dataCollectionRules/{dcrName}
ProvisioningState    :
Etag                 : "{etag}"
Id                   : /subscriptions/{subId}/resourceGroups/{rg}/providers/Microsoft.C
                       ompute/virtualMachines/{vmName}/providers/Microsoft.Insights/dataCollectionRuleAssociations/{assocName}
Name                 : {assocName}
Type                 : Microsoft.Insights/dataCollectionRuleAssociations
```

<span data-ttu-id="85ab1-123">이 명령은 데이터 수집 규칙 연결 중 하나(단일 요소가 있는 목록)를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-123">This command lists one (a list with a single element) data collection rule association.</span></span>

## <span data-ttu-id="85ab1-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="85ab1-124">PARAMETERS</span></span>

### <span data-ttu-id="85ab1-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ab1-125">-DefaultProfile</span></span>
<span data-ttu-id="85ab1-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="85ab1-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="85ab1-127">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="85ab1-127">-TargetResourceId</span></span>
<span data-ttu-id="85ab1-128">연결된 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="85ab1-128">The associated resource ID</span></span>

```yaml
Type: System.String
Parameter Sets: ByAssociatedResource (Default)
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: ResourceUri

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ab1-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="85ab1-129">-ResourceGroupName</span></span>
<span data-ttu-id="85ab1-130">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="85ab1-130">The resource group name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="85ab1-131">-RuleName</span><span class="sxs-lookup"><span data-stu-id="85ab1-131">-RuleName</span></span>
<span data-ttu-id="85ab1-132">데이터 수집 규칙 이름</span><span class="sxs-lookup"><span data-stu-id="85ab1-132">The data collection rule name</span></span>

```yaml
Type: System.String
Parameter Sets: ByRule
Aliases: DataCollectionRuleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ab1-133">-InputObject</span><span class="sxs-lookup"><span data-stu-id="85ab1-133">-InputObject</span></span>
<span data-ttu-id="85ab1-134">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="85ab1-134">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="85ab1-135">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="85ab1-135">-AssociationName</span></span>
<span data-ttu-id="85ab1-136">연결의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-136">The name of the association.</span></span>

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

### <span data-ttu-id="85ab1-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ab1-137">CommonParameters</span></span>
<span data-ttu-id="85ab1-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="85ab1-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ab1-139">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="85ab1-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ab1-140">입력</span><span class="sxs-lookup"><span data-stu-id="85ab1-140">INPUTS</span></span>

### <span data-ttu-id="85ab1-141">System.String</span><span class="sxs-lookup"><span data-stu-id="85ab1-141">System.String</span></span>
### <span data-ttu-id="85ab1-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="85ab1-142">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="85ab1-143">출력</span><span class="sxs-lookup"><span data-stu-id="85ab1-143">OUTPUTS</span></span>

### <span data-ttu-id="85ab1-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="85ab1-144">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="85ab1-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="85ab1-145">NOTES</span></span>

## <span data-ttu-id="85ab1-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85ab1-146">RELATED LINKS</span></span>

<span data-ttu-id="85ab1-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md) 
 [New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span><span class="sxs-lookup"><span data-stu-id="85ab1-147">[Remove-AzDataCollectionRuleAssociation](./Remove-AzDataCollectionRuleAssociation.md)
[New-AzDataCollectionRuleAssociation](./New-AzDataCollectionRuleAssociation.md)</span></span>
