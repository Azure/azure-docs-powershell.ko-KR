---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381207"
---
# <span data-ttu-id="62023-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="62023-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="62023-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="62023-102">SYNOPSIS</span></span>
<span data-ttu-id="62023-103">기존 Application Insights 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="62023-103">update an existing application insights resource</span></span>

## <span data-ttu-id="62023-104">구문</span><span class="sxs-lookup"><span data-stu-id="62023-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="62023-105">설명</span><span class="sxs-lookup"><span data-stu-id="62023-105">DESCRIPTION</span></span>
<span data-ttu-id="62023-106">기존 Application Insights 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="62023-106">update an existing application insights resource</span></span>

## <span data-ttu-id="62023-107">예제</span><span class="sxs-lookup"><span data-stu-id="62023-107">EXAMPLES</span></span>

### <span data-ttu-id="62023-108">예제 1 Application Insights 구성 요소 업데이트</span><span class="sxs-lookup"><span data-stu-id="62023-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="62023-109">Application Insights 구성 요소 "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery를 "Disabled"로 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="62023-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="62023-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="62023-110">PARAMETERS</span></span>

### <span data-ttu-id="62023-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="62023-111">-DefaultProfile</span></span>
<span data-ttu-id="62023-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="62023-113">-Name</span><span class="sxs-lookup"><span data-stu-id="62023-113">-Name</span></span>
<span data-ttu-id="62023-114">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="62023-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="62023-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="62023-116">Application Insights에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="62023-117">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-117">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62023-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="62023-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="62023-119">Application Insights 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="62023-120">값은 'Enabled' 또는 'Disabled'입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-120">Value should be 'Enabled' or 'Disabled'</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62023-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="62023-121">-ResourceGroupName</span></span>
<span data-ttu-id="62023-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="62023-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="62023-123">-RetentionInDays</span></span>
<span data-ttu-id="62023-124">보존 기간(일)은 기본적으로 90입니다.</span><span class="sxs-lookup"><span data-stu-id="62023-124">Retention In Days, 90 by default.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="62023-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="62023-125">-Tag</span></span>
<span data-ttu-id="62023-126">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="62023-126">Component Tags.</span></span>

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

### <span data-ttu-id="62023-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="62023-127">-Confirm</span></span>
<span data-ttu-id="62023-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="62023-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="62023-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="62023-129">-WhatIf</span></span>
<span data-ttu-id="62023-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="62023-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="62023-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="62023-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="62023-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="62023-132">CommonParameters</span></span>
<span data-ttu-id="62023-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="62023-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="62023-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="62023-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="62023-135">입력</span><span class="sxs-lookup"><span data-stu-id="62023-135">INPUTS</span></span>

### <span data-ttu-id="62023-136">System.String</span><span class="sxs-lookup"><span data-stu-id="62023-136">System.String</span></span>

## <span data-ttu-id="62023-137">출력</span><span class="sxs-lookup"><span data-stu-id="62023-137">OUTPUTS</span></span>

### <span data-ttu-id="62023-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="62023-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="62023-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="62023-139">NOTES</span></span>

## <span data-ttu-id="62023-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="62023-140">RELATED LINKS</span></span>
