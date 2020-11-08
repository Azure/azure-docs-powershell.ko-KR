---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/disconnect-azvirtualnetworkgatewayvpnconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Disconnect-AzVirtualNetworkGatewayVpnConnection.md
ms.openlocfilehash: b14d7f0ac4f70268175948b41abaa1fee564a383
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056237"
---
# <span data-ttu-id="63c8c-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span><span class="sxs-lookup"><span data-stu-id="63c8c-101">Disconnect-AzVirtualNetworkGatewayVpnConnection</span></span>

## <span data-ttu-id="63c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63c8c-102">SYNOPSIS</span></span> 
<span data-ttu-id="63c8c-103">지정 된 가상 네트워크 게이트웨이와 연결 된 특정 vpn 클라이언트 연결을 끊습니다.</span><span class="sxs-lookup"><span data-stu-id="63c8c-103">Disconnect given connected vpn client connections with a given virtual network gateway.</span></span>

## <span data-ttu-id="63c8c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63c8c-104">SYNTAX</span></span>
### <span data-ttu-id="63c8c-105">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="63c8c-105">ByVpnGatewayName (Default)</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName <String> -ResourceGroupName <String> -InputObject <PSVirtualNetworkGateway> -ResourceId <ResourceId> -VpnConnectionId <VpnConnectionIds> [-AsJob] [<CommonParameters>]
```

### <span data-ttu-id="63c8c-106">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="63c8c-106">ByVpnGatewayObject</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -InputObject <PSP2SVpnGateway> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

### <span data-ttu-id="63c8c-107">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="63c8c-107">ByVpnGatewayResourceId</span></span>
```
Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceId <String> -VpnConnectionId <VpnConnectionId> [<CommonParameters>]
```

## <span data-ttu-id="63c8c-108">설명은</span><span class="sxs-lookup"><span data-stu-id="63c8c-108">DESCRIPTION</span></span>
<span data-ttu-id="63c8c-109">**AzVirtualNetworkGatewayVpnConnection** cmdlet을 사용 하면 연결 된 vpn 클라이언트 연결을 끊을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="63c8c-109">The **Disconnect-AzVirtualNetworkGatewayVpnConnection** cmdlet enables you to disconnect given connected vpn client connection.</span></span>

## <span data-ttu-id="63c8c-110">예제의</span><span class="sxs-lookup"><span data-stu-id="63c8c-110">EXAMPLES</span></span>

### <span data-ttu-id="63c8c-111">예</span><span class="sxs-lookup"><span data-stu-id="63c8c-111">Example</span></span>
```
PS C:\> Disconnect-AzVirtualNetworkGatewayVpnConnection -ResourceName vnet-gw -ResourceGroupName vnetgwrg -VpnConnectionId @("IKEv2_7e1cfe59-5c7c-4315-a876-b11fbfdfeed4")

```

## <span data-ttu-id="63c8c-112">변수</span><span class="sxs-lookup"><span data-stu-id="63c8c-112">PARAMETERS</span></span>

### <span data-ttu-id="63c8c-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="63c8c-113">-ResourceGroupName</span></span>
<span data-ttu-id="63c8c-114">가상 네트워크 게이트웨이 리소스 그룹의 이름</span><span class="sxs-lookup"><span data-stu-id="63c8c-114">Virtual network gateway resource group's name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c8c-115">-Context.resourcename</span><span class="sxs-lookup"><span data-stu-id="63c8c-115">-ResourceName</span></span>
<span data-ttu-id="63c8c-116">가상 네트워크 게이트웨이 이름</span><span class="sxs-lookup"><span data-stu-id="63c8c-116">Virtual network gateway name</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: VirtualNetworkGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c8c-117">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="63c8c-117">-ResourceId</span></span>
<span data-ttu-id="63c8c-118">가상 네트워크 게이트웨이 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="63c8c-118">Virtual network gateway resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="63c8c-119">-VpnConnectionId</span><span class="sxs-lookup"><span data-stu-id="63c8c-119">-VpnConnectionId</span></span>
<span data-ttu-id="63c8c-120">Vpn 연결 Id</span><span class="sxs-lookup"><span data-stu-id="63c8c-120">Vpn Connection Ids</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: VpnConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="63c8c-121">-InputObject</span><span class="sxs-lookup"><span data-stu-id="63c8c-121">-InputObject</span></span>
<span data-ttu-id="63c8c-122">가상 네트워크 게이트웨이 개체</span><span class="sxs-lookup"><span data-stu-id="63c8c-122">Virtual network gateway object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VirtualNetworkGateway

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="63c8c-123">-AsJob</span><span class="sxs-lookup"><span data-stu-id="63c8c-123">-AsJob</span></span>
<span data-ttu-id="63c8c-124">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="63c8c-124">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="63c8c-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63c8c-125">CommonParameters</span></span>
<span data-ttu-id="63c8c-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63c8c-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63c8c-127">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="63c8c-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63c8c-128">입력</span><span class="sxs-lookup"><span data-stu-id="63c8c-128">INPUTS</span></span>

### <span data-ttu-id="63c8c-129">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="63c8c-129">System.String</span></span>

## <span data-ttu-id="63c8c-130">출력</span><span class="sxs-lookup"><span data-stu-id="63c8c-130">OUTPUTS</span></span>

### <span data-ttu-id="63c8c-131">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="63c8c-131">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

## <span data-ttu-id="63c8c-132">상속자</span><span class="sxs-lookup"><span data-stu-id="63c8c-132">NOTES</span></span>

## <span data-ttu-id="63c8c-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63c8c-133">RELATED LINKS</span></span>
