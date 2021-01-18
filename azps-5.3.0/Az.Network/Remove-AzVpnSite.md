---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496560"
---
# <span data-ttu-id="a09e4-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a09e4-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="a09e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a09e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a09e4-103">Azure VpnSite 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="a09e4-104">구문</span><span class="sxs-lookup"><span data-stu-id="a09e4-104">SYNTAX</span></span>

### <span data-ttu-id="a09e4-105">ByVpnSiteName(기본값)</span><span class="sxs-lookup"><span data-stu-id="a09e4-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09e4-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="a09e4-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a09e4-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="a09e4-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a09e4-108">설명</span><span class="sxs-lookup"><span data-stu-id="a09e4-108">DESCRIPTION</span></span>
<span data-ttu-id="a09e4-109">Azure VpnSite 리소스를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="a09e4-110">예제</span><span class="sxs-lookup"><span data-stu-id="a09e4-110">EXAMPLES</span></span>

### <span data-ttu-id="a09e4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="a09e4-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="a09e4-112">위의 경우 Azure의 "testRG" 리소스 그룹에 미국 서부의 Virtual WAN 리소스 그룹인 Virtual WAN이 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="a09e4-113">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 Virtual WAN에 연결합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="a09e4-114">사이트가 만들어지면 Remove-AzVpnSite 명령을 사용하여 Remove-AzVpnSite.</span><span class="sxs-lookup"><span data-stu-id="a09e4-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="a09e4-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="a09e4-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="a09e4-116">예제 1과 동일하지만 여기에서 제거는 Get-AzVpnSite의 파이프된 출력을 사용하여 발생합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="a09e4-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a09e4-117">PARAMETERS</span></span>

### <span data-ttu-id="a09e4-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a09e4-118">-DefaultProfile</span></span>
<span data-ttu-id="a09e4-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a09e4-120">-Force</span><span class="sxs-lookup"><span data-stu-id="a09e4-120">-Force</span></span>
<span data-ttu-id="a09e4-121">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-121">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a09e4-122">-InputObject</span></span>
<span data-ttu-id="a09e4-123">삭제할 vpnSite 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-123">The vpnSite object to be deleted.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSVpnSite
Parameter Sets: ByVpnSiteObject
Aliases: VpnSite

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-124">-Name</span><span class="sxs-lookup"><span data-stu-id="a09e4-124">-Name</span></span>
<span data-ttu-id="a09e4-125">vpnSite 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-125">The vpnSite name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases: ResourceName, VpnSiteName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a09e4-126">-PassThru</span></span>
<span data-ttu-id="a09e4-127">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="a09e4-128">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-128">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a09e4-129">-ResourceGroupName</span></span>
<span data-ttu-id="a09e4-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-130">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a09e4-131">-ResourceId</span></span>
<span data-ttu-id="a09e4-132">삭제할 vpnSite에 대한 Azure 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: ByVpnSiteResourceId
Aliases: VpnSiteId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a09e4-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="a09e4-133">-Confirm</span></span>
<span data-ttu-id="a09e4-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a09e4-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a09e4-135">-WhatIf</span></span>
<span data-ttu-id="a09e4-136">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="a09e4-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a09e4-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a09e4-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a09e4-138">CommonParameters</span></span>
<span data-ttu-id="a09e4-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a09e4-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a09e4-140">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a09e4-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a09e4-141">입력</span><span class="sxs-lookup"><span data-stu-id="a09e4-141">INPUTS</span></span>

### <span data-ttu-id="a09e4-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span><span class="sxs-lookup"><span data-stu-id="a09e4-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="a09e4-143">System.String</span><span class="sxs-lookup"><span data-stu-id="a09e4-143">System.String</span></span>

## <span data-ttu-id="a09e4-144">출력</span><span class="sxs-lookup"><span data-stu-id="a09e4-144">OUTPUTS</span></span>

### <span data-ttu-id="a09e4-145">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a09e4-145">System.Boolean</span></span>

## <span data-ttu-id="a09e4-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a09e4-146">NOTES</span></span>

## <span data-ttu-id="a09e4-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a09e4-147">RELATED LINKS</span></span>

[<span data-ttu-id="a09e4-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a09e4-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="a09e4-149">New-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a09e4-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="a09e4-150">Update-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="a09e4-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
