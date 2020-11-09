---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: d46cba5a939a2054bc8cc40975647a198808ca09
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310193"
---
# <span data-ttu-id="dcc56-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="dcc56-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="dcc56-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dcc56-102">SYNOPSIS</span></span>
<span data-ttu-id="dcc56-103">연결 모니터 테스트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="dcc56-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dcc56-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dcc56-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dcc56-105">DESCRIPTION</span></span>
<span data-ttu-id="dcc56-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet은 연결 모니터 테스트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="dcc56-107">예제의</span><span class="sxs-lookup"><span data-stu-id="dcc56-107">EXAMPLES</span></span>

### <span data-ttu-id="dcc56-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="dcc56-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="dcc56-109">Name: httpTC TestFrequencySec: 120 PreferredIPVersion: ProtocolConfiguration: {"Port": 443, "메서드": "GET", "RequestHeaders": [{"이름": "허용", "값": "GET"}], "ValidStatusCodeRanges": ["2xx", "300-308", "PreferHTTPS": true} SuccessThreshold: {"ChecksFailedPercent": 20, "RoundTripTimeMs": 30}</span><span class="sxs-lookup"><span data-stu-id="dcc56-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="dcc56-110">변수</span><span class="sxs-lookup"><span data-stu-id="dcc56-110">PARAMETERS</span></span>

### <span data-ttu-id="dcc56-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dcc56-111">-DefaultProfile</span></span>
<span data-ttu-id="dcc56-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dcc56-113">-이름</span><span class="sxs-lookup"><span data-stu-id="dcc56-113">-Name</span></span>
<span data-ttu-id="dcc56-114">연결 모니터 테스트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="dcc56-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="dcc56-115">-PreferredIPVersion</span></span>
<span data-ttu-id="dcc56-116">테스트 평가에 사용할 기본 설정 IP 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="dcc56-117">연결 모니터는 다른 매개 변수에 따라 다른 버전을 사용 하도록 선택할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="dcc56-118">프로토콜 구성</span><span class="sxs-lookup"><span data-stu-id="dcc56-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="dcc56-119">일부 프로토콜을 통해 테스트 평가를 수행 하는 데 사용 되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-119">The parameters used to perform test evaluation over some protocol.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorProtocolConfiguration
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="dcc56-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="dcc56-121">테스트를 성공적으로 평가할 수 있는 실패 한 검사의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="dcc56-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="dcc56-123">테스트가 성공한 것으로 평가 될 수 있는 최대 왕복 시간 (밀리초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="dcc56-124">-TestFrequencySec</span></span>
<span data-ttu-id="dcc56-125">테스트 평가 빈도 (초)입니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-125">The frequency of test evaluation, in seconds.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases: TestFrequency

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-126">-확인</span><span class="sxs-lookup"><span data-stu-id="dcc56-126">-Confirm</span></span>
<span data-ttu-id="dcc56-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-127">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dcc56-128">-WhatIf</span></span>
<span data-ttu-id="dcc56-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dcc56-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-130">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dcc56-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dcc56-131">CommonParameters</span></span>
<span data-ttu-id="dcc56-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dcc56-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dcc56-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="dcc56-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dcc56-134">입력</span><span class="sxs-lookup"><span data-stu-id="dcc56-134">INPUTS</span></span>

### <span data-ttu-id="dcc56-135">않아야</span><span class="sxs-lookup"><span data-stu-id="dcc56-135">None</span></span>

## <span data-ttu-id="dcc56-136">출력</span><span class="sxs-lookup"><span data-stu-id="dcc56-136">OUTPUTS</span></span>

### <span data-ttu-id="dcc56-137">PSNetworkWatcherConnectionMonitorTestConfigurationObject에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dcc56-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="dcc56-138">상속자</span><span class="sxs-lookup"><span data-stu-id="dcc56-138">NOTES</span></span>

## <span data-ttu-id="dcc56-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dcc56-139">RELATED LINKS</span></span>
