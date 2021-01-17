---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98380990"
---
# <span data-ttu-id="f315e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="f315e-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="f315e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f315e-102">SYNOPSIS</span></span>
<span data-ttu-id="f315e-103">이 commandlet은 지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f315e-104">구문</span><span class="sxs-lookup"><span data-stu-id="f315e-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f315e-105">설명</span><span class="sxs-lookup"><span data-stu-id="f315e-105">DESCRIPTION</span></span>
<span data-ttu-id="f315e-106">이 commandlet은 지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="f315e-107">예제</span><span class="sxs-lookup"><span data-stu-id="f315e-107">EXAMPLES</span></span>

### <span data-ttu-id="f315e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f315e-108">Example 1</span></span>
```
PS C:\> Get-AzVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="f315e-109">지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="f315e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f315e-110">PARAMETERS</span></span>

### <span data-ttu-id="f315e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f315e-111">-DefaultProfile</span></span>
<span data-ttu-id="f315e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f315e-113">-Name</span><span class="sxs-lookup"><span data-stu-id="f315e-113">-Name</span></span>
<span data-ttu-id="f315e-114">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="f315e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f315e-115">-ResourceGroupName</span></span>
<span data-ttu-id="f315e-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-116">The resource group name.</span></span>

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

### <span data-ttu-id="f315e-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f315e-117">CommonParameters</span></span>
<span data-ttu-id="f315e-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f315e-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f315e-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f315e-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f315e-120">입력</span><span class="sxs-lookup"><span data-stu-id="f315e-120">INPUTS</span></span>

### <span data-ttu-id="f315e-121">System.String</span><span class="sxs-lookup"><span data-stu-id="f315e-121">System.String</span></span>

## <span data-ttu-id="f315e-122">출력</span><span class="sxs-lookup"><span data-stu-id="f315e-122">OUTPUTS</span></span>

### <span data-ttu-id="f315e-123">System.String</span><span class="sxs-lookup"><span data-stu-id="f315e-123">System.String</span></span>

## <span data-ttu-id="f315e-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f315e-124">NOTES</span></span>

## <span data-ttu-id="f315e-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f315e-125">RELATED LINKS</span></span>
