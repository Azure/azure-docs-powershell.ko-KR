---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 9D9D079C-5557-40DC-8CFB-1DCD446D9109
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayurlpathmapconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayUrlPathMapConfig.md
ms.openlocfilehash: 3885298f58f3bc45b207ea14cdda0935d0724986
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530473"
---
# <span data-ttu-id="728be-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="728be-101">Add-AzureRmApplicationGatewayUrlPathMapConfig</span></span>

## <span data-ttu-id="728be-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="728be-102">SYNOPSIS</span></span>
<span data-ttu-id="728be-103">백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-103">Adds an array of URL path mappings to a backend server pool.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="728be-104">구문과</span><span class="sxs-lookup"><span data-stu-id="728be-104">SYNTAX</span></span>

### <span data-ttu-id="728be-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="728be-105">SetByResourceId</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPoolId <String>] [-DefaultBackendHttpSettingsId <String>]
 [-DefaultRedirectConfigurationId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="728be-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="728be-106">SetByResource</span></span>
```
Add-AzureRmApplicationGatewayUrlPathMapConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -PathRules <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayPathRule]>
 [-DefaultBackendAddressPool <PSApplicationGatewayBackendAddressPool>]
 [-DefaultBackendHttpSettings <PSApplicationGatewayBackendHttpSettings>]
 [-DefaultRedirectConfiguration <PSApplicationGatewayRedirectConfiguration>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="728be-107">설명은</span><span class="sxs-lookup"><span data-stu-id="728be-107">DESCRIPTION</span></span>
<span data-ttu-id="728be-108">**Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet은 백 엔드 서버 풀에 URL 경로 매핑 배열을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-108">The **Add-AzureRmApplicationGatewayUrlPathMapConfig** cmdlet adds an array of URL path mappings to a back end server pool.</span></span>

## <span data-ttu-id="728be-109">예제의</span><span class="sxs-lookup"><span data-stu-id="728be-109">EXAMPLES</span></span>

## <span data-ttu-id="728be-110">변수</span><span class="sxs-lookup"><span data-stu-id="728be-110">PARAMETERS</span></span>

### <span data-ttu-id="728be-111">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="728be-111">-ApplicationGateway</span></span>
<span data-ttu-id="728be-112">이 cmdlet이 URL 경로 맵 구성을 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-112">Specifies the application gateway to which this cmdlet adds a URL path map configuration.</span></span>

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

### <span data-ttu-id="728be-113">-DefaultBackendAddressPool</span><span class="sxs-lookup"><span data-stu-id="728be-113">-DefaultBackendAddressPool</span></span>
<span data-ttu-id="728be-114">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 라우팅할 기본 백 엔드 주소 풀을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-114">Specifies the default backend address pool to route in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="728be-115">-DefaultBackendAddressPoolId</span><span class="sxs-lookup"><span data-stu-id="728be-115">-DefaultBackendAddressPoolId</span></span>
<span data-ttu-id="728be-116">기본 백 엔드 주소 풀 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-116">Specifies the default backend address pool ID.</span></span>

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

### <span data-ttu-id="728be-117">-DefaultBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="728be-117">-DefaultBackendHttpSettings</span></span>
<span data-ttu-id="728be-118">*Pathrules* 매개 변수 일치에 지정 된 규칙이 없는 경우 사용할 기본 백 엔드 HTTP 설정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-118">Specifies the default backend HTTP settings to use in case none of the rules specified in the *pathRules* parameter match.</span></span>

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

### <span data-ttu-id="728be-119">-DefaultBackendHttpSettingsId</span><span class="sxs-lookup"><span data-stu-id="728be-119">-DefaultBackendHttpSettingsId</span></span>
<span data-ttu-id="728be-120">기본 백 엔드 HTTP 설정 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-120">Specifies the default backend HTTP settings ID.</span></span>

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

### <span data-ttu-id="728be-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="728be-121">-DefaultProfile</span></span>
<span data-ttu-id="728be-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="728be-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="728be-123">-DefaultRedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="728be-123">-DefaultRedirectConfiguration</span></span>
<span data-ttu-id="728be-124">Application gateway 기본 RedirectConfiguration</span><span class="sxs-lookup"><span data-stu-id="728be-124">Application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="728be-125">-DefaultRedirectConfigurationId</span><span class="sxs-lookup"><span data-stu-id="728be-125">-DefaultRedirectConfigurationId</span></span>
<span data-ttu-id="728be-126">응용 프로그램 게이트웨이 기본 RedirectConfiguration의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="728be-126">ID of the application gateway default RedirectConfiguration</span></span>

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

### <span data-ttu-id="728be-127">-이름</span><span class="sxs-lookup"><span data-stu-id="728be-127">-Name</span></span>
<span data-ttu-id="728be-128">이 cmdlet가 백 엔드 서버 풀에 추가 하는 URL 경로 맵 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-128">Specifies the URL path map name that this cmdlet adds to the backend server pool.</span></span>

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

### <span data-ttu-id="728be-129">-PathRules</span><span class="sxs-lookup"><span data-stu-id="728be-129">-PathRules</span></span>
<span data-ttu-id="728be-130">경로 규칙의 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-130">Specifies a list of path rules.</span></span>
<span data-ttu-id="728be-131">경로 규칙은 주문에 따라 구분 되며 지정 된 순서 대로 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="728be-131">The path rules are order sensitive, they are applied in order they are specified.</span></span>

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

### <span data-ttu-id="728be-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="728be-132">CommonParameters</span></span>
<span data-ttu-id="728be-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="728be-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="728be-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="728be-135">입력</span><span class="sxs-lookup"><span data-stu-id="728be-135">INPUTS</span></span>

### <span data-ttu-id="728be-136">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="728be-136">PSApplicationGateway</span></span>
<span data-ttu-id="728be-137">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="728be-137">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="728be-138">출력</span><span class="sxs-lookup"><span data-stu-id="728be-138">OUTPUTS</span></span>

### <span data-ttu-id="728be-139">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="728be-139">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="728be-140">상속자</span><span class="sxs-lookup"><span data-stu-id="728be-140">NOTES</span></span>

## <span data-ttu-id="728be-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="728be-141">RELATED LINKS</span></span>

[<span data-ttu-id="728be-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="728be-142">Get-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Get-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="728be-143">새로운 AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="728be-143">New-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./New-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="728be-144">제거-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="728be-144">Remove-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Remove-AzureRmApplicationGatewayUrlPathMapConfig.md)

[<span data-ttu-id="728be-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span><span class="sxs-lookup"><span data-stu-id="728be-145">Set-AzureRmApplicationGatewayUrlPathMapConfig</span></span>](./Set-AzureRmApplicationGatewayUrlPathMapConfig.md)


