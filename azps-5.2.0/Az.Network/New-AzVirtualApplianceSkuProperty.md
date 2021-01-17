---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: cfe9fb07854fcc5850e1c5f73f4da7fe43f172a8
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98330590"
---
# <span data-ttu-id="4078d-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="4078d-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="4078d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4078d-102">SYNOPSIS</span></span>
<span data-ttu-id="4078d-103">리소스에 대한 네트워크 가상 어플라이언스 SKU를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="4078d-104">구문</span><span class="sxs-lookup"><span data-stu-id="4078d-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4078d-105">설명</span><span class="sxs-lookup"><span data-stu-id="4078d-105">DESCRIPTION</span></span>
<span data-ttu-id="4078d-106">New-AzVirtualApplianceSkuProperties 명령은 네트워크 가상 어플라이언스 리소스에 대한 SKU를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="4078d-107">예제</span><span class="sxs-lookup"><span data-stu-id="4078d-107">EXAMPLES</span></span>

### <span data-ttu-id="4078d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4078d-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="4078d-109">가상 어플라이언스 SKU 속성 개체를 만들어 New-AzNetworkVirtualAppliance.</span><span class="sxs-lookup"><span data-stu-id="4078d-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="4078d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4078d-110">PARAMETERS</span></span>

### <span data-ttu-id="4078d-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="4078d-111">-BundledScaleUnit</span></span>
<span data-ttu-id="4078d-112">번들 배율 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="4078d-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4078d-113">-DefaultProfile</span></span>
<span data-ttu-id="4078d-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4078d-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="4078d-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="4078d-116">시장 장소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-116">The market place version.</span></span>

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

### <span data-ttu-id="4078d-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="4078d-117">-VendorName</span></span>
<span data-ttu-id="4078d-118">공급업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="4078d-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4078d-119">CommonParameters</span></span>
<span data-ttu-id="4078d-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4078d-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4078d-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4078d-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4078d-122">입력</span><span class="sxs-lookup"><span data-stu-id="4078d-122">INPUTS</span></span>

### <span data-ttu-id="4078d-123">없음</span><span class="sxs-lookup"><span data-stu-id="4078d-123">None</span></span>

## <span data-ttu-id="4078d-124">출력</span><span class="sxs-lookup"><span data-stu-id="4078d-124">OUTPUTS</span></span>

### <span data-ttu-id="4078d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="4078d-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="4078d-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4078d-126">NOTES</span></span>

## <span data-ttu-id="4078d-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4078d-127">RELATED LINKS</span></span>
