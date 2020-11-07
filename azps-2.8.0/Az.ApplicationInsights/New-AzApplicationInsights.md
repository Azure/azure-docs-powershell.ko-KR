---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsights.md
ms.openlocfilehash: d04b2e54e10a88edd3273ecd96697ab993e97c98
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697904"
---
# <span data-ttu-id="c992a-101">New-AzApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="c992a-101">New-AzApplicationInsights</span></span>

## <span data-ttu-id="c992a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c992a-102">SYNOPSIS</span></span>
<span data-ttu-id="c992a-103">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c992a-103">Create a new application insights resource</span></span>

## <span data-ttu-id="c992a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c992a-104">SYNTAX</span></span>

```
New-AzApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String> [-Kind <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c992a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c992a-105">DESCRIPTION</span></span>
<span data-ttu-id="c992a-106">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c992a-106">Create a new application insights resource</span></span>

## <span data-ttu-id="c992a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c992a-107">EXAMPLES</span></span>

### <span data-ttu-id="c992a-108">예제 1 새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="c992a-108">Example 1 Create a new application insights resource</span></span>
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
```

<span data-ttu-id="c992a-109">"Java" 라는 종류의 리소스 그룹 "testgroup"에 "test" 라고 하는 새 application insights 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="c992a-110">변수</span><span class="sxs-lookup"><span data-stu-id="c992a-110">PARAMETERS</span></span>

### <span data-ttu-id="c992a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c992a-111">-DefaultProfile</span></span>
<span data-ttu-id="c992a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c992a-113">-종류</span><span class="sxs-lookup"><span data-stu-id="c992a-113">-Kind</span></span>
<span data-ttu-id="c992a-114">응용 프로그램 종류</span><span class="sxs-lookup"><span data-stu-id="c992a-114">Application kind.</span></span>

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

### <span data-ttu-id="c992a-115">-위치</span><span class="sxs-lookup"><span data-stu-id="c992a-115">-Location</span></span>
<span data-ttu-id="c992a-116">Application Insights 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-116">Application Insights Resource Location.</span></span>

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

### <span data-ttu-id="c992a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="c992a-117">-Name</span></span>
<span data-ttu-id="c992a-118">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-118">Application Insights Resource Name.</span></span>

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

### <span data-ttu-id="c992a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c992a-119">-ResourceGroupName</span></span>
<span data-ttu-id="c992a-120">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-120">Resource Group Name.</span></span>

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

### <span data-ttu-id="c992a-121">태그</span><span class="sxs-lookup"><span data-stu-id="c992a-121">-Tag</span></span>
<span data-ttu-id="c992a-122">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="c992a-122">Component Tags.</span></span>

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

### <span data-ttu-id="c992a-123">-확인</span><span class="sxs-lookup"><span data-stu-id="c992a-123">-Confirm</span></span>
<span data-ttu-id="c992a-124">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c992a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c992a-125">-WhatIf</span></span>
<span data-ttu-id="c992a-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c992a-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c992a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c992a-128">CommonParameters</span></span>
<span data-ttu-id="c992a-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c992a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c992a-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c992a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c992a-131">입력</span><span class="sxs-lookup"><span data-stu-id="c992a-131">INPUTS</span></span>

### <span data-ttu-id="c992a-132">않아야</span><span class="sxs-lookup"><span data-stu-id="c992a-132">None</span></span>

## <span data-ttu-id="c992a-133">출력</span><span class="sxs-lookup"><span data-stu-id="c992a-133">OUTPUTS</span></span>

### <span data-ttu-id="c992a-134">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="c992a-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="c992a-135">상속자</span><span class="sxs-lookup"><span data-stu-id="c992a-135">NOTES</span></span>

## <span data-ttu-id="c992a-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c992a-136">RELATED LINKS</span></span>
