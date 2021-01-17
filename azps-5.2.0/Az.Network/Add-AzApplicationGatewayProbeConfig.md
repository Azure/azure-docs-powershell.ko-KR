---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/add-azapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Add-AzApplicationGatewayProbeConfig.md
ms.openlocfilehash: cea6f92ba15e43d5977af03dfee1054240f5ecad
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98329846"
---
# <span data-ttu-id="f917a-101">Add-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f917a-101">Add-AzApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="f917a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f917a-102">SYNOPSIS</span></span>
<span data-ttu-id="f917a-103">Application Gateway에 상태 프로브를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-103">Adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f917a-104">구문</span><span class="sxs-lookup"><span data-stu-id="f917a-104">SYNTAX</span></span>

```
Add-AzApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f917a-105">설명</span><span class="sxs-lookup"><span data-stu-id="f917a-105">DESCRIPTION</span></span>
<span data-ttu-id="f917a-106">Add-AzApplicationGatewayProbeConfig cmdlet은 Application Gateway에 상태 프로브를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-106">The Add-AzApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="f917a-107">예제</span><span class="sxs-lookup"><span data-stu-id="f917a-107">EXAMPLES</span></span>

### <span data-ttu-id="f917a-108">예제 1: 애플리케이션 게이트웨이에 상태 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="f917a-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="f917a-109">이 명령은 Gateway라는 애플리케이션 게이트웨이에 대해 Probe01이라는 상태 프로브를 추가합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="f917a-110">또한 이 명령은 Unhealthy 임계값을 8회 재시도로 설정하고 120초 후에 시간 초과됩니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="f917a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f917a-111">PARAMETERS</span></span>

### <span data-ttu-id="f917a-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f917a-112">-ApplicationGateway</span></span>
<span data-ttu-id="f917a-113">이 cmdlet이 프로브를 추가할 애플리케이션 게이트웨이를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="f917a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f917a-114">-DefaultProfile</span></span>
<span data-ttu-id="f917a-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f917a-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="f917a-116">-HostName</span></span>
<span data-ttu-id="f917a-117">이 cmdlet이 프로브를 보내는 호스트 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="f917a-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="f917a-118">-Interval</span></span>
<span data-ttu-id="f917a-119">프로브 간격을 초로 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="f917a-120">이 간격은 두 개의 연속 프로브 사이의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="f917a-121">이 값은 1초에서 86400초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f917a-122">-Match</span><span class="sxs-lookup"><span data-stu-id="f917a-122">-Match</span></span>
<span data-ttu-id="f917a-123">상태 응답에 포함되어야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="f917a-124">기본값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-124">Default value is empty</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f917a-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="f917a-125">-MinServers</span></span>
<span data-ttu-id="f917a-126">항상 정상으로 표시된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="f917a-127">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-127">Default value is 0</span></span>

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

### <span data-ttu-id="f917a-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f917a-128">-Name</span></span>
<span data-ttu-id="f917a-129">프로브의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="f917a-130">-Path</span><span class="sxs-lookup"><span data-stu-id="f917a-130">-Path</span></span>
<span data-ttu-id="f917a-131">프로브의 상대 경로를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="f917a-132">유효한 경로는 슬래시 문자(/)로 시작됩니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="f917a-133">프로브는 \<Protocol\> :// \<host\> : \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="f917a-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="f917a-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="f917a-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="f917a-135">호스트 헤더를 백end http 설정에서 선택해야 하는지 여부입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="f917a-136">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-136">Default value is false</span></span>

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

### <span data-ttu-id="f917a-137">-Protocol</span><span class="sxs-lookup"><span data-stu-id="f917a-137">-Protocol</span></span>
<span data-ttu-id="f917a-138">프로브를 보내는 데 사용되는 프로토콜을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="f917a-139">이 cmdlet은 HTTP만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="f917a-140">-Timeout</span><span class="sxs-lookup"><span data-stu-id="f917a-140">-Timeout</span></span>
<span data-ttu-id="f917a-141">프로브 시간 제한(초)을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="f917a-142">이 cmdlet은 이 시간 제한 기간에 유효한 응답을 받지 못한 경우 프로브를 실패로 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="f917a-143">유효한 값은 1초에서 86400초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="f917a-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="f917a-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="f917a-145">프로브 재시도 횟수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="f917a-146">연속 프로브 실패 횟수가 이상 임계값에 도달하면 백엔드 서버가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="f917a-147">유효한 값은 1초에서 20초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="f917a-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f917a-148">CommonParameters</span></span>
<span data-ttu-id="f917a-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f917a-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f917a-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f917a-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f917a-151">입력</span><span class="sxs-lookup"><span data-stu-id="f917a-151">INPUTS</span></span>

### <span data-ttu-id="f917a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f917a-152">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f917a-153">출력</span><span class="sxs-lookup"><span data-stu-id="f917a-153">OUTPUTS</span></span>

### <span data-ttu-id="f917a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="f917a-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="f917a-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f917a-155">NOTES</span></span>

## <span data-ttu-id="f917a-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f917a-156">RELATED LINKS</span></span>

[<span data-ttu-id="f917a-157">기존 애플리케이션 게이트웨이에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="f917a-157">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="f917a-158">Get-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f917a-158">Get-AzApplicationGatewayProbeConfig</span></span>](./Get-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f917a-159">New-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f917a-159">New-AzApplicationGatewayProbeConfig</span></span>](./New-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f917a-160">Remove-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f917a-160">Remove-AzApplicationGatewayProbeConfig</span></span>](./Remove-AzApplicationGatewayProbeConfig.md)

[<span data-ttu-id="f917a-161">Set-AzApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="f917a-161">Set-AzApplicationGatewayProbeConfig</span></span>](./Set-AzApplicationGatewayProbeConfig.md)

