---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightscontinuousexport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsContinuousExport.md
ms.openlocfilehash: b2ada8c4a58b38eee9ab235bbcd88429934ac00c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956075"
---
# <span data-ttu-id="7b939-101">Remove-AzApplicationInsightsContinuousExport</span><span class="sxs-lookup"><span data-stu-id="7b939-101">Remove-AzApplicationInsightsContinuousExport</span></span>

## <span data-ttu-id="7b939-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b939-102">SYNOPSIS</span></span>
<span data-ttu-id="7b939-103">애플리케이션 인사이트 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="7b939-103">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7b939-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b939-104">SYNTAX</span></span>

### <span data-ttu-id="7b939-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7b939-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceGroupName] <String> [-Name] <String>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b939-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b939-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ExportId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="7b939-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7b939-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsContinuousExport [-ResourceId] <String> [-ExportId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b939-108">설명</span><span class="sxs-lookup"><span data-stu-id="7b939-108">DESCRIPTION</span></span>
<span data-ttu-id="7b939-109">애플리케이션 인사이트 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="7b939-109">Remove a continuous export configuration in an application insights resource</span></span>

## <span data-ttu-id="7b939-110">예제</span><span class="sxs-lookup"><span data-stu-id="7b939-110">EXAMPLES</span></span>

### <span data-ttu-id="7b939-111">예제 1 애플리케이션 인사이트 리소스에서 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="7b939-111">Example 1 Remove a continuous export configuration in an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsightsContinuousExport -ResourceGroupName "testgroup" -Name "test" -ExportId "uGOoki0jQsyEs3IdQ83Q4QsNr4=" -PassThru
True
```

<span data-ttu-id="7b939-112">리소스 그룹 "testgroup"에서 "test"라는 리소스에 대한 내보내기 ID "uGOoki0jQsyEs3IdQ83QsNr4="를 사용하여 애플리케이션 인사이트 연속 내보내기 구성 제거</span><span class="sxs-lookup"><span data-stu-id="7b939-112">Remove application insights continuous export configuration with export id "uGOoki0jQsyEs3IdQ83Q4QsNr4=" for resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="7b939-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b939-113">PARAMETERS</span></span>

### <span data-ttu-id="7b939-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7b939-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="7b939-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="7b939-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b939-116">-DefaultProfile</span></span>
<span data-ttu-id="7b939-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7b939-118">-ExportId</span><span class="sxs-lookup"><span data-stu-id="7b939-118">-ExportId</span></span>
<span data-ttu-id="7b939-119">Application Insights 연속 내보내기 ID.</span><span class="sxs-lookup"><span data-stu-id="7b939-119">Application Insights Continuous Export ID.</span></span>

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

### <span data-ttu-id="7b939-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7b939-120">-Name</span></span>
<span data-ttu-id="7b939-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="7b939-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b939-122">-PassThru</span></span>
<span data-ttu-id="7b939-123">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="7b939-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-124">This parameter is optional.</span></span> <span data-ttu-id="7b939-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-125">Default value is false.</span></span>

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

### <span data-ttu-id="7b939-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b939-126">-ResourceGroupName</span></span>
<span data-ttu-id="7b939-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="7b939-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7b939-128">-ResourceId</span></span>
<span data-ttu-id="7b939-129">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="7b939-130">-확인</span><span class="sxs-lookup"><span data-stu-id="7b939-130">-Confirm</span></span>
<span data-ttu-id="7b939-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b939-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b939-132">-WhatIf</span></span>
<span data-ttu-id="7b939-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b939-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b939-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b939-135">CommonParameters</span></span>
<span data-ttu-id="7b939-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b939-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b939-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b939-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b939-138">입력</span><span class="sxs-lookup"><span data-stu-id="7b939-138">INPUTS</span></span>

### <span data-ttu-id="7b939-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="7b939-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="7b939-140">System.String</span><span class="sxs-lookup"><span data-stu-id="7b939-140">System.String</span></span>

## <span data-ttu-id="7b939-141">출력</span><span class="sxs-lookup"><span data-stu-id="7b939-141">OUTPUTS</span></span>

### <span data-ttu-id="7b939-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b939-142">System.Boolean</span></span>

## <span data-ttu-id="7b939-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b939-143">NOTES</span></span>

## <span data-ttu-id="7b939-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b939-144">RELATED LINKS</span></span>
