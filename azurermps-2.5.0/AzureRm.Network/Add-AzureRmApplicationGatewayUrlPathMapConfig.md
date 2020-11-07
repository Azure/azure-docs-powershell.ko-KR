---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 1b6e5c2c2a28333e51c74d9621a3fd607f6a652d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881497"
---
# <span data-ttu-id="5da65-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5da65-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="5da65-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5da65-102">SYNOPSIS</span></span>
<span data-ttu-id="5da65-103">백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5da65-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5da65-104">SYNTAX</span></span>

### <span data-ttu-id="5da65-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="5da65-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5da65-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="5da65-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5da65-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5da65-107">DESCRIPTION</span></span>
<span data-ttu-id="5da65-108">**Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="5da65-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5da65-109">EXAMPLES</span></span>

### <span data-ttu-id="5da65-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="5da65-110">1:</span></span>
```

```

## <span data-ttu-id="5da65-111">변수</span><span class="sxs-lookup"><span data-stu-id="5da65-111">PARAMETERS</span></span>

### <span data-ttu-id="5da65-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da65-112">-ApplicationGateway</span></span>
<span data-ttu-id="5da65-113">이 cmdlet이 URL 경로 맵 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-113">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

```yaml
Type: PSApplicationGateway
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5da65-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="5da65-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="5da65-115">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5da65-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="5da65-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="5da65-117">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="5da65-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="5da65-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="5da65-119">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="5da65-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="5da65-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="5da65-121">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="5da65-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5da65-122">-DefaultProfile</span></span>
<span data-ttu-id="5da65-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5da65-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da65-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="5da65-125">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="5da65-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5da65-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="5da65-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="5da65-127">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="5da65-128">-이름</span><span class="sxs-lookup"><span data-stu-id="5da65-128">-Name</span></span>
<span data-ttu-id="5da65-129">이 cmdlet가 백 엔드 서버 풀에 추가 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-129">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="5da65-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="5da65-130">-PathRules</span></span>
<span data-ttu-id="5da65-131">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="5da65-132">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-132">The path rules are order sensitive, they are applied in order they are specified.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5da65-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5da65-133">CommonParameters</span></span>
<span data-ttu-id="5da65-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5da65-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5da65-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5da65-136">입력</span><span class="sxs-lookup"><span data-stu-id="5da65-136">INPUTS</span></span>

### <span data-ttu-id="5da65-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da65-137">PSApplicationGateway</span></span>
<span data-ttu-id="5da65-138">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5da65-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="5da65-139">출력</span><span class="sxs-lookup"><span data-stu-id="5da65-139">OUTPUTS</span></span>

### <span data-ttu-id="5da65-140">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="5da65-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="5da65-141">상속자</span><span class="sxs-lookup"><span data-stu-id="5da65-141">NOTES</span></span>

## <span data-ttu-id="5da65-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5da65-142">RELATED LINKS</span></span>

[<span data-ttu-id="5da65-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5da65-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5da65-144">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5da65-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5da65-145">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5da65-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="5da65-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="5da65-146">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


