---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualwanvpnconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualWanVpnConfiguration.md
ms.openlocfilehash: be0fbc9b9fc6d91a5bf94344f432b67dfc38cab3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529534"
---
# <span data-ttu-id="79f93-101">Get-AzureRmVirtualWanVpnConfiguration</span><span class="sxs-lookup"><span data-stu-id="79f93-101">Get-AzureRmVirtualWanVpnConfiguration</span></span>

## <span data-ttu-id="79f93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79f93-102">SYNOPSIS</span></span>
<span data-ttu-id="79f93-103">VpnConnections를 통해이 WAN에 연결 된 VpnSites 하위 집합의 Vpn 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-103">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="79f93-104">생성 된 Vpn 구성을 고객이 지정한 저장소 blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-104">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79f93-105">구문과</span><span class="sxs-lookup"><span data-stu-id="79f93-105">SYNTAX</span></span>

### <span data-ttu-id="79f93-106">ByVirtualWanNameByVpnSiteObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="79f93-106">ByVirtualWanNameByVpnSiteObject (Default)</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f93-107">ByVirtualWanNameByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="79f93-107">ByVirtualWanNameByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceGroupName <String> -Name <String> -StorageSasUrl <String>
 -VpnSiteId <String[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f93-108">ByVirtualWanObjectByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="79f93-108">ByVirtualWanObjectByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String>
 -VpnSite <PSVpnSite[]> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f93-109">ByVirtualWanObjectByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="79f93-109">ByVirtualWanObjectByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -InputObject <PSVirtualWan> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f93-110">ByVirtualWanResourceIdByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="79f93-110">ByVirtualWanResourceIdByVpnSiteObject</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSite <PSVpnSite[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79f93-111">ByVirtualWanResourceIdByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="79f93-111">ByVirtualWanResourceIdByVpnSiteResourceId</span></span>
```
Get-AzureRmVirtualWanVpnConfiguration -ResourceId <String> -StorageSasUrl <String> -VpnSiteId <String[]>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79f93-112">설명은</span><span class="sxs-lookup"><span data-stu-id="79f93-112">DESCRIPTION</span></span>
<span data-ttu-id="79f93-113">VpnConnections를 통해이 WAN에 연결 된 VpnSites 하위 집합의 Vpn 구성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-113">Gets the Vpn configuration for a subset of VpnSites connected to this WAN via VpnConnections.</span></span> <span data-ttu-id="79f93-114">생성 된 Vpn 구성을 고객이 지정한 저장소 blob에 업로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-114">Uploads the generated Vpn configuration to a storage blob specified by the customer.</span></span>

## <span data-ttu-id="79f93-115">예제의</span><span class="sxs-lookup"><span data-stu-id="79f93-115">EXAMPLES</span></span>

### <span data-ttu-id="79f93-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="79f93-116">Example 1</span></span>
```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub = New-AzureRmVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\> New-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw" -VirtualHubId $virtualHub.Id -BGPPeeringWeight 10 -VpnGatewayScaleUnit 2
PS C:\> $vpnGateway = Get-AzureRmVpnGateway -ResourceGroupName "testRG" -Name "testvpngw"

PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"

PS C:\> $vpnSite = New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"

PS C:\> New-AzureRmVpnConnection -ResourceGroupName $vpnGateway.ResourceGroupName -ParentResourceName $vpnGateway.Name -Name "testConnection" -VpnSite $vpnSite

PS C:\> $vpnSitesForConfig = New-Object Microsoft.Azure.Commands.Network.Models.PSVpnSite[] 1
PS C:\> $vpnSitesForConfig[0] = $vpnSite
PS C:\> Get-AzureRmVirtualWanVpnConfiguration -VirtualWan $virtualWan -StorageSasUrl "SignedSasUrl" -VpnSite $vpnSitesForConfig

SasUrl
------
SignedSasUrl
```

<span data-ttu-id="79f93-117">위의 예는 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브 및 VpnSite을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-117">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub and a VpnSite in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="79f93-118">VPN 게이트웨이는 2 개의 배율 단위를 사용 하 여 가상 허브에서 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-118">A VPN gateway will be created thereafter in the Virtual Hub with 2 scale units.</span></span>

<span data-ttu-id="79f93-119">게이트웨이가 만들어지면 New-AzureRmVpnConnection 명령을 사용 하 여 VpnSite에 연결 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-119">Once the gateway has been created, it is connected to the VpnSite using the New-AzureRmVpnConnection command.</span></span>

<span data-ttu-id="79f93-120">그런 다음이 이상 구성을 사용 하 여 다운로드 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-120">The configuration is then downloaded using this commandlet.</span></span>

<span data-ttu-id="79f93-121">SignedSasUrl가 성공적으로 실행 되 면 다운로드 구성은이 (가) 표시 하는 blob에 기록 됩니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-121">If the commandlet is successful, then the download configuration will be written to the blob indicated by the SignedSasUrl.</span></span>

## <span data-ttu-id="79f93-122">변수</span><span class="sxs-lookup"><span data-stu-id="79f93-122">PARAMETERS</span></span>

### <span data-ttu-id="79f93-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79f93-123">-DefaultProfile</span></span>
<span data-ttu-id="79f93-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="79f93-125">-InputObject</span><span class="sxs-lookup"><span data-stu-id="79f93-125">-InputObject</span></span>
<span data-ttu-id="79f93-126">수정할 vpn 사이트 개체</span><span class="sxs-lookup"><span data-stu-id="79f93-126">The vpn site object to be modified</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVirtualWan
Parameter Sets: ByVirtualWanObjectByVpnSiteObject, ByVirtualWanObjectByVpnSiteResourceId
Aliases: VirtualWan

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-127">-이름</span><span class="sxs-lookup"><span data-stu-id="79f93-127">-Name</span></span>
<span data-ttu-id="79f93-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases: ResourceName, VirtualWanName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79f93-129">-ResourceGroupName</span></span>
<span data-ttu-id="79f93-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanNameByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="79f93-131">-ResourceId</span></span>
<span data-ttu-id="79f93-132">가상 wan에 대 한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-132">The Azure resource ID for the virtual wan.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVirtualWanResourceIdByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases: VirtualWanId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-133">-StorageSasUrl</span><span class="sxs-lookup"><span data-stu-id="79f93-133">-StorageSasUrl</span></span>
<span data-ttu-id="79f93-134">구성을 생성할 저장소 위치의 SAS Url입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-134">The SAS Url for the storage location where the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-135">-VpnSite</span><span class="sxs-lookup"><span data-stu-id="79f93-135">-VpnSite</span></span>
<span data-ttu-id="79f93-136">구성을 생성할 VpnSite 리소스 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-136">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite[]
Parameter Sets: ByVirtualWanNameByVpnSiteObject, ByVirtualWanObjectByVpnSiteObject, ByVirtualWanResourceIdByVpnSiteObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-137">-VpnSiteId</span><span class="sxs-lookup"><span data-stu-id="79f93-137">-VpnSiteId</span></span>
<span data-ttu-id="79f93-138">구성을 생성할 VpnSite 리소스 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-138">The list of VpnSite resource ids to generate configuration for.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByVirtualWanNameByVpnSiteResourceId, ByVirtualWanObjectByVpnSiteResourceId, ByVirtualWanResourceIdByVpnSiteResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79f93-139">-확인</span><span class="sxs-lookup"><span data-stu-id="79f93-139">-Confirm</span></span>
<span data-ttu-id="79f93-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79f93-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79f93-141">-WhatIf</span></span>
<span data-ttu-id="79f93-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="79f93-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79f93-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79f93-144">CommonParameters</span></span>
<span data-ttu-id="79f93-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79f93-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79f93-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79f93-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79f93-147">입력</span><span class="sxs-lookup"><span data-stu-id="79f93-147">INPUTS</span></span>

### <span data-ttu-id="79f93-148">Microsoft. 네트워크 모델. PSVirtualWan</span><span class="sxs-lookup"><span data-stu-id="79f93-148">Microsoft.Azure.Commands.Network.Models.PSVirtualWan</span></span>

### <span data-ttu-id="79f93-149">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="79f93-149">System.String</span></span>

## <span data-ttu-id="79f93-150">출력</span><span class="sxs-lookup"><span data-stu-id="79f93-150">OUTPUTS</span></span>

### <span data-ttu-id="79f93-151">PSVirtualWanVpnSitesConfiguration에 대 한.</span><span class="sxs-lookup"><span data-stu-id="79f93-151">Microsoft.Azure.Commands.Network.Models.PSVirtualWanVpnSitesConfiguration</span></span>

## <span data-ttu-id="79f93-152">상속자</span><span class="sxs-lookup"><span data-stu-id="79f93-152">NOTES</span></span>

## <span data-ttu-id="79f93-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79f93-153">RELATED LINKS</span></span>
