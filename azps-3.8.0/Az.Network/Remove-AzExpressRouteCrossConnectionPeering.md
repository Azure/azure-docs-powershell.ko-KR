---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: 462F3EF7-4C15-41F8-853D-CDCC8E67673D
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/Remove-AzExpressRouteCrossConnectionPeering
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzExpressRouteCrossConnectionPeering.md
ms.openlocfilehash: eb90b668bf0466c44e3fde0ef0a8d6777074fb37
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044055"
---
# <span data-ttu-id="a306e-101">Remove-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a306e-101">Remove-AzExpressRouteCrossConnectionPeering</span></span>

## <span data-ttu-id="a306e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a306e-102">SYNOPSIS</span></span>
<span data-ttu-id="a306e-103">Express 경로 간 연결 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-103">Removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a306e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a306e-104">SYNTAX</span></span>

```
Remove-AzExpressRouteCrossConnectionPeering -ExpressRouteCrossConnection <PSExpressRouteCrossConnection>
 [-Name <String>] [-PeerAddressType <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a306e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a306e-105">DESCRIPTION</span></span>
<span data-ttu-id="a306e-106">**AzExpressRouteCrossConnectionPeering** Cmdlet은 express 경로 간 연결 피어 링 구성을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-106">The **Remove-AzExpressRouteCrossConnectionPeering** cmdlet removes an ExpressRoute cross connection peering configuration.</span></span>

## <span data-ttu-id="a306e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a306e-107">EXAMPLES</span></span>

### <span data-ttu-id="a306e-108">예제 1: Express 경로 간 연결에서 피어 링 구성 제거</span><span class="sxs-lookup"><span data-stu-id="a306e-108">Example 1: Remove a peering configuration from an ExpressRoute cross connection</span></span>
```
$cc = Get-AzExpressRouteCrossConnection -Name $CrossConnectionName -ResourceGroupName $rg
Remove-AzExpressRouteCrossConnectionPeering -Name 'AzurePrivatePeering' -ExpressRouteCrossConnection $cc
Set-AzExpressRouteCrossConnection -ExpressRouteCrossConnection $cc
```

## <span data-ttu-id="a306e-109">변수</span><span class="sxs-lookup"><span data-stu-id="a306e-109">PARAMETERS</span></span>

### <span data-ttu-id="a306e-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a306e-110">-DefaultProfile</span></span>
<span data-ttu-id="a306e-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a306e-112">-ExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a306e-112">-ExpressRouteCrossConnection</span></span>
<span data-ttu-id="a306e-113">제거할 피어 링 구성을 포함 하는 Express 경로 간 연결입니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-113">The ExpressRoute cross connection containing the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a306e-114">-Force</span><span class="sxs-lookup"><span data-stu-id="a306e-114">-Force</span></span>
<span data-ttu-id="a306e-115">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="a306e-115">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="a306e-116">-이름</span><span class="sxs-lookup"><span data-stu-id="a306e-116">-Name</span></span>
<span data-ttu-id="a306e-117">제거할 피어 링 구성의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-117">The name of the peering configuration to be removed.</span></span>

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

### <span data-ttu-id="a306e-118">-PeerAddressType</span><span class="sxs-lookup"><span data-stu-id="a306e-118">-PeerAddressType</span></span>
<span data-ttu-id="a306e-119">피어 링의 주소 패밀리입니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-119">The Address family of the peering</span></span>

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

### <span data-ttu-id="a306e-120">-확인</span><span class="sxs-lookup"><span data-stu-id="a306e-120">-Confirm</span></span>
<span data-ttu-id="a306e-121">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a306e-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a306e-122">-WhatIf</span></span>
<span data-ttu-id="a306e-123">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a306e-124">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a306e-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a306e-125">CommonParameters</span></span>
<span data-ttu-id="a306e-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a306e-127">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a306e-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a306e-128">입력</span><span class="sxs-lookup"><span data-stu-id="a306e-128">INPUTS</span></span>

### <span data-ttu-id="a306e-129">PSExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a306e-129">PSExpressRouteCrossConnection</span></span>
<span data-ttu-id="a306e-130">' ExpressRouteCrossConnection ' 매개 변수는 파이프라인에서 ' PSExpressRouteCrossConnection ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a306e-130">Parameter 'ExpressRouteCrossConnection' accepts value of type 'PSExpressRouteCrossConnection' from the pipeline</span></span>

## <span data-ttu-id="a306e-131">출력</span><span class="sxs-lookup"><span data-stu-id="a306e-131">OUTPUTS</span></span>

### <span data-ttu-id="a306e-132">PSExpressRouteCrossConnection에 대 한.</span><span class="sxs-lookup"><span data-stu-id="a306e-132">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCrossConnection</span></span>

## <span data-ttu-id="a306e-133">상속자</span><span class="sxs-lookup"><span data-stu-id="a306e-133">NOTES</span></span>

## <span data-ttu-id="a306e-134">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a306e-134">RELATED LINKS</span></span>

[<span data-ttu-id="a306e-135">추가-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a306e-135">Add-AzExpressRouteCrossConnectionPeering</span></span>](Add-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a306e-136">Get-AzExpressRouteCrossConnectionPeering</span><span class="sxs-lookup"><span data-stu-id="a306e-136">Get-AzExpressRouteCrossConnectionPeering</span></span>](New-AzExpressRouteCrossConnectionPeering.md)

[<span data-ttu-id="a306e-137">Get-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a306e-137">Get-AzExpressRouteCrossConnection</span></span>](Get-AzExpressRouteCrossConnection.md)

[<span data-ttu-id="a306e-138">Set-AzExpressRouteCrossConnection</span><span class="sxs-lookup"><span data-stu-id="a306e-138">Set-AzExpressRouteCrossConnection</span></span>](Set-AzExpressRouteCrossConnection.md)
