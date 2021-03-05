---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azipconfigurationbgppeeringaddressobject
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzIpConfigurationBgpPeeringAddressObject.md
ms.openlocfilehash: ba713650670abdeb9c64242109b30f47d99724f1
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001104"
---
# <span data-ttu-id="22b8f-101">New-AzIpConfigurationBgpPeeringAddressObject</span><span class="sxs-lookup"><span data-stu-id="22b8f-101">New-AzIpConfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="22b8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="22b8f-102">SYNOPSIS</span></span>
<span data-ttu-id="22b8f-103">새 IpconfigurationBgpPeeringAddressObject를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-103">creates a new IpconfigurationBgpPeeringAddressObject</span></span>

## <span data-ttu-id="22b8f-104">구문</span><span class="sxs-lookup"><span data-stu-id="22b8f-104">SYNTAX</span></span>

### <span data-ttu-id="22b8f-105">기본값(기본값)</span><span class="sxs-lookup"><span data-stu-id="22b8f-105">Default (Default)</span></span>
```
New-AzIpConfigurationBgpPeeringAddressObject -IpConfigurationId <String>
 -CustomAddress <System.Collections.Generic.List`1[System.String]> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```
## <span data-ttu-id="22b8f-106">설명</span><span class="sxs-lookup"><span data-stu-id="22b8f-106">DESCRIPTION</span></span>
<span data-ttu-id="22b8f-107">**New-AzIpConfigurationBgpPeeringAddressObject는** 가상 네트워크 게이트웨이 bgpsetting에서 BgpPeeringAddress 속성을 나타내는 IpConfigurationBgpPeeringAddressObject 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-107">The **New-AzIpConfigurationBgpPeeringAddressObject** creates a IpConfigurationBgpPeeringAddressObject object which represents BgpPeeringAddresses property in your virtual network gateway bgpsettings.</span></span>

## <span data-ttu-id="22b8f-108">예제</span><span class="sxs-lookup"><span data-stu-id="22b8f-108">EXAMPLES</span></span>

### <span data-ttu-id="22b8f-109">1: AzIpConfigurationBgpPeeringAddressObject 만들기</span><span class="sxs-lookup"><span data-stu-id="22b8f-109">1: Create a AzIpConfigurationBgpPeeringAddressObject</span></span>
```
$ipconfigurationId1 = '/subscriptions/c886bc58-0000-4e01-993f-e01ba3702aaf/resourceGroups/testRg/providers/Microsoft.Network/virtualNetworkGateways/gw1/ipConfigurations/default'
$addresslist1 = @('169.254.21.5')
$gw1ipconfBgp1 = New-AzIpConfigurationBgpPeeringAddresses -IpConfigurationId $ipconfigurationId1 -CustomAddress $addresslist1
```

<span data-ttu-id="22b8f-110">위의 ipConfigurationBgpPeeringAddressObject.이 새 개체는 gw1ipconfBgp1에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-110">The above will create a IpConfigurationBgpPeeringAddressObject.This new object will be to gw1ipconfBgp1.</span></span>

## <span data-ttu-id="22b8f-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="22b8f-111">PARAMETERS</span></span>

### <span data-ttu-id="22b8f-112">-확인</span><span class="sxs-lookup"><span data-stu-id="22b8f-112">-Confirm</span></span>
<span data-ttu-id="22b8f-113">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-113">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="22b8f-114">-CustomAddress</span><span class="sxs-lookup"><span data-stu-id="22b8f-114">-CustomAddress</span></span>
<span data-ttu-id="22b8f-115">BgpPeeringAddresses에 대한 가상 네트워크 게이트웨이 CustomAddress 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-115">The virtual network gateway CustomAddress List for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="22b8f-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="22b8f-116">-DefaultProfile</span></span>
<span data-ttu-id="22b8f-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="22b8f-118">-IpConfigurationId</span><span class="sxs-lookup"><span data-stu-id="22b8f-118">-IpConfigurationId</span></span>
<span data-ttu-id="22b8f-119">BgpPeeringAddresses용 가상 네트워크 게이트웨이 IpConfigurationId.</span><span class="sxs-lookup"><span data-stu-id="22b8f-119">The virtual network gateway IpConfigurationId for BgpPeeringAddresses.</span></span>

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

### <span data-ttu-id="22b8f-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="22b8f-120">-WhatIf</span></span>
<span data-ttu-id="22b8f-121">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="22b8f-122">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="22b8f-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="22b8f-123">CommonParameters</span></span>
<span data-ttu-id="22b8f-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="22b8f-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="22b8f-125">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="22b8f-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="22b8f-126">입력</span><span class="sxs-lookup"><span data-stu-id="22b8f-126">INPUTS</span></span>

### <span data-ttu-id="22b8f-127">없음</span><span class="sxs-lookup"><span data-stu-id="22b8f-127">None</span></span>

## <span data-ttu-id="22b8f-128">출력</span><span class="sxs-lookup"><span data-stu-id="22b8f-128">OUTPUTS</span></span>

### <span data-ttu-id="22b8f-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span><span class="sxs-lookup"><span data-stu-id="22b8f-129">Microsoft.Azure.Commands.Network.Models.PSIpConfigurationBgpPeeringAddress</span></span>

## <span data-ttu-id="22b8f-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="22b8f-130">NOTES</span></span>

## <span data-ttu-id="22b8f-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="22b8f-131">RELATED LINKS</span></span>
