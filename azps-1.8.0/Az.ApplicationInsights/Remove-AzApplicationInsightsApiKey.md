---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2dde5a98f244be794eedb744623137b674a38548
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93701657"
---
# <span data-ttu-id="c2697-101">Remove-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c2697-101">Remove-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c2697-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2697-102">SYNOPSIS</span></span>
<span data-ttu-id="c2697-103">Application insights 리소스에 대 한 application insights api 키 제거</span><span class="sxs-lookup"><span data-stu-id="c2697-103">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c2697-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2697-104">SYNTAX</span></span>

### <span data-ttu-id="c2697-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2697-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-ApiKeyId] <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2697-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2697-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-ApiKeyId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c2697-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c2697-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsightsApiKey [-ResourceId] <String> [-ApiKeyId] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2697-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c2697-108">DESCRIPTION</span></span>
<span data-ttu-id="c2697-109">Application insights 리소스에 대 한 application insights api 키 제거</span><span class="sxs-lookup"><span data-stu-id="c2697-109">Remove an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c2697-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c2697-110">EXAMPLES</span></span>

### <span data-ttu-id="c2697-111">예제 1 application insights 리소스에 대 한 application insights api 키 제거</span><span class="sxs-lookup"><span data-stu-id="c2697-111">Example 1 Remove an application insights api key for an application insights resource</span></span>
```
Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId dd173f38-4fd1-4c75-8af5-9
9c29aa0f867 -PassThru
True
```

<span data-ttu-id="c2697-112">리소스 그룹 "testGroup"에서 "리소스" 테스트 "의 id 인 특정 application insights api 키를 제거 합니다." dd173f38-4fd1-4c75-8af5-9 9c29aa0f867 ".</span><span class="sxs-lookup"><span data-stu-id="c2697-112">Remove specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c2697-113">변수</span><span class="sxs-lookup"><span data-stu-id="c2697-113">PARAMETERS</span></span>

### <span data-ttu-id="c2697-114">-ApiKeyId</span><span class="sxs-lookup"><span data-stu-id="c2697-114">-ApiKeyId</span></span>
<span data-ttu-id="c2697-115">Application Insights API 키 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-115">Application Insights API Key ID.</span></span>

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

### <span data-ttu-id="c2697-116">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c2697-116">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c2697-117">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="c2697-117">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c2697-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2697-118">-DefaultProfile</span></span>
<span data-ttu-id="c2697-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2697-120">-이름</span><span class="sxs-lookup"><span data-stu-id="c2697-120">-Name</span></span>
<span data-ttu-id="c2697-121">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-121">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="c2697-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c2697-122">-PassThru</span></span>
<span data-ttu-id="c2697-123">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-123">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="c2697-124">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-124">This parameter is optional.</span></span> <span data-ttu-id="c2697-125">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-125">Default value is false.</span></span>

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

### <span data-ttu-id="c2697-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2697-126">-ResourceGroupName</span></span>
<span data-ttu-id="c2697-127">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-127">Resource Group Name.</span></span>

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

### <span data-ttu-id="c2697-128">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c2697-128">-ResourceId</span></span>
<span data-ttu-id="c2697-129">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-129">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c2697-130">-확인</span><span class="sxs-lookup"><span data-stu-id="c2697-130">-Confirm</span></span>
<span data-ttu-id="c2697-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2697-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2697-132">-WhatIf</span></span>
<span data-ttu-id="c2697-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2697-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2697-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2697-135">CommonParameters</span></span>
<span data-ttu-id="c2697-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2697-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2697-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2697-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2697-138">입력</span><span class="sxs-lookup"><span data-stu-id="c2697-138">INPUTS</span></span>

### <span data-ttu-id="c2697-139">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c2697-139">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c2697-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2697-140">System.String</span></span>

## <span data-ttu-id="c2697-141">출력</span><span class="sxs-lookup"><span data-stu-id="c2697-141">OUTPUTS</span></span>

### <span data-ttu-id="c2697-142">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c2697-142">System.Boolean</span></span>

## <span data-ttu-id="c2697-143">상속자</span><span class="sxs-lookup"><span data-stu-id="c2697-143">NOTES</span></span>

## <span data-ttu-id="c2697-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2697-144">RELATED LINKS</span></span>