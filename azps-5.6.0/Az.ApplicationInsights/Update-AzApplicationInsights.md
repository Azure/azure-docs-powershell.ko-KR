---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: ac5e8bbc65a8435042d9f525cd1a3d35fa050398
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102014320"
---
# <span data-ttu-id="3607d-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="3607d-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="3607d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3607d-102">SYNOPSIS</span></span>
<span data-ttu-id="3607d-103">기존 애플리케이션 인사이트 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="3607d-103">update an existing application insights resource</span></span>

## <span data-ttu-id="3607d-104">구문</span><span class="sxs-lookup"><span data-stu-id="3607d-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3607d-105">설명</span><span class="sxs-lookup"><span data-stu-id="3607d-105">DESCRIPTION</span></span>
<span data-ttu-id="3607d-106">기존 애플리케이션 인사이트 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="3607d-106">update an existing application insights resource</span></span>

## <span data-ttu-id="3607d-107">예제</span><span class="sxs-lookup"><span data-stu-id="3607d-107">EXAMPLES</span></span>

### <span data-ttu-id="3607d-108">예제 1 애플리케이션 인사이트 구성 요소 업데이트</span><span class="sxs-lookup"><span data-stu-id="3607d-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="3607d-109">애플리케이션 인사이트 구성 요소 "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery를 "사용 안 하여"로 업데이트</span><span class="sxs-lookup"><span data-stu-id="3607d-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="3607d-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3607d-110">PARAMETERS</span></span>

### <span data-ttu-id="3607d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3607d-111">-DefaultProfile</span></span>
<span data-ttu-id="3607d-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3607d-113">-Name</span><span class="sxs-lookup"><span data-stu-id="3607d-113">-Name</span></span>
<span data-ttu-id="3607d-114">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="3607d-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="3607d-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="3607d-116">Application Insights 분석에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="3607d-117">값은 '사용' 또는 '사용 안 되어' 입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="3607d-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="3607d-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="3607d-119">Application Insights 쿼리에 액세스하기 위한 네트워크 액세스 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="3607d-120">값은 '사용' 또는 '사용 안 되어' 입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="3607d-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3607d-121">-ResourceGroupName</span></span>
<span data-ttu-id="3607d-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="3607d-123">-RetentionInDays</span><span class="sxs-lookup"><span data-stu-id="3607d-123">-RetentionInDays</span></span>
<span data-ttu-id="3607d-124">보존 기간은 기본적으로 90일입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="3607d-125">-Tag</span><span class="sxs-lookup"><span data-stu-id="3607d-125">-Tag</span></span>
<span data-ttu-id="3607d-126">구성 요소 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-126">Component Tags.</span></span>

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

### <span data-ttu-id="3607d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="3607d-127">-Confirm</span></span>
<span data-ttu-id="3607d-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3607d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3607d-129">-WhatIf</span></span>
<span data-ttu-id="3607d-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3607d-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3607d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3607d-132">CommonParameters</span></span>
<span data-ttu-id="3607d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3607d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3607d-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3607d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3607d-135">입력</span><span class="sxs-lookup"><span data-stu-id="3607d-135">INPUTS</span></span>

### <span data-ttu-id="3607d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="3607d-136">System.String</span></span>

## <span data-ttu-id="3607d-137">출력</span><span class="sxs-lookup"><span data-stu-id="3607d-137">OUTPUTS</span></span>

### <span data-ttu-id="3607d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="3607d-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="3607d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3607d-139">NOTES</span></span>

## <span data-ttu-id="3607d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3607d-140">RELATED LINKS</span></span>
