---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 53ebb6d1a7bcfc35dafb09c377b2a4a023e327d8
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182249"
---
# <span data-ttu-id="9c591-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="9c591-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="9c591-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c591-102">SYNOPSIS</span></span>
<span data-ttu-id="9c591-103">Application Insights 리소스에 대한 Application Insights API 키 제거</span><span class="sxs-lookup"><span data-stu-id="9c591-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="9c591-104">구문</span><span class="sxs-lookup"><span data-stu-id="9c591-104">SYNTAX</span></span>

### <span data-ttu-id="9c591-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9c591-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9c591-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c591-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9c591-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9c591-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c591-108">설명</span><span class="sxs-lookup"><span data-stu-id="9c591-108">DESCRIPTION</span></span>
<span data-ttu-id="9c591-109">Application Insights 리소스에 대한 Application Insights API 키 제거</span><span class="sxs-lookup"><span data-stu-id="9c591-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="9c591-110">예제</span><span class="sxs-lookup"><span data-stu-id="9c591-110">EXAMPLES</span></span>

### <span data-ttu-id="9c591-111">예제 1 Application Insights 리소스에 대한 Application Insights API 키 제거</span><span class="sxs-lookup"><span data-stu-id="9c591-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="9c591-112">리소스 그룹 "testGroup"에서 리소스 "테스트"에 대해 ID가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867"인 특정 Application Insights API 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="9c591-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9c591-113">PARAMETERS</span></span>

### <span data-ttu-id="9c591-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="9c591-114">-ApiKeyId</span></span>
<span data-ttu-id="9c591-115">Application Insights API 키 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="9c591-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9c591-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="9c591-117">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="9c591-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c591-118">-DefaultProfile</span></span>
<span data-ttu-id="9c591-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c591-120">-Name</span><span class="sxs-lookup"><span data-stu-id="9c591-120">-Name</span></span>
<span data-ttu-id="9c591-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="9c591-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9c591-122">-PassThru</span></span>
<span data-ttu-id="9c591-123">지정된 경우 작업이 성공하는 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="9c591-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-124">This parameter is optional.</span></span> <span data-ttu-id="9c591-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-125">Default value is false.</span></span>

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

### <span data-ttu-id="9c591-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c591-126">-ResourceGroupName</span></span>
<span data-ttu-id="9c591-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="9c591-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9c591-128">-ResourceId</span></span>
<span data-ttu-id="9c591-129">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="9c591-130">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9c591-130">-Confirm</span></span>
<span data-ttu-id="9c591-131">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c591-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c591-132">-WhatIf</span></span>
<span data-ttu-id="9c591-133">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9c591-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c591-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c591-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c591-135">CommonParameters</span></span>
<span data-ttu-id="9c591-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9c591-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c591-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="9c591-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c591-138">입력</span><span class="sxs-lookup"><span data-stu-id="9c591-138">INPUTS</span></span>

### <span data-ttu-id="9c591-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="9c591-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="9c591-140">System.String</span><span class="sxs-lookup"><span data-stu-id="9c591-140">System.String</span></span>

## <span data-ttu-id="9c591-141">출력</span><span class="sxs-lookup"><span data-stu-id="9c591-141">OUTPUTS</span></span>

### <span data-ttu-id="9c591-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="9c591-142">System.Boolean</span></span>

## <span data-ttu-id="9c591-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9c591-143">NOTES</span></span>

## <span data-ttu-id="9c591-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c591-144">RELATED LINKS</span></span>
