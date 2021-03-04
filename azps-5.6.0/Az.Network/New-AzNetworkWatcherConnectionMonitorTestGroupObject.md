---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-aznetworkwatcherconnectionmonitortestgroupobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzNetworkWatcherConnectionMonitorTestGroupObject.md
ms.openlocfilehash: 4ab9feb0d99bc808cfabb481baf81bb12e050f28
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101958411"
---
# <span data-ttu-id="e4bb0-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e4bb0-101">New-AzNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e4bb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4bb0-102">SYNOPSIS</span></span>
<span data-ttu-id="e4bb0-103">연결 모니터 테스트 그룹을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-103">Create a connection monitor test group.</span></span>

## <span data-ttu-id="e4bb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="e4bb0-104">SYNTAX</span></span>

```
New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name <String>
 -TestConfiguration <PSNetworkWatcherConnectionMonitorTestConfigurationObject[]>
 -Source <PSNetworkWatcherConnectionMonitorEndpointObject[]>
 -Destination <PSNetworkWatcherConnectionMonitorEndpointObject[]> [-Disable]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e4bb0-105">설명</span><span class="sxs-lookup"><span data-stu-id="e4bb0-105">DESCRIPTION</span></span>
<span data-ttu-id="e4bb0-106">New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet은 연결 모니터 테스트 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-106">The New-AzNetworkWatcherConnectionMonitorTestGroupObject cmdlet creates a connection monitor test group.</span></span>

## <span data-ttu-id="e4bb0-107">예제</span><span class="sxs-lookup"><span data-stu-id="e4bb0-107">EXAMPLES</span></span>

### <span data-ttu-id="e4bb0-108">예제 1: 테스트 구성 2개, w 원본 및 2개 대상 엔드포인트가 있는 테스트 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="e4bb0-108">Example 1: Create a test group with 2 testConfigurations, w source and 2 destination endpoints</span></span>

```
$testGroup1 = New-AzNetworkWatcherConnectionMonitorTestGroupObject -Name testGroup1 -TestConfiguration $tcpTestConfiguration, $icmpTestConfiguration -Source $vmEndpoint, $workspaceEndpoint -Destination $bingEndpoint, $googleEndpoint
```

## <span data-ttu-id="e4bb0-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e4bb0-109">PARAMETERS</span></span>

### <span data-ttu-id="e4bb0-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4bb0-110">-DefaultProfile</span></span>
<span data-ttu-id="e4bb0-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-111">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e4bb0-112">-대상</span><span class="sxs-lookup"><span data-stu-id="e4bb0-112">-Destination</span></span>
<span data-ttu-id="e4bb0-113">대상 엔드포인트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-113">List of destination endpoints.</span></span>

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

### <span data-ttu-id="e4bb0-114">-사용 안</span><span class="sxs-lookup"><span data-stu-id="e4bb0-114">-Disable</span></span>
<span data-ttu-id="e4bb0-115">테스트 그룹을 사용하지 않도록 설정하는지 여부를 나타내는 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-115">Flag indicating whether test group is disabled.</span></span>

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

### <span data-ttu-id="e4bb0-116">-Name</span><span class="sxs-lookup"><span data-stu-id="e4bb0-116">-Name</span></span>
<span data-ttu-id="e4bb0-117">테스트 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-117">The test group name.</span></span>

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

### <span data-ttu-id="e4bb0-118">-Source</span><span class="sxs-lookup"><span data-stu-id="e4bb0-118">-Source</span></span>
<span data-ttu-id="e4bb0-119">원본 엔드포인트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-119">List of source endpoints.</span></span>

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

### <span data-ttu-id="e4bb0-120">-TestConfiguration</span><span class="sxs-lookup"><span data-stu-id="e4bb0-120">-TestConfiguration</span></span>
<span data-ttu-id="e4bb0-121">테스트 구성 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-121">List of test configuration.</span></span>

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

### <span data-ttu-id="e4bb0-122">-확인</span><span class="sxs-lookup"><span data-stu-id="e4bb0-122">-Confirm</span></span>
<span data-ttu-id="e4bb0-123">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-123">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4bb0-124">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4bb0-124">-WhatIf</span></span>
<span data-ttu-id="e4bb0-125">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-125">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4bb0-126">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-126">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4bb0-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4bb0-127">CommonParameters</span></span>
<span data-ttu-id="e4bb0-128">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e4bb0-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4bb0-129">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e4bb0-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4bb0-130">입력</span><span class="sxs-lookup"><span data-stu-id="e4bb0-130">INPUTS</span></span>

### <span data-ttu-id="e4bb0-131">없음</span><span class="sxs-lookup"><span data-stu-id="e4bb0-131">None</span></span>

## <span data-ttu-id="e4bb0-132">출력</span><span class="sxs-lookup"><span data-stu-id="e4bb0-132">OUTPUTS</span></span>

### <span data-ttu-id="e4bb0-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span><span class="sxs-lookup"><span data-stu-id="e4bb0-133">Microsoft.Azure.Commands.Network.Models.PSNetworkWatcherConnectionMonitorTestGroupObject</span></span>

## <span data-ttu-id="e4bb0-134">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e4bb0-134">NOTES</span></span>

## <span data-ttu-id="e4bb0-135">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4bb0-135">RELATED LINKS</span></span>
