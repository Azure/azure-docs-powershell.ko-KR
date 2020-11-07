---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 0ff95b3e212e61b3d8c9d01b0ad745963d7b24e7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93700468"
---
# <span data-ttu-id="c3c60-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="c3c60-101">Get-AzVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="c3c60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c3c60-102">SYNOPSIS</span></span>
<span data-ttu-id="c3c60-103">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="c3c60-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c3c60-104">SYNTAX</span></span>

```
Get-AzVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c3c60-105">설명은</span><span class="sxs-lookup"><span data-stu-id="c3c60-105">DESCRIPTION</span></span>
<span data-ttu-id="c3c60-106">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="c3c60-107">예제의</span><span class="sxs-lookup"><span data-stu-id="c3c60-107">EXAMPLES</span></span>

### <span data-ttu-id="c3c60-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c3c60-108">Example 1</span></span>
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

<span data-ttu-id="c3c60-109">지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="c3c60-110">변수</span><span class="sxs-lookup"><span data-stu-id="c3c60-110">PARAMETERS</span></span>

### <span data-ttu-id="c3c60-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c3c60-111">-DefaultProfile</span></span>
<span data-ttu-id="c3c60-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c3c60-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c3c60-113">-Name</span></span>
<span data-ttu-id="c3c60-114">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="c3c60-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c3c60-115">-ResourceGroupName</span></span>
<span data-ttu-id="c3c60-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-116">The resource group name.</span></span>

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

### <span data-ttu-id="c3c60-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c3c60-117">CommonParameters</span></span>
<span data-ttu-id="c3c60-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c3c60-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c3c60-119">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c3c60-119">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c3c60-120">입력</span><span class="sxs-lookup"><span data-stu-id="c3c60-120">INPUTS</span></span>

### <span data-ttu-id="c3c60-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3c60-121">System.String</span></span>

## <span data-ttu-id="c3c60-122">출력</span><span class="sxs-lookup"><span data-stu-id="c3c60-122">OUTPUTS</span></span>

### <span data-ttu-id="c3c60-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c3c60-123">System.String</span></span>

## <span data-ttu-id="c3c60-124">상속자</span><span class="sxs-lookup"><span data-stu-id="c3c60-124">NOTES</span></span>

## <span data-ttu-id="c3c60-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c3c60-125">RELATED LINKS</span></span>
