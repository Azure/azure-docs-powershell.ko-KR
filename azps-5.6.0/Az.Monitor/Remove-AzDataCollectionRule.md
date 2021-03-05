---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 4dfa9417b2bce7473b3d2986f503c163cb6bf42f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974800"
---
# <span data-ttu-id="8163a-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="8163a-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="8163a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8163a-102">SYNOPSIS</span></span>
<span data-ttu-id="8163a-103">데이터 수집 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="8163a-104">구문</span><span class="sxs-lookup"><span data-stu-id="8163a-104">SYNTAX</span></span>

### <span data-ttu-id="8163a-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="8163a-105">ByName (Default)</span></span>
```
Remove-AzDataCollectionRule
   -ResourceGroupName <string> 
   -RuleName <string> 
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="8163a-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="8163a-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="8163a-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="8163a-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="8163a-108">설명</span><span class="sxs-lookup"><span data-stu-id="8163a-108">DESCRIPTION</span></span>
<span data-ttu-id="8163a-109">**Remove-AzDataCollectionRule** cmdlet은 데이터 수집 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="8163a-110">DCR(데이터 수집 규칙)은 Azure Monitor로 오는 데이터를 정의하고 해당 데이터를 보내거나 저장해야 하는 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="8163a-111">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="8163a-111">Here is the complete [DCR overview article](https://docs.microsoft.com/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="8163a-112">예제</span><span class="sxs-lookup"><span data-stu-id="8163a-112">EXAMPLES</span></span>

### <span data-ttu-id="8163a-113">예제 1: 이름 및 리소스 그룹 매개 변수를 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="8163a-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="8163a-114">예제 2: 이름 및 리소스 그룹 반환 bool을 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="8163a-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="8163a-115">예제 3: InputObject에서 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="8163a-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="8163a-116">예제 4: 리소스 ID에서 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="8163a-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="8163a-117">매개 변수</span><span class="sxs-lookup"><span data-stu-id="8163a-117">PARAMETERS</span></span>

### <span data-ttu-id="8163a-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8163a-118">-DefaultProfile</span></span>
<span data-ttu-id="8163a-119">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8163a-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8163a-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8163a-120">-ResourceGroupName</span></span>
<span data-ttu-id="8163a-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="8163a-121">The resource group name</span></span>

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

### <span data-ttu-id="8163a-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="8163a-122">-RuleName</span></span>
<span data-ttu-id="8163a-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-123">The resource name.</span></span>

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

### <span data-ttu-id="8163a-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="8163a-124">-RuleId</span></span>
<span data-ttu-id="8163a-125">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-125">The resource identifier.</span></span>

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

### <span data-ttu-id="8163a-126">-확인</span><span class="sxs-lookup"><span data-stu-id="8163a-126">-Confirm</span></span>
<span data-ttu-id="8163a-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="8163a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8163a-128">-WhatIf</span></span>
<span data-ttu-id="8163a-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="8163a-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="8163a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8163a-131">CommonParameters</span></span>
<span data-ttu-id="8163a-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8163a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8163a-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="8163a-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8163a-134">입력</span><span class="sxs-lookup"><span data-stu-id="8163a-134">INPUTS</span></span>

### <span data-ttu-id="8163a-135">System.String</span><span class="sxs-lookup"><span data-stu-id="8163a-135">System.String</span></span>

## <span data-ttu-id="8163a-136">출력</span><span class="sxs-lookup"><span data-stu-id="8163a-136">OUTPUTS</span></span>

### <span data-ttu-id="8163a-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="8163a-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="8163a-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8163a-138">NOTES</span></span>

## <span data-ttu-id="8163a-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8163a-139">RELATED LINKS</span></span>

<span data-ttu-id="8163a-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="8163a-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>