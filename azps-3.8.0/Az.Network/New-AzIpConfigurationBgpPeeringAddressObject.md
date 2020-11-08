---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: 2a31aa9db3264dd24c6d77bdad7b10d6ecad10b1
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041811"
---
# <span data-ttu-id="a9286-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="a9286-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="a9286-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a9286-102">SYNOPSIS</span></span>
<span data-ttu-id="a9286-103">새 IpconfigurationBgpPeeringAddressObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="a9286-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a9286-104">SYNTAX</span></span>

### <span data-ttu-id="a9286-105">기본값 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a9286-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="a9286-106">설명은</span><span class="sxs-lookup"><span data-stu-id="a9286-106">DESCRIPTION</span></span>
<span data-ttu-id="a9286-107">**New-AzIpConfigurationBgpPeeringAddressObject** 는 가상 네트워크 게이트웨이 Bgpsettings에서 BgpPeeringAddresses 속성을 나타내는 IpConfigurationBgpPeeringAddressObject 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="a9286-108">예제의</span><span class="sxs-lookup"><span data-stu-id="a9286-108">EXAMPLES</span></span>

### <span data-ttu-id="a9286-109">1: AzIpConfigurationBgpPeeringAddressObject 만들기</span><span class="sxs-lookup"><span data-stu-id="a9286-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="a9286-110">위의 방법으로 IpConfigurationBgpPeeringAddressObject를 만들 수 있습니다 .이 새 개체는 gw1ipconfBgp1.</span><span class="sxs-lookup"><span data-stu-id="a9286-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="a9286-111">변수</span><span class="sxs-lookup"><span data-stu-id="a9286-111">PARAMETERS</span></span>

### <span data-ttu-id="a9286-112">-확인</span><span class="sxs-lookup"><span data-stu-id="a9286-112">-Confirm</span></span>
<span data-ttu-id="a9286-113">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a9286-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="a9286-114">-CustomAddress</span></span>
<span data-ttu-id="a9286-115">BgpPeeringAddresses의 가상 네트워크 게이트웨이 CustomAddress 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="a9286-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a9286-116">-DefaultProfile</span></span>
<span data-ttu-id="a9286-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a9286-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="a9286-118">-IpConfigurationId</span></span>
<span data-ttu-id="a9286-119">BgpPeeringAddresses에 대 한 가상 네트워크 게이트웨이 IpConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="a9286-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="a9286-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a9286-120">-WhatIf</span></span>
<span data-ttu-id="a9286-121">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a9286-122">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a9286-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a9286-123">CommonParameters</span></span>
<span data-ttu-id="a9286-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a9286-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a9286-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a9286-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a9286-126">입력</span><span class="sxs-lookup"><span data-stu-id="a9286-126">INPUTS</span></span>

### <span data-ttu-id="a9286-127">않아야</span><span class="sxs-lookup"><span data-stu-id="a9286-127">None</span></span>

## <span data-ttu-id="a9286-128">출력</span><span class="sxs-lookup"><span data-stu-id="a9286-128">OUTPUTS</span></span>

### <span data-ttu-id="a9286-129">PSIpConfigurationBgpPeeringAddress에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a9286-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="a9286-130">상속자</span><span class="sxs-lookup"><span data-stu-id="a9286-130">NOTES</span></span>

## <span data-ttu-id="a9286-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a9286-131">RELATED LINKS</span></span>
