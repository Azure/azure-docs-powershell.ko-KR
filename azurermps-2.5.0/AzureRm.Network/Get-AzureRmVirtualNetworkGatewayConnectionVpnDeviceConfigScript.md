---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewayconnectionvpndeviceconfigscript
schema: 2.0.0
ms.openlocfilehash: 0565956d7f40a633bc1aa2c2049ef9a7d764d77e
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93882198"
---
# <span data-ttu-id="5f304-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span><span class="sxs-lookup"><span data-stu-id="5f304-101">Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript</span></span>

## <span data-ttu-id="5f304-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5f304-102">SYNOPSIS</span></span>
<span data-ttu-id="5f304-103">이는 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 가져와 고객이 온-프레미스 VPN 장치에 직접 적용할 수 있는 해당 구성 스크립트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-103">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="5f304-104">이 스크립트는 선택한 디바이스의 구문을 따르고 Azure 게이트웨이 공용 IP 주소, 가상 네트워크 주소 접두사, VPN 터널 미리 공유한 키 등의 필요한 매개 변수를 입력 하므로, 고객은 간단히 해당 VPN 장치 구성에 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-104">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5f304-105">구문과</span><span class="sxs-lookup"><span data-stu-id="5f304-105">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -Name <String> -ResourceGroupName <String>
 -DeviceVendor <String> -DeviceFamily <String> -FirmwareVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="5f304-106">설명은</span><span class="sxs-lookup"><span data-stu-id="5f304-106">DESCRIPTION</span></span>
<span data-ttu-id="5f304-107">이는 연결 리소스, VPN 디바이스 브랜드, 모델, 펌웨어 버전을 가져와 고객이 온-프레미스 VPN 장치에 직접 적용할 수 있는 해당 구성 스크립트를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-107">This commandlet takes the connection resource, VPN device brand, model, firmware version, and return the corresponding configuration script that customers can apply directly on their on-premises VPN devices.</span></span> <span data-ttu-id="5f304-108">이 스크립트는 선택한 디바이스의 구문을 따르고 Azure 게이트웨이 공용 IP 주소, 가상 네트워크 주소 접두사, VPN 터널 미리 공유한 키 등의 필요한 매개 변수를 입력 하므로, 고객은 간단히 해당 VPN 장치 구성에 붙여넣을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-108">The script will follow the syntax of the selected device, and fill in the necessary parameters such as Azure gateway public IP addresses, virtual network address prefixes, VPN tunnel pre-shared key, etc. so customers can simply copy-paste to their VPN device configurations.</span></span>

## <span data-ttu-id="5f304-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5f304-109">EXAMPLES</span></span>

### <span data-ttu-id="5f304-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5f304-110">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway
PS C:\> Get-AzureRmVirtualNetworkGatewayConnectionVpnDeviceConfigScript -ResourceGroupName TestRG -Name TestConnection -DeviceVendor "Cisco-Test" -DeviceFamily "IOS-Test" -FirmwareVersion "20"
```

<span data-ttu-id="5f304-111">위의 예제에서는 Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice를 사용 하 여 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-111">The above example uses Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice to get the supported VPN Device brands, models, and firmware versions.</span></span>
<span data-ttu-id="5f304-112">그런 다음 반환 된 모델 정보 중 하나를 사용 하 여 VirtualNetworkGatewayConnection "TestConnection"에 대 한 VPN 장치 구성 스크립트를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-112">Then uses one of the returned models information to generate a VPN Device configuration script for the VirtualNetworkGatewayConnection "TestConnection".</span></span> <span data-ttu-id="5f304-113">이 예제에 사용 되는 장치에는 DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" 및 FirmwareVersion 20이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-113">The device used in this example has DeviceFamily "IOS-Test", DeviceVendor "Cisco-Test" and FirmwareVersion 20.</span></span>

## <span data-ttu-id="5f304-114">변수</span><span class="sxs-lookup"><span data-stu-id="5f304-114">PARAMETERS</span></span>

### <span data-ttu-id="5f304-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5f304-115">-DefaultProfile</span></span>
<span data-ttu-id="5f304-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5f304-117">DeviceFamily</span><span class="sxs-lookup"><span data-stu-id="5f304-117">-DeviceFamily</span></span>
<span data-ttu-id="5f304-118">VPN 장치 모델/패밀리의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-118">Name of the VPN device model/family.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f304-119">-DeviceVendor</span><span class="sxs-lookup"><span data-stu-id="5f304-119">-DeviceVendor</span></span>
<span data-ttu-id="5f304-120">VPN 장치 공급 업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-120">Name of the VPN device vendor.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f304-121">-FirmwareVersion</span><span class="sxs-lookup"><span data-stu-id="5f304-121">-FirmwareVersion</span></span>
<span data-ttu-id="5f304-122">VPN 장치의 펌웨어 버전.</span><span class="sxs-lookup"><span data-stu-id="5f304-122">Firmware version of the VPN device.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f304-123">-이름</span><span class="sxs-lookup"><span data-stu-id="5f304-123">-Name</span></span>
<span data-ttu-id="5f304-124">구성을 생성할 연결의 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-124">The resource name of the connection for which the configuration is to be generated.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f304-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5f304-125">-ResourceGroupName</span></span>
<span data-ttu-id="5f304-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-126">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5f304-127">-확인</span><span class="sxs-lookup"><span data-stu-id="5f304-127">-Confirm</span></span>
<span data-ttu-id="5f304-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5f304-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5f304-129">-WhatIf</span></span>
<span data-ttu-id="5f304-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5f304-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5f304-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5f304-132">CommonParameters</span></span>
<span data-ttu-id="5f304-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5f304-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5f304-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5f304-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5f304-135">입력</span><span class="sxs-lookup"><span data-stu-id="5f304-135">INPUTS</span></span>

### <span data-ttu-id="5f304-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f304-136">System.String</span></span>

## <span data-ttu-id="5f304-137">출력</span><span class="sxs-lookup"><span data-stu-id="5f304-137">OUTPUTS</span></span>

### <span data-ttu-id="5f304-138">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5f304-138">System.String</span></span>

## <span data-ttu-id="5f304-139">상속자</span><span class="sxs-lookup"><span data-stu-id="5f304-139">NOTES</span></span>

## <span data-ttu-id="5f304-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5f304-140">RELATED LINKS</span></span>

