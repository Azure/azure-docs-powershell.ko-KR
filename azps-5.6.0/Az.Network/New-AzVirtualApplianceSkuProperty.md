---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azvirtualapplianceskuproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualApplianceSkuProperty.md
ms.openlocfilehash: 0179a033d9cc99ff2f373dbaceb1bcb97ab3468f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006176"
---
# <span data-ttu-id="ae6e9-101">New-AzVirtualApplianceSkuProperty</span><span class="sxs-lookup"><span data-stu-id="ae6e9-101">New-AzVirtualApplianceSkuProperty</span></span>

## <span data-ttu-id="ae6e9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ae6e9-102">SYNOPSIS</span></span>
<span data-ttu-id="ae6e9-103">리소스에 대한 네트워크 가상 어플라이언스 sku를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-103">Define a Network Virtual Appliance sku for the resource.</span></span>

## <span data-ttu-id="ae6e9-104">구문</span><span class="sxs-lookup"><span data-stu-id="ae6e9-104">SYNTAX</span></span>

```
New-AzVirtualApplianceSkuProperty -VendorName <String> -BundledScaleUnit <String> -MarketPlaceVersion <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="ae6e9-105">설명</span><span class="sxs-lookup"><span data-stu-id="ae6e9-105">DESCRIPTION</span></span>
<span data-ttu-id="ae6e9-106">New-AzVirtualApplianceSkuProperties 명령은 네트워크 가상 어플라이언스에 대한 Sku 리소스를 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-106">The New-AzVirtualApplianceSkuProperties command defines a Sku for Network Virtual Appliance resource.</span></span>

## <span data-ttu-id="ae6e9-107">예제</span><span class="sxs-lookup"><span data-stu-id="ae6e9-107">EXAMPLES</span></span>

### <span data-ttu-id="ae6e9-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="ae6e9-108">Example 1</span></span>
```powershell
PS C:\> $var=New-AzVirtualApplianceSkuProperty -VendorName "barracudasdwanrelease" -BundledScaleUnit 1 -MarketPlaceVersion 'latest'
```

<span data-ttu-id="ae6e9-109">가상 어플라이언스 Sku New-AzNetworkVirtualAppliance 속성 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-109">Create a Virtual Appliance Sku Properties object to be used with New-AzNetworkVirtualAppliance command.</span></span> 

## <span data-ttu-id="ae6e9-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ae6e9-110">PARAMETERS</span></span>

### <span data-ttu-id="ae6e9-111">-BundledScaleUnit</span><span class="sxs-lookup"><span data-stu-id="ae6e9-111">-BundledScaleUnit</span></span>
<span data-ttu-id="ae6e9-112">번들 확장 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-112">The bundled scale unit.</span></span>

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

### <span data-ttu-id="ae6e9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ae6e9-113">-DefaultProfile</span></span>
<span data-ttu-id="ae6e9-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ae6e9-115">-MarketPlaceVersion</span><span class="sxs-lookup"><span data-stu-id="ae6e9-115">-MarketPlaceVersion</span></span>
<span data-ttu-id="ae6e9-116">시장 장소 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-116">The market place version.</span></span>

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

### <span data-ttu-id="ae6e9-117">-VendorName</span><span class="sxs-lookup"><span data-stu-id="ae6e9-117">-VendorName</span></span>
<span data-ttu-id="ae6e9-118">공급업체의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-118">The name of the vendor.</span></span>

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

### <span data-ttu-id="ae6e9-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ae6e9-119">CommonParameters</span></span>
<span data-ttu-id="ae6e9-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ae6e9-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ae6e9-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="ae6e9-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ae6e9-122">입력</span><span class="sxs-lookup"><span data-stu-id="ae6e9-122">INPUTS</span></span>

### <span data-ttu-id="ae6e9-123">없음</span><span class="sxs-lookup"><span data-stu-id="ae6e9-123">None</span></span>

## <span data-ttu-id="ae6e9-124">출력</span><span class="sxs-lookup"><span data-stu-id="ae6e9-124">OUTPUTS</span></span>

### <span data-ttu-id="ae6e9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span><span class="sxs-lookup"><span data-stu-id="ae6e9-125">Microsoft.Azure.Commands.Network.Models.PSVirtualApplianceSkuProperties</span></span>

## <span data-ttu-id="ae6e9-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ae6e9-126">NOTES</span></span>

## <span data-ttu-id="ae6e9-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ae6e9-127">RELATED LINKS</span></span>
