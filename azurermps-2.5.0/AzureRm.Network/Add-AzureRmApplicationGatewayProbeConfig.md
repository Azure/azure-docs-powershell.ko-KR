---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/add-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 87c064cbd3672a5e8d8f198432de87c0facf29cd
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882209"
---
# <span data-ttu-id="ca575-101">Add-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ca575-101">Add-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="ca575-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ca575-102">SYNOPSIS</span></span>
<span data-ttu-id="ca575-103">응용 프로그램 게이트웨이에 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-103">Adds a health probe to an Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ca575-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ca575-104">SYNTAX</span></span>

```
Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="ca575-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ca575-105">DESCRIPTION</span></span>
<span data-ttu-id="ca575-106">Add-AzureRmApplicationGatewayProbeConfig cmdlet은 응용 프로그램 게이트웨이에 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-106">The Add-AzureRmApplicationGatewayProbeConfig cmdlet adds a health probe to an Application Gateway.</span></span>

## <span data-ttu-id="ca575-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ca575-107">EXAMPLES</span></span>

### <span data-ttu-id="ca575-108">예제 1: 응용 프로그램 게이트웨이에 상태 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="ca575-108">Example 1: Add a health probe to an application gateway</span></span>
```
PS C:\>$Probe = Add-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe01" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="ca575-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 대 한 Probe01 이라는 상태 프로브를 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-109">This command adds a health probe named Probe01 for the application gateway named Gateway.</span></span>
<span data-ttu-id="ca575-110">또한이 명령은 비정상 임계값을 8 번 재시도로 설정 하 고 120 초 후에 시간 초과 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="ca575-111">변수</span><span class="sxs-lookup"><span data-stu-id="ca575-111">PARAMETERS</span></span>

### <span data-ttu-id="ca575-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca575-112">-ApplicationGateway</span></span>
<span data-ttu-id="ca575-113">이 cmdlet이 프로브를 추가 하는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-113">Specifies the application gateway to which this cmdlet adds a probe.</span></span>

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

### <span data-ttu-id="ca575-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ca575-114">-DefaultProfile</span></span>
<span data-ttu-id="ca575-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ca575-116">-HostName</span><span class="sxs-lookup"><span data-stu-id="ca575-116">-HostName</span></span>
<span data-ttu-id="ca575-117">이 cmdlet이 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-117">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="ca575-118">-Interval</span><span class="sxs-lookup"><span data-stu-id="ca575-118">-Interval</span></span>
<span data-ttu-id="ca575-119">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-119">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="ca575-120">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-120">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="ca575-121">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-121">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ca575-122">-Match</span><span class="sxs-lookup"><span data-stu-id="ca575-122">-Match</span></span>
<span data-ttu-id="ca575-123">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-123">Body that must be contained in the health response.</span></span>
<span data-ttu-id="ca575-124">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-124">Default value is empty</span></span>

```yaml
Type: PSApplicationGatewayProbeHealthResponseMatch
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ca575-125">-MinServers</span><span class="sxs-lookup"><span data-stu-id="ca575-125">-MinServers</span></span>
<span data-ttu-id="ca575-126">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-126">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="ca575-127">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-127">Default value is 0</span></span>

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

### <span data-ttu-id="ca575-128">-이름</span><span class="sxs-lookup"><span data-stu-id="ca575-128">-Name</span></span>
<span data-ttu-id="ca575-129">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-129">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="ca575-130">-Path</span><span class="sxs-lookup"><span data-stu-id="ca575-130">-Path</span></span>
<span data-ttu-id="ca575-131">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-131">Specifies the relative path of probe.</span></span>
<span data-ttu-id="ca575-132">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-132">Valid path start with the slash character (/).</span></span>
<span data-ttu-id="ca575-133">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="ca575-133">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="ca575-134">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="ca575-134">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="ca575-135">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="ca575-135">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="ca575-136">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-136">Default value is false</span></span>

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

### <span data-ttu-id="ca575-137">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="ca575-137">-Protocol</span></span>
<span data-ttu-id="ca575-138">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-138">Specifies the protocol used to send probe.</span></span>
<span data-ttu-id="ca575-139">이 cmdlet은 HTTP만 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-139">This cmdlet supports HTTP only.</span></span>

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

### <span data-ttu-id="ca575-140">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="ca575-140">-Timeout</span></span>
<span data-ttu-id="ca575-141">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-141">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="ca575-142">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-142">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="ca575-143">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-143">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="ca575-144">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="ca575-144">-UnhealthyThreshold</span></span>
<span data-ttu-id="ca575-145">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-145">Specifies the probe retry count.</span></span>
<span data-ttu-id="ca575-146">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-146">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="ca575-147">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-147">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="ca575-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ca575-148">CommonParameters</span></span>
<span data-ttu-id="ca575-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ca575-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ca575-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ca575-151">입력</span><span class="sxs-lookup"><span data-stu-id="ca575-151">INPUTS</span></span>

### <span data-ttu-id="ca575-152">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca575-152">PSApplicationGateway</span></span>
<span data-ttu-id="ca575-153">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ca575-153">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="ca575-154">출력</span><span class="sxs-lookup"><span data-stu-id="ca575-154">OUTPUTS</span></span>

### <span data-ttu-id="ca575-155">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="ca575-155">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="ca575-156">상속자</span><span class="sxs-lookup"><span data-stu-id="ca575-156">NOTES</span></span>

## <span data-ttu-id="ca575-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ca575-157">RELATED LINKS</span></span>

[<span data-ttu-id="ca575-158">기존 application gateway에 프로브 추가</span><span class="sxs-lookup"><span data-stu-id="ca575-158">Add a probe to an existing application gateway</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#add-a-probe-to-an-existing-application-gateway)

[<span data-ttu-id="ca575-159">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ca575-159">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ca575-160">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ca575-160">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ca575-161">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ca575-161">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="ca575-162">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ca575-162">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

