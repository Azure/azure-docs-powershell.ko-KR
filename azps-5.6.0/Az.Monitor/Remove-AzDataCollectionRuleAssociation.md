---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 87830eb9cb4321bf9af1476d3fa5a0db41796351
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987812"
---
# <span data-ttu-id="059ab-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="059ab-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="059ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="059ab-102">SYNOPSIS</span></span>
<span data-ttu-id="059ab-103">데이터 수집 규칙 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="059ab-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="059ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="059ab-104">SYNTAX</span></span>

### <span data-ttu-id="059ab-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="059ab-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -TargetResourceId <string> 
      -AssociationName <string> 
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="059ab-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="059ab-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="059ab-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="059ab-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="059ab-108">설명</span><span class="sxs-lookup"><span data-stu-id="059ab-108">DESCRIPTION</span></span>
<span data-ttu-id="059ab-109">**Remove-AzDataCollectionRuleAssociation** cmdlet은 DCRA(데이터 수집 규칙 연결)를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="059ab-110">가상 머신에 DCR을 적용하기 위해 가상 머신에 대한 연결 을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="059ab-111">가상 머신에는 여러 DCRS에 대한 연결이 있을 수 있으며 DCR에는 여러 가상 머신이 연결되어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="059ab-112">이렇게 하면 특정 요구 사항과 일치하는 DCRs 집합을 정의하고 해당 DCRS 집합을 적용하는 가상 머신에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="059ab-113">DCRA를 사용하여 "Azure Monitor 에이전트에 대한 데이터 수집 [구성"은](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 다음과 같은 문서입니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="059ab-114">예제</span><span class="sxs-lookup"><span data-stu-id="059ab-114">EXAMPLES</span></span>

### <span data-ttu-id="059ab-115">예제 1: 이름 및 대상 리소스 ID(연결된 가상 머신) 매개 변수와 데이터 수집 규칙 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="059ab-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="059ab-116">예제 2: 입력 개체로 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="059ab-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="059ab-117">예제 3: 연결 리소스 ID 속성을 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="059ab-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="059ab-118">매개 변수</span><span class="sxs-lookup"><span data-stu-id="059ab-118">PARAMETERS</span></span>

### <span data-ttu-id="059ab-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="059ab-119">-DefaultProfile</span></span>
<span data-ttu-id="059ab-120">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="059ab-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="059ab-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="059ab-121">-TargetResourceId</span></span>
<span data-ttu-id="059ab-122">연결된 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="059ab-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="059ab-123">-AssociationName</span></span>
<span data-ttu-id="059ab-124">연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-124">The name of the association resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName (Default)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="059ab-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="059ab-125">-InputObject</span></span>
<span data-ttu-id="059ab-126">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="059ab-126">PSDataCollectionRuleResource Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource
Parameter Sets: ByInputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True
Accept wildcard characters: False
```

### <span data-ttu-id="059ab-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="059ab-127">-AssociationId</span></span>
<span data-ttu-id="059ab-128">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-128">The resource identifier.</span></span>

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

### <span data-ttu-id="059ab-129">-확인</span><span class="sxs-lookup"><span data-stu-id="059ab-129">-Confirm</span></span>
<span data-ttu-id="059ab-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="059ab-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="059ab-131">-WhatIf</span></span>
<span data-ttu-id="059ab-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="059ab-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="059ab-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="059ab-134">CommonParameters</span></span>
<span data-ttu-id="059ab-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="059ab-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="059ab-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="059ab-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="059ab-137">입력</span><span class="sxs-lookup"><span data-stu-id="059ab-137">INPUTS</span></span>

### <span data-ttu-id="059ab-138">System.String</span><span class="sxs-lookup"><span data-stu-id="059ab-138">System.String</span></span>
###<span data-ttu-id="059ab-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="059ab-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="059ab-140">출력</span><span class="sxs-lookup"><span data-stu-id="059ab-140">OUTPUTS</span></span>

### <span data-ttu-id="059ab-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="059ab-141">System.Boolean</span></span>

## <span data-ttu-id="059ab-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="059ab-142">NOTES</span></span>

## <span data-ttu-id="059ab-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="059ab-143">RELATED LINKS</span></span>

<span data-ttu-id="059ab-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="059ab-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
