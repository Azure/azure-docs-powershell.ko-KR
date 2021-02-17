---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzExpressRoutePort.md
ms.openlocfilehash: 54cdcbbd1d9564dde4fbe4a9aa0b0bea8a0325a3
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100206765"
---
# <span data-ttu-id="6ec7b-101">New-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ec7b-101">New-AzExpressRoutePort</span></span>

## <span data-ttu-id="6ec7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ec7b-102">SYNOPSIS</span></span>
<span data-ttu-id="6ec7b-103">Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-103">Creates an Azure ExpressRoutePort.</span></span>

## <span data-ttu-id="6ec7b-104">구문</span><span class="sxs-lookup"><span data-stu-id="6ec7b-104">SYNTAX</span></span>

### <span data-ttu-id="6ec7b-105">ResourceNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="6ec7b-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob] [-Identity <PSManagedServiceIdentity>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ec7b-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6ec7b-106">ResourceIdParameterSet</span></span>
```
New-AzExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>] [-Link <PSExpressRouteLink[]>] [-Force] [-AsJob]
 [-Identity <PSManagedServiceIdentity>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ec7b-107">설명</span><span class="sxs-lookup"><span data-stu-id="6ec7b-107">DESCRIPTION</span></span>
<span data-ttu-id="6ec7b-108">**New-AzExpressRoutePort** cmdlet은 Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-108">The **New-AzExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="6ec7b-109">예제</span><span class="sxs-lookup"><span data-stu-id="6ec7b-109">EXAMPLES</span></span>

### <span data-ttu-id="6ec7b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="6ec7b-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

### <span data-ttu-id="6ec7b-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="6ec7b-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzExpressRoutePort @parameters
```

## <span data-ttu-id="6ec7b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="6ec7b-112">PARAMETERS</span></span>

### <span data-ttu-id="6ec7b-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="6ec7b-113">-AsJob</span></span>
<span data-ttu-id="6ec7b-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="6ec7b-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="6ec7b-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="6ec7b-115">-BandwidthInGbps</span></span>
<span data-ttu-id="6ec7b-116">조달된 포트의 대역폭(Gbps)</span><span class="sxs-lookup"><span data-stu-id="6ec7b-116">Bandwidth of procured ports in Gbps</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ec7b-117">-DefaultProfile</span></span>
<span data-ttu-id="6ec7b-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ec7b-119">-캡슐화</span><span class="sxs-lookup"><span data-stu-id="6ec7b-119">-Encapsulation</span></span>
<span data-ttu-id="6ec7b-120">물리적 포트의 캡슐화 메서드입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="6ec7b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="6ec7b-121">-Force</span></span>
<span data-ttu-id="6ec7b-122">리소스를 덮어 사용하려는 경우 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="6ec7b-123">-Identity</span><span class="sxs-lookup"><span data-stu-id="6ec7b-123">-Identity</span></span>
<span data-ttu-id="6ec7b-124">MacSec 구성을 읽기 위한 사용자 할당 ID</span><span class="sxs-lookup"><span data-stu-id="6ec7b-124">User Assigned Identity for reading MacSec configuration</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSManagedServiceIdentity
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-125">-Link</span><span class="sxs-lookup"><span data-stu-id="6ec7b-125">-Link</span></span>
<span data-ttu-id="6ec7b-126">ExpressRoutePort 리소스의 물리적 링크 집합</span><span class="sxs-lookup"><span data-stu-id="6ec7b-126">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-127">-Location</span><span class="sxs-lookup"><span data-stu-id="6ec7b-127">-Location</span></span>
<span data-ttu-id="6ec7b-128">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-128">The location.</span></span>

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

### <span data-ttu-id="6ec7b-129">-Name</span><span class="sxs-lookup"><span data-stu-id="6ec7b-129">-Name</span></span>
<span data-ttu-id="6ec7b-130">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-130">The name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-131">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="6ec7b-131">-PeeringLocation</span></span>
<span data-ttu-id="6ec7b-132">ExpressRoutePort가 물리적으로 매핑된 피어링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-132">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="6ec7b-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ec7b-133">-ResourceGroupName</span></span>
<span data-ttu-id="6ec7b-134">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-134">The resource group name of the ExpressRoutePort.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-135">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="6ec7b-135">-ResourceId</span></span>
<span data-ttu-id="6ec7b-136">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-136">ResourceId of the express route port.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ec7b-137">-Tag</span><span class="sxs-lookup"><span data-stu-id="6ec7b-137">-Tag</span></span>
<span data-ttu-id="6ec7b-138">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-138">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="6ec7b-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="6ec7b-139">-Confirm</span></span>
<span data-ttu-id="6ec7b-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ec7b-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ec7b-141">-WhatIf</span></span>
<span data-ttu-id="6ec7b-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="6ec7b-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ec7b-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ec7b-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ec7b-144">CommonParameters</span></span>
<span data-ttu-id="6ec7b-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ec7b-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6ec7b-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ec7b-147">입력</span><span class="sxs-lookup"><span data-stu-id="6ec7b-147">INPUTS</span></span>

### <span data-ttu-id="6ec7b-148">System.String</span><span class="sxs-lookup"><span data-stu-id="6ec7b-148">System.String</span></span>

### <span data-ttu-id="6ec7b-149">System.Int32</span><span class="sxs-lookup"><span data-stu-id="6ec7b-149">System.Int32</span></span>

### <span data-ttu-id="6ec7b-150">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="6ec7b-150">System.Collections.Hashtable</span></span>

### <span data-ttu-id="6ec7b-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span><span class="sxs-lookup"><span data-stu-id="6ec7b-151">Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink[]</span></span>

## <span data-ttu-id="6ec7b-152">출력</span><span class="sxs-lookup"><span data-stu-id="6ec7b-152">OUTPUTS</span></span>

### <span data-ttu-id="6ec7b-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ec7b-153">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="6ec7b-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6ec7b-154">NOTES</span></span>

## <span data-ttu-id="6ec7b-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6ec7b-155">RELATED LINKS</span></span>

[<span data-ttu-id="6ec7b-156">Get-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ec7b-156">Get-AzExpressRoutePort</span></span>](./Get-AzExpressRoutePort.md)

[<span data-ttu-id="6ec7b-157">Remove-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ec7b-157">Remove-AzExpressRoutePort</span></span>](./Remove-AzExpressRoutePort.md)

[<span data-ttu-id="6ec7b-158">Set-AzExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="6ec7b-158">Set-AzExpressRoutePort</span></span>](./Set-AzExpressRoutePort.md)
