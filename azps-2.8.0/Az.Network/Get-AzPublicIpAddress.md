---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 0CD03BF8-8DB6-44BC-91F0-D863949DBD17
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azpublicipaddress
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzPublicIpAddress.md
ms.openlocfilehash: 38eff375baa948098ac66c8e2b3c3fe1849f3bc0
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870105"
---
# <span data-ttu-id="9b141-101">Get-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b141-101">Get-AzPublicIpAddress</span></span>

## <span data-ttu-id="9b141-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b141-102">SYNOPSIS</span></span>
<span data-ttu-id="9b141-103">공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-103">Gets a public IP address.</span></span>

## <span data-ttu-id="9b141-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b141-104">SYNTAX</span></span>

### <span data-ttu-id="9b141-105">NoExpandStandAloneIp (기본값)</span><span class="sxs-lookup"><span data-stu-id="9b141-105">NoExpandStandAloneIp (Default)</span></span>
```
Get-AzPublicIpAddress [-Name <String>] [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="9b141-106">ExpandStandAloneIp</span><span class="sxs-lookup"><span data-stu-id="9b141-106">ExpandStandAloneIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -ExpandResource <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b141-107">NoExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="9b141-107">NoExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress [-Name <String>] -ResourceGroupName <String> [-VirtualMachineScaleSetName <String>]
 [-VirtualMachineIndex <String>] [-NetworkInterfaceName <String>] [-IpConfigurationName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="9b141-108">ExpandScaleSetIp</span><span class="sxs-lookup"><span data-stu-id="9b141-108">ExpandScaleSetIp</span></span>
```
Get-AzPublicIpAddress -Name <String> -ResourceGroupName <String> -VirtualMachineScaleSetName <String>
 -VirtualMachineIndex <String> -NetworkInterfaceName <String> -IpConfigurationName <String>
 -ExpandResource <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9b141-109">설명은</span><span class="sxs-lookup"><span data-stu-id="9b141-109">DESCRIPTION</span></span>
<span data-ttu-id="9b141-110">**AzPublicIPAddress** cmdlet은 리소스 그룹에 하나 이상의 공용 IP 주소를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-110">The **Get-AzPublicIPAddress** cmdlet gets one or more public IP addresses in a resource group.</span></span>

## <span data-ttu-id="9b141-111">예제의</span><span class="sxs-lookup"><span data-stu-id="9b141-111">EXAMPLES</span></span>

### <span data-ttu-id="9b141-112">1: 공용 IP 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b141-112">1: Get a public IP resource</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="9b141-113">이 명령은 리소스 그룹 myRg에서 이름이 myPublicIp 인 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-113">This command gets a public IP address resource with name myPublicIp in the resource group myRg.</span></span>

### <span data-ttu-id="9b141-114">2: 필터링을 사용 하 여 공용 IP 리소스 가져오기</span><span class="sxs-lookup"><span data-stu-id="9b141-114">2: Get public IP resources using filtering</span></span>
```
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
                             "Name": "Basic"
                           }
IpTags                   : []
```

<span data-ttu-id="9b141-115">이 명령은 이름이 myPublicIp로 시작 하는 모든 공용 IP 주소 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-115">This command gets all public IP address resources whose name starts with myPublicIp.</span></span>

## <span data-ttu-id="9b141-116">변수</span><span class="sxs-lookup"><span data-stu-id="9b141-116">PARAMETERS</span></span>

### <span data-ttu-id="9b141-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b141-117">-DefaultProfile</span></span>
<span data-ttu-id="9b141-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b141-119">-ExpandResource</span><span class="sxs-lookup"><span data-stu-id="9b141-119">-ExpandResource</span></span>
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

### <span data-ttu-id="9b141-120">-IpConfigurationName</span><span class="sxs-lookup"><span data-stu-id="9b141-120">-IpConfigurationName</span></span>
<span data-ttu-id="9b141-121">네트워크 인터페이스 IP 구성 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-121">Network Interface IP Configuration Name.</span></span>

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

### <span data-ttu-id="9b141-122">-이름</span><span class="sxs-lookup"><span data-stu-id="9b141-122">-Name</span></span>
<span data-ttu-id="9b141-123">이 cmdlet이 가져오는 공용 IP 주소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-123">Specifies the name of the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9b141-124">-NetworkInterfaceName</span><span class="sxs-lookup"><span data-stu-id="9b141-124">-NetworkInterfaceName</span></span>
<span data-ttu-id="9b141-125">가상 컴퓨터 네트워크 인터페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-125">Virtual Machine Network Interface Name.</span></span>

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

### <span data-ttu-id="9b141-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9b141-126">-ResourceGroupName</span></span>
<span data-ttu-id="9b141-127">이 cmdlet이 가져오는 공용 IP 주소를 포함 하는 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-127">Specifies the name of the resource group that contains the public IP address that this cmdlet gets.</span></span>

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

### <span data-ttu-id="9b141-128">-VirtualMachineIndex</span><span class="sxs-lookup"><span data-stu-id="9b141-128">-VirtualMachineIndex</span></span>
<span data-ttu-id="9b141-129">가상 머신 인덱스.</span><span class="sxs-lookup"><span data-stu-id="9b141-129">Virtual Machine Index.</span></span>

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

### <span data-ttu-id="9b141-130">-VirtualMachineScaleSetName</span><span class="sxs-lookup"><span data-stu-id="9b141-130">-VirtualMachineScaleSetName</span></span>
<span data-ttu-id="9b141-131">가상 컴퓨터 크기 조정 집합 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-131">Virtual Machine Scale Set Name.</span></span>

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

### <span data-ttu-id="9b141-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b141-132">CommonParameters</span></span>
<span data-ttu-id="9b141-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b141-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b141-134">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9b141-134">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b141-135">입력</span><span class="sxs-lookup"><span data-stu-id="9b141-135">INPUTS</span></span>

### <span data-ttu-id="9b141-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9b141-136">System.String</span></span>

## <span data-ttu-id="9b141-137">출력</span><span class="sxs-lookup"><span data-stu-id="9b141-137">OUTPUTS</span></span>

### <span data-ttu-id="9b141-138">PSPublicIpAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9b141-138">Microsoft.Azure.Commands.Network.Models.PSPublicIpAddress</span></span>

## <span data-ttu-id="9b141-139">상속자</span><span class="sxs-lookup"><span data-stu-id="9b141-139">NOTES</span></span>

## <span data-ttu-id="9b141-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b141-140">RELATED LINKS</span></span>

[<span data-ttu-id="9b141-141">새로운 AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b141-141">New-AzPublicIpAddress</span></span>](./New-AzPublicIpAddress.md)

[<span data-ttu-id="9b141-142">제거-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b141-142">Remove-AzPublicIpAddress</span></span>](./Remove-AzPublicIpAddress.md)

[<span data-ttu-id="9b141-143">Set-AzPublicIpAddress</span><span class="sxs-lookup"><span data-stu-id="9b141-143">Set-AzPublicIpAddress</span></span>](./Set-AzPublicIpAddress.md)


