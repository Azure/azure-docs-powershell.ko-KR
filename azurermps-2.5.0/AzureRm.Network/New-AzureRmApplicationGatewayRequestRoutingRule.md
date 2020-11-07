---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 622FE9AC-1CC4-489C-BB17-9D6B9D1C151D
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayrequestroutingrule
schema: 2.0.0
ms.openlocfilehash: 2f4b1abc5d6cd6d55eef3c45c01a2939842e32c6
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882190"
---
# <span data-ttu-id="45888-101">New-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45888-101">New-AzureRmApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="45888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="45888-102">SYNOPSIS</span></span>
<span data-ttu-id="45888-103">응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45888-103">Creates a request routing rule for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="45888-104">구문과</span><span class="sxs-lookup"><span data-stu-id="45888-104">SYNTAX</span></span>

### <span data-ttu-id="45888-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="45888-105">SetByResourceId</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettingsId <String>] [-HttpListenerId <String>] [-BackendAddressPoolId <String>]
 [-UrlPathMapId <String>] [-RedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="45888-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="45888-106">SetByResource</span></span>
```
New-AzureRmApplicationGatewayRequestRoutingRule -Name <String> -RuleType <String>
 [-BackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-HttpListener <PSApplicationGatewayHttpListener>]
 [-BackendAddressPool <PSApplicationGatewayBackendAddressPool>] [-UrlPathMap <PSApplicationGatewayUrlPathMap>]
 [-RedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="45888-107">설명은</span><span class="sxs-lookup"><span data-stu-id="45888-107">DESCRIPTION</span></span>
<span data-ttu-id="45888-108">**AzureRmApplicationGatewayRequestRoutingRule Cmdlet은** Azure application gateway에 대 한 요청 라우팅 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="45888-108">**The Add-AzureRmApplicationGatewayRequestRoutingRule** cmdlet creates a request routing rule for an Azure application gateway.</span></span>

## <span data-ttu-id="45888-109">예제의</span><span class="sxs-lookup"><span data-stu-id="45888-109">EXAMPLES</span></span>

### <span data-ttu-id="45888-110">예제 1: 응용 프로그램 게이트웨이에 대 한 요청 라우팅 규칙 만들기</span><span class="sxs-lookup"><span data-stu-id="45888-110">Example 1: Create a request routing rule for an application gateway</span></span>
```
PS C:\>$Rule = New-AzureRmApplicationGatewayRequestRoutingRule -Name "Rule01" -RuleType Basic -BackendHttpSettings $Setting -HttpListener $Listener -BackendAddressPool $Pool
```

<span data-ttu-id="45888-111">이 명령은 Rule01 이라는 기본 요청 라우팅 규칙을 만들고 그 결과를 $Rule 라는 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-111">This command creates a basic request routing rule named Rule01 and stores the result in the variable named $Rule.</span></span>

## <span data-ttu-id="45888-112">변수</span><span class="sxs-lookup"><span data-stu-id="45888-112">PARAMETERS</span></span>

### <span data-ttu-id="45888-113">-BackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="45888-113">-BackendAddressPool</span></span>
<span data-ttu-id="45888-114">만들 요청 라우팅 규칙에 대 한 백 엔드 주소 풀을 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-114">Specifies the back-end address pool, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendAddressPool
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-115">-BackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="45888-115">-BackendAddressPoolId</span></span>
<span data-ttu-id="45888-116">만들려는 요청 라우팅 규칙의 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-116">Specifies the back-end address pool ID of the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-117">-BackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="45888-117">-BackendHttpSettings</span></span>
<span data-ttu-id="45888-118">만들 요청 라우팅 규칙에 대 한 개체의 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-118">Specifies the back-end HTTP settings, as an object, for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayBackendHttpSettings
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-119">-BackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="45888-119">-BackendHttpSettingsId</span></span>
<span data-ttu-id="45888-120">만들려는 요청 라우팅 규칙의 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-120">Specifies the back-end HTTP settings ID of the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="45888-121">-DefaultProfile</span></span>
<span data-ttu-id="45888-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="45888-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="45888-123">-HttpListener</span><span class="sxs-lookup"><span data-stu-id="45888-123">-HttpListener</span></span>
<span data-ttu-id="45888-124">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-124">Specifies the back-end HTTP listener for the request routing rule to create.</span></span>

```yaml
Type: PSApplicationGatewayHttpListener
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-125">-HttpListenerId</span><span class="sxs-lookup"><span data-stu-id="45888-125">-HttpListenerId</span></span>
<span data-ttu-id="45888-126">만들 요청 라우팅 규칙에 대 한 백 엔드 HTTP 수신기 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-126">Specifies the backend HTTP listener ID for the request routing rule to create.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-127">-이름</span><span class="sxs-lookup"><span data-stu-id="45888-127">-Name</span></span>
<span data-ttu-id="45888-128">이 cmdlet이 만드는 요청 라우팅 규칙의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-128">Specifies the name of the request routing rule that this cmdlet creates.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-129">-RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="45888-129">-RedirectConfiguration</span></span>
<span data-ttu-id="45888-130">Application gateway RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="45888-130">Application gateway RedirectConfiguration</span></span>

```yaml
Type: PSApplicationGatewayRedirectConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-131">-RedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="45888-131">-RedirectConfigurationId</span></span>
<span data-ttu-id="45888-132">응용 프로그램 게이트웨이 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="45888-132">ID of the application gateway RedirectConfiguration</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-133">-RuleType</span><span class="sxs-lookup"><span data-stu-id="45888-133">-RuleType</span></span>
<span data-ttu-id="45888-134">요청 라우팅 규칙의 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-134">Specifies type of the request routing rule.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Basic, PathBasedRouting

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-135">-UrlPathMap</span><span class="sxs-lookup"><span data-stu-id="45888-135">-UrlPathMap</span></span>
```yaml
Type: PSApplicationGatewayUrlPathMap
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-136">-UrlPathMapId</span><span class="sxs-lookup"><span data-stu-id="45888-136">-UrlPathMapId</span></span>
```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="45888-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="45888-137">CommonParameters</span></span>
<span data-ttu-id="45888-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="45888-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="45888-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="45888-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="45888-140">입력</span><span class="sxs-lookup"><span data-stu-id="45888-140">INPUTS</span></span>

### <span data-ttu-id="45888-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="45888-141">System.String</span></span>

## <span data-ttu-id="45888-142">출력</span><span class="sxs-lookup"><span data-stu-id="45888-142">OUTPUTS</span></span>

### <span data-ttu-id="45888-143">PSApplicationGatewayRequestRoutingRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="45888-143">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayRequestRoutingRule</span></span>

## <span data-ttu-id="45888-144">상속자</span><span class="sxs-lookup"><span data-stu-id="45888-144">NOTES</span></span>

## <span data-ttu-id="45888-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="45888-145">RELATED LINKS</span></span>

[<span data-ttu-id="45888-146">추가-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45888-146">Add-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Add-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="45888-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45888-147">Get-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Get-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="45888-148">제거-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45888-148">Remove-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Remove-AzureRmApplicationGatewayRequestRoutingRule.md)

[<span data-ttu-id="45888-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span><span class="sxs-lookup"><span data-stu-id="45888-149">Set-AzureRmApplicationGatewayRequestRoutingRule</span></span>](./Set-AzureRmApplicationGatewayRequestRoutingRule.md)


