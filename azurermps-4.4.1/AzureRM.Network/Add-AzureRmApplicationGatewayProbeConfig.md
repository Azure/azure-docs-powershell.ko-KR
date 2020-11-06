---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Add-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 169a63248ebc499f577a635821131e0153e64433
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534000"
---
# <span data-ttu-id="1add1-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1add1-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="1add1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1add1-102">SYNOPSIS</span></span>
<span data-ttu-id="1add1-103">응용 프로그램 게이트웨이에 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1add1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1add1-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1add1-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1add1-105">DESCRIPTION</span></span>
<span data-ttu-id="1add1-106">Add-AzureRmApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="1add1-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1add1-107">EXAMPLES</span></span>

### <span data-ttu-id="1add1-108">예제 1: 응용 프로그램 게이트웨이에 상태 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="1add1-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="1add1-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 대 한 Probe01 이라는 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="1add1-110">또한이 명령은 비정상 임계값을 8 번 재시도로 설정 하 고 120 초 후에 시간 초과 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="1add1-111">변수</span><span class="sxs-lookup"><span data-stu-id="1add1-111">PARAMETERS</span></span>

### <span data-ttu-id="1add1-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1add1-112">-ApplicationGateway</span></span>
<span data-ttu-id="1add1-113">이 cmdlet이 프로브를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="1add1-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="1add1-114">-HostName</span></span>
<span data-ttu-id="1add1-115">이 cmdlet이 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="1add1-116">-Interval</span><span class="sxs-lookup"><span data-stu-id="1add1-116">-Interval</span></span>
<span data-ttu-id="1add1-117">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="1add1-118">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="1add1-119">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="1add1-120">-Match</span><span class="sxs-lookup"><span data-stu-id="1add1-120">-Match</span></span>
<span data-ttu-id="1add1-121">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="1add1-122">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-122">Default value is empty</span></span>

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

### <span data-ttu-id="1add1-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="1add1-123">-MinServers</span></span>
<span data-ttu-id="1add1-124">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="1add1-125">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-125">Default value is 0</span></span>

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

### <span data-ttu-id="1add1-126">-이름</span><span class="sxs-lookup"><span data-stu-id="1add1-126">-Name</span></span>
<span data-ttu-id="1add1-127">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="1add1-128">-Path</span><span class="sxs-lookup"><span data-stu-id="1add1-128">-Path</span></span>
<span data-ttu-id="1add1-129">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="1add1-130">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-130">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="1add1-131">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="1add1-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="1add1-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="1add1-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="1add1-133">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="1add1-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="1add1-134">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-134">Default value is false</span></span>

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

### <span data-ttu-id="1add1-135">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="1add1-135">-Protocol</span></span>
<span data-ttu-id="1add1-136">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-136">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="1add1-137">이 cmdlet은 HTTP만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-137">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="1add1-138">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="1add1-138">-Timeout</span></span>
<span data-ttu-id="1add1-139">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-139">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="1add1-140">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-140">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="1add1-141">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-141">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="1add1-142">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="1add1-142">-UnhealthyThreshold</span></span>
<span data-ttu-id="1add1-143">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-143">Specifies the probe retry count.</span></span>
<span data-ttu-id="1add1-144">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-144">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="1add1-145">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-145">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="1add1-146">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1add1-146">-DefaultProfile</span></span>
<span data-ttu-id="1add1-147">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-147">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1add1-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1add1-148">CommonParameters</span></span>
<span data-ttu-id="1add1-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1add1-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1add1-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1add1-151">입력</span><span class="sxs-lookup"><span data-stu-id="1add1-151">INPUTS</span></span>

### <span data-ttu-id="1add1-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1add1-152">PSApplicationGateway</span></span>
<span data-ttu-id="1add1-153">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1add1-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="1add1-154">출력</span><span class="sxs-lookup"><span data-stu-id="1add1-154">OUTPUTS</span></span>

### <span data-ttu-id="1add1-155">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="1add1-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="1add1-156">상속자</span><span class="sxs-lookup"><span data-stu-id="1add1-156">NOTES</span></span>

## <span data-ttu-id="1add1-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1add1-157">RELATED LINKS</span></span>

[<span data-ttu-id="1add1-158">기존 application gateway에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="1add1-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="1add1-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1add1-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1add1-160">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1add1-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1add1-161">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1add1-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="1add1-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="1add1-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

