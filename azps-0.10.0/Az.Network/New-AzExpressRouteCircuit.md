---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: d03b52c477686f3aa724057771285eaf9d522a56
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93875444"
---
# <span data-ttu-id="3a725-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a725-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="3a725-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a725-102">SYNOPSIS</span></span>
<span data-ttu-id="3a725-103">Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3a725-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a725-104">SYNTAX</span></span>

```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a725-105">설명은</span><span class="sxs-lookup"><span data-stu-id="3a725-105">DESCRIPTION</span></span>
<span data-ttu-id="3a725-106">**AzExpressRouteCircuit** Cmdlet은 Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-106">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="3a725-107">예제의</span><span class="sxs-lookup"><span data-stu-id="3a725-107">EXAMPLES</span></span>

### <span data-ttu-id="3a725-108">예제 1: 새 Express 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="3a725-108">Example 1: Create a new ExpressRoute circuit</span></span>
```
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ServiceProviderName='Equinix'
    PeeringLocation='Silicon Valley'
    BandwidthInMbps=200
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="3a725-109">변수</span><span class="sxs-lookup"><span data-stu-id="3a725-109">PARAMETERS</span></span>

### <span data-ttu-id="3a725-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="3a725-110">-AllowClassicOperations</span></span>
<span data-ttu-id="3a725-111">이 매개 변수를 사용 하면 기본 Azure PowerShell cmdlet을 사용 하 여 회로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a725-112">-AsJob</span></span>
<span data-ttu-id="3a725-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3a725-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a725-114">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="3a725-114">-Authorization</span></span>
<span data-ttu-id="3a725-115">회로 인증의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-115">A list of circuit authorizations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="3a725-116">-BandwidthInMbps</span></span>
<span data-ttu-id="3a725-117">회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="3a725-118">서비스 공급자가 지 원하는 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-118">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a725-119">-DefaultProfile</span></span>
<span data-ttu-id="3a725-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-121">-Force</span><span class="sxs-lookup"><span data-stu-id="3a725-121">-Force</span></span>
<span data-ttu-id="3a725-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="3a725-123">-위치</span><span class="sxs-lookup"><span data-stu-id="3a725-123">-Location</span></span>
<span data-ttu-id="3a725-124">회로의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="3a725-125">-이름</span><span class="sxs-lookup"><span data-stu-id="3a725-125">-Name</span></span>
<span data-ttu-id="3a725-126">만들고 있는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="3a725-127">-피어 링</span><span class="sxs-lookup"><span data-stu-id="3a725-127">-Peering</span></span>
<span data-ttu-id="3a725-128">목록 피어 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-128">A list peer configurations.</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="3a725-129">-PeeringLocation</span></span>
<span data-ttu-id="3a725-130">서비스 공급자가 지 원하는 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="3a725-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="3a725-131">-ResourceGroupName</span></span>
<span data-ttu-id="3a725-132">회로가 포함 될 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="3a725-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="3a725-133">-ServiceProviderName</span></span>
<span data-ttu-id="3a725-134">회로 서비스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-134">The name of the circuit service provider.</span></span> <span data-ttu-id="3a725-135">이것은 Get-AzExpressRouteServiceProvider cmdlet에 나열 된 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-135">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="3a725-136">-용 U가족</span><span class="sxs-lookup"><span data-stu-id="3a725-136">-SkuFamily</span></span>
<span data-ttu-id="3a725-137">SKU 패밀리는 청구 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-137">SKU family determines the billing type.</span></span> <span data-ttu-id="3a725-138">이 매개 변수에 사용할 수 있는 값은 `MeteredData` or `UnlimitedData` 입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="3a725-139">MeteredData에서 UnlimitedData로 청구 유형을 변경할 수 있지만, UnlimitedData에서 MeteredData로 유형을 변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-140">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="3a725-140">-SkuTier</span></span>
<span data-ttu-id="3a725-141">회로에 대 한 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-141">The tier of service for the circuit.</span></span> <span data-ttu-id="3a725-142">이 매개 변수에 사용할 수 있는 값은 `Standard` or `Premium` 입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-143">태그</span><span class="sxs-lookup"><span data-stu-id="3a725-143">-Tag</span></span>
<span data-ttu-id="3a725-144">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="3a725-145">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="3a725-145">For example:</span></span>

<span data-ttu-id="3a725-146">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="3a725-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="3a725-147">-확인</span><span class="sxs-lookup"><span data-stu-id="3a725-147">-Confirm</span></span>
<span data-ttu-id="3a725-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-148">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a725-149">-WhatIf</span></span>
<span data-ttu-id="3a725-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a725-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-151">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3a725-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a725-152">CommonParameters</span></span>
<span data-ttu-id="3a725-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a725-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a725-154">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3a725-154">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a725-155">입력</span><span class="sxs-lookup"><span data-stu-id="3a725-155">INPUTS</span></span>

## <span data-ttu-id="3a725-156">출력</span><span class="sxs-lookup"><span data-stu-id="3a725-156">OUTPUTS</span></span>

### <span data-ttu-id="3a725-157">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="3a725-157">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="3a725-158">상속자</span><span class="sxs-lookup"><span data-stu-id="3a725-158">NOTES</span></span>

## <span data-ttu-id="3a725-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a725-159">RELATED LINKS</span></span>

[<span data-ttu-id="3a725-160">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a725-160">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="3a725-161">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a725-161">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="3a725-162">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a725-162">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="3a725-163">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="3a725-163">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
