---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98353462"
---
# <span data-ttu-id="f96cc-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="f96cc-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="f96cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f96cc-102">SYNOPSIS</span></span>
<span data-ttu-id="f96cc-103">Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f96cc-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="f96cc-104">구문</span><span class="sxs-lookup"><span data-stu-id="f96cc-104">SYNTAX</span></span>

### <span data-ttu-id="f96cc-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f96cc-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f96cc-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f96cc-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f96cc-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f96cc-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f96cc-108">설명</span><span class="sxs-lookup"><span data-stu-id="f96cc-108">DESCRIPTION</span></span>
<span data-ttu-id="f96cc-109">Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f96cc-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="f96cc-110">예제</span><span class="sxs-lookup"><span data-stu-id="f96cc-110">EXAMPLES</span></span>

### <span data-ttu-id="f96cc-111">예제 1 Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f96cc-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="f96cc-112">리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 내보내기 ID "uGOoki0jQsyEs3IdQ83Q4QsNr4="를 사용하여 Application Insights 연속 내보내기 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="f96cc-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f96cc-113">PARAMETERS</span></span>

### <span data-ttu-id="f96cc-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f96cc-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="f96cc-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="f96cc-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f96cc-116">-DefaultProfile</span></span>
<span data-ttu-id="f96cc-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f96cc-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="f96cc-118">-ExportId</span></span>
<span data-ttu-id="f96cc-119">Application Insights 연속 내보내기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-119">Application Insights Continuous Export ID.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f96cc-120">-Name</span><span class="sxs-lookup"><span data-stu-id="f96cc-120">-Name</span></span>
<span data-ttu-id="f96cc-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="f96cc-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f96cc-122">-PassThru</span></span>
<span data-ttu-id="f96cc-123">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="f96cc-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-124">This parameter is optional.</span></span> <span data-ttu-id="f96cc-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-125">Default value is false.</span></span>

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

### <span data-ttu-id="f96cc-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f96cc-126">-ResourceGroupName</span></span>
<span data-ttu-id="f96cc-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="f96cc-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f96cc-128">-ResourceId</span></span>
<span data-ttu-id="f96cc-129">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="f96cc-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f96cc-130">-Confirm</span></span>
<span data-ttu-id="f96cc-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f96cc-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f96cc-132">-WhatIf</span></span>
<span data-ttu-id="f96cc-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f96cc-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f96cc-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f96cc-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f96cc-135">CommonParameters</span></span>
<span data-ttu-id="f96cc-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f96cc-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f96cc-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f96cc-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f96cc-138">입력</span><span class="sxs-lookup"><span data-stu-id="f96cc-138">INPUTS</span></span>

### <span data-ttu-id="f96cc-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="f96cc-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="f96cc-140">System.String</span><span class="sxs-lookup"><span data-stu-id="f96cc-140">System.String</span></span>

## <span data-ttu-id="f96cc-141">출력</span><span class="sxs-lookup"><span data-stu-id="f96cc-141">OUTPUTS</span></span>

### <span data-ttu-id="f96cc-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f96cc-142">System.Boolean</span></span>

## <span data-ttu-id="f96cc-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f96cc-143">NOTES</span></span>

## <span data-ttu-id="f96cc-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f96cc-144">RELATED LINKS</span></span>
