---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
ms.openlocfilehash: 7ca1d4f8ee4ab3e83badecd7856fcee35f5b9a23
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882177"
---
# <span data-ttu-id="003c0-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="003c0-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="003c0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="003c0-102">SYNOPSIS</span></span>
<span data-ttu-id="003c0-103">백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="003c0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="003c0-104">SYNTAX</span></span>

### <span data-ttu-id="003c0-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="003c0-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="003c0-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="003c0-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="003c0-107">설명은</span><span class="sxs-lookup"><span data-stu-id="003c0-107">DESCRIPTION</span></span>
<span data-ttu-id="003c0-108">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="003c0-109">예제의</span><span class="sxs-lookup"><span data-stu-id="003c0-109">EXAMPLES</span></span>

### <span data-ttu-id="003c0-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="003c0-110">1:</span></span>
```

```

## <span data-ttu-id="003c0-111">변수</span><span class="sxs-lookup"><span data-stu-id="003c0-111">PARAMETERS</span></span>

### <span data-ttu-id="003c0-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003c0-112">-ApplicationGateway</span></span>
<span data-ttu-id="003c0-113">이 cmdlet이 URL 경로 맵 구성을 설정 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="003c0-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="003c0-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="003c0-115">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="003c0-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="003c0-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="003c0-117">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="003c0-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="003c0-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="003c0-119">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="003c0-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="003c0-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="003c0-121">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="003c0-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="003c0-122">-DefaultProfile</span></span>
<span data-ttu-id="003c0-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="003c0-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="003c0-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="003c0-125">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="003c0-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="003c0-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="003c0-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="003c0-127">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="003c0-128">-이름</span><span class="sxs-lookup"><span data-stu-id="003c0-128">-Name</span></span>
<span data-ttu-id="003c0-129">이 cmdlet이 구성을 설정 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="003c0-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="003c0-130">-PathRules</span></span>
<span data-ttu-id="003c0-131">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="003c0-132">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="003c0-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="003c0-133">CommonParameters</span></span>
<span data-ttu-id="003c0-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="003c0-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="003c0-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="003c0-136">입력</span><span class="sxs-lookup"><span data-stu-id="003c0-136">INPUTS</span></span>

### <span data-ttu-id="003c0-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003c0-137">PSApplicationGateway</span></span>
<span data-ttu-id="003c0-138">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="003c0-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="003c0-139">출력</span><span class="sxs-lookup"><span data-stu-id="003c0-139">OUTPUTS</span></span>

### <span data-ttu-id="003c0-140">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="003c0-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="003c0-141">상속자</span><span class="sxs-lookup"><span data-stu-id="003c0-141">NOTES</span></span>

## <span data-ttu-id="003c0-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="003c0-142">RELATED LINKS</span></span>

[<span data-ttu-id="003c0-143">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="003c0-143">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="003c0-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="003c0-144">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="003c0-145">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="003c0-145">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="003c0-146">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="003c0-146">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


