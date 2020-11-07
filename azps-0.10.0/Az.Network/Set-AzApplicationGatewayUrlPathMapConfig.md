---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 9F5EC8E7-12E9-40E5-B98D-AAFD8F9F3C37
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/Set-AzApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 5eb4fb0f036331fe68755a3a8ebddcd7e1b6e424
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876592"
---
# <span data-ttu-id="11b92-101">Set-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b92-101">Set-AzApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="11b92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11b92-102">SYNOPSIS</span></span>
<span data-ttu-id="11b92-103">백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-103">Sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="11b92-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11b92-104">SYNTAX</span></span>

### <span data-ttu-id="11b92-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="11b92-105">SetByResourceId</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="11b92-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="11b92-106">SetByResource</span></span>
```
Set-AzApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="11b92-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11b92-107">DESCRIPTION</span></span>
<span data-ttu-id="11b92-108">**AzApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 대 한 URL 경로 매핑 배열의 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-108">The **Set-AzApplicationGatewayUrlPathMapConfig** cmdlet sets configuration for an array of URL path mappings to a backend server pool.</span></span>

## <span data-ttu-id="11b92-109">예제의</span><span class="sxs-lookup"><span data-stu-id="11b92-109">EXAMPLES</span></span>

### <span data-ttu-id="11b92-110">raid-1</span><span class="sxs-lookup"><span data-stu-id="11b92-110">1:</span></span>
```

```

## <span data-ttu-id="11b92-111">변수</span><span class="sxs-lookup"><span data-stu-id="11b92-111">PARAMETERS</span></span>

### <span data-ttu-id="11b92-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11b92-112">-ApplicationGateway</span></span>
<span data-ttu-id="11b92-113">이 cmdlet이 URL 경로 맵 구성을 설정 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-113">Specifies the application gateway to which this cmdlet sets a URL path map configuration.</span></span>

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

### <span data-ttu-id="11b92-114">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="11b92-114">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="11b92-115">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-115">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="11b92-116">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="11b92-116">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="11b92-117">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-117">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="11b92-118">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="11b92-118">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="11b92-119">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-119">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="11b92-120">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="11b92-120">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="11b92-121">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-121">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="11b92-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11b92-122">-DefaultProfile</span></span>
<span data-ttu-id="11b92-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11b92-124">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b92-124">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="11b92-125">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="11b92-125">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="11b92-126">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="11b92-126">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="11b92-127">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-127">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="11b92-128">-이름</span><span class="sxs-lookup"><span data-stu-id="11b92-128">-Name</span></span>
<span data-ttu-id="11b92-129">이 cmdlet이 구성을 설정 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-129">Specifies the URL path map name in which this cmdlet sets configuration for.</span></span>

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

### <span data-ttu-id="11b92-130">-PathRules</span><span class="sxs-lookup"><span data-stu-id="11b92-130">-PathRules</span></span>
<span data-ttu-id="11b92-131">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-131">Specifies a list of path rules.</span></span>
<span data-ttu-id="11b92-132">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-132">Note that the path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="11b92-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11b92-133">CommonParameters</span></span>
<span data-ttu-id="11b92-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11b92-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="11b92-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11b92-136">입력</span><span class="sxs-lookup"><span data-stu-id="11b92-136">INPUTS</span></span>

### <span data-ttu-id="11b92-137">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11b92-137">PSApplicationGateway</span></span>
<span data-ttu-id="11b92-138">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="11b92-138">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="11b92-139">출력</span><span class="sxs-lookup"><span data-stu-id="11b92-139">OUTPUTS</span></span>

### <span data-ttu-id="11b92-140">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="11b92-140">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="11b92-141">상속자</span><span class="sxs-lookup"><span data-stu-id="11b92-141">NOTES</span></span>

## <span data-ttu-id="11b92-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11b92-142">RELATED LINKS</span></span>

[<span data-ttu-id="11b92-143">추가-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b92-143">Add-AzApplicationGatewayUrlPathMapConfig</span></span>](./Add-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11b92-144">Get-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b92-144">Get-AzApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11b92-145">새로운 AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b92-145">New-AzApplicationGatewayUrlPathMapConfig</span></span>](./New-AzApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="11b92-146">제거-AzApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="11b92-146">Remove-AzApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzApplicationGatewayUrlPathMapConfig.md)


