---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmssnetworkinterfaceconfiguration
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Add-AzVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 43d7040543beb049f46fce45cab69d9128a8954e
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877117"
---
# <span data-ttu-id="d40f0-101">Add-AzVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="d40f0-101">Add-AzVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="d40f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d40f0-102">SYNOPSIS</span></span>
<span data-ttu-id="d40f0-103">네트워크 인터페이스 구성을 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-103">Adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="d40f0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d40f0-104">SYNTAX</span></span>

```
Add-AzVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-EnableIPForwarding] [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d40f0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d40f0-105">DESCRIPTION</span></span>
<span data-ttu-id="d40f0-106">**AzVmssNetworkInterfaceConfiguration** cmdlet은 네트워크 인터페이스 구성을 Vmss (가상 컴퓨터 크기 조정 집합)에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-106">The **Add-AzVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="d40f0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d40f0-107">EXAMPLES</span></span>

### <span data-ttu-id="d40f0-108">예제 1: VMSS에 네트워크 인터페이스 구성 추가</span><span class="sxs-lookup"><span data-stu-id="d40f0-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="d40f0-109">이 명령은 VMSS에 네트워크 인터페이스 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="d40f0-110">변수</span><span class="sxs-lookup"><span data-stu-id="d40f0-110">PARAMETERS</span></span>

### <span data-ttu-id="d40f0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d40f0-111">-DefaultProfile</span></span>
<span data-ttu-id="d40f0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="d40f0-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="d40f0-114">Dns 설정에 대 한 dns 서버 IP 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-114">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: DnsServer

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="d40f0-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="d40f0-116">네트워크 인터페이스가 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-117">-EnableIPForwarding</span><span class="sxs-lookup"><span data-stu-id="d40f0-117">-EnableIPForwarding</span></span>
<span data-ttu-id="d40f0-118">이 NIC에서 IP 전달을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-118">Specifies whether IP forwarding enabled on this NIC.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-119">-Id</span><span class="sxs-lookup"><span data-stu-id="d40f0-119">-Id</span></span>
<span data-ttu-id="d40f0-120">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-120">Specifies the Resource ID of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-121">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="d40f0-121">-IpConfiguration</span></span>
<span data-ttu-id="d40f0-122">네트워크 인터페이스의 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-122">Specifies the IP configurations of the network interface.</span></span>

```yaml
Type: VirtualMachineScaleSetIPConfiguration[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-123">-이름</span><span class="sxs-lookup"><span data-stu-id="d40f0-123">-Name</span></span>
<span data-ttu-id="d40f0-124">네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-124">Specifies the name of the network interface configuration.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-125">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="d40f0-125">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="d40f0-126">네트워크 보안 그룹의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-126">Id of the network security group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-127">-기본</span><span class="sxs-lookup"><span data-stu-id="d40f0-127">-Primary</span></span>
<span data-ttu-id="d40f0-128">네트워크 인터페이스 구성에서 만든 네트워크 인터페이스가 가상 컴퓨터의 기본 NIC (network information center)가 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-128">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-129">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d40f0-129">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="d40f0-130">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-130">Specifies the VMSS object.</span></span>
<span data-ttu-id="d40f0-131">[새 AzVmssConfig](./New-AzVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-131">You can use the [New-AzVmssConfig](./New-AzVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: PSVirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-132">-확인</span><span class="sxs-lookup"><span data-stu-id="d40f0-132">-Confirm</span></span>
<span data-ttu-id="d40f0-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d40f0-134">-WhatIf</span></span>
<span data-ttu-id="d40f0-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d40f0-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-136">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d40f0-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d40f0-137">CommonParameters</span></span>
<span data-ttu-id="d40f0-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d40f0-139">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d40f0-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d40f0-140">입력</span><span class="sxs-lookup"><span data-stu-id="d40f0-140">INPUTS</span></span>

### <span data-ttu-id="d40f0-141">VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="d40f0-141">VirtualMachineScaleSet</span></span>
<span data-ttu-id="d40f0-142">' VirtualMachineScaleSet ' 매개 변수는 파이프라인에서 ' VirtualMachineScaleSet ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-142">Parameter 'VirtualMachineScaleSet' accepts value of type 'VirtualMachineScaleSet' from the pipeline</span></span>

## <span data-ttu-id="d40f0-143">출력</span><span class="sxs-lookup"><span data-stu-id="d40f0-143">OUTPUTS</span></span>

###  
<span data-ttu-id="d40f0-144">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d40f0-144">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="d40f0-145">상속자</span><span class="sxs-lookup"><span data-stu-id="d40f0-145">NOTES</span></span>

## <span data-ttu-id="d40f0-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d40f0-146">RELATED LINKS</span></span>

[<span data-ttu-id="d40f0-147">새로운 AzVmssConfig</span><span class="sxs-lookup"><span data-stu-id="d40f0-147">New-AzVmssConfig</span></span>](./New-AzVmssConfig.md)
