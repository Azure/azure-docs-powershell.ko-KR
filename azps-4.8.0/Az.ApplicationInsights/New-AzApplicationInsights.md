---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: 3faa93ced76fee1a1023011e1570c3819f6c2013
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94047974"
---
# <span data-ttu-id="45787-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="45787-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="45787-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45787-102">SYNOPSIS</span></span>
<span data-ttu-id="45787-103">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="45787-103">Create a new application insights resource</span></span>

## <span data-ttu-id="45787-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45787-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="45787-105">설명은</span><span class="sxs-lookup"><span data-stu-id="45787-105">DESCRIPTION</span></span>
<span data-ttu-id="45787-106">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="45787-106">Create a new application insights resource</span></span>

## <span data-ttu-id="45787-107">예제의</span><span class="sxs-lookup"><span data-stu-id="45787-107">EXAMPLES</span></span>

### <span data-ttu-id="45787-108">예제 1 새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="45787-108">Example 1 Create a new application insights resource</span></span>
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

<span data-ttu-id="45787-109">"Java" 종류의 리소스 그룹 "testgroup"에서 "test" 라는 새 application insights 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="45787-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java"</span></span>

## <span data-ttu-id="45787-110">변수</span><span class="sxs-lookup"><span data-stu-id="45787-110">PARAMETERS</span></span>

### <span data-ttu-id="45787-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45787-111">-DefaultProfile</span></span>
<span data-ttu-id="45787-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45787-113">-종류</span><span class="sxs-lookup"><span data-stu-id="45787-113">-Kind</span></span>
<span data-ttu-id="45787-114">응용 프로그램 종류</span><span class="sxs-lookup"><span data-stu-id="45787-114">Application kind.</span></span>

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

### <span data-ttu-id="45787-115">-위치</span><span class="sxs-lookup"><span data-stu-id="45787-115">-Location</span></span>
<span data-ttu-id="45787-116">Application Insights 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="45787-117">-이름</span><span class="sxs-lookup"><span data-stu-id="45787-117">-Name</span></span>
<span data-ttu-id="45787-118">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="45787-119">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="45787-119">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="45787-120">Application Insights 수집에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-120">The network access type for accessing Application Insights ingestion.</span></span> <span data-ttu-id="45787-121">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45787-121">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="45787-122">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="45787-122">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="45787-123">Application Insights 쿼리에 액세스 하는 데 사용할 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-123">The network access type for accessing Application Insights query.</span></span> <span data-ttu-id="45787-124">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="45787-124">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="45787-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="45787-125">-ResourceGroupName</span></span>
<span data-ttu-id="45787-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-126">Resource Group Name.</span></span>

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

### <span data-ttu-id="45787-127">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="45787-127">-RetentionInDays</span></span>
<span data-ttu-id="45787-128">보존은 기본적으로 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="45787-128">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="45787-129">태그</span><span class="sxs-lookup"><span data-stu-id="45787-129">-Tag</span></span>
<span data-ttu-id="45787-130">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="45787-130">Component Tags.</span></span>

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

### <span data-ttu-id="45787-131">-확인</span><span class="sxs-lookup"><span data-stu-id="45787-131">-Confirm</span></span>
<span data-ttu-id="45787-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="45787-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="45787-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="45787-133">-WhatIf</span></span>
<span data-ttu-id="45787-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="45787-134">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="45787-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="45787-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="45787-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45787-136">CommonParameters</span></span>
<span data-ttu-id="45787-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45787-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45787-138">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="45787-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45787-139">입력</span><span class="sxs-lookup"><span data-stu-id="45787-139">INPUTS</span></span>

### <span data-ttu-id="45787-140">않아야</span><span class="sxs-lookup"><span data-stu-id="45787-140">None</span></span>

## <span data-ttu-id="45787-141">출력</span><span class="sxs-lookup"><span data-stu-id="45787-141">OUTPUTS</span></span>

### <span data-ttu-id="45787-142">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="45787-142">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="45787-143">상속자</span><span class="sxs-lookup"><span data-stu-id="45787-143">NOTES</span></span>

## <span data-ttu-id="45787-144">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45787-144">RELATED LINKS</span></span>
