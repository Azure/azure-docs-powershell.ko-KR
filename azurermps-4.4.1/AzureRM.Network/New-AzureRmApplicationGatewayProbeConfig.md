---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: a41daa12a126e768a4cc7842a72b031d4ca7a759
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534899"
---
# <span data-ttu-id="689ae-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="689ae-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="689ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="689ae-102">SYNOPSIS</span></span>
<span data-ttu-id="689ae-103">상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="689ae-104">구문과</span><span class="sxs-lookup"><span data-stu-id="689ae-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="689ae-105">설명은</span><span class="sxs-lookup"><span data-stu-id="689ae-105">DESCRIPTION</span></span>
<span data-ttu-id="689ae-106">New-AzureRmApplicationGatewayProbeConfig cmdlet은 상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="689ae-107">예제의</span><span class="sxs-lookup"><span data-stu-id="689ae-107">EXAMPLES</span></span>

### <span data-ttu-id="689ae-108">Example1: 상태 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="689ae-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="689ae-109">이 명령은 Probe03 이라는 상태 프로브 (HTTP 프로토콜, 30 초 간격, 120 초), 비정상 임계값 8 번 재시도 시간을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="689ae-110">변수</span><span class="sxs-lookup"><span data-stu-id="689ae-110">PARAMETERS</span></span>

### <span data-ttu-id="689ae-111">-HostName</span><span class="sxs-lookup"><span data-stu-id="689ae-111">-HostName</span></span>
<span data-ttu-id="689ae-112">이 cmdlet가 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-112">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="689ae-113">-Interval</span><span class="sxs-lookup"><span data-stu-id="689ae-113">-Interval</span></span>
<span data-ttu-id="689ae-114">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-114">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="689ae-115">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-115">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="689ae-116">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-116">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="689ae-117">-Match</span><span class="sxs-lookup"><span data-stu-id="689ae-117">-Match</span></span>
<span data-ttu-id="689ae-118">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-118">Body that must be contained in the health response.</span></span>
<span data-ttu-id="689ae-119">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-119">Default value is empty</span></span>

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

### <span data-ttu-id="689ae-120">-MinServers</span><span class="sxs-lookup"><span data-stu-id="689ae-120">-MinServers</span></span>
<span data-ttu-id="689ae-121">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-121">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="689ae-122">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-122">Default value is 0</span></span>

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

### <span data-ttu-id="689ae-123">-이름</span><span class="sxs-lookup"><span data-stu-id="689ae-123">-Name</span></span>
<span data-ttu-id="689ae-124">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-124">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="689ae-125">-Path</span><span class="sxs-lookup"><span data-stu-id="689ae-125">-Path</span></span>
<span data-ttu-id="689ae-126">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-126">Specifies the relative path of probe.</span></span>
<span data-ttu-id="689ae-127">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-127">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="689ae-128">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="689ae-128">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="689ae-129">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="689ae-129">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="689ae-130">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="689ae-130">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="689ae-131">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-131">Default value is false</span></span>

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

### <span data-ttu-id="689ae-132">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="689ae-132">-Protocol</span></span>
<span data-ttu-id="689ae-133">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-133">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="689ae-134">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="689ae-134">-Timeout</span></span>
<span data-ttu-id="689ae-135">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-135">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="689ae-136">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-136">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="689ae-137">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-137">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="689ae-138">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="689ae-138">-UnhealthyThreshold</span></span>
<span data-ttu-id="689ae-139">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-139">Specifies the probe retry count.</span></span>
<span data-ttu-id="689ae-140">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-140">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="689ae-141">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-141">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="689ae-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="689ae-142">-DefaultProfile</span></span>
<span data-ttu-id="689ae-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-143">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="689ae-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="689ae-144">CommonParameters</span></span>
<span data-ttu-id="689ae-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="689ae-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="689ae-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="689ae-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="689ae-147">입력</span><span class="sxs-lookup"><span data-stu-id="689ae-147">INPUTS</span></span>

## <span data-ttu-id="689ae-148">출력</span><span class="sxs-lookup"><span data-stu-id="689ae-148">OUTPUTS</span></span>

### <span data-ttu-id="689ae-149">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="689ae-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="689ae-150">상속자</span><span class="sxs-lookup"><span data-stu-id="689ae-150">NOTES</span></span>

## <span data-ttu-id="689ae-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="689ae-151">RELATED LINKS</span></span>

[<span data-ttu-id="689ae-152">Azure Resource Manager 용 PowerShell을 사용 하 여 응용 프로그램 게이트웨이에 대 한 사용자 지정 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="689ae-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="689ae-153">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="689ae-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="689ae-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="689ae-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="689ae-155">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="689ae-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="689ae-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="689ae-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

