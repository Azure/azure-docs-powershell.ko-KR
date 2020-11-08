---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azvpnsite
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzVpnSite.md
ms.openlocfilehash: 9b9ab59496ff52be2dc8ca538ea044ec34c34970
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214073"
---
# <span data-ttu-id="b94d8-101">Remove-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b94d8-101">Remove-AzVpnSite</span></span>

## <span data-ttu-id="b94d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b94d8-102">SYNOPSIS</span></span>
<span data-ttu-id="b94d8-103">Azure VpnSite 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-103">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="b94d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b94d8-104">SYNTAX</span></span>

### <span data-ttu-id="b94d8-105">ByVpnSiteName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b94d8-105">ByVpnSiteName (Default)</span></span>
```
Remove-AzVpnSite -ResourceGroupName <String> -Name <String> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b94d8-106">ByVpnSiteObject</span><span class="sxs-lookup"><span data-stu-id="b94d8-106">ByVpnSiteObject</span></span>
```
Remove-AzVpnSite -InputObject <PSVpnSite> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="b94d8-107">ByVpnSiteResourceId</span><span class="sxs-lookup"><span data-stu-id="b94d8-107">ByVpnSiteResourceId</span></span>
```
Remove-AzVpnSite -ResourceId <String> [-Force] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b94d8-108">설명은</span><span class="sxs-lookup"><span data-stu-id="b94d8-108">DESCRIPTION</span></span>
<span data-ttu-id="b94d8-109">Azure VpnSite 리소스를 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-109">Removes an Azure VpnSite resource.</span></span>

## <span data-ttu-id="b94d8-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b94d8-110">EXAMPLES</span></span>

### <span data-ttu-id="b94d8-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="b94d8-111">Example 1</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Remove-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite"
```

<span data-ttu-id="b94d8-112">위의 방법으로 Azure의 "testRG" 리소스 그룹에 있는 서쪽의 가상 WAN 인 리소스 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-112">The above will create a resource group, Virtual WAN in West US in "testRG" resource group in Azure.</span></span> 

<span data-ttu-id="b94d8-113">그런 다음 고객 분기를 나타내는 VpnSite를 만들고 가상 WAN에 연결 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-113">Then it creates a VpnSite to represent a customer branch and links it to the Virtual WAN.</span></span>

<span data-ttu-id="b94d8-114">사이트를 만든 후에는 Remove-AzVpnSite 명령을 사용 하 여 즉시 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-114">Once the site is created, it is immediately removed using the Remove-AzVpnSite command.</span></span>

### <span data-ttu-id="b94d8-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="b94d8-115">Example 2</span></span>

```powershell
PS C:\> New-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan = New-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $vpnSiteAddressSpaces = New-Object string[] 2
PS C:\> $vpnSiteAddressSpaces[0] = "192.168.2.0/24"
PS C:\> $vpnSiteAddressSpaces[1] = "192.168.3.0/24"
PS C:\> New-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" -Location "West US" -VirtualWan $virtualWan -IpAddress "1.2.3.4" -AddressSpace $vpnSiteAddressSpaces -DeviceModel "SomeDevice" -DeviceVendor "SomeDeviceVendor" -LinkSpeedInMbps "10"
PS C:\> Get-AzVpnSite -ResourceGroupName "testRG" -Name "testVpnSite" | Remove-AzVpnSite
```

<span data-ttu-id="b94d8-116">예제 1과 동일 하지만 여기에서 AzVpnSite의 파이핑 된 출력을 사용 하 여 제거가 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-116">Same as example 1 but here the removal happens using the piped output from Get-AzVpnSite.</span></span>

## <span data-ttu-id="b94d8-117">변수</span><span class="sxs-lookup"><span data-stu-id="b94d8-117">PARAMETERS</span></span>

### <span data-ttu-id="b94d8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b94d8-118">-DefaultProfile</span></span>
<span data-ttu-id="b94d8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b94d8-120">-Force</span><span class="sxs-lookup"><span data-stu-id="b94d8-120">-Force</span></span>
<span data-ttu-id="b94d8-121">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-121">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="b94d8-122">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b94d8-122">-InputObject</span></span>
<span data-ttu-id="b94d8-123">삭제할 vpnSite 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-123">The vpnSite object to be deleted.</span></span>

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

### <span data-ttu-id="b94d8-124">-이름</span><span class="sxs-lookup"><span data-stu-id="b94d8-124">-Name</span></span>
<span data-ttu-id="b94d8-125">VpnSite 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-125">The vpnSite name.</span></span>

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

### <span data-ttu-id="b94d8-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b94d8-126">-PassThru</span></span>
<span data-ttu-id="b94d8-127">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-127">Returns an object representing the item with which you are working.</span></span> <span data-ttu-id="b94d8-128">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-128">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="b94d8-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b94d8-129">-ResourceGroupName</span></span>
<span data-ttu-id="b94d8-130">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-130">The resource group name.</span></span>

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

### <span data-ttu-id="b94d8-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="b94d8-131">-ResourceId</span></span>
<span data-ttu-id="b94d8-132">삭제할 vpnSite의 Azure resource ID입니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-132">The Azure resource ID for the vpnSite to be deleted.</span></span>

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

### <span data-ttu-id="b94d8-133">-확인</span><span class="sxs-lookup"><span data-stu-id="b94d8-133">-Confirm</span></span>
<span data-ttu-id="b94d8-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b94d8-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b94d8-135">-WhatIf</span></span>
<span data-ttu-id="b94d8-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b94d8-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b94d8-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b94d8-138">CommonParameters</span></span>
<span data-ttu-id="b94d8-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b94d8-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b94d8-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b94d8-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b94d8-141">입력</span><span class="sxs-lookup"><span data-stu-id="b94d8-141">INPUTS</span></span>

### <span data-ttu-id="b94d8-142">PSVpnSite에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b94d8-142">Microsoft.Azure.Commands.Network.Models.PSVpnSite</span></span>

### <span data-ttu-id="b94d8-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b94d8-143">System.String</span></span>

## <span data-ttu-id="b94d8-144">출력</span><span class="sxs-lookup"><span data-stu-id="b94d8-144">OUTPUTS</span></span>

### <span data-ttu-id="b94d8-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="b94d8-145">System.Boolean</span></span>

## <span data-ttu-id="b94d8-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b94d8-146">NOTES</span></span>

## <span data-ttu-id="b94d8-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b94d8-147">RELATED LINKS</span></span>

[<span data-ttu-id="b94d8-148">Get-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b94d8-148">Get-AzVpnSite</span></span>](./Get-AzVpnSite.md)

[<span data-ttu-id="b94d8-149">새로운 AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b94d8-149">New-AzVpnSite</span></span>](./New-AzVpnSite.md)

[<span data-ttu-id="b94d8-150">업데이트-AzVpnSite</span><span class="sxs-lookup"><span data-stu-id="b94d8-150">Update-AzVpnSite</span></span>](./Update-AzVpnSite.md)
