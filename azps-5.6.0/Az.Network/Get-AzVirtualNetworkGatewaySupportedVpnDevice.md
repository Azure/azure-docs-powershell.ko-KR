---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 45cb703d6fdc87238f4d1ed35ada90aadeed501b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101987807"
---
# <span data-ttu-id="83259-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="83259-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="83259-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="83259-102">SYNOPSIS</span></span>
<span data-ttu-id="83259-103">이 명령줄은 지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83259-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="83259-104">구문</span><span class="sxs-lookup"><span data-stu-id="83259-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="83259-105">설명</span><span class="sxs-lookup"><span data-stu-id="83259-105">DESCRIPTION</span></span>
<span data-ttu-id="83259-106">이 명령줄은 지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83259-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="83259-107">예제</span><span class="sxs-lookup"><span data-stu-id="83259-107">EXAMPLES</span></span>

### <span data-ttu-id="83259-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="83259-108">Example 1</span></span>
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

<span data-ttu-id="83259-109">지원되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전 목록을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="83259-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="83259-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="83259-110">PARAMETERS</span></span>

### <span data-ttu-id="83259-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="83259-111">-DefaultProfile</span></span>
<span data-ttu-id="83259-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="83259-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="83259-113">-Name</span><span class="sxs-lookup"><span data-stu-id="83259-113">-Name</span></span>
<span data-ttu-id="83259-114">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83259-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="83259-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="83259-115">-ResourceGroupName</span></span>
<span data-ttu-id="83259-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="83259-116">The resource group name.</span></span>

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

### <span data-ttu-id="83259-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="83259-117">CommonParameters</span></span>
<span data-ttu-id="83259-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="83259-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="83259-119">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="83259-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="83259-120">입력</span><span class="sxs-lookup"><span data-stu-id="83259-120">INPUTS</span></span>

### <span data-ttu-id="83259-121">System.String</span><span class="sxs-lookup"><span data-stu-id="83259-121">System.String</span></span>

## <span data-ttu-id="83259-122">출력</span><span class="sxs-lookup"><span data-stu-id="83259-122">OUTPUTS</span></span>

### <span data-ttu-id="83259-123">System.String</span><span class="sxs-lookup"><span data-stu-id="83259-123">System.String</span></span>

## <span data-ttu-id="83259-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="83259-124">NOTES</span></span>

## <span data-ttu-id="83259-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="83259-125">RELATED LINKS</span></span>
