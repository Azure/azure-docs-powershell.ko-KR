---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: 4AA587F8-4967-439D-84B6-EDC24235D3F5
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermloadbalancerinboundnatruleconfig
schema: 2.0.0
ms.openlocfilehash: bcf937c0da7adfd0accafcd943de24744eb4a5ca
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882906"
---
# <span data-ttu-id="182cb-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-101">New-AzureRmLoadBalancerInboundNatRuleConfig</span></span>

## <span data-ttu-id="182cb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="182cb-102">SYNOPSIS</span></span>
<span data-ttu-id="182cb-103">부하 분산 장치에 대 한 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-103">Creates an inbound NAT rule configuration for a load balancer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="182cb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="182cb-104">SYNTAX</span></span>

### <span data-ttu-id="182cb-105">SetByResourceId</span><span class="sxs-lookup"><span data-stu-id="182cb-105">SetByResourceId</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String> [-FrontendIpConfigurationId <String>]
 [-Protocol <String>] [-FrontendPort <Int32>] [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>]
 [-EnableFloatingIP] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="182cb-106">SetByResource</span><span class="sxs-lookup"><span data-stu-id="182cb-106">SetByResource</span></span>
```
New-AzureRmLoadBalancerInboundNatRuleConfig -Name <String>
 [-FrontendIpConfiguration <PSFrontendIPConfiguration>] [-Protocol <String>] [-FrontendPort <Int32>]
 [-BackendPort <Int32>] [-IdleTimeoutInMinutes <Int32>] [-EnableFloatingIP]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="182cb-107">설명은</span><span class="sxs-lookup"><span data-stu-id="182cb-107">DESCRIPTION</span></span>
<span data-ttu-id="182cb-108">**AzureRmLoadBalancerInboundNatRuleConfig** Cmdlet은 Azure 부하 분산 장치에 대 한 NAT (inbound network address translation) 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-108">The **New-AzureRmLoadBalancerInboundNatRuleConfig** cmdlet creates an inbound network address translation (NAT) rule configuration for an Azure load balancer.</span></span>

## <span data-ttu-id="182cb-109">예제의</span><span class="sxs-lookup"><span data-stu-id="182cb-109">EXAMPLES</span></span>

### <span data-ttu-id="182cb-110">예제 1: 부하 분산 장치에 대 한 인바운드 NAT 규칙 구성 만들기</span><span class="sxs-lookup"><span data-stu-id="182cb-110">Example 1: Create an inbound NAT rule configuration for a load balancer</span></span>
```
PS C:\>$publicip = New-AzureRmPublicIpAddress -ResourceGroupName "MyResourceGroup" -Name "MyPublicIP" -Location "West US" -AllocationMethod "Dynamic"
PS C:\> $frontend = New-AzureRmLoadBalancerFrontendIpConfig -Name "FrontendIpConfig01" -PublicIpAddress $publicip
PS C:\> New-AzureRmLoadBalancerInboundNatRuleConfig -Name "MyInboundNatRule" -FrontendIPConfiguration $frontend -Protocol "Tcp" -FrontendPort 3389 -BackendPort 3389
```

<span data-ttu-id="182cb-111">첫 번째 명령은 MyResourceGroup 이라는 리소스 그룹에 MyPublicIP 이라는 공용 IP 주소를 만든 다음이를 $publicip 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-111">The first command creates a public IP address named MyPublicIP in the resource group named MyResourceGroup, and then stores it in the $publicip variable.</span></span>

<span data-ttu-id="182cb-112">두 번째 명령은 $publicip에서 공용 IP 주소를 사용 하 여 FrontendIpConfig01 라는 프런트 엔드 IP 구성을 만든 다음 $frontend 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-112">The second command creates a front-end IP configuration named FrontendIpConfig01 using the public IP address in $publicip, and then stores it in the $frontend variable.</span></span>

<span data-ttu-id="182cb-113">세 번째 명령은 $frontend에서 프런트 엔드 개체를 사용 하 여 MyInboundNatRule 라는 인바운드 NAT 규칙 구성을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-113">The third command creates an inbound NAT rule configuration named MyInboundNatRule using the front-end object in $frontend.</span></span>
<span data-ttu-id="182cb-114">TCP 프로토콜이 지정 되 고 프런트 엔드 포트는 3389 이며,이 경우 백 엔드 포트와 동일 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-114">The TCP protocol is specified and the front-end port is 3389, the same as the backend port in this case.</span></span>
<span data-ttu-id="182cb-115">*FrontendIpConfiguration* , *Procotol* , *FrontendPort* 및 *BackendPort* 매개 변수는 모두 인바운드 NAT 규칙 구성을 만드는 데 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-115">The *FrontendIpConfiguration* , *Procotol* , *FrontendPort* , and *BackendPort* parameters are all required to create an inbound NAT rule configuration.</span></span>

## <span data-ttu-id="182cb-116">변수</span><span class="sxs-lookup"><span data-stu-id="182cb-116">PARAMETERS</span></span>

### <span data-ttu-id="182cb-117">-BackendPort</span><span class="sxs-lookup"><span data-stu-id="182cb-117">-BackendPort</span></span>
<span data-ttu-id="182cb-118">이 규칙 구성으로 일치 하는 트래픽에 대 한 백 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-118">Specifies the backend port for traffic that is matched by this rule configuration.</span></span>

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

### <span data-ttu-id="182cb-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="182cb-119">-DefaultProfile</span></span>
<span data-ttu-id="182cb-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="182cb-121">-EnableFloatingIP</span><span class="sxs-lookup"><span data-stu-id="182cb-121">-EnableFloatingIP</span></span>
<span data-ttu-id="182cb-122">이 cmdlet이 규칙 구성에 대 한 부동 IP 주소를 사용할 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-122">Indicates that this cmdlet enables a floating IP address for a rule configuration.</span></span>

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

### <span data-ttu-id="182cb-123">-FrontendIpConfiguration</span><span class="sxs-lookup"><span data-stu-id="182cb-123">-FrontendIpConfiguration</span></span>
<span data-ttu-id="182cb-124">부하 분산 장치 규칙 구성과 연결할 프런트 엔드 IP 주소 목록을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-124">Specifies a list of front-end IP addresses to associate with a load balancer rule configuration.</span></span>

```yaml
Type: PSFrontendIPConfiguration
Parameter Sets: SetByResource
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182cb-125">-FrontendIpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="182cb-125">-FrontendIpConfigurationId</span></span>
<span data-ttu-id="182cb-126">프런트 엔드 IP 주소 구성에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-126">Specifies the ID for a front-end IP address configuration.</span></span>

```yaml
Type: String
Parameter Sets: SetByResourceId
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182cb-127">-FrontendPort</span><span class="sxs-lookup"><span data-stu-id="182cb-127">-FrontendPort</span></span>
<span data-ttu-id="182cb-128">부하 분산 장치 규칙 구성으로 일치 하는 프런트 엔드 포트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-128">Specifies the front-end port that is matched by a load balancer rule configuration.</span></span>

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

### <span data-ttu-id="182cb-129">-IdleTimeoutInMinutes</span><span class="sxs-lookup"><span data-stu-id="182cb-129">-IdleTimeoutInMinutes</span></span>
<span data-ttu-id="182cb-130">부하 분산 장치에서 대화 상태가 유지 되는 시간 (분)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-130">Specifies the length of time, in minutes, for which the state of conversations is maintained in a load balancer.</span></span>

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

### <span data-ttu-id="182cb-131">-이름</span><span class="sxs-lookup"><span data-stu-id="182cb-131">-Name</span></span>
<span data-ttu-id="182cb-132">이 cmdlet이 만드는 규칙 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-132">Specifies the name of the rule configuration that this cmdlet creates.</span></span>

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

### <span data-ttu-id="182cb-133">-프로토콜</span><span class="sxs-lookup"><span data-stu-id="182cb-133">-Protocol</span></span>
<span data-ttu-id="182cb-134">프로토콜을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-134">Specifies a protocol.</span></span>
<span data-ttu-id="182cb-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-135">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="182cb-136">Net.tcp</span><span class="sxs-lookup"><span data-stu-id="182cb-136">Tcp</span></span>
- <span data-ttu-id="182cb-137">Udp</span><span class="sxs-lookup"><span data-stu-id="182cb-137">Udp</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Tcp, Udp

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="182cb-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="182cb-138">CommonParameters</span></span>
<span data-ttu-id="182cb-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="182cb-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="182cb-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="182cb-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="182cb-141">입력</span><span class="sxs-lookup"><span data-stu-id="182cb-141">INPUTS</span></span>

## <span data-ttu-id="182cb-142">출력</span><span class="sxs-lookup"><span data-stu-id="182cb-142">OUTPUTS</span></span>

### <span data-ttu-id="182cb-143">PSInboundNatRule에 대 한.</span><span class="sxs-lookup"><span data-stu-id="182cb-143">Microsoft.Azure.Commands.Network.Models.PSInboundNatRule</span></span>

## <span data-ttu-id="182cb-144">상속자</span><span class="sxs-lookup"><span data-stu-id="182cb-144">NOTES</span></span>

## <span data-ttu-id="182cb-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="182cb-145">RELATED LINKS</span></span>

[<span data-ttu-id="182cb-146">추가-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-146">Add-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Add-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="182cb-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-147">Get-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Get-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="182cb-148">새로운 AzureRmLoadBalancerFrontendIpConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-148">New-AzureRmLoadBalancerFrontendIpConfig</span></span>](./New-AzureRmLoadBalancerFrontendIpConfig.md)

[<span data-ttu-id="182cb-149">새로운 AzureRmPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="182cb-149">New-AzureRmPublicIpAddress</span></span>](./New-AzureRmPublicIpAddress.md)

[<span data-ttu-id="182cb-150">제거-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-150">Remove-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Remove-AzureRmLoadBalancerInboundNatRuleConfig.md)

[<span data-ttu-id="182cb-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span><span class="sxs-lookup"><span data-stu-id="182cb-151">Set-AzureRmLoadBalancerInboundNatRuleConfig</span></span>](./Set-AzureRmLoadBalancerInboundNatRuleConfig.md)


