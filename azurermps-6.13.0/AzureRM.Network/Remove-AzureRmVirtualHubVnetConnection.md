---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvirtualhubvnetConnection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVirtualHubVnetConnection.md
ms.openlocfilehash: 3a7c48803f18bf73f75e721296757e37ff89d44c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702107"
---
# <span data-ttu-id="78fff-101">Remove-AzureRmVirtualHubVnetConnection</span><span class="sxs-lookup"><span data-stu-id="78fff-101">Remove-AzureRmVirtualHubVnetConnection</span></span>

## <span data-ttu-id="78fff-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="78fff-102">SYNOPSIS</span></span>
<span data-ttu-id="78fff-103">Remove-AzureRmVirtualHubVnetConnection cmdlet은 원격 VNET을 허브 VNET에 피어 하는 Azure 가상 네트워크 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-103">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="78fff-104">구문과</span><span class="sxs-lookup"><span data-stu-id="78fff-104">SYNTAX</span></span>

### <span data-ttu-id="78fff-105">ByHubVirtualNetworkConnectionName (기본값)</span><span class="sxs-lookup"><span data-stu-id="78fff-105">ByHubVirtualNetworkConnectionName (Default)</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName <String> -ParentResourceName <String> -Name <String>
 [-AsJob] [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="78fff-106">ByHubVirtualNetworkConnectionObject</span><span class="sxs-lookup"><span data-stu-id="78fff-106">ByHubVirtualNetworkConnectionObject</span></span>
```
Remove-AzureRmVirtualHubVnetConnection [-InputObject <PSHubVirtualNetworkConnection>] [-AsJob] [-Force]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="78fff-107">ByHubVirtualNetworkConnectionResourceId</span><span class="sxs-lookup"><span data-stu-id="78fff-107">ByHubVirtualNetworkConnectionResourceId</span></span>
```
Remove-AzureRmVirtualHubVnetConnection -ResourceId <String> [-AsJob] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="78fff-108">설명은</span><span class="sxs-lookup"><span data-stu-id="78fff-108">DESCRIPTION</span></span>
<span data-ttu-id="78fff-109">Remove-AzureRmVirtualHubVnetConnection cmdlet은 원격 VNET을 허브 VNET에 피어 하는 Azure 가상 네트워크 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-109">The Remove-AzureRmVirtualHubVnetConnection cmdlet removes an Azure Virtual Network Connection which peers a remote VNET to the hub VNET.</span></span>

## <span data-ttu-id="78fff-110">예제의</span><span class="sxs-lookup"><span data-stu-id="78fff-110">EXAMPLES</span></span>

### <span data-ttu-id="78fff-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="78fff-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Remove-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection
```

<span data-ttu-id="78fff-112">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="78fff-113">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-113">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="78fff-114">허브 가상 네트워크 연결을 만든 후에는 해당 리소스 그룹 이름, 허브 이름 및 연결 이름을 사용 하 여 허브 가상 네트워크 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-114">After the hub virtual network connection is created, it removes the hub virtual network connection using its resource group name, the hub name and the connection name.</span></span>

### <span data-ttu-id="78fff-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="78fff-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $frontendSubnet = New-AzureRmVirtualNetworkSubnetConfig -Name frontendSubnet -AddressPrefix "10.0.1.0/24"
PS C:\> $backendSubnet  = New-AzureRmVirtualNetworkSubnetConfig -Name backendSubnet  -AddressPrefix "10.0.2.0/24"
PS C:\> $remoteVirtualNetwork = New-AzureRmVirtualNetwork -Name "MyVirtualNetwork" -ResourceGroupName "testRG" -Location "West US" -AddressPrefix "10.0.0.0/16" -Subnet $frontendSubnet,$backendSubnet
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName "testRG" -Name "myVirtualWAN" -Location "West US"
PS C:\> New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.1.0/24"
PS C:\> New-AzureRmVirtualHubVnetConnection -ResourceGroupName "testRG" -VirtualHubName "westushub" -Name "testvnetconnection" -RemoteVirtualNetwork $remoteVirtualNetwork
PS C:\> Get-AzureRmVirtualHubVnetConnection -ResourceGroupName testRG -VirtualHubName westushub -Name testvnetconnection | Remove-AzureRmHubVnetConnection
```

<span data-ttu-id="78fff-116">Azure에서 해당 리소스 그룹의 중앙 US에 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-116">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in Central US in that resource group in Azure.</span></span> <span data-ttu-id="78fff-117">가상 네트워크 연결이 생성 되 고 그 후 가상 네트워크를 가상 허브로 피어에 게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-117">A Virtual Network Connection will be created thereafter which will peer the Virtual Network to the Virtual Hub.</span></span>

<span data-ttu-id="78fff-118">허브 가상 네트워크 연결을 만든 후에는 AzureRmHubVirtualNetworkConnection의 출력에서 powershell 파이핑을 사용 하 여 허브 가상 네트워크 연결을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-118">After the hub virtual network connection is created, it removes the hub virtual network connection using powershell piping on the output from Get-AzureRmHubVirtualNetworkConnection.</span></span>

## <span data-ttu-id="78fff-119">변수</span><span class="sxs-lookup"><span data-stu-id="78fff-119">PARAMETERS</span></span>

### <span data-ttu-id="78fff-120">-AsJob</span><span class="sxs-lookup"><span data-stu-id="78fff-120">-AsJob</span></span>
<span data-ttu-id="78fff-121">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="78fff-121">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="78fff-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="78fff-122">-DefaultProfile</span></span>
<span data-ttu-id="78fff-123">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="78fff-124">-Force</span><span class="sxs-lookup"><span data-stu-id="78fff-124">-Force</span></span>
<span data-ttu-id="78fff-125">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="78fff-125">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="78fff-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="78fff-126">-InputObject</span></span>
<span data-ttu-id="78fff-127">수정할 hubvirtualnetworkconnection 리소스입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-127">The hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="78fff-128">-이름</span><span class="sxs-lookup"><span data-stu-id="78fff-128">-Name</span></span>
<span data-ttu-id="78fff-129">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-129">The resource name.</span></span>

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

### <span data-ttu-id="78fff-130">-ParentResourceName</span><span class="sxs-lookup"><span data-stu-id="78fff-130">-ParentResourceName</span></span>
<span data-ttu-id="78fff-131">부모 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-131">The parent resource name.</span></span>

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

### <span data-ttu-id="78fff-132">-PassThru</span><span class="sxs-lookup"><span data-stu-id="78fff-132">-PassThru</span></span>
<span data-ttu-id="78fff-133">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-133">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="78fff-134">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-134">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="78fff-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="78fff-135">-ResourceGroupName</span></span>
<span data-ttu-id="78fff-136">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-136">The resource group name.</span></span>

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

### <span data-ttu-id="78fff-137">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="78fff-137">-ResourceId</span></span>
<span data-ttu-id="78fff-138">수정할 hubvirtualnetworkconnection 리소스의 리소스 id입니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-138">The resource id of the hubvirtualnetworkconnection resource to modify.</span></span>

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

### <span data-ttu-id="78fff-139">-확인</span><span class="sxs-lookup"><span data-stu-id="78fff-139">-Confirm</span></span>
<span data-ttu-id="78fff-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="78fff-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="78fff-141">-WhatIf</span></span>
<span data-ttu-id="78fff-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="78fff-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="78fff-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="78fff-144">CommonParameters</span></span>
<span data-ttu-id="78fff-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="78fff-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="78fff-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="78fff-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="78fff-147">입력</span><span class="sxs-lookup"><span data-stu-id="78fff-147">INPUTS</span></span>

### <span data-ttu-id="78fff-148">PSHubVirtualNetworkConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="78fff-148">Microsoft.Azure.Commands.Network.Models.PSHubVirtualNetworkConnection</span></span>

### <span data-ttu-id="78fff-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="78fff-149">System.String</span></span>

## <span data-ttu-id="78fff-150">출력</span><span class="sxs-lookup"><span data-stu-id="78fff-150">OUTPUTS</span></span>

### <span data-ttu-id="78fff-151">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="78fff-151">System.Boolean</span></span>

## <span data-ttu-id="78fff-152">상속자</span><span class="sxs-lookup"><span data-stu-id="78fff-152">NOTES</span></span>

## <span data-ttu-id="78fff-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="78fff-153">RELATED LINKS</span></span>
