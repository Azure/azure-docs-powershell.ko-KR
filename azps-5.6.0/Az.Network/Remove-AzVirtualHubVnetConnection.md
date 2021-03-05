---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/remove-azvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVirtualHubVnetConnection.md
ms.openlocfilehash: f5a48ec9ac28e13af7aaa763afe72437bed5fda4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006064"
---
# <span data-ttu-id="f2185-101">Remove-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f2185-101">Remove-AzVirtualHubVnetConnection</span></span>

## <span data-ttu-id="f2185-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f2185-102">SYNOPSIS</span></span>
<span data-ttu-id="f2185-103">Remove-AzVirtualHubVnetConnection cmdlet은 허브 VNET에 원격 VNET을 피어링하는 Azure Virtual Network 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-103">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f2185-104">구문</span><span class="sxs-lookup"><span data-stu-id="f2185-104">SYNTAX</span></span>

### <span data-ttu-id="f2185-105">ByHubVirtualNetworkConnectionName(기본값)</span><span class="sxs-lookup"><span data-stu-id="f2185-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f2185-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="f2185-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f2185-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="f2185-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f2185-108">설명</span><span class="sxs-lookup"><span data-stu-id="f2185-108">DESCRIPTION</span></span>
<span data-ttu-id="f2185-109">Remove-AzVirtualHubVnetConnection cmdlet은 허브 VNET에 원격 VNET을 피어링하는 Azure Virtual Network 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-109">The Remove-AzVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="f2185-110">예제</span><span class="sxs-lookup"><span data-stu-id="f2185-110">EXAMPLES</span></span>

### <span data-ttu-id="f2185-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f2185-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="f2185-112">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f2185-113">이후 가상 네트워크 연결이 만들어지며 가상 네트워크를 Virtual Hub에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f2185-114">허브 가상 네트워크 연결을 만든 후 해당 리소스 그룹 이름, 허브 이름 및 연결 이름을 사용하여 허브 가상 네트워크 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="f2185-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f2185-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzHubVnetConnection
```

<span data-ttu-id="f2185-116">위의 리소스 그룹인 Virtual WAN, Virtual Network, Virtual Hub는 Azure의 해당 리소스 그룹에 미국 중부에 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="f2185-117">이후 가상 네트워크 연결이 만들어지며 가상 네트워크를 Virtual Hub에 피어링합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="f2185-118">허브 가상 네트워크 연결을 만든 후 Get-AzHubVirtualNetworkConnection에서 출력의 powershell 배관을 사용하여 허브 가상 네트워크 연결을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="f2185-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f2185-119">PARAMETERS</span></span>

### <span data-ttu-id="f2185-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f2185-120">-AsJob</span></span>
<span data-ttu-id="f2185-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f2185-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f2185-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f2185-122">-DefaultProfile</span></span>
<span data-ttu-id="f2185-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f2185-124">-Force</span><span class="sxs-lookup"><span data-stu-id="f2185-124">-Force</span></span>
<span data-ttu-id="f2185-125">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="f2185-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f2185-126">-InputObject</span></span>
<span data-ttu-id="f2185-127">수정할 hubvirtualnetworkconnection 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-127">The hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection
Parameter Sets: ByHubVirtualNetworkConnectionObject
Aliases: HubVirtualNetworkConnection

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f2185-128">-Name</span><span class="sxs-lookup"><span data-stu-id="f2185-128">-Name</span></span>
<span data-ttu-id="f2185-129">리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-129">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: ResourceName, HubVirtualNetworkConnectionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2185-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="f2185-130">-ParentResourceName</span></span>
<span data-ttu-id="f2185-131">상위 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-131">The parent resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases: VirtualHubName, ParentVirtualHubName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2185-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f2185-132">-PassThru</span></span>
<span data-ttu-id="f2185-133">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="f2185-134">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f2185-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f2185-135">-ResourceGroupName</span></span>
<span data-ttu-id="f2185-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-136">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f2185-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f2185-137">-ResourceId</span></span>
<span data-ttu-id="f2185-138">수정할 hubvirtualnetworkconnection 리소스의 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

```yaml
Type: System.String
Parameter Sets: ByHubVirtualNetworkConnectionResourceId
Aliases: HubVirtualNetworkConnectionId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f2185-139">-확인</span><span class="sxs-lookup"><span data-stu-id="f2185-139">-Confirm</span></span>
<span data-ttu-id="f2185-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f2185-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f2185-141">-WhatIf</span></span>
<span data-ttu-id="f2185-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f2185-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f2185-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f2185-144">CommonParameters</span></span>
<span data-ttu-id="f2185-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f2185-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f2185-146">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f2185-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f2185-147">입력</span><span class="sxs-lookup"><span data-stu-id="f2185-147">INPUTS</span></span>

### <span data-ttu-id="f2185-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span><span class="sxs-lookup"><span data-stu-id="f2185-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="f2185-149">System.String</span><span class="sxs-lookup"><span data-stu-id="f2185-149">System.String</span></span>

## <span data-ttu-id="f2185-150">출력</span><span class="sxs-lookup"><span data-stu-id="f2185-150">OUTPUTS</span></span>

### <span data-ttu-id="f2185-151">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="f2185-151">System.Boolean</span></span>

## <span data-ttu-id="f2185-152">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f2185-152">NOTES</span></span>

## <span data-ttu-id="f2185-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f2185-153">RELATED LINKS</span></span>

[<span data-ttu-id="f2185-154">Get-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f2185-154">Get-AzVirtualHubVnetConnection</span></span>](./Get-AzVirtualHubVnetConnection.md)

[<span data-ttu-id="f2185-155">New-AzVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="f2185-155">New-AzVirtualHubVnetConnection</span></span>](./New-AzVirtualHubVnetConnection.md)
