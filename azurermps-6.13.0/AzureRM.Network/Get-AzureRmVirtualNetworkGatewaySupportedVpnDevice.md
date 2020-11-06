---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azurermvirtualnetworkgatewaysupportedvpndevice
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice.md
ms.openlocfilehash: 97c832994e39707c0d45963eda856028589d4b70
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531983"
---
# <span data-ttu-id="bbecd-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span><span class="sxs-lookup"><span data-stu-id="bbecd-101">Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice</span></span>

## <span data-ttu-id="bbecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bbecd-102">SYNOPSIS</span></span>
<span data-ttu-id="bbecd-103">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-103">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bbecd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bbecd-104">SYNTAX</span></span>

```
Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -Name <String> -ResourceGroupName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bbecd-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bbecd-105">DESCRIPTION</span></span>
<span data-ttu-id="bbecd-106">이 #은 지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-106">This commandlet returns a list of supported VPN device brands, models, and firmware versions.</span></span>

## <span data-ttu-id="bbecd-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bbecd-107">EXAMPLES</span></span>

### <span data-ttu-id="bbecd-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bbecd-108">Example 1</span></span>
```
PS C:\> Get-AzureRmVirtualNetworkGatewaySupportedVpnDevice -ResourceGroupName TestRG -Name TestGateway 
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>
```

<span data-ttu-id="bbecd-109">지원 되는 VPN 디바이스 브랜드, 모델 및 펌웨어 버전의 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-109">Returns list of supported VPN device brands, models and firmware versions:</span></span>
<?xml version="1.0" encoding="utf-8"?>
<RpVpnDeviceList version="1.0">
  <Vendor name="Cisco-Test">
    <DeviceFamily name="IOS-Test">
       <FirmwareVersion name="20" />
    </DeviceFamily>
  </Vendor>
</RpVpnDeviceList>

## <span data-ttu-id="bbecd-110">변수</span><span class="sxs-lookup"><span data-stu-id="bbecd-110">PARAMETERS</span></span>

### <span data-ttu-id="bbecd-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bbecd-111">-DefaultProfile</span></span>
<span data-ttu-id="bbecd-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bbecd-113">-이름</span><span class="sxs-lookup"><span data-stu-id="bbecd-113">-Name</span></span>
<span data-ttu-id="bbecd-114">가상 네트워크 게이트웨이 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-114">The virtual network gateway name.</span></span>

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

### <span data-ttu-id="bbecd-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bbecd-115">-ResourceGroupName</span></span>
<span data-ttu-id="bbecd-116">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-116">The resource group name.</span></span>

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

### <span data-ttu-id="bbecd-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bbecd-117">CommonParameters</span></span>
<span data-ttu-id="bbecd-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bbecd-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bbecd-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bbecd-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bbecd-120">입력</span><span class="sxs-lookup"><span data-stu-id="bbecd-120">INPUTS</span></span>

### <span data-ttu-id="bbecd-121">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bbecd-121">System.String</span></span>

## <span data-ttu-id="bbecd-122">출력</span><span class="sxs-lookup"><span data-stu-id="bbecd-122">OUTPUTS</span></span>

### <span data-ttu-id="bbecd-123">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="bbecd-123">System.String</span></span>

## <span data-ttu-id="bbecd-124">상속자</span><span class="sxs-lookup"><span data-stu-id="bbecd-124">NOTES</span></span>

## <span data-ttu-id="bbecd-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bbecd-125">RELATED LINKS</span></span>
