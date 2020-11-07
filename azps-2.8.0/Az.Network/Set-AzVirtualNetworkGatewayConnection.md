---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: D7065B04-1A01-4BB4-A519-1DA9002CDE02
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azvirtualnetworkgatewayconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzVirtualNetworkGatewayConnection.md
ms.openlocfilehash: 83d91b7761200813e2973dfe4a76067e92f9bf42
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872138"
---
# <span data-ttu-id="f3d42-101">Set-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f3d42-101">Set-AzVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f3d42-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3d42-102">SYNOPSIS</span></span>
<span data-ttu-id="f3d42-103">가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-103">Configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="f3d42-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3d42-104">SYNTAX</span></span>

### <span data-ttu-id="f3d42-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3d42-105">Default (Default)</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3d42-106">UpdateResourceWithTags</span><span class="sxs-lookup"><span data-stu-id="f3d42-106">UpdateResourceWithTags</span></span>
```
Set-AzVirtualNetworkGatewayConnection -VirtualNetworkGatewayConnection <PSVirtualNetworkGatewayConnection>
 [-EnableBgp <Boolean>] [-UsePolicyBasedTrafficSelectors <Boolean>] [-IpsecPolicies <PSIpsecPolicy[]>] [-IpsecPolTrafficSelectorPolicy <PSTrafficSelectorPolicy[]>] 
 -Tag <Hashtable> [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3d42-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3d42-107">DESCRIPTION</span></span>
<span data-ttu-id="f3d42-108">**AzVirtualNetworkGatewayConnection** cmdlet은 가상 네트워크 게이트웨이 연결을 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-108">The **Set-AzVirtualNetworkGatewayConnection** cmdlet configures a virtual network gateway connection.</span></span>

## <span data-ttu-id="f3d42-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3d42-109">EXAMPLES</span></span>

### <span data-ttu-id="f3d42-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="f3d42-110">Example 1:</span></span>
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

### <span data-ttu-id="f3d42-111">예제 2: 기존 VirtualNetworkGatewayConnection에 태그 추가/업데이트</span><span class="sxs-lookup"><span data-stu-id="f3d42-111">Example 2: Add/Update tags to an existing VirtualNetworkGatewayConnection</span></span>
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

## <span data-ttu-id="f3d42-112">변수</span><span class="sxs-lookup"><span data-stu-id="f3d42-112">PARAMETERS</span></span>

### <span data-ttu-id="f3d42-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3d42-113">-AsJob</span></span>
<span data-ttu-id="f3d42-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f3d42-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f3d42-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3d42-115">-DefaultProfile</span></span>
<span data-ttu-id="f3d42-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3d42-117">-EnableBgp</span><span class="sxs-lookup"><span data-stu-id="f3d42-117">-EnableBgp</span></span>
<span data-ttu-id="f3d42-118">S2S VPN 터널을 통해 BGP 세션을 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="f3d42-118">Whether to use a BGP session over a S2S VPN tunnel</span></span>

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

### <span data-ttu-id="f3d42-119">-Force</span><span class="sxs-lookup"><span data-stu-id="f3d42-119">-Force</span></span>
<span data-ttu-id="f3d42-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="f3d42-121">-계층 정책</span><span class="sxs-lookup"><span data-stu-id="f3d42-121">-IpsecPolicies</span></span>
<span data-ttu-id="f3d42-122">IPSec 정책 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-122">A list of IPSec policies.</span></span>

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

### <span data-ttu-id="f3d42-123">-TrafficSelectorPolicy</span><span class="sxs-lookup"><span data-stu-id="f3d42-123">-TrafficSelectorPolicy</span></span>
<span data-ttu-id="f3d42-124">트래픽 선택기 정책의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-124">A list of Traffic Selector policies.</span></span>

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

### <span data-ttu-id="f3d42-125">태그</span><span class="sxs-lookup"><span data-stu-id="f3d42-125">-Tag</span></span>
<span data-ttu-id="f3d42-126">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-126">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="f3d42-127">-UsePolicyBasedTrafficSelectors</span><span class="sxs-lookup"><span data-stu-id="f3d42-127">-UsePolicyBasedTrafficSelectors</span></span>
<span data-ttu-id="f3d42-128">S2S 연결에 대해 정책 기반 트래픽 선택기를 사용할지 여부</span><span class="sxs-lookup"><span data-stu-id="f3d42-128">Whether to use policy-based traffic selectors for a S2S connection</span></span>

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

### <span data-ttu-id="f3d42-129">-VirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f3d42-129">-VirtualNetworkGatewayConnection</span></span>
<span data-ttu-id="f3d42-130">이 cmdlet이 가상 네트워크 게이트웨이 연결을 수정 하는 데 사용 하는 PSVirtualNetworkGatewayConnection 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-130">Specifies the PSVirtualNetworkGatewayConnection object that this cmdlet uses to modify the virtual network gateway connection.</span></span>

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

### <span data-ttu-id="f3d42-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f3d42-131">-Confirm</span></span>
<span data-ttu-id="f3d42-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3d42-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3d42-133">-WhatIf</span></span>
<span data-ttu-id="f3d42-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3d42-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3d42-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3d42-136">CommonParameters</span></span>
<span data-ttu-id="f3d42-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3d42-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3d42-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3d42-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3d42-139">입력</span><span class="sxs-lookup"><span data-stu-id="f3d42-139">INPUTS</span></span>

### <span data-ttu-id="f3d42-140">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f3d42-140">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

### <span data-ttu-id="f3d42-141">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="f3d42-141">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="f3d42-142">PSIpsecPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f3d42-142">Microsoft.Azure.Commands.Network.Models.PSIpsecPolicy[]</span></span>

### <span data-ttu-id="f3d42-143">PSTrafficSelectorPolicy [] (으)로</span><span class="sxs-lookup"><span data-stu-id="f3d42-143">Microsoft.Azure.Commands.Network.Models.PSTrafficSelectorPolicy[]</span></span>

## <span data-ttu-id="f3d42-144">출력</span><span class="sxs-lookup"><span data-stu-id="f3d42-144">OUTPUTS</span></span>

### <span data-ttu-id="f3d42-145">PSVirtualNetworkGatewayConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f3d42-145">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGatewayConnection</span></span>

## <span data-ttu-id="f3d42-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f3d42-146">NOTES</span></span>

## <span data-ttu-id="f3d42-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3d42-147">RELATED LINKS</span></span>

[<span data-ttu-id="f3d42-148">Get-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f3d42-148">Get-AzVirtualNetworkGatewayConnection</span></span>](./Get-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f3d42-149">새로운 AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f3d42-149">New-AzVirtualNetworkGatewayConnection</span></span>](./New-AzVirtualNetworkGatewayConnection.md)

[<span data-ttu-id="f3d42-150">제거-AzVirtualNetworkGatewayConnection</span><span class="sxs-lookup"><span data-stu-id="f3d42-150">Remove-AzVirtualNetworkGatewayConnection</span></span>](./Remove-AzVirtualNetworkGatewayConnection.md)


