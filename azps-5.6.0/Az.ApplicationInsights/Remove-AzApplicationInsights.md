---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: 089561268233876976598f3cf74cd0a52fef8402
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102004848"
---
# <span data-ttu-id="6715b-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="6715b-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="6715b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6715b-102">SYNOPSIS</span></span>
<span data-ttu-id="6715b-103">애플리케이션 인사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="6715b-103">Remove an application insights resource</span></span>

## <span data-ttu-id="6715b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6715b-104">SYNTAX</span></span>

### <span data-ttu-id="6715b-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6715b-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6715b-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6715b-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6715b-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6715b-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6715b-108">설명</span><span class="sxs-lookup"><span data-stu-id="6715b-108">DESCRIPTION</span></span>
<span data-ttu-id="6715b-109">애플리케이션 인사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="6715b-109">Remove an application insights resource</span></span>

## <span data-ttu-id="6715b-110">예제</span><span class="sxs-lookup"><span data-stu-id="6715b-110">EXAMPLES</span></span>

### <span data-ttu-id="6715b-111">예제 1 애플리케이션 인사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="6715b-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="6715b-112">리소스 그룹 "testgroup"에서 "test"라는 애플리케이션 인사이트 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="6715b-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="6715b-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6715b-113">PARAMETERS</span></span>

### <span data-ttu-id="6715b-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6715b-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="6715b-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="6715b-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6715b-116">-DefaultProfile</span></span>
<span data-ttu-id="6715b-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6715b-118">-Name</span><span class="sxs-lookup"><span data-stu-id="6715b-118">-Name</span></span>
<span data-ttu-id="6715b-119">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="6715b-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6715b-120">-PassThru</span></span>
<span data-ttu-id="6715b-121">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="6715b-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-122">This parameter is optional.</span></span> <span data-ttu-id="6715b-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-123">Default value is false.</span></span>

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

### <span data-ttu-id="6715b-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6715b-124">-ResourceGroupName</span></span>
<span data-ttu-id="6715b-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="6715b-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6715b-126">-ResourceId</span></span>
<span data-ttu-id="6715b-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="6715b-128">-확인</span><span class="sxs-lookup"><span data-stu-id="6715b-128">-Confirm</span></span>
<span data-ttu-id="6715b-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6715b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6715b-130">-WhatIf</span></span>
<span data-ttu-id="6715b-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6715b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6715b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6715b-133">CommonParameters</span></span>
<span data-ttu-id="6715b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6715b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6715b-135">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="6715b-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6715b-136">입력</span><span class="sxs-lookup"><span data-stu-id="6715b-136">INPUTS</span></span>

### <span data-ttu-id="6715b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="6715b-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="6715b-138">System.String</span><span class="sxs-lookup"><span data-stu-id="6715b-138">System.String</span></span>

## <span data-ttu-id="6715b-139">출력</span><span class="sxs-lookup"><span data-stu-id="6715b-139">OUTPUTS</span></span>

### <span data-ttu-id="6715b-140">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="6715b-140">System.Boolean</span></span>

## <span data-ttu-id="6715b-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6715b-141">NOTES</span></span>

## <span data-ttu-id="6715b-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6715b-142">RELATED LINKS</span></span>
