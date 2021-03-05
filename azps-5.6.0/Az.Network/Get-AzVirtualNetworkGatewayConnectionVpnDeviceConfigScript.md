---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript.md
ms.openlocfilehash: 967e45ce124ead583a7c2f3e36a80dedb80d4e20
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101978288"
---
# <span data-ttu-id="9929d-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="9929d-101">Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="9929d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9929d-102">SYNOPSIS</span></span>
<span data-ttu-id="9929d-103">이 명령줄은 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 사용하며 고객이 해당온-프레미스 VPN 디바이스에 직접 적용할 수 있는 해당 구성 스크립트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9929d-104">이 스크립트는 선택한 디바이스의 구문을 따라 Azure Gateway 공용 IP 주소, 가상 네트워크 주소 미리 공유 키, VPN 터널 미리 공유 키와 같은 필요한 매개 변수를 채우고 고객이 VPN 디바이스 구성에 복사 붙여넣기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="9929d-105">구문</span><span class="sxs-lookup"><span data-stu-id="9929d-105">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9929d-106">설명</span><span class="sxs-lookup"><span data-stu-id="9929d-106">DESCRIPTION</span></span>
<span data-ttu-id="9929d-107">이 명령줄은 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 사용하며 고객이 해당온-프레미스 VPN 디바이스에 직접 적용할 수 있는 해당 구성 스크립트를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="9929d-108">이 스크립트는 선택한 디바이스의 구문을 따라 Azure Gateway 공용 IP 주소, 가상 네트워크 주소 미리 공유 키, VPN 터널 미리 공유 키와 같은 필요한 매개 변수를 채우고 고객이 VPN 디바이스 구성에 복사 붙여넣기만 하면 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="9929d-109">예제</span><span class="sxs-lookup"><span data-stu-id="9929d-109">EXAMPLES</span></span>

### <span data-ttu-id="9929d-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="9929d-110">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="9929d-111">위의 예제에서는 Get-AzVirtualNetworkGatewaySupportedVpnDevice VPN Device 브랜드, 모델 및 펌웨어 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-111">The above example uses Get-AzVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="9929d-112">그런 다음 반환된 모델 정보 중 하나를 사용하여 VirtualNetworkGatewayConnection "TestConnection"에 대한 VPN 디바이스 구성 스크립트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="9929d-113">이 예제에 사용되는 디바이스에는 DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" 및 펌웨어Version 20이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="9929d-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="9929d-114">PARAMETERS</span></span>

### <span data-ttu-id="9929d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9929d-115">-DefaultProfile</span></span>
<span data-ttu-id="9929d-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9929d-117">-DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="9929d-117">-DeviceFamily</span></span>
<span data-ttu-id="9929d-118">VPN 디바이스 모델/패밀리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-118">Name of the VPN device model/family.</span></span>

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

### <span data-ttu-id="9929d-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="9929d-119">-DeviceVendor</span></span>
<span data-ttu-id="9929d-120">VPN 디바이스 공급업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-120">Name of the VPN device vendor.</span></span>

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

### <span data-ttu-id="9929d-121">-펌웨어Version</span><span class="sxs-lookup"><span data-stu-id="9929d-121">-FirmwareVersion</span></span>
<span data-ttu-id="9929d-122">VPN 디바이스의 펌웨어 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-122">Firmware version of the VPN device.</span></span>

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

### <span data-ttu-id="9929d-123">-Name</span><span class="sxs-lookup"><span data-stu-id="9929d-123">-Name</span></span>
<span data-ttu-id="9929d-124">구성을 생성할 연결의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-124">The resource name of the connection for which the configuration is to be generated.</span></span>

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

### <span data-ttu-id="9929d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9929d-125">-ResourceGroupName</span></span>
<span data-ttu-id="9929d-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-126">The resource group name.</span></span>

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

### <span data-ttu-id="9929d-127">-확인</span><span class="sxs-lookup"><span data-stu-id="9929d-127">-Confirm</span></span>
<span data-ttu-id="9929d-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9929d-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9929d-129">-WhatIf</span></span>
<span data-ttu-id="9929d-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9929d-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9929d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9929d-132">CommonParameters</span></span>
<span data-ttu-id="9929d-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9929d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9929d-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="9929d-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9929d-135">입력</span><span class="sxs-lookup"><span data-stu-id="9929d-135">INPUTS</span></span>

### <span data-ttu-id="9929d-136">System.String</span><span class="sxs-lookup"><span data-stu-id="9929d-136">System.String</span></span>

## <span data-ttu-id="9929d-137">출력</span><span class="sxs-lookup"><span data-stu-id="9929d-137">OUTPUTS</span></span>

### <span data-ttu-id="9929d-138">System.String</span><span class="sxs-lookup"><span data-stu-id="9929d-138">System.String</span></span>

## <span data-ttu-id="9929d-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9929d-139">NOTES</span></span>

## <span data-ttu-id="9929d-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9929d-140">RELATED LINKS</span></span>
