---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182284"
---
# <span data-ttu-id="c6d26-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c6d26-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="c6d26-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6d26-102">SYNOPSIS</span></span>
<span data-ttu-id="c6d26-103">새 Application Insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c6d26-103">Create a new application insights resource</span></span>

## <span data-ttu-id="c6d26-104">구문</span><span class="sxs-lookup"><span data-stu-id="c6d26-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c6d26-105">설명</span><span class="sxs-lookup"><span data-stu-id="c6d26-105">DESCRIPTION</span></span>
<span data-ttu-id="c6d26-106">새 Application Insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c6d26-106">Create a new application insights resource</span></span>

## <span data-ttu-id="c6d26-107">예제</span><span class="sxs-lookup"><span data-stu-id="c6d26-107">EXAMPLES</span></span>

### <span data-ttu-id="c6d26-108">예제 1 새 Application Insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c6d26-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
Id                 : /subscriptions/{subid}/resourceGroups/testgroup/providers/microsoft.insights/components/test1027
ResourceGroupName  : testgroup
Name               : test1027
Kind               : web
Location           : eastus
Type               : microsoft.insights/components
AppId              : 8323fb13-32aa-46af-b467-8355cf4f8f98
ApplicationType    : web
Tags               : {}
CreationDate       : 10/27/2017 4:56:40 PM
FlowType           :
HockeyAppId        :
HockeyAppToken     :
InstrumentationKey : 083112ed-ed9b-464e-a9b0-8cf126fbfced
ProvisioningState  : Succeeded
RequestSource      : AzurePowerShell
SamplingPercentage :
TenantId           : {subid}
PublicNetworkAccessForIngestion : Enabled
PublicNetworkAccessForQuery     : Enabled
PrivateLinkScopedResources      :
```

<span data-ttu-id="c6d26-109">종류가 "java"인 리소스 그룹 "testgroup"에서 "test"로 명명된 새 Application Insights 리소스를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="c6d26-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c6d26-110">PARAMETERS</span></span>

### <span data-ttu-id="c6d26-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6d26-111">-DefaultProfile</span></span>
<span data-ttu-id="c6d26-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6d26-113">-Kind</span><span class="sxs-lookup"><span data-stu-id="c6d26-113">-Kind</span></span>
<span data-ttu-id="c6d26-114">애플리케이션 종류입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-114">Application kind.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-115">-Location</span><span class="sxs-lookup"><span data-stu-id="c6d26-115">-Location</span></span>
<span data-ttu-id="c6d26-116">Application Insights 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="c6d26-117">-Name</span><span class="sxs-lookup"><span data-stu-id="c6d26-117">-Name</span></span>
<span data-ttu-id="c6d26-118">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-118">Application Insights Resource Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="c6d26-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="c6d26-120">Application Insights에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="c6d26-121">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-121">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="c6d26-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="c6d26-123">Application Insights 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="c6d26-124">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-124">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6d26-125">-ResourceGroupName</span></span>
<span data-ttu-id="c6d26-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-126">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-127">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="c6d26-127">-RetentionInDays</span></span>
<span data-ttu-id="c6d26-128">보존 기간(일)은 기본적으로 90입니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-128">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="c6d26-129">-Tag</span></span>
<span data-ttu-id="c6d26-130">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="c6d26-130">Component Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6d26-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c6d26-131">-Confirm</span></span>
<span data-ttu-id="c6d26-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6d26-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6d26-133">-WhatIf</span></span>
<span data-ttu-id="c6d26-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c6d26-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c6d26-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6d26-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6d26-136">CommonParameters</span></span>
<span data-ttu-id="c6d26-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c6d26-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6d26-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c6d26-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6d26-139">입력</span><span class="sxs-lookup"><span data-stu-id="c6d26-139">INPUTS</span></span>

### <span data-ttu-id="c6d26-140">없음</span><span class="sxs-lookup"><span data-stu-id="c6d26-140">None</span></span>

## <span data-ttu-id="c6d26-141">출력</span><span class="sxs-lookup"><span data-stu-id="c6d26-141">OUTPUTS</span></span>

### <span data-ttu-id="c6d26-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6d26-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c6d26-143">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c6d26-143">NOTES</span></span>

## <span data-ttu-id="c6d26-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c6d26-144">RELATED LINKS</span></span>
