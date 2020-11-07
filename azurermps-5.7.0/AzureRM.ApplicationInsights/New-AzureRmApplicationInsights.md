---
external help file: Microsoft.Azure.Commands.ApplicationInsights.dll-Help.xml
Module Name: AzureRM.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.applicationinsights/new-azurermapplicationinsights
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ApplicationInsights/Commands.ApplicationInsights/help/New-AzureRmApplicationInsights.md
ms.openlocfilehash: 23c79f4ceed4e6b9dc537cb6e04fb602fd7a4bbf
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702876"
---
# <span data-ttu-id="a1794-101">New-AzureRmApplicationInsights</span><span class="sxs-lookup"><span data-stu-id="a1794-101">New-AzureRmApplicationInsights</span></span>

## <span data-ttu-id="a1794-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a1794-102">SYNOPSIS</span></span>
<span data-ttu-id="a1794-103">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="a1794-103">Create a new application insights resource</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a1794-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a1794-104">SYNTAX</span></span>

```
New-AzureRmApplicationInsights [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-Kind <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="a1794-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a1794-105">DESCRIPTION</span></span>
<span data-ttu-id="a1794-106">새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="a1794-106">Create a new application insights resource</span></span>

## <span data-ttu-id="a1794-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a1794-107">EXAMPLES</span></span>

### <span data-ttu-id="a1794-108">예제 1 새 application insights 리소스 만들기</span><span class="sxs-lookup"><span data-stu-id="a1794-108">Example 1 Create a new application insights resource</span></span>
```
PS C:\>  New-AzureRmApplicationInsights -Kind java -ResourceGroupName testgroup -Name test1027 -location eastus
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

<span data-ttu-id="a1794-109">"Java" 라는 종류의 리소스 그룹 "testgroup"에 "test" 라고 하는 새 application insights 리소스를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-109">Add a new application insights resource named as "test" in resource group "testgroup" with kind "java".</span></span>

## <span data-ttu-id="a1794-110">변수</span><span class="sxs-lookup"><span data-stu-id="a1794-110">PARAMETERS</span></span>

### <span data-ttu-id="a1794-111">-확인</span><span class="sxs-lookup"><span data-stu-id="a1794-111">-Confirm</span></span>
<span data-ttu-id="a1794-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-112">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a1794-113">-DefaultProfile</span></span>
<span data-ttu-id="a1794-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-115">-종류</span><span class="sxs-lookup"><span data-stu-id="a1794-115">-Kind</span></span>
<span data-ttu-id="a1794-116">응용 프로그램 종류</span><span class="sxs-lookup"><span data-stu-id="a1794-116">Application kind.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationKind
Accepted values: web, other, Node.js, java

Required: False
Position: Named
Default value: web
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-117">-위치</span><span class="sxs-lookup"><span data-stu-id="a1794-117">-Location</span></span>
<span data-ttu-id="a1794-118">Application Insights 리소스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-118">Application Insights Resource Location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-119">-이름</span><span class="sxs-lookup"><span data-stu-id="a1794-119">-Name</span></span>
<span data-ttu-id="a1794-120">Application Insights 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-120">Application Insights Resource Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a1794-121">-ResourceGroupName</span></span>
<span data-ttu-id="a1794-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-122">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-123">태그</span><span class="sxs-lookup"><span data-stu-id="a1794-123">-Tag</span></span>
<span data-ttu-id="a1794-124">구성 요소 태그.</span><span class="sxs-lookup"><span data-stu-id="a1794-124">Component Tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a1794-125">-WhatIf</span></span>
<span data-ttu-id="a1794-126">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-126">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a1794-127">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a1794-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a1794-128">CommonParameters</span></span>
<span data-ttu-id="a1794-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a1794-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a1794-130">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a1794-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a1794-131">입력</span><span class="sxs-lookup"><span data-stu-id="a1794-131">INPUTS</span></span>

### <span data-ttu-id="a1794-132">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a1794-132">System.String</span></span>

## <span data-ttu-id="a1794-133">출력</span><span class="sxs-lookup"><span data-stu-id="a1794-133">OUTPUTS</span></span>

### <span data-ttu-id="a1794-134">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="a1794-134">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

## <span data-ttu-id="a1794-135">상속자</span><span class="sxs-lookup"><span data-stu-id="a1794-135">NOTES</span></span>

## <span data-ttu-id="a1794-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a1794-136">RELATED LINKS</span></span>

