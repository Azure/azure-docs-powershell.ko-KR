---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 014309ceb54b1d16b2a55c97b03887deaf4ef281
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870562"
---
# <span data-ttu-id="2abb4-101">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2abb4-101">New-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="2abb4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2abb4-102">SYNOPSIS</span></span>
<span data-ttu-id="2abb4-103">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-103">Creates back-end HTTP setting for an application gateway.</span></span>

## <span data-ttu-id="2abb4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2abb4-104">SYNTAX</span></span>

```
New-AzApplicationGatewayBackendHttpSetting -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2abb4-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2abb4-105">DESCRIPTION</span></span>
<span data-ttu-id="2abb4-106">New-AzApplicationGatewayBackendHttpSetting cmdlet은 응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-106">The New-AzApplicationGatewayBackendHttpSetting cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="2abb4-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="2abb4-108">예제의</span><span class="sxs-lookup"><span data-stu-id="2abb4-108">EXAMPLES</span></span>

### <span data-ttu-id="2abb4-109">예제 1: 백 엔드 HTTP 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="2abb4-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzApplicationGatewayBackendHttpSetting -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="2abb4-110">이 명령은 HTTP 프로토콜을 사용 하 여 포트 80에서 Setting01 라는 백 엔드 HTTP 설정을 만들고, 쿠키 기반 선호도는 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="2abb4-111">설정이 $Setting 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="2abb4-112">변수</span><span class="sxs-lookup"><span data-stu-id="2abb4-112">PARAMETERS</span></span>

### <span data-ttu-id="2abb4-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="2abb4-113">-AffinityCookieName</span></span>
<span data-ttu-id="2abb4-114">선호도 쿠키에 사용할 쿠키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-114">Cookie name to use for the affinity cookie</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="2abb4-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="2abb4-116">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-116">Specifies authentication certificates for the application gateway.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="2abb4-117">-ConnectionDraining</span></span>
<span data-ttu-id="2abb4-118">백 엔드 http 설정 리소스의 연결 드레이닝</span><span class="sxs-lookup"><span data-stu-id="2abb4-118">Connection draining of the backend http settings resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayConnectionDraining
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="2abb4-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="2abb4-120">백 엔드 서버 풀에 대해 쿠키 기반 선호도를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Enabled, Disabled

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2abb4-121">-DefaultProfile</span></span>
<span data-ttu-id="2abb4-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-122">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2abb4-123">-HostName</span><span class="sxs-lookup"><span data-stu-id="2abb4-123">-HostName</span></span>
<span data-ttu-id="2abb4-124">백 엔드 서버로 보낼 호스트 헤더를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-124">Sets host header to be sent to the backend servers.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="2abb4-125">-Name</span></span>
<span data-ttu-id="2abb4-126">이 cmdlet이 만드는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-126">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="2abb4-127">-Path</span><span class="sxs-lookup"><span data-stu-id="2abb4-127">-Path</span></span>
<span data-ttu-id="2abb4-128">모든 HTTP 요청에 대 한 접두사로 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-128">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="2abb4-129">이 매개 변수에 대 한 값을 제공 하지 않으면 경로에 접두사를 붙일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-129">If no value is provided for this parameter, then no path will be prefixed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-130">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="2abb4-130">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="2abb4-131">백 엔드 서버의 호스트 이름에서 호스트 헤더를 선택 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-131">Flag if host header should be picked from the host name of the backend server.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-132">-포트</span><span class="sxs-lookup"><span data-stu-id="2abb4-132">-Port</span></span>
<span data-ttu-id="2abb4-133">백 엔드 서버 풀의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-133">Specifies the port of the back-end server pool.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-134">-프로브</span><span class="sxs-lookup"><span data-stu-id="2abb4-134">-Probe</span></span>
<span data-ttu-id="2abb4-135">백 엔드 서버 풀에 연결 하는 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-135">Specifies a probe to associate with the back-end server pool.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="2abb4-136">-ProbeId</span></span>
<span data-ttu-id="2abb4-137">백 엔드 서버 풀에 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="2abb4-138">-Protocol</span></span>
<span data-ttu-id="2abb4-139">응용 프로그램 게이트웨이와 백 엔드 서버 간의 통신에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="2abb4-140">이 매개 변수에 허용 되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-140">The acceptable values for this parameter are: Http and Https.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Http, Https

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="2abb4-141">-RequestTimeout</span></span>
<span data-ttu-id="2abb4-142">요청 시간 초과 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-142">Specifies a request time-out value.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-143">-을 (를)로 하는 Rootcertificate</span><span class="sxs-lookup"><span data-stu-id="2abb4-143">-TrustedRootCertificate</span></span>
<span data-ttu-id="2abb4-144">Application gateway 신뢰할 수 있는 루트 인증서</span><span class="sxs-lookup"><span data-stu-id="2abb4-144">Application gateway Trusted Root Certificates</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayTrustedRootCertificate[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2abb4-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2abb4-145">CommonParameters</span></span>
<span data-ttu-id="2abb4-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2abb4-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2abb4-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2abb4-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2abb4-148">입력</span><span class="sxs-lookup"><span data-stu-id="2abb4-148">INPUTS</span></span>

### <span data-ttu-id="2abb4-149">않아야</span><span class="sxs-lookup"><span data-stu-id="2abb4-149">None</span></span>

## <span data-ttu-id="2abb4-150">출력</span><span class="sxs-lookup"><span data-stu-id="2abb4-150">OUTPUTS</span></span>

### <span data-ttu-id="2abb4-151">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="2abb4-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="2abb4-152">상속자</span><span class="sxs-lookup"><span data-stu-id="2abb4-152">NOTES</span></span>

## <span data-ttu-id="2abb4-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2abb4-153">RELATED LINKS</span></span>

[<span data-ttu-id="2abb4-154">추가-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2abb4-154">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2abb4-155">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2abb4-155">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2abb4-156">제거-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2abb4-156">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="2abb4-157">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="2abb4-157">Set-AzApplicationGatewayBackendHttpSetting</span></span>](./Set-AzApplicationGatewayBackendHttpSetting.md)

