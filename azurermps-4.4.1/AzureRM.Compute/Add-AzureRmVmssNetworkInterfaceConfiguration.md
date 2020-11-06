---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: BAC2FA68-1D82-411D-A853-FD4EE525B533
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Add-AzureRmVmssNetworkInterfaceConfiguration.md
ms.openlocfilehash: 651e339de5782d288350535ba1b0527d7a3eb0de
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531838"
---
# <span data-ttu-id="144d6-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span><span class="sxs-lookup"><span data-stu-id="144d6-101">Add-AzureRmVmssNetworkInterfaceConfiguration</span></span>

## <span data-ttu-id="144d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="144d6-102">SYNOPSIS</span></span>
<span data-ttu-id="144d6-103">네트워크 인터페이스 구성을 VMSS에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-103">Adds a network interface configuration to the VMSS.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="144d6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="144d6-104">SYNTAX</span></span>

```
Add-AzureRmVmssNetworkInterfaceConfiguration [-VirtualMachineScaleSet] <PSVirtualMachineScaleSet>
 [[-Name] <String>] [[-Primary] <Boolean>] [[-Id] <String>]
 [[-IpConfiguration] <VirtualMachineScaleSetIPConfiguration[]>] [-EnableAcceleratedNetworking]
 [-NetworkSecurityGroupId <String>] [-DnsSettingsDnsServer <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="144d6-105">설명은</span><span class="sxs-lookup"><span data-stu-id="144d6-105">DESCRIPTION</span></span>
<span data-ttu-id="144d6-106">**AzureRmVmssNetworkInterfaceConfiguration** cmdlet은 네트워크 인터페이스 구성을 Vmss (가상 컴퓨터 크기 조정 집합)에 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-106">The **Add-AzureRmVmssNetworkInterfaceConfiguration** cmdlet adds a network interface configuration to the Virtual Machine Scale Set (VMSS).</span></span>

## <span data-ttu-id="144d6-107">예제의</span><span class="sxs-lookup"><span data-stu-id="144d6-107">EXAMPLES</span></span>

### <span data-ttu-id="144d6-108">예제 1: VMSS에 네트워크 인터페이스 구성 추가</span><span class="sxs-lookup"><span data-stu-id="144d6-108">Example 1: Add a network interface configuration to the VMSS</span></span>
```
PS C:\> Add-AzureRmVmssNetworkInterfaceConfiguration -VirtualMachineScaleSet $VMSS -Name "Test" -Primary $True -IPConfiguration $IPCfg
```

<span data-ttu-id="144d6-109">이 명령은 VMSS에 네트워크 인터페이스 구성을 추가 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-109">This command adds a network interface configuration to the VMSS.</span></span>

## <span data-ttu-id="144d6-110">변수</span><span class="sxs-lookup"><span data-stu-id="144d6-110">PARAMETERS</span></span>

### <span data-ttu-id="144d6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="144d6-111">-DefaultProfile</span></span>
<span data-ttu-id="144d6-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="144d6-113">-DnsSettingsDnsServer</span><span class="sxs-lookup"><span data-stu-id="144d6-113">-DnsSettingsDnsServer</span></span>
<span data-ttu-id="144d6-114">Dns 설정에 대 한 dns 서버 IP 주소 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-114">List of dns server IP addresses for dns settings.</span></span>

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

### <span data-ttu-id="144d6-115">-EnableAcceleratedNetworking</span><span class="sxs-lookup"><span data-stu-id="144d6-115">-EnableAcceleratedNetworking</span></span>
<span data-ttu-id="144d6-116">네트워크 인터페이스가 가속 네트워킹을 사용할 수 있는지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-116">Specifies whether the network interface is accelerated networking-enabled.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: False
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="144d6-117">-Id</span><span class="sxs-lookup"><span data-stu-id="144d6-117">-Id</span></span>
<span data-ttu-id="144d6-118">가상 컴퓨터의 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-118">Specifies the Resource ID of the virtual machine.</span></span>

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

### <span data-ttu-id="144d6-119">-IpConfiguration</span><span class="sxs-lookup"><span data-stu-id="144d6-119">-IpConfiguration</span></span>
<span data-ttu-id="144d6-120">네트워크 인터페이스의 IP 구성을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-120">Specifies the IP configurations of the network interface.</span></span>

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

### <span data-ttu-id="144d6-121">-이름</span><span class="sxs-lookup"><span data-stu-id="144d6-121">-Name</span></span>
<span data-ttu-id="144d6-122">네트워크 인터페이스 구성의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-122">Specifies the name of the network interface configuration.</span></span>

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

### <span data-ttu-id="144d6-123">-NetworkSecurityGroupId</span><span class="sxs-lookup"><span data-stu-id="144d6-123">-NetworkSecurityGroupId</span></span>
<span data-ttu-id="144d6-124">네트워크 보안 그룹의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-124">Id of the network security group.</span></span>

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

### <span data-ttu-id="144d6-125">-기본</span><span class="sxs-lookup"><span data-stu-id="144d6-125">-Primary</span></span>
<span data-ttu-id="144d6-126">네트워크 인터페이스 구성에서 만든 네트워크 인터페이스가 가상 컴퓨터의 기본 NIC (network information center)가 되는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-126">Indicates whether network interfaces created from the network interface configuration will be the primary network information center (NIC) of the virtual machine.</span></span>

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

### <span data-ttu-id="144d6-127">-VirtualMachineScaleSet</span><span class="sxs-lookup"><span data-stu-id="144d6-127">-VirtualMachineScaleSet</span></span>
<span data-ttu-id="144d6-128">VMSS 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-128">Specifies the VMSS object.</span></span>
<span data-ttu-id="144d6-129">[새 AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet을 사용 하 여 개체를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-129">You can use the [New-AzureRmVmssConfig](./New-AzureRmVmssConfig.md) cmdlet to create the object.</span></span>

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

### <span data-ttu-id="144d6-130">-확인</span><span class="sxs-lookup"><span data-stu-id="144d6-130">-Confirm</span></span>
<span data-ttu-id="144d6-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="144d6-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="144d6-132">-WhatIf</span></span>
<span data-ttu-id="144d6-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="144d6-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="144d6-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="144d6-135">CommonParameters</span></span>
<span data-ttu-id="144d6-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="144d6-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="144d6-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="144d6-138">입력</span><span class="sxs-lookup"><span data-stu-id="144d6-138">INPUTS</span></span>

## <span data-ttu-id="144d6-139">출력</span><span class="sxs-lookup"><span data-stu-id="144d6-139">OUTPUTS</span></span>

###  
<span data-ttu-id="144d6-140">이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="144d6-140">This cmdlet does not generate any output.</span></span>

## <span data-ttu-id="144d6-141">상속자</span><span class="sxs-lookup"><span data-stu-id="144d6-141">NOTES</span></span>

## <span data-ttu-id="144d6-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="144d6-142">RELATED LINKS</span></span>

[<span data-ttu-id="144d6-143">새로운 AzureRmVmssConfig</span><span class="sxs-lookup"><span data-stu-id="144d6-143">New-AzureRmVmssConfig</span></span>](./New-AzureRmVmssConfig.md)
