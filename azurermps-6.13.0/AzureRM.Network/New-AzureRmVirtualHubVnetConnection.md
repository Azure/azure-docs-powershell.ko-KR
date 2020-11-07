---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 6805d6671d0335599dc95f206ddb8482867734fc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703148"
---
# <span data-ttu-id="d1dfb-101">New-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d1dfb-101">New-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d1dfb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1dfb-102">SYNOPSIS</span></span>
<span data-ttu-id="d1dfb-103">New-AzureRmVirtualHubVnetConnection cmdlet은 가상 네트워크를 Azure 가상 허브에 피어 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-103">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d1dfb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1dfb-104">SYNTAX</span></span>

### <span data-ttu-id="d1dfb-105">ByVirtualHubNameByRemoteVirtualNetworkObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1dfb-105">ByVirtualHubNameByRemoteVirtualNetworkObject (Default)</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1dfb-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d1dfb-106">ByVirtualHubNameByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1dfb-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="d1dfb-107">ByVirtualHubObjectByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1dfb-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d1dfb-108">ByVirtualHubObjectByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> -Name <String>
 -RemoteVirtualNetworkId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d1dfb-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span><span class="sxs-lookup"><span data-stu-id="d1dfb-109">ByVirtualHubResourceIdByRemoteVirtualNetworkObject</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String>
 -RemoteVirtualNetwork <PSVirtualNetwork> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d1dfb-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span><span class="sxs-lookup"><span data-stu-id="d1dfb-110">ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId</span></span>
```
New-AzureRmVirtualHubVnetConnection -ParentResourceId <String> -Name <String> -RemoteVirtualNetworkId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d1dfb-111">설명은</span><span class="sxs-lookup"><span data-stu-id="d1dfb-111">DESCRIPTION</span></span>
<span data-ttu-id="d1dfb-112">New-AzureRmVirtualHubVnetConnection cmdlet은 가상 네트워크를 Azure 가상 허브에 피어 HubVirtualNetworkConnection 리소스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-112">The New-AzureRmVirtualHubVnetConnection cmdlet creates a HubVirtualNetworkConnection resource that peers a Virtual Network to the Azure Virtual Hub.</span></span>

## <span data-ttu-id="d1dfb-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d1dfb-113">EXAMPLES</span></span>

### <span data-ttu-id="d1dfb-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="d1dfb-114">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="d1dfb-115">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-115">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d1dfb-116">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-116">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

## <span data-ttu-id="d1dfb-117">변수</span><span class="sxs-lookup"><span data-stu-id="d1dfb-117">PARAMETERS</span></span>

### <span data-ttu-id="d1dfb-118">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d1dfb-118">-AsJob</span></span>
<span data-ttu-id="d1dfb-119">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d1dfb-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d1dfb-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1dfb-120">-DefaultProfile</span></span>
<span data-ttu-id="d1dfb-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1dfb-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d1dfb-122">-Name</span></span>
<span data-ttu-id="d1dfb-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d1dfb-124">-ParentObject</span></span>
<span data-ttu-id="d1dfb-125">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkResourceId
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d1dfb-126">-ParentResourceId</span></span>
<span data-ttu-id="d1dfb-127">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-127">The parent resource.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceIdByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d1dfb-128">-ParentResourceName</span></span>
<span data-ttu-id="d1dfb-129">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-130">-RemoteVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="d1dfb-130">-RemoteVirtualNetwork</span></span>
<span data-ttu-id="d1dfb-131">이 허브 가상 네트워크 연결이 연결 되는 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-131">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualNetwork
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubObjectByRemoteVirtualNetworkObject, ByVirtualHubResourceIdByRemoteVirtualNetworkObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-132">-RemoteVirtualNetworkId</span><span class="sxs-lookup"><span data-stu-id="d1dfb-132">-RemoteVirtualNetworkId</span></span>
<span data-ttu-id="d1dfb-133">이 허브 가상 네트워크 연결이 연결 되는 원격 가상 네트워크입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-133">The remote virtual network to which this hub virtual network connection is connected.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkResourceId, ByVirtualHubObjectByRemoteVirtualNetworkResourceId, ByVirtualHubResourceIdByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1dfb-134">-ResourceGroupName</span></span>
<span data-ttu-id="d1dfb-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubNameByRemoteVirtualNetworkObject, ByVirtualHubNameByRemoteVirtualNetworkResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d1dfb-136">-확인</span><span class="sxs-lookup"><span data-stu-id="d1dfb-136">-Confirm</span></span>
<span data-ttu-id="d1dfb-137">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d1dfb-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d1dfb-138">-WhatIf</span></span>
<span data-ttu-id="d1dfb-139">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d1dfb-140">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d1dfb-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1dfb-141">CommonParameters</span></span>
<span data-ttu-id="d1dfb-142">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1dfb-143">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d1dfb-143">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1dfb-144">입력</span><span class="sxs-lookup"><span data-stu-id="d1dfb-144">INPUTS</span></span>

### <span data-ttu-id="d1dfb-145">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="d1dfb-145">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="d1dfb-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d1dfb-146">System.String</span></span>

## <span data-ttu-id="d1dfb-147">출력</span><span class="sxs-lookup"><span data-stu-id="d1dfb-147">OUTPUTS</span></span>

### <span data-ttu-id="d1dfb-148">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d1dfb-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d1dfb-149">상속자</span><span class="sxs-lookup"><span data-stu-id="d1dfb-149">NOTES</span></span>

## <span data-ttu-id="d1dfb-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1dfb-150">RELATED LINKS</span></span>
