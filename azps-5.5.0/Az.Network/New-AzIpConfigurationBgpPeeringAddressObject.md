---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184449"
---
# <span data-ttu-id="6026e-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="6026e-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="6026e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6026e-102">SYNOPSIS</span></span>
<span data-ttu-id="6026e-103">새 IpconfigurationBgpPeeringAddressObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="6026e-104">구문</span><span class="sxs-lookup"><span data-stu-id="6026e-104">SYNTAX</span></span>

### <span data-ttu-id="6026e-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="6026e-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="6026e-106">설명</span><span class="sxs-lookup"><span data-stu-id="6026e-106">DESCRIPTION</span></span>
<span data-ttu-id="6026e-107">**New-AzIpConfigurationBgpPeeringAddressObject는** 가상 네트워크 게이트웨이 bgpsettings에서 BgpPeeringAddresses 속성을 나타내는 IpConfigurationBgpPeeringAddressObject 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="6026e-108">예제</span><span class="sxs-lookup"><span data-stu-id="6026e-108">EXAMPLES</span></span>

### <span data-ttu-id="6026e-109">1: AzIpConfigurationBgpPeeringAddressObject 만들기</span><span class="sxs-lookup"><span data-stu-id="6026e-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="6026e-110">위에서는 IpConfigurationBgpPeeringAddressObject를 만듭니다. 이 새 개체는 gw1ipconfBgp1이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="6026e-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6026e-111">PARAMETERS</span></span>

### <span data-ttu-id="6026e-112">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6026e-112">-Confirm</span></span>
<span data-ttu-id="6026e-113">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6026e-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="6026e-114">-CustomAddress</span></span>
<span data-ttu-id="6026e-115">BgpPeeringAddresses에 대한 가상 네트워크 게이트웨이 CustomAddress 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026e-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6026e-116">-DefaultProfile</span></span>
<span data-ttu-id="6026e-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026e-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="6026e-118">-IpConfigurationId</span></span>
<span data-ttu-id="6026e-119">BgpPeeringAddresses에 대한 가상 네트워크 게이트웨이 IpConfigurationId입니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6026e-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6026e-120">-WhatIf</span></span>
<span data-ttu-id="6026e-121">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6026e-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6026e-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6026e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6026e-123">CommonParameters</span></span>
<span data-ttu-id="6026e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6026e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6026e-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="6026e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6026e-126">입력</span><span class="sxs-lookup"><span data-stu-id="6026e-126">INPUTS</span></span>

### <span data-ttu-id="6026e-127">없음</span><span class="sxs-lookup"><span data-stu-id="6026e-127">None</span></span>

## <span data-ttu-id="6026e-128">출력</span><span class="sxs-lookup"><span data-stu-id="6026e-128">OUTPUTS</span></span>

### <span data-ttu-id="6026e-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="6026e-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="6026e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6026e-130">NOTES</span></span>

## <span data-ttu-id="6026e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6026e-131">RELATED LINKS</span></span>
