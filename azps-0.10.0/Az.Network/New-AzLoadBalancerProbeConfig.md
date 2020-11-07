---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 2049CB74-E3CB-4294-B97C-B41E91209A1E
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azloadbalancerprobeconfig
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzLoadBalancerProbeConfig.md
ms.openlocfilehash: 6e647cbc20e74c5c473fe91b2ec592177c0713ba
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875425"
---
# <span data-ttu-id="73461-101">New-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="73461-101">New-AzLoadBalancerProbeConfig</span></span>

## <span data-ttu-id="73461-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="73461-102">SYNOPSIS</span></span>
<span data-ttu-id="73461-103">부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73461-103">Creates a probe configuration for a load balancer.</span></span>

## <span data-ttu-id="73461-104">구문과</span><span class="sxs-lookup"><span data-stu-id="73461-104">SYNTAX</span></span>

```
New-AzLoadBalancerProbeConfig -Name <String> [-RequestPath <String>] [-Protocol <String>] -Port <Int32>
 -IntervalInSeconds <Int32> -ProbeCount <Int32> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="73461-105">설명은</span><span class="sxs-lookup"><span data-stu-id="73461-105">DESCRIPTION</span></span>
<span data-ttu-id="73461-106">**AzLoadBalancerProbeConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73461-106">The **New-AzLoadBalancerProbeConfig** cmdlet creates a probe configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="73461-107">예제의</span><span class="sxs-lookup"><span data-stu-id="73461-107">EXAMPLES</span></span>

### <span data-ttu-id="73461-108">예제 1: 프로브 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="73461-108">Example 1: Create a probe configuration</span></span>
```
PS C:\>New-AzLoadBalancerProbeConfig -Name "MyProbe" -Protocol "http" -Port 80 -IntervalInSeconds 15 -ProbeCount 15
```

<span data-ttu-id="73461-109">이 명령은 HTTP 프로토콜을 사용 하 여 MyProbe 라는 프로브 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="73461-109">This command creates a probe configuration named MyProbe using the HTTP protocol.</span></span>
<span data-ttu-id="73461-110">새 프로브는 포트 80의 부하 분산 서비스에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="73461-110">The new probe will connect to a load-balanced service on port 80.</span></span>

## <span data-ttu-id="73461-111">변수</span><span class="sxs-lookup"><span data-stu-id="73461-111">PARAMETERS</span></span>

### <span data-ttu-id="73461-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="73461-112">-DefaultProfile</span></span>
<span data-ttu-id="73461-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="73461-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="73461-114">-IntervalInSeconds</span><span class="sxs-lookup"><span data-stu-id="73461-114">-IntervalInSeconds</span></span>
<span data-ttu-id="73461-115">부하 분산 서비스의 각 인스턴스에 대 한 프로브 사이의 간격 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-115">Specifies the interval, in seconds, between probes to each instance of a load-balanced service.</span></span>

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

### <span data-ttu-id="73461-116">-이름</span><span class="sxs-lookup"><span data-stu-id="73461-116">-Name</span></span>
<span data-ttu-id="73461-117">만들려는 프로브 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-117">Specifies the name of the probe configuration to create.</span></span>

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

### <span data-ttu-id="73461-118">-포트</span><span class="sxs-lookup"><span data-stu-id="73461-118">-Port</span></span>
<span data-ttu-id="73461-119">새 프로브가 부하 분산 서비스에 연결할 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-119">Specifies the port on which the new probe should connect to a load-balanced service.</span></span>

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

### <span data-ttu-id="73461-120">-ProbeCount</span><span class="sxs-lookup"><span data-stu-id="73461-120">-ProbeCount</span></span>
<span data-ttu-id="73461-121">비정상으로 간주 되는 인스턴스에 대 한 인스턴스 별 연속 된 실패의 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-121">Specifies the number of per-instance consecutive failures for an instance to be considered unhealthy.</span></span>

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

### <span data-ttu-id="73461-122">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="73461-122">-Protocol</span></span>
<span data-ttu-id="73461-123">프로브 구성에 사용할 프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-123">Specifies the protocol to use for the probe configuration.</span></span>
<span data-ttu-id="73461-124">이 매개 변수에 허용 되는 값은 Tcp 또는 Http입니다.</span><span class="sxs-lookup"><span data-stu-id="73461-124">The acceptable values for this parameter are: Tcp or Http.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Http

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="73461-125">-RequestPath</span><span class="sxs-lookup"><span data-stu-id="73461-125">-RequestPath</span></span>
<span data-ttu-id="73461-126">부하 분산 서비스에서 상태를 확인 하기 위해 경로를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-126">Specifies the path in a load-balanced service to probe to determine health.</span></span>

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

### <span data-ttu-id="73461-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="73461-127">CommonParameters</span></span>
<span data-ttu-id="73461-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="73461-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="73461-129">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="73461-129">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="73461-130">입력</span><span class="sxs-lookup"><span data-stu-id="73461-130">INPUTS</span></span>

## <span data-ttu-id="73461-131">출력</span><span class="sxs-lookup"><span data-stu-id="73461-131">OUTPUTS</span></span>

### <span data-ttu-id="73461-132">Microsoft. 네트워크. PSProbe</span><span class="sxs-lookup"><span data-stu-id="73461-132">Microsoft.Azure.Commands.Network.Models.PSProbe</span></span>

## <span data-ttu-id="73461-133">상속자</span><span class="sxs-lookup"><span data-stu-id="73461-133">NOTES</span></span>

## <span data-ttu-id="73461-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="73461-134">RELATED LINKS</span></span>

[<span data-ttu-id="73461-135">추가-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="73461-135">Add-AzLoadBalancerProbeConfig</span></span>](./Add-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="73461-136">Get-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="73461-136">Get-AzLoadBalancerProbeConfig</span></span>](./Get-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="73461-137">제거-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="73461-137">Remove-AzLoadBalancerProbeConfig</span></span>](./Remove-AzLoadBalancerProbeConfig.md)

[<span data-ttu-id="73461-138">Set-AzLoadBalancerProbeConfig</span><span class="sxs-lookup"><span data-stu-id="73461-138">Set-AzLoadBalancerProbeConfig</span></span>](./Set-AzLoadBalancerProbeConfig.md)


