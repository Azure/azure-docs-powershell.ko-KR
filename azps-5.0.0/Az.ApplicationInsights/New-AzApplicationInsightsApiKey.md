---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/new-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/New-AzApplicationInsightsApiKey.md
ms.openlocfilehash: 2afb8ebfa1305e736a226f48022f4c56ded2d809
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217672"
---
# <span data-ttu-id="19c22-101">New-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="19c22-101">New-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="19c22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="19c22-102">SYNOPSIS</span></span>
<span data-ttu-id="19c22-103">Application insights 리소스에 대 한 application insights api 키 만들기</span><span class="sxs-lookup"><span data-stu-id="19c22-103">Create an application insights api key for an application insights resource</span></span>

## <span data-ttu-id="19c22-104">구문과</span><span class="sxs-lookup"><span data-stu-id="19c22-104">SYNTAX</span></span>

### <span data-ttu-id="19c22-105">ComponentNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="19c22-105">ComponentNameParameterSet (Default)</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [-Permissions] <String[]>
 [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c22-106">ComponentObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="19c22-106">ComponentObjectParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [-Permissions] <String[]> [-Description] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="19c22-107">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="19c22-107">ResourceIdParameterSet</span></span>
```
New-AzApplicationInsightsApiKey [-ResourceId] <String> [-Permissions] <String[]> [-Description] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="19c22-108">설명은</span><span class="sxs-lookup"><span data-stu-id="19c22-108">DESCRIPTION</span></span>
<span data-ttu-id="19c22-109">Application insights 리소스에 대 한 application insights api 키 만들기</span><span class="sxs-lookup"><span data-stu-id="19c22-109">Create an application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="19c22-110">예제의</span><span class="sxs-lookup"><span data-stu-id="19c22-110">EXAMPLES</span></span>

### <span data-ttu-id="19c22-111">예제 1 application insights 리소스에 대 한 새 Api 키 만들기</span><span class="sxs-lookup"><span data-stu-id="19c22-111">Example 1 Create a new Api Key for an application insights resource</span></span>
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

<span data-ttu-id="19c22-112">Application insights api 키 설명을 "testapiKey"로 사용 하 고 리소스 그룹 "testGroup"의 리소스 "테스트"에 대 한 "ReadTelemetry 분석", "WriteAnnotations 있는 주석"으로 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-112">Create application insights api key description as "testapiKey" with permissions "ReadTelemetry", "WriteAnnotations" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="19c22-113">변수</span><span class="sxs-lookup"><span data-stu-id="19c22-113">PARAMETERS</span></span>

### <span data-ttu-id="19c22-114">-ApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="19c22-114">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="19c22-115">Application Insights 구성 요소 개체.</span><span class="sxs-lookup"><span data-stu-id="19c22-115">Application Insights Component Object.</span></span>

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

### <span data-ttu-id="19c22-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="19c22-116">-DefaultProfile</span></span>
<span data-ttu-id="19c22-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="19c22-118">-설명</span><span class="sxs-lookup"><span data-stu-id="19c22-118">-Description</span></span>
<span data-ttu-id="19c22-119">이 API 키를 식별 하는 데 도움이 되는 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-119">Description to help identify this API key.</span></span>

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

### <span data-ttu-id="19c22-120">-이름</span><span class="sxs-lookup"><span data-stu-id="19c22-120">-Name</span></span>
<span data-ttu-id="19c22-121">구성 요소 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-121">Component Name.</span></span>

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

### <span data-ttu-id="19c22-122">-사용 권한</span><span class="sxs-lookup"><span data-stu-id="19c22-122">-Permissions</span></span>
<span data-ttu-id="19c22-123">API 키에서 앱을 실행할 수 있는 사용 권한입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-123">Permissions that API key allow apps to do.</span></span>

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

### <span data-ttu-id="19c22-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="19c22-124">-ResourceGroupName</span></span>
<span data-ttu-id="19c22-125">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="19c22-126">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="19c22-126">-ResourceId</span></span>
<span data-ttu-id="19c22-127">Application Insights 구성 요소 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-127">Application Insights Component Resource Id.</span></span>

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

### <span data-ttu-id="19c22-128">-확인</span><span class="sxs-lookup"><span data-stu-id="19c22-128">-Confirm</span></span>
<span data-ttu-id="19c22-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="19c22-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="19c22-130">-WhatIf</span></span>
<span data-ttu-id="19c22-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="19c22-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="19c22-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="19c22-133">CommonParameters</span></span>
<span data-ttu-id="19c22-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="19c22-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="19c22-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="19c22-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="19c22-136">입력</span><span class="sxs-lookup"><span data-stu-id="19c22-136">INPUTS</span></span>

### <span data-ttu-id="19c22-137">PSApplicationInsightsComponent-ApplicationInsights.</span><span class="sxs-lookup"><span data-stu-id="19c22-137">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="19c22-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="19c22-138">System.String</span></span>

## <span data-ttu-id="19c22-139">출력</span><span class="sxs-lookup"><span data-stu-id="19c22-139">OUTPUTS</span></span>

### <span data-ttu-id="19c22-140">Microsoft. Azure. m Apikey</span><span class="sxs-lookup"><span data-stu-id="19c22-140">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="19c22-141">상속자</span><span class="sxs-lookup"><span data-stu-id="19c22-141">NOTES</span></span>

## <span data-ttu-id="19c22-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="19c22-142">RELATED LINKS</span></span>
