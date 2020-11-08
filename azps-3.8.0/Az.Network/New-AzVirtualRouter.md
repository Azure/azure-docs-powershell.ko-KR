---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azvirtualrouter
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzVirtualRouter.md
ms.openlocfilehash: 75315de4e6ca2cf799f6cefb1d3b9c143631f5a3
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043222"
---
# <span data-ttu-id="f3ee4-101">New-AzVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3ee4-101">New-AzVirtualRouter</span></span>

## <span data-ttu-id="f3ee4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3ee4-102">SYNOPSIS</span></span>
<span data-ttu-id="f3ee4-103">Azure VirtualRouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-103">Creates an Azure VirtualRouter.</span></span>

## <span data-ttu-id="f3ee4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f3ee4-104">SYNTAX</span></span>

### <span data-ttu-id="f3ee4-105">HostedGatewayParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3ee4-105">HostedGatewayParameterSet (Default)</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGateway <PSVirtualNetworkGateway>
 -Location <String> [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3ee4-106">HostedGatewayIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3ee4-106">HostedGatewayIdParameterSet</span></span>
```
New-AzVirtualRouter -ResourceGroupName <String> -Name <String> -HostedGatewayId <String> -Location <String>
 [-Tag <Hashtable>] [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f3ee4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f3ee4-107">DESCRIPTION</span></span>
<span data-ttu-id="f3ee4-108">**AzVirtualRouter** Cmdlet은 Azure virtualrouter를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-108">The **New-AzVirtualRouter** cmdlet creates an Azure VirtualRouter</span></span>


## <span data-ttu-id="f3ee4-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f3ee4-109">EXAMPLES</span></span>

### <span data-ttu-id="f3ee4-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3ee4-110">Example 1</span></span>
```powershell
$gatewayId = '/subscriptions/8c992d64-fce9-426d-b278-85642dfeab03/resourceGroups/virtualRouterRG/providers/Microsoft.Network/virtualNetworkGateways/erGateway'
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGatewayId $gatewayId
```

### <span data-ttu-id="f3ee4-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="f3ee4-111">Example 2</span></span>
```powershell
$gateway = Get-AzVirtualNetworkGateway -Name erGateway -ResourceGroupName virtualRouterRG
New-AzVirtualRouter -RouterName virtualRouter -ResourceGroupName virtualRouterRG -Location 'West US'  -HostedGateway $gateway
```

## <span data-ttu-id="f3ee4-112">변수</span><span class="sxs-lookup"><span data-stu-id="f3ee4-112">PARAMETERS</span></span>

### <span data-ttu-id="f3ee4-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f3ee4-113">-AsJob</span></span>
<span data-ttu-id="f3ee4-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f3ee4-114">Run cmdlet in the background</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3ee4-115">-DefaultProfile</span></span>
<span data-ttu-id="f3ee4-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3ee4-117">-Force</span><span class="sxs-lookup"><span data-stu-id="f3ee4-117">-Force</span></span>
<span data-ttu-id="f3ee4-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="f3ee4-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-119">-HostedGateway</span><span class="sxs-lookup"><span data-stu-id="f3ee4-119">-HostedGateway</span></span>
<span data-ttu-id="f3ee4-120">가상 라우터를 호스트 해야 하는 게이트웨이입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-120">The gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: PSVirtualNetworkGateway
Parameter Sets: HostedGatewayParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-121">-HostedGatewayId</span><span class="sxs-lookup"><span data-stu-id="f3ee4-121">-HostedGatewayId</span></span>
<span data-ttu-id="f3ee4-122">가상 라우터를 호스트 해야 하는 게이트웨이의 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-122">The id of gateway where Virtual Router needs to be hosted.</span></span>

```yaml
Type: String
Parameter Sets: HostedGatewayIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-123">-위치</span><span class="sxs-lookup"><span data-stu-id="f3ee4-123">-Location</span></span>
<span data-ttu-id="f3ee4-124">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-124">The location.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-125">-이름</span><span class="sxs-lookup"><span data-stu-id="f3ee4-125">-Name</span></span>
<span data-ttu-id="f3ee4-126">가상 라우터의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-126">The name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3ee4-127">-ResourceGroupName</span></span>
<span data-ttu-id="f3ee4-128">가상 라우터의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-128">The resource group name of the virtual router.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-129">태그</span><span class="sxs-lookup"><span data-stu-id="f3ee4-129">-Tag</span></span>
<span data-ttu-id="f3ee4-130">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-130">A hashtable which represents resource tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3ee4-131">-확인</span><span class="sxs-lookup"><span data-stu-id="f3ee4-131">-Confirm</span></span>
<span data-ttu-id="f3ee4-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3ee4-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3ee4-133">-WhatIf</span></span>
<span data-ttu-id="f3ee4-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3ee4-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3ee4-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3ee4-136">CommonParameters</span></span>
<span data-ttu-id="f3ee4-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f3ee4-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f3ee4-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3ee4-139">입력</span><span class="sxs-lookup"><span data-stu-id="f3ee4-139">INPUTS</span></span>

### <span data-ttu-id="f3ee4-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f3ee4-140">System.String</span></span>

### <span data-ttu-id="f3ee4-141">PSVirtualNetworkGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="f3ee4-141">Microsoft.Azure.Commands.Network.Models.PSVirtualNetworkGateway</span></span>

### <span data-ttu-id="f3ee4-142">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f3ee4-142">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f3ee4-143">출력</span><span class="sxs-lookup"><span data-stu-id="f3ee4-143">OUTPUTS</span></span>

### <span data-ttu-id="f3ee4-144">Microsoft. 네트워크 모델. PSVirtualRouter</span><span class="sxs-lookup"><span data-stu-id="f3ee4-144">Microsoft.Azure.Commands.Network.Models.PSVirtualRouter</span></span>

## <span data-ttu-id="f3ee4-145">상속자</span><span class="sxs-lookup"><span data-stu-id="f3ee4-145">NOTES</span></span>

## <span data-ttu-id="f3ee4-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3ee4-146">RELATED LINKS</span></span>
