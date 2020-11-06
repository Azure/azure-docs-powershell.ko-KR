---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/new-azurermexpressrouteport
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/New-AzureRmExpressRoutePort.md
ms.openlocfilehash: 8d3b204815fc273f97a549582a193002f5f4a48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529505"
---
# <span data-ttu-id="dc7ee-101">New-AzureRmExpressRoutePort</span><span class="sxs-lookup"><span data-stu-id="dc7ee-101">New-AzureRmExpressRoutePort</span></span>

## <span data-ttu-id="dc7ee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc7ee-102">SYNOPSIS</span></span>
<span data-ttu-id="dc7ee-103">Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-103">Creates an Azure ExpressRoutePort.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dc7ee-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dc7ee-104">SYNTAX</span></span>

### <span data-ttu-id="dc7ee-105">ResourceNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="dc7ee-105">ResourceNameParameterSet (Default)</span></span>
```
New-AzureRmExpressRoutePort -ResourceGroupName <String> -Name <String> -PeeringLocation <String>
 -BandwidthInGbps <Int32> -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="dc7ee-106">ResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc7ee-106">ResourceIdParameterSet</span></span>
```
New-AzureRmExpressRoutePort -ResourceId <String> -PeeringLocation <String> -BandwidthInGbps <Int32>
 -Encapsulation <String> -Location <String> [-Tag <Hashtable>]
 [-Link <System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="dc7ee-107">설명은</span><span class="sxs-lookup"><span data-stu-id="dc7ee-107">DESCRIPTION</span></span>
<span data-ttu-id="dc7ee-108">**AzureRmExpressRoutePort** Cmdlet은 Azure ExpressRoutePort를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-108">The **New-AzureRmExpressRoutePort** cmdlet creates an Azure ExpressRoutePort</span></span>

## <span data-ttu-id="dc7ee-109">예제의</span><span class="sxs-lookup"><span data-stu-id="dc7ee-109">EXAMPLES</span></span>

### <span data-ttu-id="dc7ee-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="dc7ee-110">Example 1</span></span>
```powershell
PS C:\> $parameters = @{
    Name='ExpressRoutePort'
    ResourceGroupName='ExpressRouteResourceGroup'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

### <span data-ttu-id="dc7ee-111">예제 2</span><span class="sxs-lookup"><span data-stu-id="dc7ee-111">Example 2</span></span>
```powershell
PS C:\> $parameters = @{
    ResourceId='/subscriptions/<SubId>/resourceGroups/<ResourceGroupName>/providers/Microsoft.Network/expressRoutePorts/<PortName>'
    Location='West US'
    PeeringLocation='Silicon Valley'
    BandwidthInGbps=100
    Encapsulation='QinQ'
}
PS C:\> New-AzureRmExpressRoutePort @parameters
```

## <span data-ttu-id="dc7ee-112">변수</span><span class="sxs-lookup"><span data-stu-id="dc7ee-112">PARAMETERS</span></span>

### <span data-ttu-id="dc7ee-113">-AsJob</span><span class="sxs-lookup"><span data-stu-id="dc7ee-113">-AsJob</span></span>
<span data-ttu-id="dc7ee-114">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="dc7ee-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="dc7ee-115">-BandwidthInGbps</span><span class="sxs-lookup"><span data-stu-id="dc7ee-115">-BandwidthInGbps</span></span>
<span data-ttu-id="dc7ee-116">Gbps의 확보 포트 대역폭</span><span class="sxs-lookup"><span data-stu-id="dc7ee-116">Bandwidth of procured ports in Gbps</span></span>

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

### <span data-ttu-id="dc7ee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc7ee-117">-DefaultProfile</span></span>
<span data-ttu-id="dc7ee-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc7ee-119">-캡슐화</span><span class="sxs-lookup"><span data-stu-id="dc7ee-119">-Encapsulation</span></span>
<span data-ttu-id="dc7ee-120">실제 포트의 캡슐화 방법</span><span class="sxs-lookup"><span data-stu-id="dc7ee-120">Encapsulation method on physical ports.</span></span>

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

### <span data-ttu-id="dc7ee-121">-Force</span><span class="sxs-lookup"><span data-stu-id="dc7ee-121">-Force</span></span>
<span data-ttu-id="dc7ee-122">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="dc7ee-122">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="dc7ee-123">-링크</span><span class="sxs-lookup"><span data-stu-id="dc7ee-123">-Link</span></span>
<span data-ttu-id="dc7ee-124">ExpressRoutePort 리소스의 실제 링크 집합</span><span class="sxs-lookup"><span data-stu-id="dc7ee-124">The set of physical links of the ExpressRoutePort resource</span></span>

```yaml
Type: System.Collections.Generic.List`1[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc7ee-125">-위치</span><span class="sxs-lookup"><span data-stu-id="dc7ee-125">-Location</span></span>
<span data-ttu-id="dc7ee-126">위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-126">The location.</span></span>

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

### <span data-ttu-id="dc7ee-127">-이름</span><span class="sxs-lookup"><span data-stu-id="dc7ee-127">-Name</span></span>
<span data-ttu-id="dc7ee-128">ExpressRoutePort의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-128">The name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="dc7ee-129">-PeeringLocation</span><span class="sxs-lookup"><span data-stu-id="dc7ee-129">-PeeringLocation</span></span>
<span data-ttu-id="dc7ee-130">ExpressRoutePort가 물리적으로 매핑된 피어 링 위치의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-130">The name of the peering location that the ExpressRoutePort is mapped to physically.</span></span>

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

### <span data-ttu-id="dc7ee-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc7ee-131">-ResourceGroupName</span></span>
<span data-ttu-id="dc7ee-132">ExpressRoutePort의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-132">The resource group name of the ExpressRoutePort.</span></span>

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

### <span data-ttu-id="dc7ee-133">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="dc7ee-133">-ResourceId</span></span>
<span data-ttu-id="dc7ee-134">Express 경로 포트의 ResourceId입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-134">ResourceId of the express route port.</span></span>

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

### <span data-ttu-id="dc7ee-135">태그</span><span class="sxs-lookup"><span data-stu-id="dc7ee-135">-Tag</span></span>
<span data-ttu-id="dc7ee-136">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-136">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="dc7ee-137">-확인</span><span class="sxs-lookup"><span data-stu-id="dc7ee-137">-Confirm</span></span>
<span data-ttu-id="dc7ee-138">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-138">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc7ee-139">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc7ee-139">-WhatIf</span></span>
<span data-ttu-id="dc7ee-140">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-140">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="dc7ee-141">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-141">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc7ee-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc7ee-142">CommonParameters</span></span>
<span data-ttu-id="dc7ee-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc7ee-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dc7ee-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc7ee-145">입력</span><span class="sxs-lookup"><span data-stu-id="dc7ee-145">INPUTS</span></span>

### <span data-ttu-id="dc7ee-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="dc7ee-146">System.String</span></span>

### <span data-ttu-id="dc7ee-147">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-147">System.Int32</span></span>

### <span data-ttu-id="dc7ee-148">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="dc7ee-148">System.Collections.Hashtable</span></span>

### <span data-ttu-id="dc7ee-149">System.webserver. List ' 1 [[PSExpressRouteLink, Microsoft azure. 6.3.0.0,. \*. \*. \*. e l e = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="dc7ee-149">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Network.Models.PSExpressRouteLink, Microsoft.Azure.Commands.Network, Version=6.3.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="dc7ee-150">출력</span><span class="sxs-lookup"><span data-stu-id="dc7ee-150">OUTPUTS</span></span>

### <span data-ttu-id="dc7ee-151">PSExpressRoutePort에 대 한.</span><span class="sxs-lookup"><span data-stu-id="dc7ee-151">Microsoft.Azure.Commands.Network.Models.PSExpressRoutePort</span></span>

## <span data-ttu-id="dc7ee-152">상속자</span><span class="sxs-lookup"><span data-stu-id="dc7ee-152">NOTES</span></span>

## <span data-ttu-id="dc7ee-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc7ee-153">RELATED LINKS</span></span>
