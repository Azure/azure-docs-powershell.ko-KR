---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayBackendHttpSettings.md
ms.openlocfilehash: 6183b3cd61380b139bd74d676c6ab5225bf338fe
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532217"
---
# <span data-ttu-id="c2fff-101">New-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2fff-101">New-AzureRmApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c2fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fff-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fff-103">응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-103">Creates back-end HTTP settings for an application gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2fff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2fff-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayBackendHttpSettings -Name <String> -Port <Int32> -Protocol <String>
 -CookieBasedAffinity <String> [-RequestTimeout <Int32>]
 [-ConnectionDraining <PSApplicationGatewayConnectionDraining>] [-ProbeId <String>]
 [-Probe <PSApplicationGatewayProbe>]
 [-AuthenticationCertificates <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayAuthenticationCertificate]>]
 [-PickHostNameFromBackendAddress] [-HostName <String>] [-AffinityCookieName <String>] [-ProbeEnabled]
 [-Path <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2fff-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c2fff-105">DESCRIPTION</span></span>
<span data-ttu-id="c2fff-106">New-AzureRmApplicationGatewayBackendHttpSettings cmdlet은 응용 프로그램 게이트웨이에 대 한 백 엔드 HTTP 설정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-106">The New-AzureRmApplicationGatewayBackendHttpSettings cmdlet creates back-end HTTP settings for an application gateway.</span></span>
<span data-ttu-id="c2fff-107">백 엔드 HTTP 설정은 풀의 모든 백 엔드 서버에 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-107">Back-end HTTP settings are applied to all back-end servers in a pool.</span></span>

## <span data-ttu-id="c2fff-108">예제의</span><span class="sxs-lookup"><span data-stu-id="c2fff-108">EXAMPLES</span></span>

### <span data-ttu-id="c2fff-109">예제 1: 백 엔드 HTTP 설정 만들기</span><span class="sxs-lookup"><span data-stu-id="c2fff-109">Example 1: Create back-end HTTP settings</span></span>
```
PS C:\>$Setting = New-AzureRmApplicationGatewayBackendHttpSettings -Name "Setting01" -Port 80 -Protocol Http -CookieBasedAffinity Disabled
```

<span data-ttu-id="c2fff-110">이 명령은 HTTP 프로토콜을 사용 하 여 포트 80에서 Setting01 라는 백 엔드 HTTP 설정을 만들고, 쿠키 기반 선호도는 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-110">This command creates back-end HTTP settings named Setting01 on port 80, using the HTTP protocol, with cookie-based affinity disabled.</span></span>
<span data-ttu-id="c2fff-111">설정이 $Setting 변수에 저장 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-111">The settings are stored in the $Setting variable.</span></span>

## <span data-ttu-id="c2fff-112">변수</span><span class="sxs-lookup"><span data-stu-id="c2fff-112">PARAMETERS</span></span>

### <span data-ttu-id="c2fff-113">-AffinityCookieName</span><span class="sxs-lookup"><span data-stu-id="c2fff-113">-AffinityCookieName</span></span>
<span data-ttu-id="c2fff-114">선호도 쿠키에 사용할 쿠키 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-114">Cookie name to use for the affinity cookie</span></span>

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

### <span data-ttu-id="c2fff-115">-AuthenticationCertificates</span><span class="sxs-lookup"><span data-stu-id="c2fff-115">-AuthenticationCertificates</span></span>
<span data-ttu-id="c2fff-116">Application gateway에 대 한 인증 인증서를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-116">Specifies authentication certificates for the application gateway.</span></span>

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

### <span data-ttu-id="c2fff-117">-ConnectionDraining</span><span class="sxs-lookup"><span data-stu-id="c2fff-117">-ConnectionDraining</span></span>
<span data-ttu-id="c2fff-118">백 엔드 http 설정 리소스의 연결 드레이닝</span><span class="sxs-lookup"><span data-stu-id="c2fff-118">Connection draining of the backend http settings resource.</span></span>

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

### <span data-ttu-id="c2fff-119">-CookieBasedAffinity</span><span class="sxs-lookup"><span data-stu-id="c2fff-119">-CookieBasedAffinity</span></span>
<span data-ttu-id="c2fff-120">백 엔드 서버 풀에 대해 쿠키 기반 선호도를 사용할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-120">Specifies whether cookie-based affinity should be enabled or disabled for the back-end server pool.</span></span>

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

### <span data-ttu-id="c2fff-121">-HostName</span><span class="sxs-lookup"><span data-stu-id="c2fff-121">-HostName</span></span>
<span data-ttu-id="c2fff-122">백 엔드 서버로 보낼 호스트 헤더를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-122">Sets host header to be sent to the backend servers.</span></span>

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

### <span data-ttu-id="c2fff-123">-이름</span><span class="sxs-lookup"><span data-stu-id="c2fff-123">-Name</span></span>
<span data-ttu-id="c2fff-124">이 cmdlet이 만드는 백 엔드 HTTP 설정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-124">Specifies the name of the back-end HTTP settings that this cmdlet creates.</span></span>

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

### <span data-ttu-id="c2fff-125">-Path</span><span class="sxs-lookup"><span data-stu-id="c2fff-125">-Path</span></span>
<span data-ttu-id="c2fff-126">모든 HTTP 요청에 대 한 접두사로 사용할 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-126">Path which should be used as a prefix for all HTTP requests.</span></span>
<span data-ttu-id="c2fff-127">이 매개 변수에 대 한 값을 제공 하지 않으면 경로에 접두사를 붙일 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-127">If no value is provided for this parameter, then no path will be prefixed.</span></span>

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

### <span data-ttu-id="c2fff-128">-PickHostNameFromBackendAddress</span><span class="sxs-lookup"><span data-stu-id="c2fff-128">-PickHostNameFromBackendAddress</span></span>
<span data-ttu-id="c2fff-129">백 엔드 서버의 호스트 이름에서 호스트 헤더를 선택 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-129">Flag if host header should be picked from the host name of the backend server.</span></span>

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

### <span data-ttu-id="c2fff-130">-포트</span><span class="sxs-lookup"><span data-stu-id="c2fff-130">-Port</span></span>
<span data-ttu-id="c2fff-131">백 엔드 서버 풀의 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-131">Specifies the port of the back-end server pool.</span></span>

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

### <span data-ttu-id="c2fff-132">-프로브</span><span class="sxs-lookup"><span data-stu-id="c2fff-132">-Probe</span></span>
<span data-ttu-id="c2fff-133">백 엔드 서버 풀에 연결 하는 프로브를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-133">Specifies a probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="c2fff-134">-ProbeEnabled</span><span class="sxs-lookup"><span data-stu-id="c2fff-134">-ProbeEnabled</span></span>
<span data-ttu-id="c2fff-135">프로브를 사용 해야 하는 경우의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-135">Flag if probe should be enabled.</span></span>

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

### <span data-ttu-id="c2fff-136">-ProbeId</span><span class="sxs-lookup"><span data-stu-id="c2fff-136">-ProbeId</span></span>
<span data-ttu-id="c2fff-137">백 엔드 서버 풀에 연결할 프로브 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-137">Specifies the ID of the probe to associate with the back-end server pool.</span></span>

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

### <span data-ttu-id="c2fff-138">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="c2fff-138">-Protocol</span></span>
<span data-ttu-id="c2fff-139">응용 프로그램 게이트웨이와 백 엔드 서버 간의 통신에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-139">Specifies the protocol to use for communication between the application gateway and the back-end servers.</span></span>
<span data-ttu-id="c2fff-140">이 매개 변수에 허용 되는 값은 Http 및 Https입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-140">The acceptable values for this parameter are: Http and Https.</span></span>

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

### <span data-ttu-id="c2fff-141">-RequestTimeout</span><span class="sxs-lookup"><span data-stu-id="c2fff-141">-RequestTimeout</span></span>
<span data-ttu-id="c2fff-142">요청 시간 초과 값을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-142">Specifies a request time-out value.</span></span>

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

### <span data-ttu-id="c2fff-143">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fff-143">-DefaultProfile</span></span>
<span data-ttu-id="c2fff-144">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-144">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2fff-145">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fff-145">CommonParameters</span></span>
<span data-ttu-id="c2fff-146">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2fff-146">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fff-147">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2fff-147">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fff-148">입력</span><span class="sxs-lookup"><span data-stu-id="c2fff-148">INPUTS</span></span>

### <span data-ttu-id="c2fff-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c2fff-149">System.String</span></span>

## <span data-ttu-id="c2fff-150">출력</span><span class="sxs-lookup"><span data-stu-id="c2fff-150">OUTPUTS</span></span>

### <span data-ttu-id="c2fff-151">PSApplicationGatewayBackendHttpSettings에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c2fff-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayBackendHttpSettings</span></span>

## <span data-ttu-id="c2fff-152">상속자</span><span class="sxs-lookup"><span data-stu-id="c2fff-152">NOTES</span></span>

## <span data-ttu-id="c2fff-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2fff-153">RELATED LINKS</span></span>

[<span data-ttu-id="c2fff-154">추가-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2fff-154">Add-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2fff-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2fff-155">Get-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2fff-156">제거-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2fff-156">Remove-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

[<span data-ttu-id="c2fff-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="c2fff-157">Set-AzureRmApplicationGatewayBackendHttpSettings</span></span>]()

