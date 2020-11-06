---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmLoadBalancerProbeConfig.md
ms.openlocfilehash: 8a4889190e58edd896d1a93222a35688dd5884c1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530191"
---
# <span data-ttu-id="ec7bc-101">New-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec7bc-101">New-AzureRmLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="ec7bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec7bc-102">SYNOPSIS</span></span>
<span data-ttu-id="ec7bc-103">부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-103">Creates a probe configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ec7bc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ec7bc-104">SYNTAX</span></span>

```
New-AzureRmLoadBalancerProbeConfig -Name <String> [-Protocol <String>] -Port <Int32> -IntervalInSeconds <Int32>
 -ProbeCount <Int32> [-RequestPath <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="ec7bc-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ec7bc-105">DESCRIPTION</span></span>
<span data-ttu-id="ec7bc-106">**AzureRmLoadBalancerProbeConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-106">The **New-AzureRmLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="ec7bc-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ec7bc-107">EXAMPLES</span></span>

### <span data-ttu-id="ec7bc-108">예제 1: 프로브 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="ec7bc-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzureRmLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="ec7bc-109">이 명령은 HTTP 프로토콜을 사용 하 여 MyProbe 라는 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="ec7bc-110">새 프로브는 포트 80의 부하 분산 서비스에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="ec7bc-111">변수</span><span class="sxs-lookup"><span data-stu-id="ec7bc-111">PARAMETERS</span></span>

### <span data-ttu-id="ec7bc-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec7bc-112">-DefaultProfile</span></span>
<span data-ttu-id="ec7bc-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ec7bc-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="ec7bc-114">-IntervalInSeconds</span></span>
<span data-ttu-id="ec7bc-115">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bc-116">-이름</span><span class="sxs-lookup"><span data-stu-id="ec7bc-116">-Name</span></span>
<span data-ttu-id="ec7bc-117">만들려는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="ec7bc-118">-포트</span><span class="sxs-lookup"><span data-stu-id="ec7bc-118">-Port</span></span>
<span data-ttu-id="ec7bc-119">새 프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bc-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="ec7bc-120">-ProbeCount</span></span>
<span data-ttu-id="ec7bc-121">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bc-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="ec7bc-122">-Protocol</span></span>
<span data-ttu-id="ec7bc-123">프로브 구성에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="ec7bc-124">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bc-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="ec7bc-125">-RequestPath</span></span>
<span data-ttu-id="ec7bc-126">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec7bc-127">-확인</span><span class="sxs-lookup"><span data-stu-id="ec7bc-127">-Confirm</span></span>
<span data-ttu-id="ec7bc-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec7bc-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec7bc-129">-WhatIf</span></span>
<span data-ttu-id="ec7bc-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec7bc-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec7bc-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec7bc-132">CommonParameters</span></span>
<span data-ttu-id="ec7bc-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec7bc-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec7bc-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ec7bc-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec7bc-135">입력</span><span class="sxs-lookup"><span data-stu-id="ec7bc-135">INPUTS</span></span>

### <span data-ttu-id="ec7bc-136">않아야</span><span class="sxs-lookup"><span data-stu-id="ec7bc-136">None</span></span>

## <span data-ttu-id="ec7bc-137">출력</span><span class="sxs-lookup"><span data-stu-id="ec7bc-137">OUTPUTS</span></span>

### <span data-ttu-id="ec7bc-138">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="ec7bc-138">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="ec7bc-139">상속자</span><span class="sxs-lookup"><span data-stu-id="ec7bc-139">NOTES</span></span>

## <span data-ttu-id="ec7bc-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec7bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="ec7bc-141">추가-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec7bc-141">Add-AzureRmLoadBalancerProbeConfig</span></span>](./Add-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec7bc-142">Get-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec7bc-142">Get-AzureRmLoadBalancerProbeConfig</span></span>](./Get-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec7bc-143">제거-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec7bc-143">Remove-AzureRmLoadBalancerProbeConfig</span></span>](./Remove-AzureRmLoadBalancerProbeConfig.md)

[<span data-ttu-id="ec7bc-144">Set-AzureRmLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="ec7bc-144">Set-AzureRmLoadBalancerProbeConfig</span></span>](./Set-AzureRmLoadBalancerProbeConfig.md)


