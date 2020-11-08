---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 9e52131bd5f53d48b4c958c26a0ef37b5ebd23ec
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217632"
---
# <span data-ttu-id="11f64-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="11f64-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="11f64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11f64-102">SYNOPSIS</span></span>
<span data-ttu-id="11f64-103">네트워크 인터페이스 구성을 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="11f64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11f64-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet> [[-Name] <String>]
 [[-Primary] <Boolean>] [[-Id] <String>] [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>]
 [-EnableAcceleratedNetworking] [-EnableIPForwarding] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="11f64-105">설명은</span><span class="sxs-lookup"><span data-stu-id="11f64-105">DESCRIPTION</span></span>
<span data-ttu-id="11f64-106">**AzVmssNetworkInterfaceConfiguration** cmdlet은 네트워크 인터페이스 구성을 Vmss (가상 컴퓨터 크기 조정 집합)에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="11f64-107">예제의</span><span class="sxs-lookup"><span data-stu-id="11f64-107">EXAMPLES</span></span>

### <span data-ttu-id="11f64-108">예제 1: VMSS에 네트워크 인터페이스 구성 추가</span><span class="sxs-lookup"><span data-stu-id="11f64-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="11f64-109">이 명령은 VMSS에 네트워크 인터페이스 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="11f64-110">변수</span><span class="sxs-lookup"><span data-stu-id="11f64-110">PARAMETERS</span></span>

### <span data-ttu-id="11f64-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11f64-111">-DefaultProfile</span></span>
<span data-ttu-id="11f64-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="11f64-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="11f64-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="11f64-114">Dns 설정에 대 한 dns 서버 IP 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="11f64-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="11f64-116">네트워크 인터페이스가 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

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

### <span data-ttu-id="11f64-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="11f64-117">-EnableIPForwarding</span></span>
<span data-ttu-id="11f64-118">이 NIC에서 IP 전달을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

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

### <span data-ttu-id="11f64-119">-Id</span><span class="sxs-lookup"><span data-stu-id="11f64-119">-Id</span></span>
<span data-ttu-id="11f64-120">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="11f64-121">-IpConfiguration</span></span>
<span data-ttu-id="11f64-122">네트워크 인터페이스의 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-123">-이름</span><span class="sxs-lookup"><span data-stu-id="11f64-123">-Name</span></span>
<span data-ttu-id="11f64-124">네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="11f64-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="11f64-126">네트워크 보안 그룹의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-126">Id of the network security group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-127">-기본</span><span class="sxs-lookup"><span data-stu-id="11f64-127">-Primary</span></span>
<span data-ttu-id="11f64-128">네트워크 인터페이스 구성에서 만든 네트워크 인터페이스가 가상 컴퓨터의 기본 NIC (network information center)가 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="11f64-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="11f64-130">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="11f64-131">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="11f64-132">-확인</span><span class="sxs-lookup"><span data-stu-id="11f64-132">-Confirm</span></span>
<span data-ttu-id="11f64-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11f64-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11f64-134">-WhatIf</span></span>
<span data-ttu-id="11f64-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11f64-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11f64-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11f64-137">CommonParameters</span></span>
<span data-ttu-id="11f64-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11f64-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11f64-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11f64-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11f64-140">입력</span><span class="sxs-lookup"><span data-stu-id="11f64-140">INPUTS</span></span>

### <span data-ttu-id="11f64-141">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="11f64-141">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

### <span data-ttu-id="11f64-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11f64-142">System.String</span></span>

### <span data-ttu-id="11f64-143">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="11f64-143">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="11f64-144">Microsoft VirtualMachineScaleSetIPConfiguration []을 (를)</span><span class="sxs-lookup"><span data-stu-id="11f64-144">Microsoft.Azure.Management.Compute.Models.VirtualMachineScaleSetIPConfiguration[]</span></span>

### <span data-ttu-id="11f64-145">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="11f64-145">System.String[]</span></span>

## <span data-ttu-id="11f64-146">출력</span><span class="sxs-lookup"><span data-stu-id="11f64-146">OUTPUTS</span></span>

### <span data-ttu-id="11f64-147">PSVirtualMachineScaleSet의. m a.</span><span class="sxs-lookup"><span data-stu-id="11f64-147">Microsoft.Azure.Commands.Compute.Automation.Models.PSVirtualMachineScaleSet</span></span>

## <span data-ttu-id="11f64-148">상속자</span><span class="sxs-lookup"><span data-stu-id="11f64-148">NOTES</span></span>

## <span data-ttu-id="11f64-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11f64-149">RELATED LINKS</span></span>

[<span data-ttu-id="11f64-150">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="11f64-150">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
