---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
ms.openlocfilehash: 0e3c0c9a3f1c47163a28dc1732ef488f87014c63
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880386"
---
# <span data-ttu-id="e77e6-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e77e6-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="e77e6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e77e6-102">SYNOPSIS</span></span>
<span data-ttu-id="e77e6-103">상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e77e6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e77e6-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e77e6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="e77e6-105">DESCRIPTION</span></span>
<span data-ttu-id="e77e6-106">New-AzureRmApplicationGatewayProbeConfig cmdlet은 상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="e77e6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="e77e6-107">EXAMPLES</span></span>

### <span data-ttu-id="e77e6-108">Example1: 상태 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="e77e6-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="e77e6-109">이 명령은 Probe03 이라는 상태 프로브 (HTTP 프로토콜, 30 초 간격, 120 초), 비정상 임계값 8 번 재시도 시간을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="e77e6-110">변수</span><span class="sxs-lookup"><span data-stu-id="e77e6-110">PARAMETERS</span></span>

### <span data-ttu-id="e77e6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e77e6-111">-DefaultProfile</span></span>
<span data-ttu-id="e77e6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e77e6-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="e77e6-113">-HostName</span></span>
<span data-ttu-id="e77e6-114">이 cmdlet가 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="e77e6-115">-Interval</span><span class="sxs-lookup"><span data-stu-id="e77e6-115">-Interval</span></span>
<span data-ttu-id="e77e6-116">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="e77e6-117">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="e77e6-118">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e77e6-119">-Match</span><span class="sxs-lookup"><span data-stu-id="e77e6-119">-Match</span></span>
<span data-ttu-id="e77e6-120">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="e77e6-121">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-121">Default value is empty</span></span>

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

### <span data-ttu-id="e77e6-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="e77e6-122">-MinServers</span></span>
<span data-ttu-id="e77e6-123">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="e77e6-124">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-124">Default value is 0</span></span>

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

### <span data-ttu-id="e77e6-125">-이름</span><span class="sxs-lookup"><span data-stu-id="e77e6-125">-Name</span></span>
<span data-ttu-id="e77e6-126">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="e77e6-127">-Path</span><span class="sxs-lookup"><span data-stu-id="e77e6-127">-Path</span></span>
<span data-ttu-id="e77e6-128">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="e77e6-129">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="e77e6-130">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="e77e6-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="e77e6-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="e77e6-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="e77e6-132">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="e77e6-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="e77e6-133">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-133">Default value is false</span></span>

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

### <span data-ttu-id="e77e6-134">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="e77e6-134">-Protocol</span></span>
<span data-ttu-id="e77e6-135">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="e77e6-136">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="e77e6-136">-Timeout</span></span>
<span data-ttu-id="e77e6-137">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="e77e6-138">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="e77e6-139">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="e77e6-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="e77e6-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="e77e6-141">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="e77e6-142">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="e77e6-143">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="e77e6-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e77e6-144">CommonParameters</span></span>
<span data-ttu-id="e77e6-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e77e6-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e77e6-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e77e6-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e77e6-147">입력</span><span class="sxs-lookup"><span data-stu-id="e77e6-147">INPUTS</span></span>

## <span data-ttu-id="e77e6-148">출력</span><span class="sxs-lookup"><span data-stu-id="e77e6-148">OUTPUTS</span></span>

### <span data-ttu-id="e77e6-149">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="e77e6-149">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="e77e6-150">상속자</span><span class="sxs-lookup"><span data-stu-id="e77e6-150">NOTES</span></span>

## <span data-ttu-id="e77e6-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e77e6-151">RELATED LINKS</span></span>

[<span data-ttu-id="e77e6-152">Azure Resource Manager 용 PowerShell을 사용 하 여 응용 프로그램 게이트웨이에 대 한 사용자 지정 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="e77e6-152">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="e77e6-153">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e77e6-153">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e77e6-154">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e77e6-154">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e77e6-155">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e77e6-155">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="e77e6-156">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="e77e6-156">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

