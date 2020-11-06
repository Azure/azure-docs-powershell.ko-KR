---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
ms.assetid: E40CAF2F-ED57-4AC1-8B9A-E48042DD8F91
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressroutecircuit
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRouteCircuit.md
ms.openlocfilehash: cee0318367ad764a9cc9e37995f092462cd157a5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530200"
---
# <span data-ttu-id="d994a-101">New-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d994a-101">New-AzureRmExpressRouteCircuit</span></span>

## <span data-ttu-id="d994a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d994a-102">SYNOPSIS</span></span>
<span data-ttu-id="d994a-103">Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-103">Creates an Azure express route circuit.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d994a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d994a-104">SYNTAX</span></span>

### <span data-ttu-id="d994a-105">ServiceProvider</span><span class="sxs-lookup"><span data-stu-id="d994a-105">ServiceProvider</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ServiceProviderName <String>] [-PeeringLocation <String>]
 [-BandwidthInMbps <Int32>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d994a-106">ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d994a-106">ExpressRoutePort</span></span>
```
New-AzureRmExpressRouteCircuit -Name <String> -ResourceGroupName <String> -Location <String>
 [-SkuTier <String>] [-SkuFamily <String>] [-ExpressRoutePort <PSExpressRoutePort>] [-BandwidthInGbps <Double>]
 [-Peering <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSPeering]>]
 [-Authorization <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization]>]
 [-AllowClassicOperations <Boolean>] [-Tag <Hashtable>] [-Force] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d994a-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d994a-107">DESCRIPTION</span></span>
<span data-ttu-id="d994a-108">**AzureRmExpressRouteCircuit** Cmdlet은 Azure express 경로 회로를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-108">The **New-AzureRmExpressRouteCircuit** cmdlet creates an Azure express route circuit.</span></span>

## <span data-ttu-id="d994a-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d994a-109">EXAMPLES</span></span>

### <span data-ttu-id="d994a-110">예제 1: 새 Express 경로 만들기</span><span class="sxs-lookup"><span data-stu-id="d994a-110">Example 1: Create a new ExpressRoute circuit</span></span>
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

### <span data-ttu-id="d994a-111">예제 2: ExpressRoutePort에서 새 Express 서킷 만들기</span><span class="sxs-lookup"><span data-stu-id="d994a-111">Example 2: Create a new ExpressRoute circuit on ExpressRoutePort</span></span>
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
New-AzureRmExpressRouteCircuit @parameters
```

## <span data-ttu-id="d994a-112">변수</span><span class="sxs-lookup"><span data-stu-id="d994a-112">PARAMETERS</span></span>

### <span data-ttu-id="d994a-113">-AllowClassicOperations</span><span class="sxs-lookup"><span data-stu-id="d994a-113">-AllowClassicOperations</span></span>
<span data-ttu-id="d994a-114">이 매개 변수를 사용 하면 기본 Azure PowerShell cmdlet을 사용 하 여 회로를 관리할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-114">The use of this parameter allows you to use the classic Azure PowerShell cmdlets to manage the circuit.</span></span>

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

### <span data-ttu-id="d994a-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="d994a-115">-AsJob</span></span>
<span data-ttu-id="d994a-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="d994a-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="d994a-117">-권한 부여</span><span class="sxs-lookup"><span data-stu-id="d994a-117">-Authorization</span></span>
<span data-ttu-id="d994a-118">회로 인증의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-118">A list of circuit authorizations.</span></span>

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

### <span data-ttu-id="d994a-119">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="d994a-119">-BandwidthInGbps</span></span>
<span data-ttu-id="d994a-120">회로가 ExpressRoutePort 리소스에서 프로 비전 될 때 회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-120">The bandwidth of the circuit when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: Double
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-121">-BandwidthInMbps</span><span class="sxs-lookup"><span data-stu-id="d994a-121">-BandwidthInMbps</span></span>
<span data-ttu-id="d994a-122">회로의 대역폭입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-122">The bandwidth of the circuit.</span></span> <span data-ttu-id="d994a-123">서비스 공급자가 지 원하는 값 이어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-123">This must be a value that is supported by the service provider.</span></span>

```yaml
Type: System.Int32
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d994a-124">-DefaultProfile</span></span>
<span data-ttu-id="d994a-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-126">-ExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="d994a-126">-ExpressRoutePort</span></span>
<span data-ttu-id="d994a-127">회로가 ExpressRoutePort 리소스에 프로 비전 될 때 ExpressRoutePort 리소스에 대 한 참조입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-127">The reference to the ExpressRoutePort resource when the circuit is provisioned on an ExpressRoutePort resource.</span></span>

```yaml
Type: PSExpressRoutePort
Parameter Sets: ExpressRoutePort
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-128">-Force</span><span class="sxs-lookup"><span data-stu-id="d994a-128">-Force</span></span>
<span data-ttu-id="d994a-129">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-129">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="d994a-130">-위치</span><span class="sxs-lookup"><span data-stu-id="d994a-130">-Location</span></span>
<span data-ttu-id="d994a-131">회로의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-131">The location of the circuit.</span></span>

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

### <span data-ttu-id="d994a-132">-이름</span><span class="sxs-lookup"><span data-stu-id="d994a-132">-Name</span></span>
<span data-ttu-id="d994a-133">만들고 있는 Express 경로 회로의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-133">The name of the ExpressRoute circuit being created.</span></span>

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

### <span data-ttu-id="d994a-134">-피어 링</span><span class="sxs-lookup"><span data-stu-id="d994a-134">-Peering</span></span>
<span data-ttu-id="d994a-135">목록 피어 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-135">A list peer configurations.</span></span>

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

### <span data-ttu-id="d994a-136">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="d994a-136">-PeeringLocation</span></span>
<span data-ttu-id="d994a-137">서비스 공급자가 지 원하는 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-137">The name of the peering location supported by the service provider.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-138">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d994a-138">-ResourceGroupName</span></span>
<span data-ttu-id="d994a-139">회로가 포함 될 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-139">The resource group that will contain the circuit.</span></span>

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

### <span data-ttu-id="d994a-140">-ServiceProviderName</span><span class="sxs-lookup"><span data-stu-id="d994a-140">-ServiceProviderName</span></span>
<span data-ttu-id="d994a-141">회로 서비스 공급자의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-141">The name of the circuit service provider.</span></span> <span data-ttu-id="d994a-142">이것은 Get-AzureRmExpressRouteServiceProvider cmdlet에 나열 된 이름과 일치 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-142">This must match a name listed by the Get-AzureRmExpressRouteServiceProvider cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: ServiceProvider
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-143">-용 U가족</span><span class="sxs-lookup"><span data-stu-id="d994a-143">-SkuFamily</span></span>
<span data-ttu-id="d994a-144">SKU 패밀리는 청구 유형을 결정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-144">SKU family determines the billing type.</span></span> <span data-ttu-id="d994a-145">이 매개 변수에 사용할 수 있는 값은 `MeteredData` or `UnlimitedData` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-145">Possible values for this parameter are: `MeteredData` or `UnlimitedData`.</span></span> <span data-ttu-id="d994a-146">MeteredData에서 UnlimitedData로 청구 유형을 변경할 수 있지만, UnlimitedData에서 MeteredData로 유형을 변경할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-146">Note that you can change the billing type from MeteredData to UnlimitedData, but you can't change the type from UnlimitedData to MeteredData.</span></span>

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

### <span data-ttu-id="d994a-147">-서 고 U계층</span><span class="sxs-lookup"><span data-stu-id="d994a-147">-SkuTier</span></span>
<span data-ttu-id="d994a-148">회로에 대 한 서비스 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-148">The tier of service for the circuit.</span></span> <span data-ttu-id="d994a-149">이 매개 변수에 사용할 수 있는 값은 `Standard` or `Premium` 입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-149">Possible values for this parameter are: `Standard` or `Premium`.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Standard, Premium

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d994a-150">태그</span><span class="sxs-lookup"><span data-stu-id="d994a-150">-Tag</span></span>
<span data-ttu-id="d994a-151">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-151">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="d994a-152">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="d994a-152">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="d994a-153">-확인</span><span class="sxs-lookup"><span data-stu-id="d994a-153">-Confirm</span></span>
<span data-ttu-id="d994a-154">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-154">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d994a-155">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d994a-155">-WhatIf</span></span>
<span data-ttu-id="d994a-156">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-156">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d994a-157">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-157">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d994a-158">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d994a-158">CommonParameters</span></span>
<span data-ttu-id="d994a-159">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d994a-159">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d994a-160">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d994a-160">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d994a-161">입력</span><span class="sxs-lookup"><span data-stu-id="d994a-161">INPUTS</span></span>

### <span data-ttu-id="d994a-162">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d994a-162">System.String</span></span>

### <span data-ttu-id="d994a-163">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="d994a-163">System.Int32</span></span>

### <span data-ttu-id="d994a-164">System.webserver. List ' 1 [[PSPeering, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d994a-164">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSPeering, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d994a-165">System.webserver. List ' 1 [[PSExpressRouteCircuitAuthorization, Microsoft azure. 6.4.1.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="d994a-165">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuitAuthorization, Microsoft.Azure.Commands.Network, Version=6.4.1.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="d994a-166">시스템 Null 허용 ' 1 [[b77a5c561934e089] [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="d994a-166">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d994a-167">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d994a-167">System.Collections.Hashtable</span></span>

## <span data-ttu-id="d994a-168">출력</span><span class="sxs-lookup"><span data-stu-id="d994a-168">OUTPUTS</span></span>

### <span data-ttu-id="d994a-169">PSExpressRouteCircuit에 대 한.</span><span class="sxs-lookup"><span data-stu-id="d994a-169">Microsoft.Azure.Commands.Network.Models.PSExpressRouteCircuit</span></span>

## <span data-ttu-id="d994a-170">상속자</span><span class="sxs-lookup"><span data-stu-id="d994a-170">NOTES</span></span>

## <span data-ttu-id="d994a-171">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d994a-171">RELATED LINKS</span></span>

[<span data-ttu-id="d994a-172">Get-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d994a-172">Get-AzureRmExpressRouteCircuit</span></span>](Get-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d994a-173">이동-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d994a-173">Move-AzureRmExpressRouteCircuit</span></span>](Move-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d994a-174">제거-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d994a-174">Remove-AzureRmExpressRouteCircuit</span></span>](Remove-AzureRmExpressRouteCircuit.md)

[<span data-ttu-id="d994a-175">Set-AzureRmExpressRouteCircuit</span><span class="sxs-lookup"><span data-stu-id="d994a-175">Set-AzureRmExpressRouteCircuit</span></span>](Set-AzureRmExpressRouteCircuit.md)
