---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpngateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnGateway.md
ms.openlocfilehash: 34e143b3ca6114fd90d52a5ad6ee8c022fda5688
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535723"
---
# <span data-ttu-id="02206-101">Remove-AzureRmVpnGateway</span><span class="sxs-lookup"><span data-stu-id="02206-101">Remove-AzureRmVpnGateway</span></span>

## <span data-ttu-id="02206-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="02206-102">SYNOPSIS</span></span>
<span data-ttu-id="02206-103">Remove-AzureRmVpnGateway cmdlet은 Azure VPN 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-103">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="02206-104">Azure 가상 WAN의 소프트웨어 정의 연결과 관련 된 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-104">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="02206-105">구문과</span><span class="sxs-lookup"><span data-stu-id="02206-105">SYNTAX</span></span>

### <span data-ttu-id="02206-106">ByVpnGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="02206-106">ByVpnGatewayName (Default)</span></span>
```
Remove-AzureRmVpnGateway -ResourceGroupName <String> -Name <String> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02206-107">ByVpnGatewayObject</span><span class="sxs-lookup"><span data-stu-id="02206-107">ByVpnGatewayObject</span></span>
```
Remove-AzureRmVpnGateway -InputObject <PSVpnGateway> [-PassThru] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="02206-108">ByVpnGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="02206-108">ByVpnGatewayResourceId</span></span>
```
Remove-AzureRmVpnGateway -ResourceId <String> [-PassThru] [-Force] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="02206-109">설명은</span><span class="sxs-lookup"><span data-stu-id="02206-109">DESCRIPTION</span></span>
<span data-ttu-id="02206-110">Remove-AzureRmVpnGateway cmdlet은 Azure VPN 게이트웨이를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-110">The Remove-AzureRmVpnGateway cmdlet removes an Azure VPN gateway.</span></span> <span data-ttu-id="02206-111">Azure 가상 WAN의 소프트웨어 정의 연결과 관련 된 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-111">This is a gateway specific to Azure Virtual WAN's software defined connectivity.</span></span>

## <span data-ttu-id="02206-112">예제의</span><span class="sxs-lookup"><span data-stu-id="02206-112">EXAMPLES</span></span>

### <span data-ttu-id="02206-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="02206-113">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Remove-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -Passthru
```

<span data-ttu-id="02206-114">이 예제에서는 중앙 US에 리소스 그룹, 가상 WAN, 가상 허브, 확장 가능한 VPN 게이트웨이를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-114">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="02206-115">가상 게이트웨이를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-115">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="02206-116">VpnGateway 및이에 연결 된 모든 VpnConnections 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02206-116">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

### <span data-ttu-id="02206-117">예제 2</span><span class="sxs-lookup"><span data-stu-id="02206-117">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" | Remove-AzureRmVpnGateway-Passthru
```

<span data-ttu-id="02206-118">이 예제에서는 중앙 US에 리소스 그룹, 가상 WAN, 가상 허브, 확장 가능한 VPN 게이트웨이를 만든 다음 즉시 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-118">This example creates a Resource group, Virtual WAN, Virtual Hub, scalable VPN gateway in Central US and then immediately deletes it.</span></span> <span data-ttu-id="02206-119">이 삭제는 Get-AzureRmVpnGateway 명령으로 반환 된 VpnGateway 개체를 사용 하는 powershell 파이핑을 사용 하 여 수행 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02206-119">This deletion happens using powershell piping, which uses the VpnGateway object returned by the Get-AzureRmVpnGateway command.</span></span>
<span data-ttu-id="02206-120">가상 게이트웨이를 삭제할 때 메시지가 표시 되지 않도록 하려면-Force 플래그를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-120">To suppress the prompt when deleting the Virtual Gateway, use the -Force flag.</span></span>
<span data-ttu-id="02206-121">VpnGateway 및이에 연결 된 모든 VpnConnections 삭제 됩니다.</span><span class="sxs-lookup"><span data-stu-id="02206-121">This will delete the VpnGateway and all VpnConnections attached to it.</span></span>

## <span data-ttu-id="02206-122">변수</span><span class="sxs-lookup"><span data-stu-id="02206-122">PARAMETERS</span></span>

### <span data-ttu-id="02206-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="02206-123">-DefaultProfile</span></span>
<span data-ttu-id="02206-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="02206-125">-Force</span><span class="sxs-lookup"><span data-stu-id="02206-125">-Force</span></span>
<span data-ttu-id="02206-126">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02206-126">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="02206-127">-InputObject</span><span class="sxs-lookup"><span data-stu-id="02206-127">-InputObject</span></span>
<span data-ttu-id="02206-128">삭제할 vpnGateway 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-128">The vpnGateway object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnGateway
Parameter Sets: ByVpnGatewayObject
Aliases: VpnGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="02206-129">-이름</span><span class="sxs-lookup"><span data-stu-id="02206-129">-Name</span></span>
<span data-ttu-id="02206-130">VpnGateway 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-130">The vpnGateway name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases: ResourceName, VpnGatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02206-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="02206-131">-PassThru</span></span>
<span data-ttu-id="02206-132">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-132">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="02206-133">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02206-133">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="02206-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="02206-134">-ResourceGroupName</span></span>
<span data-ttu-id="02206-135">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-135">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="02206-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="02206-136">-ResourceId</span></span>
<span data-ttu-id="02206-137">삭제할 vpnGateway의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="02206-137">The Azure resource ID for the vpnGateway to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnGatewayResourceId
Aliases: vpnGatewayId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="02206-138">-확인</span><span class="sxs-lookup"><span data-stu-id="02206-138">-Confirm</span></span>
<span data-ttu-id="02206-139">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="02206-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="02206-140">-WhatIf</span></span>
<span data-ttu-id="02206-141">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="02206-141">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="02206-142">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="02206-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="02206-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="02206-143">CommonParameters</span></span>
<span data-ttu-id="02206-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="02206-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="02206-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="02206-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="02206-146">입력</span><span class="sxs-lookup"><span data-stu-id="02206-146">INPUTS</span></span>

### <span data-ttu-id="02206-147">PSVpnGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="02206-147">Microsoft.Azure.Commands.Network.Models.PSVpnGateway</span></span>

### <span data-ttu-id="02206-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="02206-148">System.String</span></span>

## <span data-ttu-id="02206-149">출력</span><span class="sxs-lookup"><span data-stu-id="02206-149">OUTPUTS</span></span>

### <span data-ttu-id="02206-150">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="02206-150">System.Boolean</span></span>

## <span data-ttu-id="02206-151">상속자</span><span class="sxs-lookup"><span data-stu-id="02206-151">NOTES</span></span>

## <span data-ttu-id="02206-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="02206-152">RELATED LINKS</span></span>
