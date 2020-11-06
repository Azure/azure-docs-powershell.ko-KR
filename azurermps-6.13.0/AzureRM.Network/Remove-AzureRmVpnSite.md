---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azurermvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmVpnSite.md
ms.openlocfilehash: ac0513b7d411c2c95864aa6f619e80d2373a3554
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530173"
---
# <span data-ttu-id="f4afc-101">Remove-AzureRmVpnSite</span><span class="sxs-lookup"><span data-stu-id="f4afc-101">Remove-AzureRmVpnSite</span></span>

## <span data-ttu-id="f4afc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f4afc-102">SYNOPSIS</span></span>
<span data-ttu-id="f4afc-103">Azure VpnSite 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-103">Removes an Azure VpnSite resource.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f4afc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f4afc-104">SYNTAX</span></span>

### <span data-ttu-id="f4afc-105">ByVpnSiteName (기본값)</span><span class="sxs-lookup"><span data-stu-id="f4afc-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzureRmVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4afc-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="f4afc-106">ByVpnSiteObject</span></span>
```
Remove-AzureRmVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f4afc-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="f4afc-107">ByVpnSiteResourceId</span></span>
```
Remove-AzureRmVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f4afc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f4afc-108">DESCRIPTION</span></span>
<span data-ttu-id="f4afc-109">Azure VpnSite 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="f4afc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="f4afc-110">EXAMPLES</span></span>

### <span data-ttu-id="f4afc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="f4afc-111">Example 1</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="f4afc-112">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="f4afc-113">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="f4afc-114">사이트를 만든 후에는 Remove-AzureRmVpnSite 명령을 사용 하 여 즉시 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-114">Once the site is created, it is immediately removed using the Remove-AzureRmVpnSite command.</span></span>

### <span data-ttu-id="f4afc-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="f4afc-115">Example 2</span></span>

```powershell
PS C:\> New-AzureRmResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzureRmVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzureRmVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzureRmVpnSite
```

<span data-ttu-id="f4afc-116">예제 1과 동일 하지만 여기에서 AzureRmVpnSite의 파이핑 된 출력을 사용 하 여 제거가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-116">Same as example 1 but here the removal happens using the piped output from Get-AzureRmVpnSite.</span></span>

## <span data-ttu-id="f4afc-117">변수</span><span class="sxs-lookup"><span data-stu-id="f4afc-117">PARAMETERS</span></span>

### <span data-ttu-id="f4afc-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f4afc-118">-DefaultProfile</span></span>
<span data-ttu-id="f4afc-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f4afc-120">-Force</span><span class="sxs-lookup"><span data-stu-id="f4afc-120">-Force</span></span>
<span data-ttu-id="f4afc-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="f4afc-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f4afc-122">-InputObject</span></span>
<span data-ttu-id="f4afc-123">삭제할 vpnSite 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="f4afc-124">-이름</span><span class="sxs-lookup"><span data-stu-id="f4afc-124">-Name</span></span>
<span data-ttu-id="f4afc-125">VpnSite 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="f4afc-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f4afc-126">-PassThru</span></span>
<span data-ttu-id="f4afc-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="f4afc-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="f4afc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f4afc-129">-ResourceGroupName</span></span>
<span data-ttu-id="f4afc-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-130">The resource group name.</span></span>

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

### <span data-ttu-id="f4afc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="f4afc-131">-ResourceId</span></span>
<span data-ttu-id="f4afc-132">삭제할 vpnSite의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="f4afc-133">-확인</span><span class="sxs-lookup"><span data-stu-id="f4afc-133">-Confirm</span></span>
<span data-ttu-id="f4afc-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f4afc-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f4afc-135">-WhatIf</span></span>
<span data-ttu-id="f4afc-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f4afc-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f4afc-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f4afc-138">CommonParameters</span></span>
<span data-ttu-id="f4afc-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f4afc-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f4afc-140">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f4afc-140">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f4afc-141">입력</span><span class="sxs-lookup"><span data-stu-id="f4afc-141">INPUTS</span></span>

### <span data-ttu-id="f4afc-142">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f4afc-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="f4afc-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f4afc-143">System.String</span></span>

## <span data-ttu-id="f4afc-144">출력</span><span class="sxs-lookup"><span data-stu-id="f4afc-144">OUTPUTS</span></span>

### <span data-ttu-id="f4afc-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="f4afc-145">System.Boolean</span></span>

## <span data-ttu-id="f4afc-146">상속자</span><span class="sxs-lookup"><span data-stu-id="f4afc-146">NOTES</span></span>

## <span data-ttu-id="f4afc-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f4afc-147">RELATED LINKS</span></span>
