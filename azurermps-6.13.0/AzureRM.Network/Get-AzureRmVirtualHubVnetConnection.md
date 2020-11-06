---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualhubvnetconnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 8aeb992b08e2749168ef3da2db6c264158c6a9ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528515"
---
# <span data-ttu-id="d6f38-101">Get-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="d6f38-101">Get-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="d6f38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d6f38-102">SYNOPSIS</span></span>
<span data-ttu-id="d6f38-103">가상 허브에서 가상 네트워크 연결을 가져오거나 가상 허브의 모든 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-103">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d6f38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d6f38-104">SYNTAX</span></span>

### <span data-ttu-id="d6f38-105">ByVirtualHubName (기본값)</span><span class="sxs-lookup"><span data-stu-id="d6f38-105">ByVirtualHubName (Default)</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f38-106">ByVirtualHubObject</span><span class="sxs-lookup"><span data-stu-id="d6f38-106">ByVirtualHubObject</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentObject <PSVirtualHub> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d6f38-107">ByVirtualHubResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f38-107">ByVirtualHubResourceId</span></span>
```
Get-AzureRmVirtualHubVnetConnection -ParentResourceId <String> [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d6f38-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d6f38-108">DESCRIPTION</span></span>
<span data-ttu-id="d6f38-109">가상 허브에서 가상 네트워크 연결을 가져오거나 가상 허브의 모든 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-109">Gets a Virtual Network Connection in a virtual hub or lists all virtual network connections in a virtual hub.</span></span>

## <span data-ttu-id="d6f38-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d6f38-110">EXAMPLES</span></span>

### <span data-ttu-id="d6f38-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="d6f38-111">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet

PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork

PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="d6f38-112">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d6f38-113">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d6f38-114">허브 가상 네트워크 연결을 만든 후에는 해당 리소스 그룹 이름, 허브 이름 및 연결 이름을 사용 하 여 허브 가상 네트워크 연결을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-114">After the hub virtual network connection is created, it gets the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="d6f38-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="d6f38-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub

Name                 : testvnetconnection
Id                   : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualHubs/westushub/hubVirtualNetworkConnections/testvnetconnection
RemoteVirtualNetwork : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/virtualNetworks/MyVirtualNetwork
ProvisioningState    : Succeeded
```

<span data-ttu-id="d6f38-116">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="d6f38-117">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="d6f38-118">허브 가상 네트워크 연결을 만든 후에는 해당 리소스 그룹 이름과 허브 이름을 사용 하 여 모든 허브 가상 네트워크 연결을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-118">After the hub virtual network connection is created, it lists all the hub virtual network connection using its resource group name and the hub name.</span></span>

## <span data-ttu-id="d6f38-119">변수</span><span class="sxs-lookup"><span data-stu-id="d6f38-119">PARAMETERS</span></span>

### <span data-ttu-id="d6f38-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d6f38-120">-DefaultProfile</span></span>
<span data-ttu-id="d6f38-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d6f38-122">-이름</span><span class="sxs-lookup"><span data-stu-id="d6f38-122">-Name</span></span>
<span data-ttu-id="d6f38-123">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-123">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f38-124">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="d6f38-124">-ParentObject</span></span>
<span data-ttu-id="d6f38-125">부모 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-125">The parent resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualHub
Parameter Sets: ByVirtualHubObject
Aliases: VirtualHub, ParentVirtualHub

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f38-126">-ParentResourceId</span><span class="sxs-lookup"><span data-stu-id="d6f38-126">-ParentResourceId</span></span>
<span data-ttu-id="d6f38-127">부모 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-127">The parent resource id.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubResourceId
Aliases: VirtualHubId, ParentVirtualHubId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d6f38-128">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="d6f38-128">-ParentResourceName</span></span>
<span data-ttu-id="d6f38-129">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-129">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f38-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d6f38-130">-ResourceGroupName</span></span>
<span data-ttu-id="d6f38-131">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-131">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualHubName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d6f38-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d6f38-132">CommonParameters</span></span>
<span data-ttu-id="d6f38-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d6f38-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d6f38-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d6f38-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d6f38-135">입력</span><span class="sxs-lookup"><span data-stu-id="d6f38-135">INPUTS</span></span>

### <span data-ttu-id="d6f38-136">않아야</span><span class="sxs-lookup"><span data-stu-id="d6f38-136">None</span></span>

## <span data-ttu-id="d6f38-137">출력</span><span class="sxs-lookup"><span data-stu-id="d6f38-137">OUTPUTS</span></span>

### <span data-ttu-id="d6f38-138">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d6f38-138">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

## <span data-ttu-id="d6f38-139">상속자</span><span class="sxs-lookup"><span data-stu-id="d6f38-139">NOTES</span></span>

## <span data-ttu-id="d6f38-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d6f38-140">RELATED LINKS</span></span>
