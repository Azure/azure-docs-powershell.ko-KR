---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/set-azurermapplicationgatewaybackendhttpsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 784c71a284e2cf7711f50e86ea1b726d83eb6e40
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93538008"
---
# <span data-ttu-id="060e6-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="060e6-101">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="060e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="060e6-102">SYNOPSIS</span></span>
<span data-ttu-id="060e6-103">Application gateway에 대 한 백 엔드 HTTP 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-103">Updates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="060e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="060e6-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="060e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="060e6-105">DESCRIPTION</span></span>
<span data-ttu-id="060e6-106">Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet은 Azure application gateway의 백 엔드 HTTP (하이퍼텍스트 전송 프로토콜) 설정을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-106">The Set-AzureRmApplicationGatewayBackendHttpSettings cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="060e6-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="060e6-108">예제의</span><span class="sxs-lookup"><span data-stu-id="060e6-108">EXAMPLES</span></span>

### <span data-ttu-id="060e6-109">예제 1: 응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="060e6-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzureRmApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzureRmApplicationGatewayBackendHttpSettings -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="060e6-110">첫 번째 명령은 ResourceGroup01 이라는 리소스 그룹에 속하는 ApplicationGateway01 라는 응용 프로그램 게이트웨이를 가져온 다음이를 $AppGw 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>

<span data-ttu-id="060e6-111">두 번째 명령은 포트 88, HTTP 프로토콜을 사용 하도록 $AppGw 변수에 있는 응용 프로그램 게이트웨이의 HTTP 설정을 업데이트 하 고 쿠키 기반 선호도를 활성화 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="060e6-112">변수</span><span class="sxs-lookup"><span data-stu-id="060e6-112">PARAMETERS</span></span>

### <span data-ttu-id="060e6-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="060e6-113">-AffinityCookieName</span></span>
<span data-ttu-id="060e6-114">선호도 쿠키에 사용할 쿠키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="060e6-115">-ApplicationGateway</span></span>
<span data-ttu-id="060e6-116">이 cmdlet이 백 엔드 HTTP 설정을 연결 하는 데 사용 되는 응용 프로그램 게이트웨이 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

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

### <span data-ttu-id="060e6-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="060e6-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="060e6-118">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-118">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="060e6-119">-ConnectionDraining</span></span>
<span data-ttu-id="060e6-120">백 엔드 http 설정 리소스의 연결 드레이닝</span><span class="sxs-lookup"><span data-stu-id="060e6-120">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="060e6-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="060e6-122">백 엔드 서버 풀에 대해 쿠키 기반 선호도를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="060e6-123">이 매개 변수에 허용 되는 값은 사용 되지 않거나 사용 하도록 설정 된 것입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="060e6-124">-DefaultProfile</span></span>
<span data-ttu-id="060e6-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="060e6-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="060e6-126">-HostName</span></span>
<span data-ttu-id="060e6-127">백 엔드 서버로 보낼 호스트 헤더를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-127">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-128">-이름</span><span class="sxs-lookup"><span data-stu-id="060e6-128">-Name</span></span>
<span data-ttu-id="060e6-129">백 엔드 HTTP 설정 개체의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="060e6-130">-Path</span><span class="sxs-lookup"><span data-stu-id="060e6-130">-Path</span></span>
<span data-ttu-id="060e6-131">모든 HTTP 요청에 대 한 접두사로 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="060e6-132">이 매개 변수에 대 한 값을 제공 하지 않으면 경로에 접두사를 붙일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="060e6-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="060e6-134">백 엔드 서버의 호스트 이름에서 호스트 헤더를 선택 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-134">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-135">-포트</span><span class="sxs-lookup"><span data-stu-id="060e6-135">-Port</span></span>
<span data-ttu-id="060e6-136">백 엔드 서버 풀의 각 서버에 사용할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-136">Specifies the port to use for each server in the back-end server pool.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-137">-프로브</span><span class="sxs-lookup"><span data-stu-id="060e6-137">-Probe</span></span>
<span data-ttu-id="060e6-138">백 엔드 HTTP 설정과 연결할 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-139">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="060e6-139">-ProbeEnabled</span></span>
<span data-ttu-id="060e6-140">프로브를 사용 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-140">Flag if probe should be enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-141">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="060e6-141">-ProbeId</span></span>
<span data-ttu-id="060e6-142">백 엔드 HTTP 설정과 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-142">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-143">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="060e6-143">-Protocol</span></span>
<span data-ttu-id="060e6-144">응용 프로그램 게이트웨이 및 백 엔드 서버 간 통신에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-144">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="060e6-145">이 매개 변수에 허용 되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-145">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="060e6-146">이 매개 변수는 대/소문자를 구분 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-146">This parameter is case-sensitive.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-147">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="060e6-147">-RequestTimeout</span></span>
<span data-ttu-id="060e6-148">요청 시간 초과 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-148">Specifies a request time-out value.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="060e6-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="060e6-149">CommonParameters</span></span>
<span data-ttu-id="060e6-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="060e6-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="060e6-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="060e6-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="060e6-152">입력</span><span class="sxs-lookup"><span data-stu-id="060e6-152">INPUTS</span></span>

### <span data-ttu-id="060e6-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="060e6-153">System.String</span></span>

## <span data-ttu-id="060e6-154">출력</span><span class="sxs-lookup"><span data-stu-id="060e6-154">OUTPUTS</span></span>

### <span data-ttu-id="060e6-155">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="060e6-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="060e6-156">상속자</span><span class="sxs-lookup"><span data-stu-id="060e6-156">NOTES</span></span>

## <span data-ttu-id="060e6-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="060e6-157">RELATED LINKS</span></span>

[<span data-ttu-id="060e6-158">추가-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="060e6-158">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="060e6-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="060e6-159">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="060e6-160">새로운 AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="060e6-160">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="060e6-161">제거-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="060e6-161">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

