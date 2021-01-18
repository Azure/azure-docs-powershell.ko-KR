---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 5421c33c4858c99be4dd84ba7f0c1bff401e1182
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495210"
---
# <span data-ttu-id="7f380-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="7f380-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="7f380-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f380-102">SYNOPSIS</span></span>
<span data-ttu-id="7f380-103">이 commandlet은 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 사용하며, 고객이 해당온-프레미스 VPN 디바이스에 직접 적용할 수 있는 해당 구성 스크립트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="7f380-104">스크립트는 선택한 디바이스의 구문을 따르고 Azure 게이트웨이 공용 IP 주소, 가상 네트워크 주소 주소, VPN 터널 미리 공유 키와 같은 필요한 매개 변수를 채우기 때문에 고객이 VPN 디바이스 구성에 복사하여 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="7f380-105">구문</span><span class="sxs-lookup"><span data-stu-id="7f380-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f380-106">설명</span><span class="sxs-lookup"><span data-stu-id="7f380-106">DESCRIPTION</span></span>
<span data-ttu-id="7f380-107">이 commandlet은 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 사용하며, 고객이 해당온-프레미스 VPN 디바이스에 직접 적용할 수 있는 해당 구성 스크립트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="7f380-108">스크립트는 선택한 디바이스의 구문을 따르고 Azure 게이트웨이 공용 IP 주소, 가상 네트워크 주소 주소, VPN 터널 미리 공유 키와 같은 필요한 매개 변수를 채우기 때문에 고객이 VPN 디바이스 구성에 복사하여 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="7f380-109">예제</span><span class="sxs-lookup"><span data-stu-id="7f380-109">EXAMPLES</span></span>

### <span data-ttu-id="7f380-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f380-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="7f380-111">위의 예제에서는 Get-AzVirtualNetworkGatewaySupportedVpnDevice VPN 디바이스 브랜드, 모델 및 펌웨어 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="7f380-112">그런 다음, 반환된 모델 정보 중 하나를 사용하여 VirtualNetworkGatewayConnection "TestConnection"에 대한 VPN 디바이스 구성 스크립트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="7f380-113">이 예제에 사용된 디바이스에는 DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" 및 FirmwareVersion 20이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="7f380-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7f380-114">PARAMETERS</span></span>

### <span data-ttu-id="7f380-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7f380-115">-DefaultProfile</span></span>
<span data-ttu-id="7f380-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7f380-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="7f380-117">-DeviceFamily</span></span>
<span data-ttu-id="7f380-118">VPN 디바이스 모델/패밀리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-118">Name of the VPN device model/family.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f380-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="7f380-119">-DeviceVendor</span></span>
<span data-ttu-id="7f380-120">VPN 디바이스 공급업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-120">Name of the VPN device vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f380-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="7f380-121">-FirmwareVersion</span></span>
<span data-ttu-id="7f380-122">VPN 디바이스의 펌웨어 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-122">Firmware version of the VPN device.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f380-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7f380-123">-Name</span></span>
<span data-ttu-id="7f380-124">구성을 생성하는 연결의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f380-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7f380-125">-ResourceGroupName</span></span>
<span data-ttu-id="7f380-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-126">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7f380-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7f380-127">-Confirm</span></span>
<span data-ttu-id="7f380-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7f380-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f380-129">-WhatIf</span></span>
<span data-ttu-id="7f380-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7f380-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f380-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7f380-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f380-132">CommonParameters</span></span>
<span data-ttu-id="7f380-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7f380-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f380-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7f380-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f380-135">입력</span><span class="sxs-lookup"><span data-stu-id="7f380-135">INPUTS</span></span>

### <span data-ttu-id="7f380-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7f380-136">System.String</span></span>

## <span data-ttu-id="7f380-137">출력</span><span class="sxs-lookup"><span data-stu-id="7f380-137">OUTPUTS</span></span>

### <span data-ttu-id="7f380-138">System.String</span><span class="sxs-lookup"><span data-stu-id="7f380-138">System.String</span></span>

## <span data-ttu-id="7f380-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7f380-139">NOTES</span></span>

## <span data-ttu-id="7f380-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f380-140">RELATED LINKS</span></span>
