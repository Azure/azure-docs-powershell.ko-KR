---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 0137a349408234f31f0002849230e023c0544f68
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987079"
---
# <span data-ttu-id="c313c-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c313c-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c313c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c313c-102">SYNOPSIS</span></span>
<span data-ttu-id="c313c-103">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 만들기</span><span class="sxs-lookup"><span data-stu-id="c313c-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="c313c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c313c-104">SYNTAX</span></span>

### <span data-ttu-id="c313c-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="c313c-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c313c-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c313c-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c313c-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c313c-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c313c-108">설명</span><span class="sxs-lookup"><span data-stu-id="c313c-108">DESCRIPTION</span></span>
<span data-ttu-id="c313c-109">애플리케이션 인사이트 리소스에 대한 애플리케이션 인사이트 API 키 만들기</span><span class="sxs-lookup"><span data-stu-id="c313c-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c313c-110">예제</span><span class="sxs-lookup"><span data-stu-id="c313c-110">EXAMPLES</span></span>

### <span data-ttu-id="c313c-111">예제 1 애플리케이션 인사이트 리소스에 대한 새 Api 키 만들기</span><span class="sxs-lookup"><span data-stu-id="c313c-111">Example 1 Create a new Api Key for an application insights resource</span></span>
```
PS C:\>$apiKeyDescription="testapiKey"
PS C:\>$permissions = @("ReadTelemetry", "WriteAnnotations")
PS C:\>New-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test" -Description $apiKeyDescription -Permissions $permissions

ApiKey      : st0rfelw7m3oimfspozrtwgccxihiftbdwqjdfkg
CreatedDate : Fri, 27 Oct 2017 16:59:19 GMT
Id          : 1ed593f9-1561-4981-922d-6917971eecd3
Permissions : {ReadTelemetry, WriteAnnotations}
Description : testapiKey
```

<span data-ttu-id="c313c-112">리소스 그룹 "testGroup"의 리소스 "test"에 대한 "ReadTelemetry", "WriteAnnotations"를 사용하여 "testapiKey"로 애플리케이션 인사이트 api 키 설명을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c313c-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c313c-113">PARAMETERS</span></span>

### <span data-ttu-id="c313c-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c313c-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c313c-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="c313c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c313c-116">-DefaultProfile</span></span>
<span data-ttu-id="c313c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c313c-118">-Description</span><span class="sxs-lookup"><span data-stu-id="c313c-118">-Description</span></span>
<span data-ttu-id="c313c-119">이 API 키를 식별하는 데 도움이 되는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-119">Description to help identify this API key.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c313c-120">-Name</span><span class="sxs-lookup"><span data-stu-id="c313c-120">-Name</span></span>
<span data-ttu-id="c313c-121">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-121">Component Name.</span></span>

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

### <span data-ttu-id="c313c-122">-권한</span><span class="sxs-lookup"><span data-stu-id="c313c-122">-Permissions</span></span>
<span data-ttu-id="c313c-123">API 키에서 앱이 할 수 있는 사용 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-123">Permissions that API key allow apps to do.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:
Accepted values: ReadTelemetry, WriteAnnotations, AuthenticateSDKControlChannel

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c313c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c313c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c313c-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="c313c-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c313c-126">-ResourceId</span></span>
<span data-ttu-id="c313c-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="c313c-128">-확인</span><span class="sxs-lookup"><span data-stu-id="c313c-128">-Confirm</span></span>
<span data-ttu-id="c313c-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c313c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c313c-130">-WhatIf</span></span>
<span data-ttu-id="c313c-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="c313c-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c313c-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c313c-133">CommonParameters</span></span>
<span data-ttu-id="c313c-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c313c-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c313c-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c313c-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c313c-136">입력</span><span class="sxs-lookup"><span data-stu-id="c313c-136">INPUTS</span></span>

### <span data-ttu-id="c313c-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c313c-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c313c-138">System.String</span><span class="sxs-lookup"><span data-stu-id="c313c-138">System.String</span></span>

## <span data-ttu-id="c313c-139">출력</span><span class="sxs-lookup"><span data-stu-id="c313c-139">OUTPUTS</span></span>

### <span data-ttu-id="c313c-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c313c-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c313c-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c313c-141">NOTES</span></span>

## <span data-ttu-id="c313c-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c313c-142">RELATED LINKS</span></span>
