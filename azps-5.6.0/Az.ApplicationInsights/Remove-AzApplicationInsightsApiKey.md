---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 95f99f629fd32333e06c6194fcaf51837224f4a6
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101956091"
---
# <span data-ttu-id="76080-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="76080-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="76080-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76080-102">SYNOPSIS</span></span>
<span data-ttu-id="76080-103">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 제거</span><span class="sxs-lookup"><span data-stu-id="76080-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="76080-104">구문</span><span class="sxs-lookup"><span data-stu-id="76080-104">SYNTAX</span></span>

### <span data-ttu-id="76080-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="76080-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76080-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="76080-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="76080-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="76080-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76080-108">설명</span><span class="sxs-lookup"><span data-stu-id="76080-108">DESCRIPTION</span></span>
<span data-ttu-id="76080-109">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 제거</span><span class="sxs-lookup"><span data-stu-id="76080-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="76080-110">예제</span><span class="sxs-lookup"><span data-stu-id="76080-110">EXAMPLES</span></span>

### <span data-ttu-id="76080-111">예제 1 애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 제거</span><span class="sxs-lookup"><span data-stu-id="76080-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Remove-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="76080-112">리소스 그룹 "testGroup"의 리소스 "테스트"에 대한 ID가 "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867"인 특정 애플리케이션 인사이트 api 키를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="76080-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="76080-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="76080-113">PARAMETERS</span></span>

### <span data-ttu-id="76080-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="76080-114">-ApiKeyId</span></span>
<span data-ttu-id="76080-115">Application Insights API 키 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="76080-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="76080-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="76080-117">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="76080-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76080-118">-DefaultProfile</span></span>
<span data-ttu-id="76080-119">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="76080-120">-Name</span><span class="sxs-lookup"><span data-stu-id="76080-120">-Name</span></span>
<span data-ttu-id="76080-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="76080-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="76080-122">-PassThru</span></span>
<span data-ttu-id="76080-123">지정한 경우 작업이 성공할 경우 true를 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="76080-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="76080-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-124">This parameter is optional.</span></span> <span data-ttu-id="76080-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-125">Default value is false.</span></span>

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

### <span data-ttu-id="76080-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76080-126">-ResourceGroupName</span></span>
<span data-ttu-id="76080-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="76080-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="76080-128">-ResourceId</span></span>
<span data-ttu-id="76080-129">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76080-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="76080-130">-확인</span><span class="sxs-lookup"><span data-stu-id="76080-130">-Confirm</span></span>
<span data-ttu-id="76080-131">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76080-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76080-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76080-132">-WhatIf</span></span>
<span data-ttu-id="76080-133">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="76080-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="76080-134">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76080-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76080-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76080-135">CommonParameters</span></span>
<span data-ttu-id="76080-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76080-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76080-137">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="76080-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76080-138">입력</span><span class="sxs-lookup"><span data-stu-id="76080-138">INPUTS</span></span>

### <span data-ttu-id="76080-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="76080-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="76080-140">System.String</span><span class="sxs-lookup"><span data-stu-id="76080-140">System.String</span></span>

## <span data-ttu-id="76080-141">출력</span><span class="sxs-lookup"><span data-stu-id="76080-141">OUTPUTS</span></span>

### <span data-ttu-id="76080-142">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="76080-142">System.Boolean</span></span>

## <span data-ttu-id="76080-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76080-143">NOTES</span></span>

## <span data-ttu-id="76080-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76080-144">RELATED LINKS</span></span>
