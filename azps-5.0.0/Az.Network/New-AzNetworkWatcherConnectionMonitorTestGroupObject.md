---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: af924210c8f1fb465881f054815f874ff5d99429
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94310157"
---
# <span data-ttu-id="85ce0-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="85ce0-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="85ce0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="85ce0-102">SYNOPSIS</span></span>
<span data-ttu-id="85ce0-103">연결 모니터 테스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="85ce0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="85ce0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="85ce0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="85ce0-105">DESCRIPTION</span></span>
<span data-ttu-id="85ce0-106">New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet은 연결 모니터 테스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="85ce0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="85ce0-107">EXAMPLES</span></span>

### <span data-ttu-id="85ce0-108">예제 1:2 개의 testConfigurations, w 원본 및 2 개의 대상 끝점을 사용 하 여 테스트 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="85ce0-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="85ce0-109">변수</span><span class="sxs-lookup"><span data-stu-id="85ce0-109">PARAMETERS</span></span>

### <span data-ttu-id="85ce0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="85ce0-110">-DefaultProfile</span></span>
<span data-ttu-id="85ce0-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="85ce0-112">-대상</span><span class="sxs-lookup"><span data-stu-id="85ce0-112">-Destination</span></span>
<span data-ttu-id="85ce0-113">대상 끝점의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-113">List of destination endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ce0-114">-Disable</span><span class="sxs-lookup"><span data-stu-id="85ce0-114">-Disable</span></span>
<span data-ttu-id="85ce0-115">테스트 그룹을 사용할 수 있는지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="85ce0-116">-이름</span><span class="sxs-lookup"><span data-stu-id="85ce0-116">-Name</span></span>
<span data-ttu-id="85ce0-117">테스트 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-117">The test group name.</span></span>

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

### <span data-ttu-id="85ce0-118">-원본</span><span class="sxs-lookup"><span data-stu-id="85ce0-118">-Source</span></span>
<span data-ttu-id="85ce0-119">소스 끝점의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-119">List of source endpoints.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorEndpointObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ce0-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="85ce0-120">-TestConfiguration</span></span>
<span data-ttu-id="85ce0-121">테스트 구성의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-121">List of test configuration.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestConfigurationObject[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="85ce0-122">-확인</span><span class="sxs-lookup"><span data-stu-id="85ce0-122">-Confirm</span></span>
<span data-ttu-id="85ce0-123">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="85ce0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="85ce0-124">-WhatIf</span></span>
<span data-ttu-id="85ce0-125">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="85ce0-126">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="85ce0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="85ce0-127">CommonParameters</span></span>
<span data-ttu-id="85ce0-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="85ce0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="85ce0-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="85ce0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="85ce0-130">입력</span><span class="sxs-lookup"><span data-stu-id="85ce0-130">INPUTS</span></span>

### <span data-ttu-id="85ce0-131">않아야</span><span class="sxs-lookup"><span data-stu-id="85ce0-131">None</span></span>

## <span data-ttu-id="85ce0-132">출력</span><span class="sxs-lookup"><span data-stu-id="85ce0-132">OUTPUTS</span></span>

### <span data-ttu-id="85ce0-133">PSNetworkWatcherConnectionMonitorTestGroupObject에 대 한.</span><span class="sxs-lookup"><span data-stu-id="85ce0-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="85ce0-134">상속자</span><span class="sxs-lookup"><span data-stu-id="85ce0-134">NOTES</span></span>

## <span data-ttu-id="85ce0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="85ce0-135">RELATED LINKS</span></span>
