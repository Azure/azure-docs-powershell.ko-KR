---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualHubVnetConnection.md
ms.openlocfilehash: 3be41be3c62b0676ea10e9fe7c9d89927c4de757
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043237"
---
# <span data-ttu-id="8454a-101">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8454a-101">New-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="8454a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8454a-102">SYNOPSIS</span></span>
<span data-ttu-id="8454a-103">New-AzVirtualHubVnetConnection cmdlet은 가상 네트워크를 Azure 가상 허브에 피어 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-103">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="8454a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8454a-104">SYNTAX</span></span>

### <span data-ttu-id="8454a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="8454a-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8454a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8454a-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8454a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="8454a-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8454a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8454a-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="8454a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="8454a-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-EnableInternetSecurity] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="8454a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="8454a-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-EnableInternetSecurity] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="8454a-111">설명은</span><span class="sxs-lookup"><span data-stu-id="8454a-111">DESCRIPTION</span></span>
<span data-ttu-id="8454a-112">New-AzVirtualHubVnetConnection cmdlet은 가상 네트워크를 Azure 가상 허브에 피어 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-112">The New-AzVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="8454a-113">예제의</span><span class="sxs-lookup"><span data-stu-id="8454a-113">EXAMPLES</span></span>

### <span data-ttu-id="8454a-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="8454a-114">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
EnableInternetSecurity : False
ProvisioningState    : Succeeded
```

<span data-ttu-id="8454a-115">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="8454a-116">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="8454a-117">변수</span><span class="sxs-lookup"><span data-stu-id="8454a-117">PARAMETERS</span></span>

### <span data-ttu-id="8454a-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="8454a-118">-AsJob</span></span>
<span data-ttu-id="8454a-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="8454a-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="8454a-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8454a-120">-DefaultProfile</span></span>
<span data-ttu-id="8454a-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-122">-EnableInternetSecurity</span><span class="sxs-lookup"><span data-stu-id="8454a-122">-EnableInternetSecurity</span></span>
<span data-ttu-id="8454a-123">이 연결에 인터넷 보안 설정</span><span class="sxs-lookup"><span data-stu-id="8454a-123">Enable internet security for this connection</span></span>

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

### <span data-ttu-id="8454a-124">-이름</span><span class="sxs-lookup"><span data-stu-id="8454a-124">-Name</span></span>
<span data-ttu-id="8454a-125">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-125">The resource name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="8454a-126">-ParentObject</span></span>
<span data-ttu-id="8454a-127">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-127">The parent resource.</span></span>

```yaml
Type: PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-128">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="8454a-128">-ParentResourceId</span></span>
<span data-ttu-id="8454a-129">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-129">The parent resource.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="8454a-130">-ParentResourceName</span></span>
<span data-ttu-id="8454a-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-131">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-132">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="8454a-132">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="8454a-133">이 허브 가상 네트워크 연결이 연결 되는 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-134">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="8454a-134">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="8454a-135">이 허브 가상 네트워크 연결이 연결 되는 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-135">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8454a-136">-ResourceGroupName</span></span>
<span data-ttu-id="8454a-137">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-137">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-138">-확인</span><span class="sxs-lookup"><span data-stu-id="8454a-138">-Confirm</span></span>
<span data-ttu-id="8454a-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-139">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="8454a-140">-WhatIf</span></span>
<span data-ttu-id="8454a-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="8454a-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-142">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8454a-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8454a-143">CommonParameters</span></span>
<span data-ttu-id="8454a-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8454a-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8454a-145">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8454a-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8454a-146">입력</span><span class="sxs-lookup"><span data-stu-id="8454a-146">INPUTS</span></span>

### <span data-ttu-id="8454a-147">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="8454a-147">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="8454a-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="8454a-148">System.String</span></span>

## <span data-ttu-id="8454a-149">출력</span><span class="sxs-lookup"><span data-stu-id="8454a-149">OUTPUTS</span></span>

### <span data-ttu-id="8454a-150">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="8454a-150">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="8454a-151">상속자</span><span class="sxs-lookup"><span data-stu-id="8454a-151">NOTES</span></span>

## <span data-ttu-id="8454a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8454a-152">RELATED LINKS</span></span>

[<span data-ttu-id="8454a-153">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8454a-153">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="8454a-154">제거-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="8454a-154">Remove-AzVirtualHubVnetConnection</span></span>](./Remove-AzVirtualHubVnetConnection.md)
