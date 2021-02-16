---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: fe7c4550e3f54268e600414f8516095132b72115
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100402289"
---
# <span data-ttu-id="f3e5b-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f3e5b-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="f3e5b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3e5b-102">SYNOPSIS</span></span>
<span data-ttu-id="f3e5b-103">ExpressRoute 교차 연결 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="f3e5b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f3e5b-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3e5b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f3e5b-105">DESCRIPTION</span></span>
<span data-ttu-id="f3e5b-106">**Remove-AzExpressRouteCrossConnectionPeering** cmdlet은 ExpressRoute 교차 연결 피어링 구성을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="f3e5b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f3e5b-107">EXAMPLES</span></span>

### <span data-ttu-id="f3e5b-108">예제 1: ExpressRoute 교차 연결에서 피어링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="f3e5b-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="f3e5b-109">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f3e5b-109">PARAMETERS</span></span>

### <span data-ttu-id="f3e5b-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3e5b-110">-DefaultProfile</span></span>
<span data-ttu-id="f3e5b-111">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f3e5b-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3e5b-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="f3e5b-113">제거할 피어링 구성을 포함하는 ExpressRoute 교차 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f3e5b-114">-Force</span><span class="sxs-lookup"><span data-stu-id="f3e5b-114">-Force</span></span>
<span data-ttu-id="f3e5b-115">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-115">Do not ask for confirmation if you want to overrite a resource</span></span>

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

### <span data-ttu-id="f3e5b-116">-Name</span><span class="sxs-lookup"><span data-stu-id="f3e5b-116">-Name</span></span>
<span data-ttu-id="f3e5b-117">제거할 피어링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="f3e5b-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="f3e5b-118">-PeerAddressType</span></span>
<span data-ttu-id="f3e5b-119">피어링의 주소 패밀리</span><span class="sxs-lookup"><span data-stu-id="f3e5b-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="f3e5b-120">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f3e5b-120">-Confirm</span></span>
<span data-ttu-id="f3e5b-121">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3e5b-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3e5b-122">-WhatIf</span></span>
<span data-ttu-id="f3e5b-123">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f3e5b-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f3e5b-124">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3e5b-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3e5b-125">CommonParameters</span></span>
<span data-ttu-id="f3e5b-126">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3e5b-127">자세한 내용은 다음 about_CommonParameters https://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3e5b-128">입력</span><span class="sxs-lookup"><span data-stu-id="f3e5b-128">INPUTS</span></span>

### <span data-ttu-id="f3e5b-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3e5b-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="f3e5b-130">'ExpressRouteCrossConnection' 매개 변수는 파이프라인에서 'PSExpressRouteCrossConnection' 형식의 값을 허용합니다.</span><span class="sxs-lookup"><span data-stu-id="f3e5b-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="f3e5b-131">출력</span><span class="sxs-lookup"><span data-stu-id="f3e5b-131">OUTPUTS</span></span>

### <span data-ttu-id="f3e5b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3e5b-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="f3e5b-133">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f3e5b-133">NOTES</span></span>

## <span data-ttu-id="f3e5b-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3e5b-134">RELATED LINKS</span></span>

[<span data-ttu-id="f3e5b-135">Add-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="f3e5b-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)



[<span data-ttu-id="f3e5b-136">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3e5b-136">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="f3e5b-137">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="f3e5b-137">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
