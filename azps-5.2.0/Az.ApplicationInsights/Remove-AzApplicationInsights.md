---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: b63f1b350daad55a26dc91f46e89b28675622fbb
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353486"
---
# <span data-ttu-id="0fcf5-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="0fcf5-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="0fcf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0fcf5-102">SYNOPSIS</span></span>
<span data-ttu-id="0fcf5-103">Application Insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="0fcf5-103">Remove an application insights resource</span></span>

## <span data-ttu-id="0fcf5-104">구문</span><span class="sxs-lookup"><span data-stu-id="0fcf5-104">SYNTAX</span></span>

### <span data-ttu-id="0fcf5-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0fcf5-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fcf5-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcf5-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0fcf5-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0fcf5-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0fcf5-108">설명</span><span class="sxs-lookup"><span data-stu-id="0fcf5-108">DESCRIPTION</span></span>
<span data-ttu-id="0fcf5-109">Application Insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="0fcf5-109">Remove an application insights resource</span></span>

## <span data-ttu-id="0fcf5-110">예제</span><span class="sxs-lookup"><span data-stu-id="0fcf5-110">EXAMPLES</span></span>

### <span data-ttu-id="0fcf5-111">예제 1 Application Insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="0fcf5-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="0fcf5-112">리소스 그룹 "testgroup"에서 "test"라는 Application Insights 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="0fcf5-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0fcf5-113">PARAMETERS</span></span>

### <span data-ttu-id="0fcf5-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0fcf5-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0fcf5-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-115">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0fcf5-116">-DefaultProfile</span></span>
<span data-ttu-id="0fcf5-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0fcf5-118">-Name</span><span class="sxs-lookup"><span data-stu-id="0fcf5-118">-Name</span></span>
<span data-ttu-id="0fcf5-119">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-119">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="0fcf5-120">-PassThru</span></span>
<span data-ttu-id="0fcf5-121">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="0fcf5-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-122">This parameter is optional.</span></span> <span data-ttu-id="0fcf5-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-123">Default value is false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0fcf5-124">-ResourceGroupName</span></span>
<span data-ttu-id="0fcf5-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0fcf5-126">-ResourceId</span></span>
<span data-ttu-id="0fcf5-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0fcf5-128">-Confirm</span></span>
<span data-ttu-id="0fcf5-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0fcf5-130">-WhatIf</span></span>
<span data-ttu-id="0fcf5-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0fcf5-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0fcf5-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0fcf5-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0fcf5-133">CommonParameters</span></span>
<span data-ttu-id="0fcf5-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0fcf5-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0fcf5-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0fcf5-136">입력</span><span class="sxs-lookup"><span data-stu-id="0fcf5-136">INPUTS</span></span>

### <span data-ttu-id="0fcf5-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0fcf5-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0fcf5-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0fcf5-138">System.String</span></span>

## <span data-ttu-id="0fcf5-139">출력</span><span class="sxs-lookup"><span data-stu-id="0fcf5-139">OUTPUTS</span></span>

### <span data-ttu-id="0fcf5-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="0fcf5-140">System.Boolean</span></span>

## <span data-ttu-id="0fcf5-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0fcf5-141">NOTES</span></span>

## <span data-ttu-id="0fcf5-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0fcf5-142">RELATED LINKS</span></span>
