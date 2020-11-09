---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309185"
---
# <span data-ttu-id="4d65e-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="4d65e-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="4d65e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d65e-102">SYNOPSIS</span></span>
<span data-ttu-id="4d65e-103">리소스에 대 한 네트워크 가상 기기 sku를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="4d65e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d65e-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4d65e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4d65e-105">DESCRIPTION</span></span>
<span data-ttu-id="4d65e-106">New-AzVirtualApplianceSkuProperties 명령은 네트워크 가상 기기 리소스에 대 한 Sku를 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4d65e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4d65e-107">EXAMPLES</span></span>

### <span data-ttu-id="4d65e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4d65e-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="4d65e-109">New-AzNetworkVirtualAppliance 명령에 사용할 가상 기기 Sku 속성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="4d65e-110">변수</span><span class="sxs-lookup"><span data-stu-id="4d65e-110">PARAMETERS</span></span>

### <span data-ttu-id="4d65e-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4d65e-111">-BundledScaleUnit</span></span>
<span data-ttu-id="4d65e-112">번들 눈금 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-112">The bundled scale unit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d65e-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d65e-113">-DefaultProfile</span></span>
<span data-ttu-id="4d65e-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4d65e-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="4d65e-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="4d65e-116">시장 위치 버전.</span><span class="sxs-lookup"><span data-stu-id="4d65e-116">The market place version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d65e-117">-공급 업체 이름</span><span class="sxs-lookup"><span data-stu-id="4d65e-117">-VendorName</span></span>
<span data-ttu-id="4d65e-118">공급 업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-118">The name of the vendor.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4d65e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d65e-119">CommonParameters</span></span>
<span data-ttu-id="4d65e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d65e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d65e-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4d65e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d65e-122">입력</span><span class="sxs-lookup"><span data-stu-id="4d65e-122">INPUTS</span></span>

### <span data-ttu-id="4d65e-123">않아야</span><span class="sxs-lookup"><span data-stu-id="4d65e-123">None</span></span>

## <span data-ttu-id="4d65e-124">출력</span><span class="sxs-lookup"><span data-stu-id="4d65e-124">OUTPUTS</span></span>

### <span data-ttu-id="4d65e-125">PSVirtualApplianceSkuProperties에 대 한.</span><span class="sxs-lookup"><span data-stu-id="4d65e-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="4d65e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="4d65e-126">NOTES</span></span>

## <span data-ttu-id="4d65e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d65e-127">RELATED LINKS</span></span>
