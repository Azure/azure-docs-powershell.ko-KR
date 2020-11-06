---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Set-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 212e418c3fdaf8ba7f67ebdae0565d5d230daa0d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530762"
---
# <span data-ttu-id="7014b-101">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7014b-101">Set-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="7014b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7014b-102">SYNOPSIS</span></span>
<span data-ttu-id="7014b-103">기존 응용 프로그램 게이트웨이에서 상태 프로브 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-103">Sets the health probe configuration on an existing Application Gateway.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7014b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7014b-104">SYNTAX</span></span>

```
Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway <PSApplicationGateway> -Name <String>
 -Protocol <String> [-HostName <String>] -Path <String> -Interval <Int32> -Timeout <Int32>
 -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings] [-MinServers <Int32>]
 [-Match <PSApplicationGatewayProbeHealthResponseMatch>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7014b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7014b-105">DESCRIPTION</span></span>
<span data-ttu-id="7014b-106">Set-AzureRmApplicationGatewayProbeConfig cmdlet은 기존 응용 프로그램 게이트웨이에서 상태 프로브 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-106">The Set-AzureRmApplicationGatewayProbeConfig cmdlet sets the health probe configuration on an existing Application Gateway.</span></span>

## <span data-ttu-id="7014b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7014b-107">EXAMPLES</span></span>

### <span data-ttu-id="7014b-108">예제 1: 응용 프로그램 게이트웨이에서 상태 프로브에 대 한 구성 설정</span><span class="sxs-lookup"><span data-stu-id="7014b-108">Example 1: Set the configuration for a health probe on an application gateway</span></span>
```
PS C:\>Set-AzureRmApplicationGatewayProbeConfig -ApplicationGateway Gateway -Name "Probe05" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="7014b-109">이 명령은 Gateway 라는 응용 프로그램 게이트웨이에 대 한 Probe05 이라는 상태 프로브에 대 한 구성을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-109">This command sets the configuration for a health probe named Probe05 for the application gateway named Gateway.</span></span>
<span data-ttu-id="7014b-110">또한이 명령은 비정상 임계값을 8 번 재시도로 설정 하 고 120 초 후에 시간 초과 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-110">The command also sets the unhealthy threshold to 8 retries and times out after 120 seconds.</span></span>

## <span data-ttu-id="7014b-111">변수</span><span class="sxs-lookup"><span data-stu-id="7014b-111">PARAMETERS</span></span>

### <span data-ttu-id="7014b-112">-ApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7014b-112">-ApplicationGateway</span></span>
<span data-ttu-id="7014b-113">이 cmdlet이 프로브를 보내는 응용 프로그램 게이트웨이를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-113">Specifies the application gateway to which this cmdlet sends a probe.</span></span>

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

### <span data-ttu-id="7014b-114">-HostName</span><span class="sxs-lookup"><span data-stu-id="7014b-114">-HostName</span></span>
<span data-ttu-id="7014b-115">이 cmdlet이 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-115">Specifies the host name that this cmdlet sends the probe to.</span></span>

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

### <span data-ttu-id="7014b-116">-Interval</span><span class="sxs-lookup"><span data-stu-id="7014b-116">-Interval</span></span>
<span data-ttu-id="7014b-117">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-117">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="7014b-118">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-118">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="7014b-119">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-119">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="7014b-120">-Match</span><span class="sxs-lookup"><span data-stu-id="7014b-120">-Match</span></span>
<span data-ttu-id="7014b-121">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-121">Body that must be contained in the health response.</span></span>
<span data-ttu-id="7014b-122">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-122">Default value is empty</span></span>

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

### <span data-ttu-id="7014b-123">-MinServers</span><span class="sxs-lookup"><span data-stu-id="7014b-123">-MinServers</span></span>
<span data-ttu-id="7014b-124">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-124">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="7014b-125">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-125">Default value is 0</span></span>

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

### <span data-ttu-id="7014b-126">-이름</span><span class="sxs-lookup"><span data-stu-id="7014b-126">-Name</span></span>
<span data-ttu-id="7014b-127">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-127">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="7014b-128">-Path</span><span class="sxs-lookup"><span data-stu-id="7014b-128">-Path</span></span>
<span data-ttu-id="7014b-129">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-129">Specifies the relative path of probe.</span></span>
<span data-ttu-id="7014b-130">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-130">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="7014b-131">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="7014b-131">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="7014b-132">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="7014b-132">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="7014b-133">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="7014b-133">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="7014b-134">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-134">Default value is false</span></span>

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

### <span data-ttu-id="7014b-135">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="7014b-135">-Protocol</span></span>
<span data-ttu-id="7014b-136">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-136">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="7014b-137">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="7014b-137">-Timeout</span></span>
<span data-ttu-id="7014b-138">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-138">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="7014b-139">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-139">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="7014b-140">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-140">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="7014b-141">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="7014b-141">-UnhealthyThreshold</span></span>
<span data-ttu-id="7014b-142">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-142">Specifies the probe retry count.</span></span>
<span data-ttu-id="7014b-143">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-143">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="7014b-144">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-144">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="7014b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7014b-145">-DefaultProfile</span></span>
<span data-ttu-id="7014b-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-146">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7014b-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7014b-147">CommonParameters</span></span>
<span data-ttu-id="7014b-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7014b-149">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7014b-149">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7014b-150">입력</span><span class="sxs-lookup"><span data-stu-id="7014b-150">INPUTS</span></span>

### <span data-ttu-id="7014b-151">PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7014b-151">PSApplicationGateway</span></span>
<span data-ttu-id="7014b-152">' ApplicationGateway ' 매개 변수는 파이프라인에서 ' PSApplicationGateway ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="7014b-152">Parameter 'ApplicationGateway' accepts value of type 'PSApplicationGateway' from the pipeline</span></span>

## <span data-ttu-id="7014b-153">출력</span><span class="sxs-lookup"><span data-stu-id="7014b-153">OUTPUTS</span></span>

### <span data-ttu-id="7014b-154">Microsoft. \* PSApplicationGateway</span><span class="sxs-lookup"><span data-stu-id="7014b-154">Microsoft.Azure.Commands.Network.Models.PSApplicationGateway</span></span>

## <span data-ttu-id="7014b-155">상속자</span><span class="sxs-lookup"><span data-stu-id="7014b-155">NOTES</span></span>

## <span data-ttu-id="7014b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7014b-156">RELATED LINKS</span></span>

[<span data-ttu-id="7014b-157">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7014b-157">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7014b-158">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7014b-158">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7014b-159">새로운 AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7014b-159">New-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="7014b-160">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="7014b-160">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

