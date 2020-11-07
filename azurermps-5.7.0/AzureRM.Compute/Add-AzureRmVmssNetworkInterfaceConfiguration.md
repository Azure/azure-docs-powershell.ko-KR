---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 0b21b5fa3b5b605ee3092a61eaf67a2c63c4346b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702037"
---
# <span data-ttu-id="7203a-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="7203a-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="7203a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7203a-102">SYNOPSIS</span></span>
<span data-ttu-id="7203a-103">네트워크 인터페이스 구성을 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7203a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7203a-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <VirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-NetworkSecurityGroupId <String>]
 [-DnsSettingsDnsServer <String[]>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7203a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7203a-105">DESCRIPTION</span></span>
<span data-ttu-id="7203a-106">**AzureRmVmssNetworkInterfaceConfiguration** cmdlet은 네트워크 인터페이스 구성을 Vmss (가상 컴퓨터 크기 조정 집합)에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="7203a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7203a-107">EXAMPLES</span></span>

### <span data-ttu-id="7203a-108">예제 1: VMSS에 네트워크 인터페이스 구성 추가</span><span class="sxs-lookup"><span data-stu-id="7203a-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="7203a-109">이 명령은 VMSS에 네트워크 인터페이스 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="7203a-110">변수</span><span class="sxs-lookup"><span data-stu-id="7203a-110">PARAMETERS</span></span>

### <span data-ttu-id="7203a-111">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="7203a-111">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="7203a-112">Dns 설정에 대 한 dns 서버 IP 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-112">List of dns server IP addresses for dns settings.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7203a-113">-Id</span><span class="sxs-lookup"><span data-stu-id="7203a-113">-Id</span></span>
<span data-ttu-id="7203a-114">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-114">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="7203a-115">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="7203a-115">-IpConfiguration</span></span>
<span data-ttu-id="7203a-116">네트워크 인터페이스의 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-116">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="7203a-117">-이름</span><span class="sxs-lookup"><span data-stu-id="7203a-117">-Name</span></span>
<span data-ttu-id="7203a-118">네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-118">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="7203a-119">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="7203a-119">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="7203a-120">네트워크 보안 그룹의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-120">Id of the network security group.</span></span>

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

### <span data-ttu-id="7203a-121">-기본</span><span class="sxs-lookup"><span data-stu-id="7203a-121">-Primary</span></span>
<span data-ttu-id="7203a-122">네트워크 인터페이스 구성에서 만든 네트워크 인터페이스가 가상 컴퓨터의 기본 NIC (network information center)가 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-122">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="7203a-123">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="7203a-123">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="7203a-124">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-124">Specifies the VMSS object.</span></span>
<span data-ttu-id="7203a-125">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-125">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

```yaml
Type: VirtualMachineScaleSet
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7203a-126">-확인</span><span class="sxs-lookup"><span data-stu-id="7203a-126">-Confirm</span></span>
<span data-ttu-id="7203a-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7203a-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7203a-128">-WhatIf</span></span>
<span data-ttu-id="7203a-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="7203a-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7203a-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7203a-131">CommonParameters</span></span>
<span data-ttu-id="7203a-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7203a-133">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7203a-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7203a-134">입력</span><span class="sxs-lookup"><span data-stu-id="7203a-134">INPUTS</span></span>

### <span data-ttu-id="7203a-135">않아야</span><span class="sxs-lookup"><span data-stu-id="7203a-135">None</span></span>
<span data-ttu-id="7203a-136">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7203a-137">출력</span><span class="sxs-lookup"><span data-stu-id="7203a-137">OUTPUTS</span></span>

###  
<span data-ttu-id="7203a-138">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7203a-138">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="7203a-139">상속자</span><span class="sxs-lookup"><span data-stu-id="7203a-139">NOTES</span></span>

## <span data-ttu-id="7203a-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7203a-140">RELATED LINKS</span></span>

[<span data-ttu-id="7203a-141">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="7203a-141">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
