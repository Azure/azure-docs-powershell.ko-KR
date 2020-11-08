---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitorprotocolconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject.md
ms.openlocfilehash: 5a0994a5328390a928fd60cda8e8004deaaab162
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034480"
---
# <span data-ttu-id="efd58-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="efd58-101">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject</span></span>

## <span data-ttu-id="efd58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="efd58-102">SYNOPSIS</span></span>
<span data-ttu-id="efd58-103">TCP, HTTP 또는 ICMP를 통해 테스트 평가를 수행 하는 데 사용 되는 프로토콜 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-103">Create protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="efd58-104">구문과</span><span class="sxs-lookup"><span data-stu-id="efd58-104">SYNTAX</span></span>

### <span data-ttu-id="efd58-105">NET.TCP</span><span class="sxs-lookup"><span data-stu-id="efd58-105">TCP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-TcpProtocol] -Port <Int32>
 [-DisableTraceRoute] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efd58-106">HTTP</span><span class="sxs-lookup"><span data-stu-id="efd58-106">HTTP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-HttpProtocol] [-Port <Int32>]
 [-Method <String>] [-Path <String>] [-RequestHeader <Hashtable>] [-ValidStatusCodeRange <String[]>]
 [-PreferHTTPS] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="efd58-107">차단한 ICMP</span><span class="sxs-lookup"><span data-stu-id="efd58-107">ICMP</span></span>
```
New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject [-IcmpProtocol] [-DisableTraceRoute]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="efd58-108">설명은</span><span class="sxs-lookup"><span data-stu-id="efd58-108">DESCRIPTION</span></span>
<span data-ttu-id="efd58-109">New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet은 TCP, HTTP 또는 ICMP를 통해 테스트 평가를 수행 하는 데 사용 되는 프로토콜 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-109">The New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject cmdlet creates protocol configuration used to perform test evaluation over TCP, HTTP or ICMP.</span></span>

## <span data-ttu-id="efd58-110">예제의</span><span class="sxs-lookup"><span data-stu-id="efd58-110">EXAMPLES</span></span>

### <span data-ttu-id="efd58-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="efd58-111">Example 1</span></span>
```powershell
PS C:\>$TcpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -TcpProtocol -Port 80 -DisableTraceRoute $false
```

<span data-ttu-id="efd58-112">포트: 80 DisableTraceRoute: False</span><span class="sxs-lookup"><span data-stu-id="efd58-112">Port              : 80 DisableTraceRoute : False</span></span>

## <span data-ttu-id="efd58-113">변수</span><span class="sxs-lookup"><span data-stu-id="efd58-113">PARAMETERS</span></span>

### <span data-ttu-id="efd58-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="efd58-114">-DefaultProfile</span></span>
<span data-ttu-id="efd58-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="efd58-116">-DisableTraceRoute</span><span class="sxs-lookup"><span data-stu-id="efd58-116">-DisableTraceRoute</span></span>
<span data-ttu-id="efd58-117">추적 경로를 사용한 경로 평가를 사용 하지 않아야 하는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-117">Value indicating whether path evaluation with trace route should be disabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP, ICMP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-118">-HttpProtocol</span><span class="sxs-lookup"><span data-stu-id="efd58-118">-HttpProtocol</span></span>
<span data-ttu-id="efd58-119">HTTP 프로토콜 스위치</span><span class="sxs-lookup"><span data-stu-id="efd58-119">HTTP protocol switch</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-120">-IcmpProtocol</span><span class="sxs-lookup"><span data-stu-id="efd58-120">-IcmpProtocol</span></span>
<span data-ttu-id="efd58-121">ICMP 프로토콜 스위치.</span><span class="sxs-lookup"><span data-stu-id="efd58-121">ICMP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ICMP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-122">-메서드</span><span class="sxs-lookup"><span data-stu-id="efd58-122">-Method</span></span>
<span data-ttu-id="efd58-123">사용할 HTTP 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-123">The HTTP method to use.</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-124">-Path</span><span class="sxs-lookup"><span data-stu-id="efd58-124">-Path</span></span>
<span data-ttu-id="efd58-125">URI의 경로 구성 요소입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-125">The path component of the URI.</span></span> <span data-ttu-id="efd58-126">예를 들어 \" /t1/2 \"</span><span class="sxs-lookup"><span data-stu-id="efd58-126">For instance, \"/dir1/dir2\".</span></span>

```yaml
Type: System.String
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-127">-포트</span><span class="sxs-lookup"><span data-stu-id="efd58-127">-Port</span></span>
<span data-ttu-id="efd58-128">연결할 포트입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-128">The port to connect to.</span></span>

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.Nullable`1[System.UInt16]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-129">-PreferHTTPS</span><span class="sxs-lookup"><span data-stu-id="efd58-129">-PreferHTTPS</span></span>
<span data-ttu-id="efd58-130">Choice가 명시적이 아닌 경우 HTTP를 통해 HTTPS가 기본 설정 되어 있는지 여부를 나타내는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-130">Value indicating whether HTTPS is preferred over HTTP in cases where the choice is not explicit.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-131">-RequestHeader</span><span class="sxs-lookup"><span data-stu-id="efd58-131">-RequestHeader</span></span>
<span data-ttu-id="efd58-132">요청과 함께 전송할 HTTP 헤더입니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-132">The HTTP headers to transmit with the request.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-133">-TcpProtocol</span><span class="sxs-lookup"><span data-stu-id="efd58-133">-TcpProtocol</span></span>
<span data-ttu-id="efd58-134">TCP 프로토콜 스위치.</span><span class="sxs-lookup"><span data-stu-id="efd58-134">TCP protocol switch.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: TCP
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-135">-ValidStatusCodeRange</span><span class="sxs-lookup"><span data-stu-id="efd58-135">-ValidStatusCodeRange</span></span>
<span data-ttu-id="efd58-136">HTTP 상태 코드를 성공적으로 고려 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-136">HTTP status codes to consider successful.</span></span> <span data-ttu-id="efd58-137">예를 들어 \" 2xx, 301-304418 \" .</span><span class="sxs-lookup"><span data-stu-id="efd58-137">For instance, \"2xx,301-304,418\".</span></span>

```yaml
Type: System.String[]
Parameter Sets: HTTP
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="efd58-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="efd58-138">CommonParameters</span></span>
<span data-ttu-id="efd58-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="efd58-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="efd58-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="efd58-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="efd58-141">입력</span><span class="sxs-lookup"><span data-stu-id="efd58-141">INPUTS</span></span>

### <span data-ttu-id="efd58-142">않아야</span><span class="sxs-lookup"><span data-stu-id="efd58-142">None</span></span>

## <span data-ttu-id="efd58-143">출력</span><span class="sxs-lookup"><span data-stu-id="efd58-143">OUTPUTS</span></span>

### <span data-ttu-id="efd58-144">Microsoft. 네트워크 모델. PSConnectionMonitorTcpConfiguration</span><span class="sxs-lookup"><span data-stu-id="efd58-144">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorTcpConfiguration</span></span>

### <span data-ttu-id="efd58-145">Microsoft. 네트워크 모델. PSConnectionMonitorHttpConfiguration</span><span class="sxs-lookup"><span data-stu-id="efd58-145">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorHttpConfiguration</span></span>

### <span data-ttu-id="efd58-146">PSConnectionMonitorIcmpConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="efd58-146">Microsoft.Azure.Commands.Network.Models.PSConnectionMonitorIcmpConfiguration</span></span>

## <span data-ttu-id="efd58-147">상속자</span><span class="sxs-lookup"><span data-stu-id="efd58-147">NOTES</span></span>

## <span data-ttu-id="efd58-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="efd58-148">RELATED LINKS</span></span>
