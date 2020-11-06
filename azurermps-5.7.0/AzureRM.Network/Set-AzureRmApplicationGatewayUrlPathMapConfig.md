---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 949de1a2016ffbecb96a8f10a34435cedd284ec5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535283"
---
# <span data-ttu-id="88620-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="88620-101">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="88620-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88620-102">SYNOPSIS</span></span>
<span data-ttu-id="88620-103">백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="88620-104">구문과</span><span class="sxs-lookup"><span data-stu-id="88620-104">SYNTAX</span></span>

### <span data-ttu-id="88620-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="88620-105">SetByResourceId</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="88620-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="88620-106">SetByResource</span></span>
```
Set-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="88620-107">설명은</span><span class="sxs-lookup"><span data-stu-id="88620-107">DESCRIPTION</span></span>
<span data-ttu-id="88620-108">**AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-108">The **Set-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="88620-109">예제의</span><span class="sxs-lookup"><span data-stu-id="88620-109">EXAMPLES</span></span>

## <span data-ttu-id="88620-110">변수</span><span class="sxs-lookup"><span data-stu-id="88620-110">PARAMETERS</span></span>

### <span data-ttu-id="88620-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88620-111">-ApplicationGateway</span></span>
<span data-ttu-id="88620-112">이 cmdlet이 URL 경로 맵 구성을 설정 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-112">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="88620-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="88620-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="88620-114">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="88620-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="88620-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="88620-116">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="88620-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="88620-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="88620-118">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="88620-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="88620-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="88620-120">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="88620-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88620-121">-DefaultProfile</span></span>
<span data-ttu-id="88620-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88620-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88620-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="88620-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="88620-124">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="88620-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="88620-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="88620-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="88620-126">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="88620-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="88620-127">-이름</span><span class="sxs-lookup"><span data-stu-id="88620-127">-Name</span></span>
<span data-ttu-id="88620-128">이 cmdlet이 구성을 설정 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-128">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="88620-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="88620-129">-PathRules</span></span>
<span data-ttu-id="88620-130">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="88620-131">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="88620-131">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="88620-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88620-132">CommonParameters</span></span>
<span data-ttu-id="88620-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88620-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="88620-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88620-135">입력</span><span class="sxs-lookup"><span data-stu-id="88620-135">INPUTS</span></span>

### <span data-ttu-id="88620-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88620-136">PSApplicationGateway</span></span>
<span data-ttu-id="88620-137">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="88620-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="88620-138">출력</span><span class="sxs-lookup"><span data-stu-id="88620-138">OUTPUTS</span></span>

### <span data-ttu-id="88620-139">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="88620-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="88620-140">상속자</span><span class="sxs-lookup"><span data-stu-id="88620-140">NOTES</span></span>

## <span data-ttu-id="88620-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88620-141">RELATED LINKS</span></span>

[<span data-ttu-id="88620-142">추가-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="88620-142">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="88620-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="88620-143">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="88620-144">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="88620-144">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="88620-145">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="88620-145">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)


