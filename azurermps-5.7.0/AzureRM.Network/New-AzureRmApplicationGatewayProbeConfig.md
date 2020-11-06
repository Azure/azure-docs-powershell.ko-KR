---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermapplicationgatewayprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmApplicationGatewayProbeConfig.md
ms.openlocfilehash: 955f5179340351dd662979385ca3d3dc2a39b9f7
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532736"
---
# <span data-ttu-id="bba42-101">New-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bba42-101">New-AzureRmApplicationGatewayProbeConfig</span></span>

## <span data-ttu-id="bba42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bba42-102">SYNOPSIS</span></span>
<span data-ttu-id="bba42-103">상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-103">Creates a health probe.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bba42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bba42-104">SYNTAX</span></span>

```
New-AzureRmApplicationGatewayProbeConfig -Name <String> -Protocol <String> [-HostName <String>] -Path <String>
 -Interval <Int32> -Timeout <Int32> -UnhealthyThreshold <Int32> [-PickHostNameFromBackendHttpSettings]
 [-MinServers <Int32>] [-Match <PSApplicationGatewayProbeHealthResponseMatch>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bba42-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bba42-105">DESCRIPTION</span></span>
<span data-ttu-id="bba42-106">New-AzureRmApplicationGatewayProbeConfig cmdlet은 상태 프로브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-106">The New-AzureRmApplicationGatewayProbeConfig cmdlet creates a health probe.</span></span>

## <span data-ttu-id="bba42-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bba42-107">EXAMPLES</span></span>

### <span data-ttu-id="bba42-108">Example1: 상태 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="bba42-108">Example1: Create a health probe</span></span>
```
PS C:\>New-AzureRmApplicationGatewayProbeConfig -Name "Probe03" -Protocol Http -HostName "contoso.com" -Path "/path/custompath.htm" -Interval 30 -Timeout 120 -UnhealthyThreshold 8
```

<span data-ttu-id="bba42-109">이 명령은 Probe03 이라는 상태 프로브 (HTTP 프로토콜, 30 초 간격, 120 초), 비정상 임계값 8 번 재시도 시간을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-109">This command creates a health probe named Probe03, with HTTP protocol, a 30 second interval, timeout of 120 seconds, and an unhealthy threshold of 8 retries.</span></span>

## <span data-ttu-id="bba42-110">변수</span><span class="sxs-lookup"><span data-stu-id="bba42-110">PARAMETERS</span></span>

### <span data-ttu-id="bba42-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bba42-111">-DefaultProfile</span></span>
<span data-ttu-id="bba42-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bba42-113">-HostName</span><span class="sxs-lookup"><span data-stu-id="bba42-113">-HostName</span></span>
<span data-ttu-id="bba42-114">이 cmdlet가 프로브를 보내는 호스트 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-114">Specifies the host name that this cmdlet sends the probe.</span></span>

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

### <span data-ttu-id="bba42-115">-Interval</span><span class="sxs-lookup"><span data-stu-id="bba42-115">-Interval</span></span>
<span data-ttu-id="bba42-116">검색 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-116">Specifies the probe interval in seconds.</span></span>
<span data-ttu-id="bba42-117">두 연속 프로브 간의 시간 간격입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-117">This is the time interval between two consecutive probes.</span></span>
<span data-ttu-id="bba42-118">이 값의 범위는 1 초에서 86400 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-118">This value is between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="bba42-119">-Match</span><span class="sxs-lookup"><span data-stu-id="bba42-119">-Match</span></span>
<span data-ttu-id="bba42-120">상태 응답에 포함 해야 하는 본문입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-120">Body that must be contained in the health response.</span></span>
<span data-ttu-id="bba42-121">Default 값이 비어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-121">Default value is empty</span></span>

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

### <span data-ttu-id="bba42-122">-MinServers</span><span class="sxs-lookup"><span data-stu-id="bba42-122">-MinServers</span></span>
<span data-ttu-id="bba42-123">항상 정상 상태로 표시 된 최소 서버 수입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-123">Minimum number of servers that are always marked healthy.</span></span>
<span data-ttu-id="bba42-124">기본값은 0입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-124">Default value is 0</span></span>

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

### <span data-ttu-id="bba42-125">-이름</span><span class="sxs-lookup"><span data-stu-id="bba42-125">-Name</span></span>
<span data-ttu-id="bba42-126">프로브의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-126">Specifies the name of the probe.</span></span>

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

### <span data-ttu-id="bba42-127">-Path</span><span class="sxs-lookup"><span data-stu-id="bba42-127">-Path</span></span>
<span data-ttu-id="bba42-128">프로브에 대 한 상대 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-128">Specifies the relative path of probe.</span></span>
<span data-ttu-id="bba42-129">유효한 경로는 슬래시 문자 (/)로 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-129">Valid paths start with the slash character (/).</span></span>
<span data-ttu-id="bba42-130">프로브가 \<Protocol\> //:로 전송 됩니다 \<host\> \<port\> \<path\> .</span><span class="sxs-lookup"><span data-stu-id="bba42-130">The probe is sent to \<Protocol\>://\<host\>:\<port\>\<path\>.</span></span>

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

### <span data-ttu-id="bba42-131">-PickHostNameFromBackendHttpSettings</span><span class="sxs-lookup"><span data-stu-id="bba42-131">-PickHostNameFromBackendHttpSettings</span></span>
<span data-ttu-id="bba42-132">백 엔드 http 설정에서 호스트 헤더를 선택 해야 하는지 여부</span><span class="sxs-lookup"><span data-stu-id="bba42-132">Whether the host header should be picked from the backend http settings.</span></span>
<span data-ttu-id="bba42-133">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-133">Default value is false</span></span>

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

### <span data-ttu-id="bba42-134">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="bba42-134">-Protocol</span></span>
<span data-ttu-id="bba42-135">프로브 전송에 사용 되는 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-135">Specifies the protocol used to send probe.</span></span>

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

### <span data-ttu-id="bba42-136">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="bba42-136">-Timeout</span></span>
<span data-ttu-id="bba42-137">프로브 시간 제한을 초 단위로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-137">Specifies the probe timeout in seconds.</span></span>
<span data-ttu-id="bba42-138">이 cmdlet은이 시간 초과 기간으로 유효한 응답을 받지 못한 경우 프로브를 실패로 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-138">This cmdlet marks the probe as failed if a valid response is not received with this timeout period.</span></span>
<span data-ttu-id="bba42-139">유효한 값의 범위는 1 초에서 86400 초입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-139">Valid values are between 1 second and 86400 seconds.</span></span>

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

### <span data-ttu-id="bba42-140">-UnhealthyThreshold</span><span class="sxs-lookup"><span data-stu-id="bba42-140">-UnhealthyThreshold</span></span>
<span data-ttu-id="bba42-141">프로브 재시도 횟수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-141">Specifies the probe retry count.</span></span>
<span data-ttu-id="bba42-142">연속 검색 실패 횟수가 비정상 임계값에 도달 하면 백 엔드 서버가 아래로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-142">The backend server is marked down after consecutive probe failure count reaches the unhealthy threshold.</span></span>
<span data-ttu-id="bba42-143">유효한 값의 범위는 1 초에서 20 초 사이입니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-143">Valid values are between 1 second and 20 seconds.</span></span>

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

### <span data-ttu-id="bba42-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bba42-144">CommonParameters</span></span>
<span data-ttu-id="bba42-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bba42-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bba42-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bba42-147">입력</span><span class="sxs-lookup"><span data-stu-id="bba42-147">INPUTS</span></span>

### <span data-ttu-id="bba42-148">않아야</span><span class="sxs-lookup"><span data-stu-id="bba42-148">None</span></span>
<span data-ttu-id="bba42-149">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bba42-149">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="bba42-150">출력</span><span class="sxs-lookup"><span data-stu-id="bba42-150">OUTPUTS</span></span>

### <span data-ttu-id="bba42-151">Microsoft. \*. m i m a. 모델. m i m a 검색</span><span class="sxs-lookup"><span data-stu-id="bba42-151">Microsoft.Azure.Commands.Network.Models.PSApplicationGatewayProbe</span></span>

## <span data-ttu-id="bba42-152">상속자</span><span class="sxs-lookup"><span data-stu-id="bba42-152">NOTES</span></span>

## <span data-ttu-id="bba42-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bba42-153">RELATED LINKS</span></span>

[<span data-ttu-id="bba42-154">Azure Resource Manager 용 PowerShell을 사용 하 여 응용 프로그램 게이트웨이에 대 한 사용자 지정 프로브 만들기</span><span class="sxs-lookup"><span data-stu-id="bba42-154">Create custom probe for Application Gateway using PowerShell for Azure Resource Manager</span></span>](https://azure.microsoft.com/en-us/documentation/articles/application-gateway-create-probe-ps/#)

[<span data-ttu-id="bba42-155">추가-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bba42-155">Add-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bba42-156">Get-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bba42-156">Get-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bba42-157">제거-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bba42-157">Remove-AzureRmApplicationGatewayProbeConfig</span></span>]()

[<span data-ttu-id="bba42-158">Set-AzureRmApplicationGatewayProbeConfig</span><span class="sxs-lookup"><span data-stu-id="bba42-158">Set-AzureRmApplicationGatewayProbeConfig</span></span>]()

