---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayRequestRoutingRule.md
ms.openlocfilehash: e812d0cbe6bd587e02a88cf59f8d8df5bccd1766
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532431"
---
# <span data-ttu-id="90bb7-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90bb7-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90bb7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90bb7-102">SYNOPSIS</span></span>
<span data-ttu-id="90bb7-103">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90bb7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90bb7-104">SYNTAX</span></span>

### <span data-ttu-id="90bb7-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="90bb7-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90bb7-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="90bb7-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="90bb7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="90bb7-107">DESCRIPTION</span></span>
<span data-ttu-id="90bb7-108">**AzureRmApplicationGatewayRequestRoutingRule Cmdlet은** Azure application gateway에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="90bb7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="90bb7-109">EXAMPLES</span></span>

### <span data-ttu-id="90bb7-110">예제 1: 응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="90bb7-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="90bb7-111">이 명령은 Rule01 이라는 기본 요청 라우팅 규칙을 만들고 그 결과를 $Rule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="90bb7-112">변수</span><span class="sxs-lookup"><span data-stu-id="90bb7-112">PARAMETERS</span></span>

### <span data-ttu-id="90bb7-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="90bb7-113">-BackendAddressPool</span></span>
<span data-ttu-id="90bb7-114">만들 요청 라우팅 규칙에 대 한 백 엔드 주소 풀을 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="90bb7-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="90bb7-116">만들려는 요청 라우팅 규칙의 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="90bb7-117">-BackendHttpSettings</span></span>
<span data-ttu-id="90bb7-118">만들 요청 라우팅 규칙에 대 한 개체의 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="90bb7-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="90bb7-120">만들려는 요청 라우팅 규칙의 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90bb7-121">-DefaultProfile</span></span>
<span data-ttu-id="90bb7-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="90bb7-123">-HttpListener</span></span>
<span data-ttu-id="90bb7-124">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="90bb7-125">-HttpListenerId</span></span>
<span data-ttu-id="90bb7-126">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-127">-이름</span><span class="sxs-lookup"><span data-stu-id="90bb7-127">-Name</span></span>
<span data-ttu-id="90bb7-128">이 cmdlet이 만드는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="90bb7-129">-RedirectConfiguration</span></span>
<span data-ttu-id="90bb7-130">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="90bb7-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="90bb7-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="90bb7-132">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-132">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="90bb7-133">-RuleType</span></span>
<span data-ttu-id="90bb7-134">요청 라우팅 규칙의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-134">Specifies type of the request routing rule.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="90bb7-135">-UrlPathMap</span></span>
```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="90bb7-136">-UrlPathMapId</span></span>
```yaml
Type: System.String
Parameter Sets: SetByResourceId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90bb7-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90bb7-137">CommonParameters</span></span>
<span data-ttu-id="90bb7-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90bb7-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90bb7-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90bb7-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90bb7-140">입력</span><span class="sxs-lookup"><span data-stu-id="90bb7-140">INPUTS</span></span>

### <span data-ttu-id="90bb7-141">않아야</span><span class="sxs-lookup"><span data-stu-id="90bb7-141">None</span></span>

## <span data-ttu-id="90bb7-142">출력</span><span class="sxs-lookup"><span data-stu-id="90bb7-142">OUTPUTS</span></span>

### <span data-ttu-id="90bb7-143">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="90bb7-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="90bb7-144">상속자</span><span class="sxs-lookup"><span data-stu-id="90bb7-144">NOTES</span></span>

## <span data-ttu-id="90bb7-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90bb7-145">RELATED LINKS</span></span>

[<span data-ttu-id="90bb7-146">추가-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90bb7-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90bb7-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90bb7-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90bb7-148">제거-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90bb7-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="90bb7-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="90bb7-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


