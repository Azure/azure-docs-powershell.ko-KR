---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/remove-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Remove-AzApplicationInsights.md
ms.openlocfilehash: d9aa737a34e106fc8514c0e9bbbcfb70b73f015a
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044143"
---
# <span data-ttu-id="22d8f-101">Remove-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="22d8f-101">Remove-AzApplicationInsights</span></span>

## <span data-ttu-id="22d8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22d8f-102">SYNOPSIS</span></span>
<span data-ttu-id="22d8f-103">Application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="22d8f-103">Remove an application insights resource</span></span>

## <span data-ttu-id="22d8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="22d8f-104">SYNTAX</span></span>

### <span data-ttu-id="22d8f-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="22d8f-105">ComponentNameParameterSet (Default)</span></span>
```
Remove-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d8f-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d8f-106">ComponentObjectParameterSet</span></span>
```
Remove-AzApplicationInsights [-ApplicationInsightsComponent] <PSApplicationInsightsComponent> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="22d8f-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="22d8f-107">ResourceIdParameterSet</span></span>
```
Remove-AzApplicationInsights [-ResourceId] <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="22d8f-108">설명은</span><span class="sxs-lookup"><span data-stu-id="22d8f-108">DESCRIPTION</span></span>
<span data-ttu-id="22d8f-109">Application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="22d8f-109">Remove an application insights resource</span></span>

## <span data-ttu-id="22d8f-110">예제의</span><span class="sxs-lookup"><span data-stu-id="22d8f-110">EXAMPLES</span></span>

### <span data-ttu-id="22d8f-111">예제 1 application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="22d8f-111">Example 1 Remove an application insights resource</span></span>
```
PS C:\> Remove-AzApplicationInsights -ResourceGroupName "testgroup" -Name "test" -PassThru
True
```

<span data-ttu-id="22d8f-112">리소스 그룹 "testgroup"에서 "test" 라는 application insights 리소스 제거</span><span class="sxs-lookup"><span data-stu-id="22d8f-112">Remove an application insights resource named "test" in resource group "testgroup"</span></span>

## <span data-ttu-id="22d8f-113">변수</span><span class="sxs-lookup"><span data-stu-id="22d8f-113">PARAMETERS</span></span>

### <span data-ttu-id="22d8f-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="22d8f-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="22d8f-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="22d8f-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="22d8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22d8f-116">-DefaultProfile</span></span>
<span data-ttu-id="22d8f-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="22d8f-118">-이름</span><span class="sxs-lookup"><span data-stu-id="22d8f-118">-Name</span></span>
<span data-ttu-id="22d8f-119">Application Insights 구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-119">Application Insights Component Name.</span></span>

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

### <span data-ttu-id="22d8f-120">-PassThru</span><span class="sxs-lookup"><span data-stu-id="22d8f-120">-PassThru</span></span>
<span data-ttu-id="22d8f-121">지정 된 경우 대/소문자 구분 작업이 성공한 경우 true를 씁니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-121">If specified will write true in case operation succeeds.</span></span> <span data-ttu-id="22d8f-122">이 매개 변수는 선택 사항입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-122">This parameter is optional.</span></span> <span data-ttu-id="22d8f-123">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-123">Default value is false.</span></span>

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

### <span data-ttu-id="22d8f-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="22d8f-124">-ResourceGroupName</span></span>
<span data-ttu-id="22d8f-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="22d8f-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="22d8f-126">-ResourceId</span></span>
<span data-ttu-id="22d8f-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="22d8f-128">-확인</span><span class="sxs-lookup"><span data-stu-id="22d8f-128">-Confirm</span></span>
<span data-ttu-id="22d8f-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22d8f-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22d8f-130">-WhatIf</span></span>
<span data-ttu-id="22d8f-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22d8f-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22d8f-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22d8f-133">CommonParameters</span></span>
<span data-ttu-id="22d8f-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="22d8f-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22d8f-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="22d8f-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22d8f-136">입력</span><span class="sxs-lookup"><span data-stu-id="22d8f-136">INPUTS</span></span>

### <span data-ttu-id="22d8f-137">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="22d8f-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="22d8f-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="22d8f-138">System.String</span></span>

## <span data-ttu-id="22d8f-139">출력</span><span class="sxs-lookup"><span data-stu-id="22d8f-139">OUTPUTS</span></span>

### <span data-ttu-id="22d8f-140">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="22d8f-140">System.Boolean</span></span>

## <span data-ttu-id="22d8f-141">상속자</span><span class="sxs-lookup"><span data-stu-id="22d8f-141">NOTES</span></span>

## <span data-ttu-id="22d8f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22d8f-142">RELATED LINKS</span></span>
