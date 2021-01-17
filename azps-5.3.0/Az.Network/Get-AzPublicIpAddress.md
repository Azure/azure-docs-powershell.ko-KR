---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 7a369fafec712d23c7ac2aac30d3aa6928877355
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98492180"
---
# <span data-ttu-id="7ecce-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ecce-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="7ecce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7ecce-102">SYNOPSIS</span></span>
<span data-ttu-id="7ecce-103">공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-103">Gets a public IP address.</span></span>

## <span data-ttu-id="7ecce-104">구문</span><span class="sxs-lookup"><span data-stu-id="7ecce-104">SYNTAX</span></span>

### <span data-ttu-id="7ecce-105">NoExpandStandAloneIp(기본값)</span><span class="sxs-lookup"><span data-stu-id="7ecce-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7ecce-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="7ecce-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ecce-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="7ecce-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7ecce-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="7ecce-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7ecce-109">설명</span><span class="sxs-lookup"><span data-stu-id="7ecce-109">DESCRIPTION</span></span>
<span data-ttu-id="7ecce-110">**Get-AzPublicIPAddress** cmdlet은 리소스 그룹에서 하나 이상의 공용 IP 주소를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="7ecce-111">예제</span><span class="sxs-lookup"><span data-stu-id="7ecce-111">EXAMPLES</span></span>

### <span data-ttu-id="7ecce-112">예제 1: 공용 IP 리소스 얻기</span><span class="sxs-lookup"><span data-stu-id="7ecce-112">Example 1: Get a public IP resource</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp1 -ResourceGroupName myRg

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic", 
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="7ecce-113">이 명령은 리소스 그룹 myRg에서 myPublicIp 이름이 있는 공용 IP 주소 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="7ecce-114">예제 2: 필터링을 사용하여 공용 IP 리소스 확보</span><span class="sxs-lookup"><span data-stu-id="7ecce-114">Example 2: Get public IP resources using filtering</span></span>
```powershell
Get-AzPublicIpAddress -Name myPublicIp*

Name                     : myPublicIp1
ResourceGroupName        : myRg
Location                 : westus2
Id                       : /subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/Microsoft
                           .Network/publicIPAddresses/myPublicIp1
Etag                     : W/"00000000-0000-0000-0000-000000000000"
ResourceGuid             : 00000000-0000-0000-0000-000000000000
ProvisioningState        : Succeeded
Tags                     :
PublicIpAllocationMethod : Dynamic
IpAddress                : Not Assigned
PublicIpAddressVersion   : IPv4
IdleTimeoutInMinutes     : 4
IpConfiguration          : {
                             "Id": "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myRg/providers/
                           Microsoft.Network/networkInterfaces/ps-azure-env407/ipConfigurations/ipconfig1"
                           }
DnsSettings              : null
Zones                    : {}
Sku                      : {
                             "Name": "Basic",
                             "Tier": "Regional"
                           }
IpTags                   : []
```

<span data-ttu-id="7ecce-115">이 명령은 이름이 myPublicIp로 시작하는 모든 공용 IP 주소 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="7ecce-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7ecce-116">PARAMETERS</span></span>

### <span data-ttu-id="7ecce-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7ecce-117">-DefaultProfile</span></span>
<span data-ttu-id="7ecce-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7ecce-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="7ecce-119">-ExpandResource</span></span>
```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecce-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="7ecce-120">-IpConfigurationName</span></span>
<span data-ttu-id="7ecce-121">네트워크 인터페이스 IP 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-121">Network Interface IP Configuration Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecce-122">-Name</span><span class="sxs-lookup"><span data-stu-id="7ecce-122">-Name</span></span>
<span data-ttu-id="7ecce-123">이 cmdlet에서 얻을 공용 IP 주소의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp, NoExpandScaleSetIp
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, ExpandScaleSetIp
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7ecce-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="7ecce-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="7ecce-125">Virtual Machine 네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-125">Virtual Machine Network Interface Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecce-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7ecce-126">-ResourceGroupName</span></span>
<span data-ttu-id="7ecce-127">이 cmdlet에서 얻을 공용 IP 주소를 포함하는 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandStandAloneIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

```yaml
Type: System.String
Parameter Sets: ExpandStandAloneIp, NoExpandScaleSetIp, ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="7ecce-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="7ecce-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="7ecce-129">Virtual Machine 인덱스.</span><span class="sxs-lookup"><span data-stu-id="7ecce-129">Virtual Machine Index.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecce-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="7ecce-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="7ecce-131">가상 머신 확장 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-131">Virtual Machine Scale Set Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NoExpandScaleSetIp
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: ExpandScaleSetIp
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7ecce-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7ecce-132">CommonParameters</span></span>
<span data-ttu-id="7ecce-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7ecce-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7ecce-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7ecce-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7ecce-135">입력</span><span class="sxs-lookup"><span data-stu-id="7ecce-135">INPUTS</span></span>

### <span data-ttu-id="7ecce-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7ecce-136">System.String</span></span>

## <span data-ttu-id="7ecce-137">출력</span><span class="sxs-lookup"><span data-stu-id="7ecce-137">OUTPUTS</span></span>

### <span data-ttu-id="7ecce-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ecce-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="7ecce-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7ecce-139">NOTES</span></span>

## <span data-ttu-id="7ecce-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7ecce-140">RELATED LINKS</span></span>

[<span data-ttu-id="7ecce-141">New-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ecce-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="7ecce-142">Remove-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ecce-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="7ecce-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="7ecce-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


