---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionruleassociation
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRuleAssociation.md
ms.openlocfilehash: 798bb97b9e84121894341dd807bbaa9b3658a039
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100203406"
---
# <span data-ttu-id="dc5ac-101">Remove-AzDataCollectionRuleAssociation</span><span class="sxs-lookup"><span data-stu-id="dc5ac-101">Remove-AzDataCollectionRuleAssociation</span></span>

## <span data-ttu-id="dc5ac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc5ac-102">SYNOPSIS</span></span>
<span data-ttu-id="dc5ac-103">데이터 컬렉션 규칙 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="dc5ac-103">Delete a data collection rule association.</span></span>

## <span data-ttu-id="dc5ac-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc5ac-104">SYNTAX</span></span>

### <span data-ttu-id="dc5ac-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc5ac-105">ByName (Default)</span></span>
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

### <span data-ttu-id="dc5ac-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="dc5ac-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -InputObject <PSDataCollectionRuleAssociationProxyOnlyResource>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

### <span data-ttu-id="dc5ac-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5ac-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRuleAssociation
      -AssociationId <string>
      [-PassThru]
      [-DefaultProfile <IAzureContextContainer>]
      [-WhatIf]
      [-Confirm]
      [<CommonParameters>]
```

## <span data-ttu-id="dc5ac-108">설명</span><span class="sxs-lookup"><span data-stu-id="dc5ac-108">DESCRIPTION</span></span>
<span data-ttu-id="dc5ac-109">**Remove-AzDataCollectionRuleAssociation** cmdlet은 DCRA(데이터 수집 규칙 연결)를 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-109">The **Remove-AzDataCollectionRuleAssociation** cmdlet delete a data collection rule association (DCRA).</span></span>

<span data-ttu-id="dc5ac-110">가상 머신에 DCR을 적용하기 위해 가상 머신에 대한 연결 만들기</span><span class="sxs-lookup"><span data-stu-id="dc5ac-110">To apply a DCR to a virtual machine, you create an association for the virtual machine.</span></span> <span data-ttu-id="dc5ac-111">가상 머신은 여러 DCRS에 연결될 수 있으며 DCR에는 여러 가상 머신이 연결되어 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-111">A virtual machine may have an association to multiple DCRs, and a DCR may have multiple virtual machines associated to it.</span></span> <span data-ttu-id="dc5ac-112">이렇게 하면 각각 특정 요구 사항과 일치하는 DCRS 집합을 정의하고 해당 요구 사항이 적용되는 가상 머신에만 적용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-112">This allows you to define a set of DCRs, each matching a particular requirement, and apply them to only the virtual machines where they apply.</span></span> <span data-ttu-id="dc5ac-113">다음은 DCRA 문서를 사용하여 ["Azure Monitor 에이전트에 대한](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) 데이터 수집 구성"입니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-113">Here is the ["Configure data collection for the Azure Monitor agent"](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-azure-monitor-agent) using DCRA article.</span></span>

## <span data-ttu-id="dc5ac-114">예제</span><span class="sxs-lookup"><span data-stu-id="dc5ac-114">EXAMPLES</span></span>

### <span data-ttu-id="dc5ac-115">예제 1: 이름 및 대상 리소스 ID(연결된 가상 머신) 매개 변수와 데이터 수집 규칙 연결 삭제</span><span class="sxs-lookup"><span data-stu-id="dc5ac-115">Example 1: Delete data collection rule association with name and target resource ID (associated virtual machine) parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRuleAssociation -TargetResourceId $vm.Id -AssociationName $assocName
```

### <span data-ttu-id="dc5ac-116">예제 2: 입력 개체를 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="dc5ac-116">Example 2: Delete data collection rule with Input Object</span></span>
```
PS C:\>$dcrAssoc | Remove-AzDataCollectionRule
```

### <span data-ttu-id="dc5ac-117">예제 3: 연결 리소스 ID 속성을 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="dc5ac-117">Example 3: Delete data collection rule with the association resource ID property</span></span>
```
PS C:\>Remove-AzDataCollectionRule -AssociationId $dcrAssoc.Id
```

## <span data-ttu-id="dc5ac-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc5ac-118">PARAMETERS</span></span>

### <span data-ttu-id="dc5ac-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc5ac-119">-DefaultProfile</span></span>
<span data-ttu-id="dc5ac-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc5ac-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc5ac-121">-TargetResourceId</span><span class="sxs-lookup"><span data-stu-id="dc5ac-121">-TargetResourceId</span></span>
<span data-ttu-id="dc5ac-122">연결된 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-122">The associated resource ID.</span></span>

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

### <span data-ttu-id="dc5ac-123">-AssociationName</span><span class="sxs-lookup"><span data-stu-id="dc5ac-123">-AssociationName</span></span>
<span data-ttu-id="dc5ac-124">연결 리소스의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-124">The name of the association resource.</span></span>

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

### <span data-ttu-id="dc5ac-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="dc5ac-125">-InputObject</span></span>
<span data-ttu-id="dc5ac-126">PSDataCollectionRuleResource 개체</span><span class="sxs-lookup"><span data-stu-id="dc5ac-126">PSDataCollectionRuleResource Object</span></span>

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

### <span data-ttu-id="dc5ac-127">-AssociationId</span><span class="sxs-lookup"><span data-stu-id="dc5ac-127">-AssociationId</span></span>
<span data-ttu-id="dc5ac-128">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-128">The resource identifier.</span></span>

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

### <span data-ttu-id="dc5ac-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc5ac-129">-Confirm</span></span>
<span data-ttu-id="dc5ac-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc5ac-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc5ac-131">-WhatIf</span></span>
<span data-ttu-id="dc5ac-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc5ac-132">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc5ac-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc5ac-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc5ac-134">CommonParameters</span></span>
<span data-ttu-id="dc5ac-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc5ac-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc5ac-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc5ac-137">입력</span><span class="sxs-lookup"><span data-stu-id="dc5ac-137">INPUTS</span></span>

### <span data-ttu-id="dc5ac-138">System.String</span><span class="sxs-lookup"><span data-stu-id="dc5ac-138">System.String</span></span>
###<span data-ttu-id="dc5ac-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span><span class="sxs-lookup"><span data-stu-id="dc5ac-139">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleAssociationProxyOnlyResource</span></span>

## <span data-ttu-id="dc5ac-140">출력</span><span class="sxs-lookup"><span data-stu-id="dc5ac-140">OUTPUTS</span></span>

### <span data-ttu-id="dc5ac-141">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="dc5ac-141">System.Boolean</span></span>

## <span data-ttu-id="dc5ac-142">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc5ac-142">NOTES</span></span>

## <span data-ttu-id="dc5ac-143">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc5ac-143">RELATED LINKS</span></span>

<span data-ttu-id="dc5ac-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="dc5ac-144">[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)</span></span>
