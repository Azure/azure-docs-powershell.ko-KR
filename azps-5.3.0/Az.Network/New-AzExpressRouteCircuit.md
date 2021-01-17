---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 479b89296ae52221f714992791ed73cd14bf2fe0
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98379205"
---
# <span data-ttu-id="88ae9-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="88ae9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="88ae9-102">SYNOPSIS</span></span>
<span data-ttu-id="88ae9-103">Azure Express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="88ae9-104">구문</span><span class="sxs-lookup"><span data-stu-id="88ae9-104">SYNTAX</span></span>

### <span data-ttu-id="88ae9-105">ServiceProvider(기본값)</span><span class="sxs-lookup"><span data-stu-id="88ae9-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="88ae9-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ae9-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="88ae9-107">설명</span><span class="sxs-lookup"><span data-stu-id="88ae9-107">DESCRIPTION</span></span>
<span data-ttu-id="88ae9-108">**New-AzExpressRouteCircuit** cmdlet은 Azure Express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="88ae9-109">예제</span><span class="sxs-lookup"><span data-stu-id="88ae9-109">EXAMPLES</span></span>

### <span data-ttu-id="88ae9-110">예제 1: 새 ExpressRoute 회로 만들기</span><span class="sxs-lookup"><span data-stu-id="88ae9-110">Example 1: Create a new ExpressRoute circuit</span></span>
```powershell
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

### <span data-ttu-id="88ae9-111">예제 2: ExpressRoutePort에서 새 ExpressRoute 회로 만들기</span><span class="sxs-lookup"><span data-stu-id="88ae9-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```powershell
$parameters = @{
    Name='ExpressRouteCircuit'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    SkuTier='Standard'
    SkuFamily='MeteredData'
    ExpressRoutePort=$PSExpressRoutePort
    BandwidthInGbps=10.0
}
New-AzExpressRouteCircuit @parameters
```

## <span data-ttu-id="88ae9-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="88ae9-112">PARAMETERS</span></span>

### <span data-ttu-id="88ae9-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="88ae9-113">-AllowClassicOperations</span></span>
<span data-ttu-id="88ae9-114">이 매개 변수를 사용하면 클래식 Azure PowerShell cmdlet을 사용하여 회로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="88ae9-115">-AsJob</span></span>
<span data-ttu-id="88ae9-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="88ae9-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="88ae9-117">-Authorization</span><span class="sxs-lookup"><span data-stu-id="88ae9-117">-Authorization</span></span>
<span data-ttu-id="88ae9-118">회로 권한 부여 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-118">A list of circuit authorizations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="88ae9-119">-BandwidthInGbps</span></span>
<span data-ttu-id="88ae9-120">회로가 ExpressRoutePort 리소스에 프로비전될 때 회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: System.Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="88ae9-121">-BandwidthInMbps</span></span>
<span data-ttu-id="88ae9-122">회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="88ae9-123">서비스 공급자가 지원하는 값입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="88ae9-124">-DefaultProfile</span></span>
<span data-ttu-id="88ae9-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="88ae9-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ae9-126">-ExpressRoutePort</span></span>
<span data-ttu-id="88ae9-127">회로가 ExpressRoutePort 리소스에 프로비전될 때 ExpressRoutePort 리소스에 대한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-128">-Force</span><span class="sxs-lookup"><span data-stu-id="88ae9-128">-Force</span></span>
<span data-ttu-id="88ae9-129">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="88ae9-130">-Location</span><span class="sxs-lookup"><span data-stu-id="88ae9-130">-Location</span></span>
<span data-ttu-id="88ae9-131">회로의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-131">The location of the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-132">-Name</span><span class="sxs-lookup"><span data-stu-id="88ae9-132">-Name</span></span>
<span data-ttu-id="88ae9-133">생성되는 ExpressRoute 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-133">The name of the ExpressRoute circuit being created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-134">-피어링</span><span class="sxs-lookup"><span data-stu-id="88ae9-134">-Peering</span></span>
<span data-ttu-id="88ae9-135">목록 피어 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-135">A list peer configurations.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPeering[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="88ae9-136">-PeeringLocation</span></span>
<span data-ttu-id="88ae9-137">서비스 공급자가 지원하는 피어링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="88ae9-138">-ResourceGroupName</span></span>
<span data-ttu-id="88ae9-139">회로를 포함할 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-139">The resource group that will contain the circuit.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="88ae9-140">-ServiceProviderName</span></span>
<span data-ttu-id="88ae9-141">회로 서비스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-141">The name of the circuit service provider.</span></span> <span data-ttu-id="88ae9-142">이 이름은 Get-AzExpressRouteServiceProvider cmdlet에 나열된 이름과 일치해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-143">-SkuFamily</span><span class="sxs-lookup"><span data-stu-id="88ae9-143">-SkuFamily</span></span>
<span data-ttu-id="88ae9-144">SKU 패밀리는 청구 유형을 결정합니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-144">SKU family determines the billing type.</span></span> <span data-ttu-id="88ae9-145">이 매개 변수에 사용할 수 있는 값은 `MeteredData` `UnlimitedData`</span><span class="sxs-lookup"><span data-stu-id="88ae9-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="88ae9-146">청구 유형을 MeteredData에서 UnlimitedData로 변경할 수 있지만 UnlimitedData에서 MeteredData로는 변경할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: MeteredData, UnlimitedData

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-147">-SkuTier</span><span class="sxs-lookup"><span data-stu-id="88ae9-147">-SkuTier</span></span>
<span data-ttu-id="88ae9-148">회로에 대한 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-148">The tier of service for the circuit.</span></span> <span data-ttu-id="88ae9-149">이 매개 변수에 사용할 수 있는 값은 `Standard` `Premium` `Local`</span><span class="sxs-lookup"><span data-stu-id="88ae9-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium, Local

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-150">-Tag</span><span class="sxs-lookup"><span data-stu-id="88ae9-150">-Tag</span></span>
<span data-ttu-id="88ae9-151">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="88ae9-152">예: @{key0="value0";key1=$null;key2="value2"}</span><span class="sxs-lookup"><span data-stu-id="88ae9-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-153">-Confirm</span><span class="sxs-lookup"><span data-stu-id="88ae9-153">-Confirm</span></span>
<span data-ttu-id="88ae9-154">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-154">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="88ae9-155">-WhatIf</span></span>
<span data-ttu-id="88ae9-156">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="88ae9-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="88ae9-157">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-157">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="88ae9-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="88ae9-158">CommonParameters</span></span>
<span data-ttu-id="88ae9-159">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="88ae9-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="88ae9-160">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="88ae9-160">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="88ae9-161">입력</span><span class="sxs-lookup"><span data-stu-id="88ae9-161">INPUTS</span></span>

### <span data-ttu-id="88ae9-162">System.String</span><span class="sxs-lookup"><span data-stu-id="88ae9-162">System.String</span></span>

### <span data-ttu-id="88ae9-163">System.Int32</span><span class="sxs-lookup"><span data-stu-id="88ae9-163">System.Int32</span></span>

### <span data-ttu-id="88ae9-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="88ae9-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="88ae9-165">System.Double</span><span class="sxs-lookup"><span data-stu-id="88ae9-165">System.Double</span></span>

### <span data-ttu-id="88ae9-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span><span class="sxs-lookup"><span data-stu-id="88ae9-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="88ae9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span><span class="sxs-lookup"><span data-stu-id="88ae9-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="88ae9-168">System.Nullable'1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="88ae9-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="88ae9-169">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="88ae9-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="88ae9-170">출력</span><span class="sxs-lookup"><span data-stu-id="88ae9-170">OUTPUTS</span></span>

### <span data-ttu-id="88ae9-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="88ae9-172">참고 사항</span><span class="sxs-lookup"><span data-stu-id="88ae9-172">NOTES</span></span>

## <span data-ttu-id="88ae9-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="88ae9-173">RELATED LINKS</span></span>

[<span data-ttu-id="88ae9-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="88ae9-175">Move-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="88ae9-176">Remove-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="88ae9-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="88ae9-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
