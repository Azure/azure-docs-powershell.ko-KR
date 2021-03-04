---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestconfigurationobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestConfigurationObject.md
ms.openlocfilehash: 542a207e60e451d97ba5edcbdccc45b84b14f760
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958432"
---
# <span data-ttu-id="e5d62-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e5d62-101">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="e5d62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5d62-102">SYNOPSIS</span></span>
<span data-ttu-id="e5d62-103">연결 모니터 테스트 구성을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-103">Create a connection monitor test configuration.</span></span>

## <span data-ttu-id="e5d62-104">구문</span><span class="sxs-lookup"><span data-stu-id="e5d62-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name <String> -TestFrequencySec <Int32>
 -ProtocolConfiguration <PSNetworkWatcherConnectionMonitorProtocolConfiguration>
 [-SuccessThresholdChecksFailedPercent <Int32>] [-SuccessThresholdRoundTripTimeMs <Double>]
 [-PreferredIPVersion <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e5d62-105">설명</span><span class="sxs-lookup"><span data-stu-id="e5d62-105">DESCRIPTION</span></span>
<span data-ttu-id="e5d62-106">New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet은 연결 모니터 테스트 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-106">The New-AzNetworkWatcherConnectionMonitorTestConfigurationObject cmdlet creates a connection monitor test configuration.</span></span>

## <span data-ttu-id="e5d62-107">예제</span><span class="sxs-lookup"><span data-stu-id="e5d62-107">EXAMPLES</span></span>

### <span data-ttu-id="e5d62-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="e5d62-108">Example 1</span></span>
```powershell
PS C:\>$httpProtocolConfiguration = New-AzNetworkWatcherConnectionMonitorProtocolConfigurationObject -HttpProtocol -Port 443 -Method GET -RequestHeader @{"Allow" = "GET"} -ValidStatusCodeRange 2xx, 300-308 -PreferHTTPS
PS C:\>$httpTestConfiguration = New-AzNetworkWatcherConnectionMonitorTestConfigurationObject -Name httpTC -TestFrequencySec 120 -ProtocolConfiguration $httpProtocolConfiguration -SuccessThresholdChecksFailedPercent 20 -SuccessThresholdRoundTripTimeMs 30
```

<span data-ttu-id="e5d62-109">이름 : httpTC TestFrequencySec : 120 PreferredIPVersion : ProtocolConfiguration : { "Port": 443, "메서드": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold : { "ChecksFailedPercent": { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span><span class="sxs-lookup"><span data-stu-id="e5d62-109">Name                  : httpTC TestFrequencySec      : 120 PreferredIPVersion    : ProtocolConfiguration : { "Port": 443, "Method": "GET", "RequestHeaders": [ { "Name": "Allow", "Value": "GET" } ], "ValidStatusCodeRanges": [ "2xx", "300-308" ], "PreferHTTPS": true } SuccessThreshold      : { "ChecksFailedPercent": 20, "RoundTripTimeMs": 30 }</span></span> 

## <span data-ttu-id="e5d62-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e5d62-110">PARAMETERS</span></span>

### <span data-ttu-id="e5d62-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e5d62-111">-DefaultProfile</span></span>
<span data-ttu-id="e5d62-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e5d62-113">-Name</span><span class="sxs-lookup"><span data-stu-id="e5d62-113">-Name</span></span>
<span data-ttu-id="e5d62-114">연결 모니터 테스트 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-114">The name of the connection monitor test configuration.</span></span>

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

### <span data-ttu-id="e5d62-115">-PreferredIPVersion</span><span class="sxs-lookup"><span data-stu-id="e5d62-115">-PreferredIPVersion</span></span>
<span data-ttu-id="e5d62-116">테스트 평가에 사용할 기본 IP 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-116">The preferred IP version to use in test evaluation.</span></span> <span data-ttu-id="e5d62-117">연결 모니터는 다른 매개 변수에 따라 다른 버전을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-117">The connection monitor may choose to use a different version depending on other parameters.</span></span>

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

### <span data-ttu-id="e5d62-118">-ProtocolConfiguration</span><span class="sxs-lookup"><span data-stu-id="e5d62-118">-ProtocolConfiguration</span></span>
<span data-ttu-id="e5d62-119">일부 프로토콜에 대한 테스트 평가를 수행하는 데 사용되는 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-119">The parameters used to perform test evaluation over some protocol.</span></span>

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

### <span data-ttu-id="e5d62-120">-SuccessThresholdChecksFailedPercent</span><span class="sxs-lookup"><span data-stu-id="e5d62-120">-SuccessThresholdChecksFailedPercent</span></span>
<span data-ttu-id="e5d62-121">테스트가 성공한 것으로 평가할 수 있는 실패한 검사의 최대 백분율입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-121">The maximum percentage of failed checks permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="e5d62-122">-SuccessThresholdRoundTripTimeMs</span><span class="sxs-lookup"><span data-stu-id="e5d62-122">-SuccessThresholdRoundTripTimeMs</span></span>
<span data-ttu-id="e5d62-123">테스트가 성공한 것으로 평가할 수 있는 최대 왕복 시간(밀리초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-123">The maximum round-trip time in milliseconds permitted for a test to evaluate as successful.</span></span>

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

### <span data-ttu-id="e5d62-124">-TestFrequencySec</span><span class="sxs-lookup"><span data-stu-id="e5d62-124">-TestFrequencySec</span></span>
<span data-ttu-id="e5d62-125">테스트 평가 빈도(초)입니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-125">The frequency of test evaluation, in seconds.</span></span>

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

### <span data-ttu-id="e5d62-126">-확인</span><span class="sxs-lookup"><span data-stu-id="e5d62-126">-Confirm</span></span>
<span data-ttu-id="e5d62-127">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e5d62-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5d62-128">-WhatIf</span></span>
<span data-ttu-id="e5d62-129">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e5d62-130">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e5d62-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5d62-131">CommonParameters</span></span>
<span data-ttu-id="e5d62-132">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e5d62-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5d62-133">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e5d62-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5d62-134">입력</span><span class="sxs-lookup"><span data-stu-id="e5d62-134">INPUTS</span></span>

### <span data-ttu-id="e5d62-135">없음</span><span class="sxs-lookup"><span data-stu-id="e5d62-135">None</span></span>

## <span data-ttu-id="e5d62-136">출력</span><span class="sxs-lookup"><span data-stu-id="e5d62-136">OUTPUTS</span></span>

### <span data-ttu-id="e5d62-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span><span class="sxs-lookup"><span data-stu-id="e5d62-137">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject</span></span>

## <span data-ttu-id="e5d62-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e5d62-138">NOTES</span></span>

## <span data-ttu-id="e5d62-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e5d62-139">RELATED LINKS</span></span>
