---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azapplicationgatewaybackendhttpsetting
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzApplicationGatewayBackendHttpSetting.md
ms.openlocfilehash: 35742a6dc65bd84359d08f4e30533a0a49488053
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325905"
---
# <span data-ttu-id="e706e-101">Set-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e706e-101">Set-AzApplicationGatewayBackendHttpSetting</span></span>

## <span data-ttu-id="e706e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e706e-102">SYNOPSIS</span></span>
<span data-ttu-id="e706e-103">애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-103">Updates back-end HTTP settings for an application gateway.</span></span>

## <span data-ttu-id="e706e-104">구문</span><span class="sxs-lookup"><span data-stu-id="e706e-104">SYNTAX</span></span>

```
Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Port <Int32> -Protocol <String> -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <PSApplicationGatewayAuthenticationCertificate[]>]
 [-TrustedRootCertificate <PSApplicationGatewayTrustedRootCertificate[]>] [-PickHostNameFromBackendAddress]
 [-HostName <String>] [-AffinityCookieName <String>] [-Path <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e706e-105">설명</span><span class="sxs-lookup"><span data-stu-id="e706e-105">DESCRIPTION</span></span>
<span data-ttu-id="e706e-106">이 Set-AzApplicationGatewayBackendHttpSetting cmdlet은 Azure 애플리케이션 게이트웨이에 대한 백 엔드 HTTP(Hypertext Transfer Protocol) 설정을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-106">The Set-AzApplicationGatewayBackendHttpSetting cmdlet updates the back-end Hypertext Transfer Protocol (HTTP) settings for an Azure application gateway.</span></span>
<span data-ttu-id="e706e-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="e706e-108">예제</span><span class="sxs-lookup"><span data-stu-id="e706e-108">EXAMPLES</span></span>

### <span data-ttu-id="e706e-109">예제 1: 애플리케이션 게이트웨이에 대한 백 엔드 HTTP 설정 업데이트</span><span class="sxs-lookup"><span data-stu-id="e706e-109">Example 1: Update the back-end HTTP settings for an application gateway</span></span>
```
PS C:\>$AppGw = Get-AzApplicationGateway -Name "ApplicationGateway01" -ResourceGroupName "ResourceGroup01"
PS C:\> $AppGw = Set-AzApplicationGatewayBackendHttpSetting -ApplicationGateway $AppGw -Name "Setting02" -Port 88 -Protocol "Http" -CookieBasedAffinity "Disabled"
```

<span data-ttu-id="e706e-110">첫 번째 명령은 ResourceGroup01이라는 리소스 그룹에 속하는 ApplicationGateway01이라는 애플리케이션 게이트웨이를 $AppGw 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-110">The first command gets the application gateway named ApplicationGateway01 that belongs to the resource group named ResourceGroup01 and stores it in the $AppGw variable.</span></span>
<span data-ttu-id="e706e-111">두 번째 명령은 $AppGw 변수에서 애플리케이션 게이트웨이의 HTTP 설정을 업데이트하여 포트 88, HTTP 프로토콜을 사용하며 쿠키 기반의 효율성을 가능하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-111">The second command updates the HTTP settings of the application gateway in the $AppGw variable to use port 88, the HTTP protocol and enables cookie-based affinity.</span></span>

## <span data-ttu-id="e706e-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e706e-112">PARAMETERS</span></span>

### <span data-ttu-id="e706e-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="e706e-113">-AffinityCookieName</span></span>
<span data-ttu-id="e706e-114">Affinity 쿠키에 사용할 쿠키 이름</span><span class="sxs-lookup"><span data-stu-id="e706e-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="e706e-115">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706e-115">-ApplicationGateway</span></span>
<span data-ttu-id="e706e-116">이 cmdlet이 백 엔드 HTTP 설정을 연결하는 애플리케이션 게이트웨이 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-116">Specifies an application gateway object with which this cmdlet associates back-end HTTP settings.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGateway
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e706e-117">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="e706e-117">-AuthenticationCertificates</span></span>
<span data-ttu-id="e706e-118">애플리케이션 게이트웨이에 대한 인증 인증서를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-118">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="e706e-119">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="e706e-119">-ConnectionDraining</span></span>
<span data-ttu-id="e706e-120">백end http 설정 리소스의 연결 드레인입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-120">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="e706e-121">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="e706e-121">-CookieBasedAffinity</span></span>
<span data-ttu-id="e706e-122">백end 서버 풀에 대해 쿠키 기반의 효율성을 사용할지 또는 사용하지 않도록 설정해야 하는지 여부를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-122">Specifies whether cookie-based affinity should be enabled or disabled for the backend server pool.</span></span>
<span data-ttu-id="e706e-123">이 매개 변수에 허용되는 값은 Disabled 또는 Enabled입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-123">The acceptable values for this parameter are: Disabled or Enabled.</span></span>

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

### <span data-ttu-id="e706e-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e706e-124">-DefaultProfile</span></span>
<span data-ttu-id="e706e-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e706e-126">-HostName</span><span class="sxs-lookup"><span data-stu-id="e706e-126">-HostName</span></span>
<span data-ttu-id="e706e-127">백end 서버로 보낼 호스트 헤더를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-127">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="e706e-128">-Name</span><span class="sxs-lookup"><span data-stu-id="e706e-128">-Name</span></span>
<span data-ttu-id="e706e-129">백 엔드 HTTP 설정 개체의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-129">Specifies the name of the back-end HTTP settings object.</span></span>

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

### <span data-ttu-id="e706e-130">-Path</span><span class="sxs-lookup"><span data-stu-id="e706e-130">-Path</span></span>
<span data-ttu-id="e706e-131">모든 HTTP 요청에 대한 사전으로 사용되어야 하는 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-131">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="e706e-132">이 매개 변수에 대한 값이 제공되지 않았다면 경로가 추가되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-132">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="e706e-133">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="e706e-133">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="e706e-134">호스트 헤더를 백end 서버의 호스트 이름에서 선택해야 하는지 플래그를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-134">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="e706e-135">-Port</span><span class="sxs-lookup"><span data-stu-id="e706e-135">-Port</span></span>
<span data-ttu-id="e706e-136">백 엔드 서버 풀의 각 서버에 사용할 포트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-136">Specifies the port to use for each server in the back-end server pool.</span></span>

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

### <span data-ttu-id="e706e-137">-Probe</span><span class="sxs-lookup"><span data-stu-id="e706e-137">-Probe</span></span>
<span data-ttu-id="e706e-138">백 엔드 HTTP 설정과 연결하기 위해 프로브를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-138">Specifies a probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e706e-139">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="e706e-139">-ProbeId</span></span>
<span data-ttu-id="e706e-140">백 엔드 HTTP 설정과 연결하기 위해 프로브의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-140">Specifies the ID of the probe to associate with the back-end HTTP settings.</span></span>

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

### <span data-ttu-id="e706e-141">-Protocol</span><span class="sxs-lookup"><span data-stu-id="e706e-141">-Protocol</span></span>
<span data-ttu-id="e706e-142">애플리케이션 게이트웨이와 백 엔드 서버 간의 통신에 사용할 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-142">Specifies the protocol to use for communication between the application gateway and back-end servers.</span></span>
<span data-ttu-id="e706e-143">이 매개 변수에 허용되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-143">The acceptable values for this parameter are: Http and Https.</span></span>
<span data-ttu-id="e706e-144">이 매개 변수는 대소문자 구분입니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-144">This parameter is case-sensitive.</span></span>

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

### <span data-ttu-id="e706e-145">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="e706e-145">-RequestTimeout</span></span>
<span data-ttu-id="e706e-146">요청 시간 시간 값을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-146">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="e706e-147">-TrustedRootCertificate</span><span class="sxs-lookup"><span data-stu-id="e706e-147">-TrustedRootCertificate</span></span>
<span data-ttu-id="e706e-148">Application Gateway 신뢰할 수 있는 루트 인증서</span><span class="sxs-lookup"><span data-stu-id="e706e-148">Application gateway Trusted Root Certificates</span></span>

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

### <span data-ttu-id="e706e-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e706e-149">CommonParameters</span></span>
<span data-ttu-id="e706e-150">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e706e-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e706e-151">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="e706e-151">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e706e-152">입력</span><span class="sxs-lookup"><span data-stu-id="e706e-152">INPUTS</span></span>

### <span data-ttu-id="e706e-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706e-153">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e706e-154">출력</span><span class="sxs-lookup"><span data-stu-id="e706e-154">OUTPUTS</span></span>

### <span data-ttu-id="e706e-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="e706e-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="e706e-156">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e706e-156">NOTES</span></span>

## <span data-ttu-id="e706e-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e706e-157">RELATED LINKS</span></span>

[<span data-ttu-id="e706e-158">Add-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e706e-158">Add-AzApplicationGatewayBackendHttpSetting</span></span>](./Add-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e706e-159">Get-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e706e-159">Get-AzApplicationGatewayBackendHttpSetting</span></span>](./Get-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e706e-160">New-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e706e-160">New-AzApplicationGatewayBackendHttpSetting</span></span>](./New-AzApplicationGatewayBackendHttpSetting.md)

[<span data-ttu-id="e706e-161">Remove-AzApplicationGatewayBackendHttpSetting</span><span class="sxs-lookup"><span data-stu-id="e706e-161">Remove-AzApplicationGatewayBackendHttpSetting</span></span>](./Remove-AzApplicationGatewayBackendHttpSetting.md)

