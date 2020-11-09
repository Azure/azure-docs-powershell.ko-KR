---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/update-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Update-AzApplicationInsights.md
ms.openlocfilehash: f34868c31a99e67596d244a1f69224db5c25349a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308612"
---
# <span data-ttu-id="084b2-101">Update-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="084b2-101">Update-AzApplicationInsights</span></span>

## <span data-ttu-id="084b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="084b2-102">SYNOPSIS</span></span>
<span data-ttu-id="084b2-103">기존 application insights 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="084b2-103">update an existing application insights resource</span></span>

## <span data-ttu-id="084b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="084b2-104">SYNTAX</span></span>

```
Update-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Tag <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [[-RetentionInDays] <Int32>]
 [[-PublicNetworkAccessForIngestion] <String>] [[-PublicNetworkAccessForQuery] <String>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="084b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="084b2-105">DESCRIPTION</span></span>
<span data-ttu-id="084b2-106">기존 application insights 리소스 업데이트</span><span class="sxs-lookup"><span data-stu-id="084b2-106">update an existing application insights resource</span></span>

## <span data-ttu-id="084b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="084b2-107">EXAMPLES</span></span>

### <span data-ttu-id="084b2-108">예제 1 업데이트 application insights 구성 요소</span><span class="sxs-lookup"><span data-stu-id="084b2-108">Example 1 Update application insights component</span></span>
```powershell
Update-AzApplicationInsights -ResourceGroupName "rgName" -Name "aiName" -PublicNetworkAccessForIngestion "Disabled" -PublicNetworkAccessForQuery "Disabled"
```

<span data-ttu-id="084b2-109">application insights 구성 요소 업데이트 "aiName" PublicNetworkAccessForIngestion/Publicnetworkaccessforingestion를 "사용 안 함"으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-109">update application insights component "aiName" PublicNetworkAccessForIngestion/PublicNetworkAccessForQuery both to "Disabled"</span></span>

## <span data-ttu-id="084b2-110">변수</span><span class="sxs-lookup"><span data-stu-id="084b2-110">PARAMETERS</span></span>

### <span data-ttu-id="084b2-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="084b2-111">-DefaultProfile</span></span>
<span data-ttu-id="084b2-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="084b2-113">-이름</span><span class="sxs-lookup"><span data-stu-id="084b2-113">-Name</span></span>
<span data-ttu-id="084b2-114">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-114">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="084b2-115">-PublicNetworkAccessForIngestion</span><span class="sxs-lookup"><span data-stu-id="084b2-115">-PublicNetworkAccessForIngestion</span></span>
<span data-ttu-id="084b2-116">Application Insights 수집에 액세스 하는 데 사용 되는 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-116">The network access type for accessing Application Insights ingestion.</span></span>
<span data-ttu-id="084b2-117">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-117">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="084b2-118">-PublicNetworkAccessForQuery</span><span class="sxs-lookup"><span data-stu-id="084b2-118">-PublicNetworkAccessForQuery</span></span>
<span data-ttu-id="084b2-119">Application Insights 쿼리에 액세스 하는 데 사용할 네트워크 액세스 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-119">The network access type for accessing Application Insights query.</span></span>
<span data-ttu-id="084b2-120">값은 ' Enabled ' 또는 ' Disabled ' 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-120">Value should be 'Enabled' or 'Disabled'</span></span>

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

### <span data-ttu-id="084b2-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="084b2-121">-ResourceGroupName</span></span>
<span data-ttu-id="084b2-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-122">Resource Group Name.</span></span>

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

### <span data-ttu-id="084b2-123">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="084b2-123">-RetentionInDays</span></span>
<span data-ttu-id="084b2-124">보존은 기본적으로 90 일입니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-124">Retention In Days, 90 by default.</span></span>

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

### <span data-ttu-id="084b2-125">태그</span><span class="sxs-lookup"><span data-stu-id="084b2-125">-Tag</span></span>
<span data-ttu-id="084b2-126">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="084b2-126">Component Tags.</span></span>

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

### <span data-ttu-id="084b2-127">-확인</span><span class="sxs-lookup"><span data-stu-id="084b2-127">-Confirm</span></span>
<span data-ttu-id="084b2-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="084b2-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="084b2-129">-WhatIf</span></span>
<span data-ttu-id="084b2-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="084b2-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="084b2-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="084b2-132">CommonParameters</span></span>
<span data-ttu-id="084b2-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="084b2-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="084b2-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="084b2-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="084b2-135">입력</span><span class="sxs-lookup"><span data-stu-id="084b2-135">INPUTS</span></span>

### <span data-ttu-id="084b2-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="084b2-136">System.String</span></span>

## <span data-ttu-id="084b2-137">출력</span><span class="sxs-lookup"><span data-stu-id="084b2-137">OUTPUTS</span></span>

### <span data-ttu-id="084b2-138">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="084b2-138">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="084b2-139">상속자</span><span class="sxs-lookup"><span data-stu-id="084b2-139">NOTES</span></span>

## <span data-ttu-id="084b2-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="084b2-140">RELATED LINKS</span></span>
