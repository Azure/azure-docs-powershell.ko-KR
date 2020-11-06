---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: 0c611edc0ef8cb117e556a19e22f93d1f8db96ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532119"
---
# <span data-ttu-id="9c91b-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c91b-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="9c91b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c91b-102">SYNOPSIS</span></span>
<span data-ttu-id="9c91b-103">Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c91b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9c91b-104">SYNTAX</span></span>

```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String>
 -BandwidthInMbps <Int32>
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c91b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9c91b-105">DESCRIPTION</span></span>
<span data-ttu-id="9c91b-106">**AzureRmExpressRouteCircuit** Cmdlet은 Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-106">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="9c91b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9c91b-107">EXAMPLES</span></span>

### <span data-ttu-id="9c91b-108">예제 1: 새 Express 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="9c91b-108">Example 1: Create a new ExpressRoute circuit</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="9c91b-109">변수</span><span class="sxs-lookup"><span data-stu-id="9c91b-109">PARAMETERS</span></span>

### <span data-ttu-id="9c91b-110">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="9c91b-110">-AllowClassicOperations</span></span>
<span data-ttu-id="9c91b-111">이 매개 변수를 사용 하면 기본 Azure PowerShell cmdlet을 사용 하 여 회로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-111">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="9c91b-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9c91b-112">-AsJob</span></span>
<span data-ttu-id="9c91b-113">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9c91b-113">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9c91b-114">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="9c91b-114">-Authorization</span></span>
<span data-ttu-id="9c91b-115">회로 인증의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-115">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="9c91b-116">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="9c91b-116">-BandwidthInMbps</span></span>
<span data-ttu-id="9c91b-117">회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-117">The bandwidth of the circuit.</span></span> <span data-ttu-id="9c91b-118">서비스 공급자가 지 원하는 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-118">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="9c91b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c91b-119">-DefaultProfile</span></span>
<span data-ttu-id="9c91b-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c91b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="9c91b-121">-Force</span></span>
<span data-ttu-id="9c91b-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="9c91b-123">-위치</span><span class="sxs-lookup"><span data-stu-id="9c91b-123">-Location</span></span>
<span data-ttu-id="9c91b-124">회로의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-124">The location of the circuit.</span></span>

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

### <span data-ttu-id="9c91b-125">-이름</span><span class="sxs-lookup"><span data-stu-id="9c91b-125">-Name</span></span>
<span data-ttu-id="9c91b-126">만들고 있는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-126">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="9c91b-127">-피어 링</span><span class="sxs-lookup"><span data-stu-id="9c91b-127">-Peering</span></span>
<span data-ttu-id="9c91b-128">목록 피어 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-128">A list peer configurations.</span></span>

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

### <span data-ttu-id="9c91b-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="9c91b-129">-PeeringLocation</span></span>
<span data-ttu-id="9c91b-130">서비스 공급자가 지 원하는 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-130">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="9c91b-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9c91b-131">-ResourceGroupName</span></span>
<span data-ttu-id="9c91b-132">회로가 포함 될 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-132">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="9c91b-133">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="9c91b-133">-ServiceProviderName</span></span>
<span data-ttu-id="9c91b-134">회로 서비스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-134">The name of the circuit service provider.</span></span> <span data-ttu-id="9c91b-135">이것은 Get-AzureRmExpressRouteServiceProvider cmdlet에 나열 된 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-135">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="9c91b-136">-용 U가족</span><span class="sxs-lookup"><span data-stu-id="9c91b-136">-SkuFamily</span></span>
<span data-ttu-id="9c91b-137">SKU 패밀리는 청구 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-137">SKU family determines the billing type.</span></span> <span data-ttu-id="9c91b-138">이 매개 변수에 사용할 수 있는 값은 `MeteredData` or `UnlimitedData` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-138">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="9c91b-139">MeteredData에서 UnlimitedData로 청구 유형을 변경할 수 있지만, UnlimitedData에서 MeteredData로 유형을 변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-139">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="9c91b-140">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="9c91b-140">-SkuTier</span></span>
<span data-ttu-id="9c91b-141">회로에 대 한 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-141">The tier of service for the circuit.</span></span> <span data-ttu-id="9c91b-142">이 매개 변수에 사용할 수 있는 값은 `Standard` or `Premium` 입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-142">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

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

### <span data-ttu-id="9c91b-143">태그</span><span class="sxs-lookup"><span data-stu-id="9c91b-143">-Tag</span></span>
<span data-ttu-id="9c91b-144">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-144">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="9c91b-145">예를 들어:</span><span class="sxs-lookup"><span data-stu-id="9c91b-145">For example:</span></span>

<span data-ttu-id="9c91b-146">@ {key0 = "value0", key1 = $null, key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="9c91b-146">@{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="9c91b-147">-확인</span><span class="sxs-lookup"><span data-stu-id="9c91b-147">-Confirm</span></span>
<span data-ttu-id="9c91b-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c91b-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c91b-149">-WhatIf</span></span>
<span data-ttu-id="9c91b-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9c91b-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c91b-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c91b-152">CommonParameters</span></span>
<span data-ttu-id="9c91b-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c91b-154">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c91b-154">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c91b-155">입력</span><span class="sxs-lookup"><span data-stu-id="9c91b-155">INPUTS</span></span>

### <span data-ttu-id="9c91b-156">않아야</span><span class="sxs-lookup"><span data-stu-id="9c91b-156">None</span></span>
<span data-ttu-id="9c91b-157">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9c91b-157">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9c91b-158">출력</span><span class="sxs-lookup"><span data-stu-id="9c91b-158">OUTPUTS</span></span>

### <span data-ttu-id="9c91b-159">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="9c91b-159">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="9c91b-160">상속자</span><span class="sxs-lookup"><span data-stu-id="9c91b-160">NOTES</span></span>

## <span data-ttu-id="9c91b-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9c91b-161">RELATED LINKS</span></span>

[<span data-ttu-id="9c91b-162">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c91b-162">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9c91b-163">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c91b-163">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9c91b-164">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c91b-164">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="9c91b-165">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="9c91b-165">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
