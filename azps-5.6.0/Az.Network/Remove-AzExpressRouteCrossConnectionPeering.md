---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: 26e924bc94258480e0ae91f30d61c9cfd2adb72c
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101993785"
---
# <span data-ttu-id="ba1d4-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ba1d4-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="ba1d4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ba1d4-102">SYNOPSIS</span></span>
<span data-ttu-id="ba1d4-103">ExpressRoute 교차 연결 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ba1d4-104">구문</span><span class="sxs-lookup"><span data-stu-id="ba1d4-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ba1d4-105">설명</span><span class="sxs-lookup"><span data-stu-id="ba1d4-105">DESCRIPTION</span></span>
<span data-ttu-id="ba1d4-106">**Remove-AzExpressRouteCrossConnectionPeering** cmdlet은 ExpressRoute 교차 연결 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="ba1d4-107">예제</span><span class="sxs-lookup"><span data-stu-id="ba1d4-107">EXAMPLES</span></span>

### <span data-ttu-id="ba1d4-108">예제 1: ExpressRoute 교차 연결에서 피어링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="ba1d4-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="ba1d4-109">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ba1d4-109">PARAMETERS</span></span>

### <span data-ttu-id="ba1d4-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ba1d4-110">-DefaultProfile</span></span>
<span data-ttu-id="ba1d4-111">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="ba1d4-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ba1d4-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="ba1d4-113">제거할 피어링 구성을 포함하는 ExpressRoute 교차 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-114">-Force</span><span class="sxs-lookup"><span data-stu-id="ba1d4-114">-Force</span></span>
<span data-ttu-id="ba1d4-115">리소스를 덮어 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-116">-Name</span><span class="sxs-lookup"><span data-stu-id="ba1d4-116">-Name</span></span>
<span data-ttu-id="ba1d4-117">제거할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-117">The name of the peering configuration to be removed.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="ba1d4-118">-PeerAddressType</span></span>
<span data-ttu-id="ba1d4-119">피어링의 주소 패밀리</span><span class="sxs-lookup"><span data-stu-id="ba1d4-119">The Address family of the peering</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: IPv4, IPv6, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-120">-확인</span><span class="sxs-lookup"><span data-stu-id="ba1d4-120">-Confirm</span></span>
<span data-ttu-id="ba1d4-121">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ba1d4-122">-WhatIf</span></span>
<span data-ttu-id="ba1d4-123">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ba1d4-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ba1d4-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ba1d4-125">CommonParameters</span></span>
<span data-ttu-id="ba1d4-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ba1d4-127">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ba1d4-128">입력</span><span class="sxs-lookup"><span data-stu-id="ba1d4-128">INPUTS</span></span>

### <span data-ttu-id="ba1d4-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ba1d4-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="ba1d4-130">매개 변수 'ExpressRouteCrossConnection'은 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="ba1d4-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="ba1d4-131">출력</span><span class="sxs-lookup"><span data-stu-id="ba1d4-131">OUTPUTS</span></span>

### <span data-ttu-id="ba1d4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ba1d4-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="ba1d4-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ba1d4-133">NOTES</span></span>

## <span data-ttu-id="ba1d4-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ba1d4-134">RELATED LINKS</span></span>

[<span data-ttu-id="ba1d4-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ba1d4-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ba1d4-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="ba1d4-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](./Get-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="ba1d4-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ba1d4-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="ba1d4-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="ba1d4-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
