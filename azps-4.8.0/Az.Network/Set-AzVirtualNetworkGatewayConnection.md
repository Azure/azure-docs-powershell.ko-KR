---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: c7f7f8603c03300f4f1df1d47a62ed35ca3b93d0
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214054"
---
# <span data-ttu-id="6d633-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d633-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6d633-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6d633-102">SYNOPSIS</span></span>
<span data-ttu-id="6d633-103">가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="6d633-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6d633-104">SYNTAX</span></span>

### <span data-ttu-id="6d633-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6d633-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6d633-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="6d633-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-DpdTimeoutInSeconds <Int32>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-UseLocalAzureIpAddress <Boolean>]
 [-IpsecPolicies <PSIpsecPolicy[]>] [-TrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] -Tag <Hashtable>
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6d633-107">설명은</span><span class="sxs-lookup"><span data-stu-id="6d633-107">DESCRIPTION</span></span>
<span data-ttu-id="6d633-108">**AzVirtualNetworkGatewayConnection** cmdlet은 가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="6d633-109">예제의</span><span class="sxs-lookup"><span data-stu-id="6d633-109">EXAMPLES</span></span>

### <span data-ttu-id="6d633-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="6d633-110">Example 1:</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

### <span data-ttu-id="6d633-111">예제 2: 기존 VirtualNetworkGatewayConnection에 태그 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="6d633-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
```
$conn = Get-AzVirtualNetworkGatewayConnection -Name 1 -ResourceGroupName myRG
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection $conn -Tag @{ testtagKey="SomeTagKey"; testtagValue="SomeKeyValue" }

Confirm
Are you sure you want to overwrite resource '1'
[Y] Yes  [N] No  [S] Suspend  [?] Help (default is "Y"): y


Name                    : 1
ResourceGroupName       : myRG
Location                : westus
Id                      : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/Mi
                          crosoft.Network/connections/1
Etag                    : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid            : 00000000-0000-0000-0000-000000000000
ProvisioningState       : Succeeded
Tags                    :
                          Name          Value
                          ============  ============
                          testtagValue  SomeKeyValue
                          testtagKey    SomeTagKey
AuthorizationKey        :
VirtualNetworkGateway1  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRG/providers/M
                          icrosoft.Network/virtualNetworkGateways/myGateway"
VirtualNetworkGateway2  : "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/S2SVnetConn/providers/Mic
                          rosoft.Network/virtualNetworkGateways/S2SConnGW"
LocalNetworkGateway2    :
Peer                    :
RoutingWeight           : 0
SharedKey               :
ConnectionStatus        : Connected
EgressBytesTransferred  : 91334484
IngressBytesTransferred : 100386089
TunnelConnectionStatus  : []
```

## <span data-ttu-id="6d633-112">변수</span><span class="sxs-lookup"><span data-stu-id="6d633-112">PARAMETERS</span></span>

### <span data-ttu-id="6d633-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6d633-113">-AsJob</span></span>
<span data-ttu-id="6d633-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6d633-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6d633-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6d633-115">-DefaultProfile</span></span>
<span data-ttu-id="6d633-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6d633-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="6d633-117">-EnableBgp</span></span>
<span data-ttu-id="6d633-118">S2S VPN 터널을 통해 BGP 세션을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="6d633-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-119">-DpdTimeoutInSeconds</span><span class="sxs-lookup"><span data-stu-id="6d633-119">-DpdTimeoutInSeconds</span></span>
<span data-ttu-id="6d633-120">연결의 배달 되지 않은 피어 검색 시간 제한 (초)</span><span class="sxs-lookup"><span data-stu-id="6d633-120">Dead Peer Detection Timeout of the connection in seconds</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6d633-121">-Force</span></span>
<span data-ttu-id="6d633-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="6d633-123">-계층 정책</span><span class="sxs-lookup"><span data-stu-id="6d633-123">-IpsecPolicies</span></span>
<span data-ttu-id="6d633-124">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-124">A list of IPSec policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-125">태그</span><span class="sxs-lookup"><span data-stu-id="6d633-125">-Tag</span></span>
<span data-ttu-id="6d633-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-126">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateResourceWithTags
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-127">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="6d633-127">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="6d633-128">트래픽 선택기 정책의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-128">A list of Traffic Selector policies.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-129">-UseLocalAzureIpAddress</span><span class="sxs-lookup"><span data-stu-id="6d633-129">-UseLocalAzureIpAddress</span></span>
<span data-ttu-id="6d633-130">S2S 연결에 PrivateIP 사용 여부</span><span class="sxs-lookup"><span data-stu-id="6d633-130">Whether to use PrivateIP for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-131">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="6d633-131">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="6d633-132">S2S 연결에 대해 정책 기반 트래픽 선택기를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="6d633-132">Whether to use policy-based traffic selectors for a S2S connection</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-133">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d633-133">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="6d633-134">이 cmdlet이 가상 네트워크 게이트웨이 연결을 수정 하는 데 사용 하는 PSVirtualNetworkGatewayConnection 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-134">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-135">-확인</span><span class="sxs-lookup"><span data-stu-id="6d633-135">-Confirm</span></span>
<span data-ttu-id="6d633-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-136">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6d633-137">-WhatIf</span></span>
<span data-ttu-id="6d633-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6d633-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-139">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6d633-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6d633-140">CommonParameters</span></span>
<span data-ttu-id="6d633-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6d633-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6d633-142">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6d633-142">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6d633-143">입력</span><span class="sxs-lookup"><span data-stu-id="6d633-143">INPUTS</span></span>

### <span data-ttu-id="6d633-144">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6d633-144">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="6d633-145">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="6d633-145">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="6d633-146">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="6d633-146">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="6d633-147">PSTrafficSelectorPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="6d633-147">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="6d633-148">출력</span><span class="sxs-lookup"><span data-stu-id="6d633-148">OUTPUTS</span></span>

### <span data-ttu-id="6d633-149">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="6d633-149">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="6d633-150">상속자</span><span class="sxs-lookup"><span data-stu-id="6d633-150">NOTES</span></span>

## <span data-ttu-id="6d633-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6d633-151">RELATED LINKS</span></span>

[<span data-ttu-id="6d633-152">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d633-152">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6d633-153">새로운 AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d633-153">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="6d633-154">제거-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="6d633-154">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


