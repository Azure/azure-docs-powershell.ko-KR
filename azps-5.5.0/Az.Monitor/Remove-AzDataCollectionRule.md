---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/remove-azdatacollectionrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Remove-AzDataCollectionRule.md
ms.openlocfilehash: 24b5d7dc4209edfbd9bb3080bc87fc18a14977b0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190105"
---
# <span data-ttu-id="74e22-101">Remove-AzDataCollectionRule</span><span class="sxs-lookup"><span data-stu-id="74e22-101">Remove-AzDataCollectionRule</span></span>

## <span data-ttu-id="74e22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="74e22-102">SYNOPSIS</span></span>
<span data-ttu-id="74e22-103">데이터 수집 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-103">Delete a data collection rule.</span></span>

## <span data-ttu-id="74e22-104">구문</span><span class="sxs-lookup"><span data-stu-id="74e22-104">SYNTAX</span></span>

### <span data-ttu-id="74e22-105">ByName(기본값)</span><span class="sxs-lookup"><span data-stu-id="74e22-105">ByName (Default)</span></span>
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

### <span data-ttu-id="74e22-106">ByInputObject</span><span class="sxs-lookup"><span data-stu-id="74e22-106">ByInputObject</span></span>
```
Remove-AzDataCollectionRule
   -InputObject <PSDataCollectionRuleResource>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

### <span data-ttu-id="74e22-107">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="74e22-107">ByResourceId</span></span>
```
Remove-AzDataCollectionRule
   -RuleId <string>
   [-PassThru]
   [-DefaultProfile <IAzureContextContainer>]
   [-WhatIf]
   [-Confirm]
   [<CommonParameters>]
```

## <span data-ttu-id="74e22-108">설명</span><span class="sxs-lookup"><span data-stu-id="74e22-108">DESCRIPTION</span></span>
<span data-ttu-id="74e22-109">**Remove-AzDataCollectionRule** cmdlet은 데이터 컬렉션 규칙을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-109">The **Remove-AzDataCollectionRule** cmdlet delete a data collection rule.</span></span>

<span data-ttu-id="74e22-110">DCR(데이터 수집 규칙)은 Azure Monitor로 들어오는 데이터를 정의하고 해당 데이터를 보내거나 저장할 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-110">Data Collection Rules (DCR) define data coming into Azure Monitor and specify where that data should be sent or stored.</span></span> <span data-ttu-id="74e22-111">다음은 전체 [DCR 개요 문서입니다.](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview)</span><span class="sxs-lookup"><span data-stu-id="74e22-111">Here is the complete [DCR overview article](https://docs.microsoft.com/en-us/azure/azure-monitor/platform/data-collection-rule-overview).</span></span>

## <span data-ttu-id="74e22-112">예제</span><span class="sxs-lookup"><span data-stu-id="74e22-112">EXAMPLES</span></span>

### <span data-ttu-id="74e22-113">예제 1: 이름 및 리소스 그룹 매개 변수를 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="74e22-113">Example 1: Delete data collection rule with name and resource group parameters</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr"             
```

### <span data-ttu-id="74e22-114">예제 2: 이름 및 리소스 그룹 반환 bool을 사용하여 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="74e22-114">Example 2: Delete data collection rule with name and resource group return bool</span></span>
```
PS C:\>Remove-AzDataCollectionRule -ResourceGroupName "testgroup" -RuleName "testDcr" -PassThru

True
```

### <span data-ttu-id="74e22-115">예제 3: InputObject에서 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="74e22-115">Example 3: Delete data collection rule from InputObject</span></span>
```
PS C:\>Get-AzDataCollectionRule -ResourceGroupName "testdcr" -RuleName "dcrFromPipe95" | Remove-AzDataCollectionRule
```

### <span data-ttu-id="74e22-116">예제 4: 리소스 ID에서 데이터 수집 규칙 삭제</span><span class="sxs-lookup"><span data-stu-id="74e22-116">Example 4: Delete data collection rule from resource id</span></span>
```
PS C:\>Remove-AzDataCollectionRule -RuleId "/subscriptions/{subId}/resourceGroups/testdcr/providers/Microsoft.Insights/dataCollectionRules/{dcrName}"
```

## <span data-ttu-id="74e22-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="74e22-117">PARAMETERS</span></span>

### <span data-ttu-id="74e22-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="74e22-118">-DefaultProfile</span></span>
<span data-ttu-id="74e22-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="74e22-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="74e22-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="74e22-120">-ResourceGroupName</span></span>
<span data-ttu-id="74e22-121">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="74e22-121">The resource group name</span></span>

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

### <span data-ttu-id="74e22-122">-RuleName</span><span class="sxs-lookup"><span data-stu-id="74e22-122">-RuleName</span></span>
<span data-ttu-id="74e22-123">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-123">The resource name.</span></span>

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

### <span data-ttu-id="74e22-124">-RuleId</span><span class="sxs-lookup"><span data-stu-id="74e22-124">-RuleId</span></span>
<span data-ttu-id="74e22-125">리소스 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-125">The resource identifier.</span></span>

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

### <span data-ttu-id="74e22-126">-Confirm</span><span class="sxs-lookup"><span data-stu-id="74e22-126">-Confirm</span></span>
<span data-ttu-id="74e22-127">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="74e22-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="74e22-128">-WhatIf</span></span>
<span data-ttu-id="74e22-129">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="74e22-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="74e22-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="74e22-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="74e22-131">CommonParameters</span></span>
<span data-ttu-id="74e22-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="74e22-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="74e22-133">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="74e22-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="74e22-134">입력</span><span class="sxs-lookup"><span data-stu-id="74e22-134">INPUTS</span></span>

### <span data-ttu-id="74e22-135">System.String</span><span class="sxs-lookup"><span data-stu-id="74e22-135">System.String</span></span>

## <span data-ttu-id="74e22-136">출력</span><span class="sxs-lookup"><span data-stu-id="74e22-136">OUTPUTS</span></span>

### <span data-ttu-id="74e22-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span><span class="sxs-lookup"><span data-stu-id="74e22-137">Microsoft.Azure.Commands.Insights.OutputClasses.PSDataCollectionRuleResource</span></span>

## <span data-ttu-id="74e22-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="74e22-138">NOTES</span></span>

## <span data-ttu-id="74e22-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="74e22-139">RELATED LINKS</span></span>

<span data-ttu-id="74e22-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md) 
 [Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md) 
 [New-AzDataCollectionRule](./New-AzDataCollectionRule.md) 
 [Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span><span class="sxs-lookup"><span data-stu-id="74e22-140">[Set-AzDataCollectionRule](./Set-AzDataCollectionRule.md)
[Get-AzDataCollectionRule](./Get-AzDataCollectionRule.md)
[New-AzDataCollectionRule](./New-AzDataCollectionRule.md)
[Update-AzDataCollectionRule](./Update-AzDataCollectionRule.md)</span></span>