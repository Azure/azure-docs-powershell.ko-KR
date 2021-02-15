---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100182276"
---
# <span data-ttu-id="0bf9e-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="0bf9e-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="0bf9e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0bf9e-102">SYNOPSIS</span></span>
<span data-ttu-id="0bf9e-103">Application Insights 리소스에 대한 Application Insights API 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0bf9e-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="0bf9e-104">구문</span><span class="sxs-lookup"><span data-stu-id="0bf9e-104">SYNTAX</span></span>

### <span data-ttu-id="0bf9e-105">ComponentNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="0bf9e-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bf9e-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf9e-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0bf9e-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0bf9e-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0bf9e-108">설명</span><span class="sxs-lookup"><span data-stu-id="0bf9e-108">DESCRIPTION</span></span>
<span data-ttu-id="0bf9e-109">Application Insights 리소스에 대한 Application Insights API 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0bf9e-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="0bf9e-110">예제</span><span class="sxs-lookup"><span data-stu-id="0bf9e-110">EXAMPLES</span></span>

### <span data-ttu-id="0bf9e-111">예제 1 Application Insights 리소스에 대한 새 API 키 만들기</span><span class="sxs-lookup"><span data-stu-id="0bf9e-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="0bf9e-112">리소스 그룹 "testGroup"에서 리소스 "test"에 대한 "ReadTelemetry", "WriteAnnotations" 권한이 있는 "testapiKey"로 Application Insights API 키 설명을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="0bf9e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0bf9e-113">PARAMETERS</span></span>

### <span data-ttu-id="0bf9e-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0bf9e-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="0bf9e-115">Application Insights 구성 요소 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="0bf9e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0bf9e-116">-DefaultProfile</span></span>
<span data-ttu-id="0bf9e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0bf9e-118">-Description</span><span class="sxs-lookup"><span data-stu-id="0bf9e-118">-Description</span></span>
<span data-ttu-id="0bf9e-119">이 API 키를 식별하는 데 도움이 되는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="0bf9e-120">-Name</span><span class="sxs-lookup"><span data-stu-id="0bf9e-120">-Name</span></span>
<span data-ttu-id="0bf9e-121">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-121">Component Name.</span></span>

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

### <span data-ttu-id="0bf9e-122">-Permissions</span><span class="sxs-lookup"><span data-stu-id="0bf9e-122">-Permissions</span></span>
<span data-ttu-id="0bf9e-123">API 키가 앱이 할 수 있는 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="0bf9e-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0bf9e-124">-ResourceGroupName</span></span>
<span data-ttu-id="0bf9e-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="0bf9e-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0bf9e-126">-ResourceId</span></span>
<span data-ttu-id="0bf9e-127">Application Insights 구성 요소 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="0bf9e-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0bf9e-128">-Confirm</span></span>
<span data-ttu-id="0bf9e-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0bf9e-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0bf9e-130">-WhatIf</span></span>
<span data-ttu-id="0bf9e-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0bf9e-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0bf9e-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0bf9e-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0bf9e-133">CommonParameters</span></span>
<span data-ttu-id="0bf9e-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0bf9e-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="0bf9e-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0bf9e-136">입력</span><span class="sxs-lookup"><span data-stu-id="0bf9e-136">INPUTS</span></span>

### <span data-ttu-id="0bf9e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="0bf9e-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="0bf9e-138">System.String</span><span class="sxs-lookup"><span data-stu-id="0bf9e-138">System.String</span></span>

## <span data-ttu-id="0bf9e-139">출력</span><span class="sxs-lookup"><span data-stu-id="0bf9e-139">OUTPUTS</span></span>

### <span data-ttu-id="0bf9e-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span><span class="sxs-lookup"><span data-stu-id="0bf9e-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="0bf9e-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0bf9e-141">NOTES</span></span>

## <span data-ttu-id="0bf9e-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0bf9e-142">RELATED LINKS</span></span>
