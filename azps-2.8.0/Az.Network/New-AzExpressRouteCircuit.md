---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRouteCircuit.md
ms.openlocfilehash: 45e9d14f9761e5072f6c391c9439d2245d53f3ca
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93869969"
---
# <span data-ttu-id="07741-101">New-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07741-101">New-AzExpressRouteCircuit</span></span>

## <span data-ttu-id="07741-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="07741-102">SYNOPSIS</span></span>
<span data-ttu-id="07741-103">Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07741-103">Creates an Azure express route circuit.</span></span>

## <span data-ttu-id="07741-104">구문과</span><span class="sxs-lookup"><span data-stu-id="07741-104">SYNTAX</span></span>

### <span data-ttu-id="07741-105">ServiceProvider (기본값)</span><span class="sxs-lookup"><span data-stu-id="07741-105">ServiceProvider (Default)</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ServiceProviderName <String> -PeeringLocation <String> -BandwidthInMbps <Int32>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="07741-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="07741-106">ExpressRoutePort</span></span>
```
New-AzExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String> [-SkuTier <String>]
 [-SkuFamily <String>] -ExpressRoutePort <PSExpressRoutePort> -BandwidthInGbps <Double>
 [-Peering <PSPeering[]>] [-Authorization <PSExpressRouteCircuitAuthorization[]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="07741-107">설명은</span><span class="sxs-lookup"><span data-stu-id="07741-107">DESCRIPTION</span></span>
<span data-ttu-id="07741-108">**AzExpressRouteCircuit** Cmdlet은 Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="07741-108">The **New-AzExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="07741-109">예제의</span><span class="sxs-lookup"><span data-stu-id="07741-109">EXAMPLES</span></span>

### <span data-ttu-id="07741-110">예제 1: 새 Express 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="07741-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="07741-111">예제 2: ExpressRoutePort에서 새 Express 서킷 만들기</span><span class="sxs-lookup"><span data-stu-id="07741-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
```
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

## <span data-ttu-id="07741-112">변수</span><span class="sxs-lookup"><span data-stu-id="07741-112">PARAMETERS</span></span>

### <span data-ttu-id="07741-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="07741-113">-AllowClassicOperations</span></span>
<span data-ttu-id="07741-114">이 매개 변수를 사용 하면 기본 Azure PowerShell cmdlet을 사용 하 여 회로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="07741-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="07741-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="07741-115">-AsJob</span></span>
<span data-ttu-id="07741-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="07741-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="07741-117">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="07741-117">-Authorization</span></span>
<span data-ttu-id="07741-118">회로 인증의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="07741-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="07741-119">-BandwidthInGbps</span></span>
<span data-ttu-id="07741-120">회로가 ExpressRoutePort 리소스에서 프로 비전 될 때 회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="07741-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="07741-121">-BandwidthInMbps</span></span>
<span data-ttu-id="07741-122">회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="07741-123">서비스 공급자가 지 원하는 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-123">This must be a value that is supported by the service provider.</span></span>

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

### <span data-ttu-id="07741-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="07741-124">-DefaultProfile</span></span>
<span data-ttu-id="07741-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="07741-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="07741-126">-ExpressRoutePort</span></span>
<span data-ttu-id="07741-127">회로가 ExpressRoutePort 리소스에 프로 비전 될 때 ExpressRoutePort 리소스에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

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

### <span data-ttu-id="07741-128">-Force</span><span class="sxs-lookup"><span data-stu-id="07741-128">-Force</span></span>
<span data-ttu-id="07741-129">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="07741-130">-위치</span><span class="sxs-lookup"><span data-stu-id="07741-130">-Location</span></span>
<span data-ttu-id="07741-131">회로의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="07741-132">-이름</span><span class="sxs-lookup"><span data-stu-id="07741-132">-Name</span></span>
<span data-ttu-id="07741-133">만들고 있는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="07741-134">-피어 링</span><span class="sxs-lookup"><span data-stu-id="07741-134">-Peering</span></span>
<span data-ttu-id="07741-135">목록 피어 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="07741-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="07741-136">-PeeringLocation</span></span>
<span data-ttu-id="07741-137">서비스 공급자가 지 원하는 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-137">The name of the peering location supported by the service provider.</span></span>

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

### <span data-ttu-id="07741-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="07741-138">-ResourceGroupName</span></span>
<span data-ttu-id="07741-139">회로가 포함 될 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="07741-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="07741-140">-ServiceProviderName</span></span>
<span data-ttu-id="07741-141">회로 서비스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-141">The name of the circuit service provider.</span></span> <span data-ttu-id="07741-142">이것은 Get-AzExpressRouteServiceProvider cmdlet에 나열 된 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-142">This must match a name listed by the Get-AzExpressRouteServiceProvider cmdlet.</span></span>

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

### <span data-ttu-id="07741-143">-용 U가족</span><span class="sxs-lookup"><span data-stu-id="07741-143">-SkuFamily</span></span>
<span data-ttu-id="07741-144">SKU 패밀리는 청구 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-144">SKU family determines the billing type.</span></span> <span data-ttu-id="07741-145">이 매개 변수에 사용할 수 있는 값은 `MeteredData` or `UnlimitedData` 입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="07741-146">MeteredData에서 UnlimitedData로 청구 유형을 변경할 수 있지만, UnlimitedData에서 MeteredData로 유형을 변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="07741-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="07741-147">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="07741-147">-SkuTier</span></span>
<span data-ttu-id="07741-148">회로에 대 한 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-148">The tier of service for the circuit.</span></span> <span data-ttu-id="07741-149">이 매개 변수에 사용할 수 있는 값 `Standard` 은 다음과 같습니다. `Premium` `Local`</span><span class="sxs-lookup"><span data-stu-id="07741-149">Possible values for this parameter are: `Standard`, `Premium` or `Local`.</span></span>

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

### <span data-ttu-id="07741-150">태그</span><span class="sxs-lookup"><span data-stu-id="07741-150">-Tag</span></span>
<span data-ttu-id="07741-151">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="07741-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="07741-152">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="07741-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="07741-153">-확인</span><span class="sxs-lookup"><span data-stu-id="07741-153">-Confirm</span></span>
<span data-ttu-id="07741-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="07741-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="07741-155">-WhatIf</span></span>
<span data-ttu-id="07741-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="07741-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="07741-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="07741-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="07741-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="07741-158">CommonParameters</span></span>
<span data-ttu-id="07741-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="07741-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="07741-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="07741-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="07741-161">입력</span><span class="sxs-lookup"><span data-stu-id="07741-161">INPUTS</span></span>

### <span data-ttu-id="07741-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="07741-162">System.String</span></span>

### <span data-ttu-id="07741-163">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="07741-163">System.Int32</span></span>

### <span data-ttu-id="07741-164">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07741-164">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

### <span data-ttu-id="07741-165">System. 2</span><span class="sxs-lookup"><span data-stu-id="07741-165">System.Double</span></span>

### <span data-ttu-id="07741-166">PSPeering [] (으)로</span><span class="sxs-lookup"><span data-stu-id="07741-166">Microsoft.Azure.Commands.Network.Models.PSPeering[]</span></span>

### <span data-ttu-id="07741-167">PSExpressRouteCircuitAuthorization [] (으)로</span><span class="sxs-lookup"><span data-stu-id="07741-167">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization[]</span></span>

### <span data-ttu-id="07741-168">시스템 Null 허용 ' 1 [[CoreLib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="07741-168">System.Nullable\`1[[System.Boolean, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="07741-169">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="07741-169">System.Collections.Hashtable</span></span>

## <span data-ttu-id="07741-170">출력</span><span class="sxs-lookup"><span data-stu-id="07741-170">OUTPUTS</span></span>

### <span data-ttu-id="07741-171">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="07741-171">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="07741-172">상속자</span><span class="sxs-lookup"><span data-stu-id="07741-172">NOTES</span></span>

## <span data-ttu-id="07741-173">관련 링크</span><span class="sxs-lookup"><span data-stu-id="07741-173">RELATED LINKS</span></span>

[<span data-ttu-id="07741-174">Get-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07741-174">Get-AzExpressRouteCircuit</span></span>](Get-AzExpressRouteCircuit.md)

[<span data-ttu-id="07741-175">이동-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07741-175">Move-AzExpressRouteCircuit</span></span>](Move-AzExpressRouteCircuit.md)

[<span data-ttu-id="07741-176">제거-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07741-176">Remove-AzExpressRouteCircuit</span></span>](Remove-AzExpressRouteCircuit.md)

[<span data-ttu-id="07741-177">Set-AzExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="07741-177">Set-AzExpressRouteCircuit</span></span>](Set-AzExpressRouteCircuit.md)
