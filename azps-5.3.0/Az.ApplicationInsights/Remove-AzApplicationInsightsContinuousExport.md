---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: 6138d3d454a23cdbdbaa67d7ee668c5ffa752b4a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381291"
---
# <span data-ttu-id="23e18-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="23e18-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="23e18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="23e18-102">SYNOPSIS</span></span>
<span data-ttu-id="23e18-103">Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="23e18-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="23e18-104">구문</span><span class="sxs-lookup"><span data-stu-id="23e18-104">SYNTAX</span></span>

### <span data-ttu-id="23e18-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="23e18-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23e18-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e18-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="23e18-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="23e18-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="23e18-108">설명</span><span class="sxs-lookup"><span data-stu-id="23e18-108">DESCRIPTION</span></span>
<span data-ttu-id="23e18-109">Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="23e18-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="23e18-110">예제</span><span class="sxs-lookup"><span data-stu-id="23e18-110">EXAMPLES</span></span>

### <span data-ttu-id="23e18-111">예제 1 Application Insights 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="23e18-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="23e18-112">리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 내보내기 ID "uGOoki0jQsyEs3IdQ83Q4QsNr4="를 사용하여 Application Insights 연속 내보내기 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="23e18-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="23e18-113">PARAMETERS</span></span>

### <span data-ttu-id="23e18-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="23e18-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="23e18-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="23e18-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="23e18-116">-DefaultProfile</span></span>
<span data-ttu-id="23e18-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="23e18-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="23e18-118">-ExportId</span></span>
<span data-ttu-id="23e18-119">Application Insights 연속 내보내기 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="23e18-120">-Name</span><span class="sxs-lookup"><span data-stu-id="23e18-120">-Name</span></span>
<span data-ttu-id="23e18-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="23e18-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="23e18-122">-PassThru</span></span>
<span data-ttu-id="23e18-123">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="23e18-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-124">This parameter is optional.</span></span> <span data-ttu-id="23e18-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-125">Default value is false.</span></span>

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

### <span data-ttu-id="23e18-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="23e18-126">-ResourceGroupName</span></span>
<span data-ttu-id="23e18-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="23e18-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="23e18-128">-ResourceId</span></span>
<span data-ttu-id="23e18-129">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="23e18-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="23e18-130">-Confirm</span></span>
<span data-ttu-id="23e18-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="23e18-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="23e18-132">-WhatIf</span></span>
<span data-ttu-id="23e18-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="23e18-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="23e18-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="23e18-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="23e18-135">CommonParameters</span></span>
<span data-ttu-id="23e18-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="23e18-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="23e18-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="23e18-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="23e18-138">입력</span><span class="sxs-lookup"><span data-stu-id="23e18-138">INPUTS</span></span>

### <span data-ttu-id="23e18-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="23e18-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="23e18-140">System.String</span><span class="sxs-lookup"><span data-stu-id="23e18-140">System.String</span></span>

## <span data-ttu-id="23e18-141">출력</span><span class="sxs-lookup"><span data-stu-id="23e18-141">OUTPUTS</span></span>

### <span data-ttu-id="23e18-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="23e18-142">System.Boolean</span></span>

## <span data-ttu-id="23e18-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="23e18-143">NOTES</span></span>

## <span data-ttu-id="23e18-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="23e18-144">RELATED LINKS</span></span>
