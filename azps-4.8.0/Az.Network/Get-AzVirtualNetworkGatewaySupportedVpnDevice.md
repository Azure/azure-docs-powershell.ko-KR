---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: f643b280e0777f3251380ecf36f4fcc070b545c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204489"
---
# <span data-ttu-id="faaaa-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="faaaa-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="faaaa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="faaaa-102">SYNOPSIS</span></span>
<span data-ttu-id="faaaa-103">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="faaaa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="faaaa-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="faaaa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="faaaa-105">DESCRIPTION</span></span>
<span data-ttu-id="faaaa-106">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="faaaa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="faaaa-107">EXAMPLES</span></span>

### <span data-ttu-id="faaaa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="faaaa-108">Example 1</span></span>
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

<span data-ttu-id="faaaa-109">지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="faaaa-110">변수</span><span class="sxs-lookup"><span data-stu-id="faaaa-110">PARAMETERS</span></span>

### <span data-ttu-id="faaaa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="faaaa-111">-DefaultProfile</span></span>
<span data-ttu-id="faaaa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="faaaa-113">-이름</span><span class="sxs-lookup"><span data-stu-id="faaaa-113">-Name</span></span>
<span data-ttu-id="faaaa-114">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="faaaa-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="faaaa-115">-ResourceGroupName</span></span>
<span data-ttu-id="faaaa-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-116">The resource group name.</span></span>

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

### <span data-ttu-id="faaaa-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="faaaa-117">CommonParameters</span></span>
<span data-ttu-id="faaaa-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="faaaa-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="faaaa-119">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="faaaa-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="faaaa-120">입력</span><span class="sxs-lookup"><span data-stu-id="faaaa-120">INPUTS</span></span>

### <span data-ttu-id="faaaa-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="faaaa-121">System.String</span></span>

## <span data-ttu-id="faaaa-122">출력</span><span class="sxs-lookup"><span data-stu-id="faaaa-122">OUTPUTS</span></span>

### <span data-ttu-id="faaaa-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="faaaa-123">System.String</span></span>

## <span data-ttu-id="faaaa-124">상속자</span><span class="sxs-lookup"><span data-stu-id="faaaa-124">NOTES</span></span>

## <span data-ttu-id="faaaa-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="faaaa-125">RELATED LINKS</span></span>
