---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/set-azexpressroutegateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Set-AzExpressRouteGateway.md
ms.openlocfilehash: c3d311cc091026bcd08225e5a11a8232102a03a3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871089"
---
# <span data-ttu-id="c0ecc-101">Set-AzExpressRouteGateway</span><span class="sxs-lookup"><span data-stu-id="c0ecc-101">Set-AzExpressRouteGateway</span></span>

## <span data-ttu-id="c0ecc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c0ecc-102">SYNOPSIS</span></span>
<span data-ttu-id="c0ecc-103">확장 가능 하 인 Express 경로 게이트웨이를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-103">Updates a Scalable ExpressRoute Gateway.</span></span>

## <span data-ttu-id="c0ecc-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c0ecc-104">SYNTAX</span></span>

### <span data-ttu-id="c0ecc-105">ByExpressRouteGatewayName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c0ecc-105">ByExpressRouteGatewayName (Default)</span></span>
```
Set-AzExpressRouteGateway -ResourceGroupName <String> -Name <String> -MinScaleUnits <UInt32>
 -MaxScaleUnits <UInt32> [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c0ecc-106">ByExpressRouteGatewayObject</span><span class="sxs-lookup"><span data-stu-id="c0ecc-106">ByExpressRouteGatewayObject</span></span>
```
Set-AzExpressRouteGateway -InputObject <PSExpressRouteGateway> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c0ecc-107">ByExpressRouteGatewayResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ecc-107">ByExpressRouteGatewayResourceId</span></span>
```
Set-AzExpressRouteGateway -ResourceId <String> -MinScaleUnits <UInt32> -MaxScaleUnits <UInt32>
 [-Tag <Hashtable>] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="c0ecc-108">설명은</span><span class="sxs-lookup"><span data-stu-id="c0ecc-108">DESCRIPTION</span></span>

<span data-ttu-id="c0ecc-109">Set-AzExpressRouteGateway에서 ExpressRouteGateway 배율 단위를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-109">Set-AzExpressRouteGateway updates the scale units for the ExpressRouteGateway</span></span>

## <span data-ttu-id="c0ecc-110">예제의</span><span class="sxs-lookup"><span data-stu-id="c0ecc-110">EXAMPLES</span></span>

### <span data-ttu-id="c0ecc-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="c0ecc-111">Example 1</span></span>

```powershell
PS C:\>Set-AzResourceGroup -Location "West US" -Name "testRG"
PS C:\> $virtualWan =Set-AzVirtualWan -ResourceGroupName testRG -Name myVirtualWAN -Location "West US"
PS C:\> $virtualHub =Set-AzVirtualHub -VirtualWan $virtualWan -ResourceGroupName "testRG" -Name "westushub" -AddressPrefix "10.0.0.1/24"
PS C:\>New-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -VirtualHubId $virtualHub.Id -MinScaleUnits 2
PS C:\>Set-AzExpressRouteGateway -ResourceGroupName "testRG" -Name "testergw" -MinScaleUnits 3

ResourceGroupName   : testRG
Name                : testergw
Id                  : /subscriptions/{subscriptionId}/resourceGroups/testRG/providers/Microsoft.Network/expressRouteGateways/testergw
Location            : West US
MinScaleUnits       : 3
Type                : Microsoft.Network/expressRouteGateways
ProvisioningState   : Succeeded
```

<span data-ttu-id="c0ecc-112">위의 방법을 통해 Azure의 "testRG" 리소스 그룹에 미국 내에서 리소스 그룹, 가상 WAN, 가상 네트워크, 가상 허브를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-112">The above will create a resource group, Virtual WAN, Virtual Network, Virtual Hub in West US in "testRG" resource group in Azure.</span></span> <span data-ttu-id="c0ecc-113">두 개의 배율 단위를 사용 하 고 그 후에는 3 개의 배율 단위로 수정 되는 가상 허브에 Express 경로 게이트웨이가 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-113">An ExpressRoute gateway will be created thereafter in the Virtual Hub with 2 scale units which will then be modified to 3 scale units</span></span>

## <span data-ttu-id="c0ecc-114">변수</span><span class="sxs-lookup"><span data-stu-id="c0ecc-114">PARAMETERS</span></span>

### <span data-ttu-id="c0ecc-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c0ecc-115">-AsJob</span></span>
<span data-ttu-id="c0ecc-116">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c0ecc-116">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c0ecc-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c0ecc-117">-DefaultProfile</span></span>
<span data-ttu-id="c0ecc-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c0ecc-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c0ecc-119">-InputObject</span></span>
<span data-ttu-id="c0ecc-120">업데이트 해야 하는 ExpressRouteGateway.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-120">The ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway
Parameter Sets: ByExpressRouteGatewayObject
Aliases: ExpressRouteGateway

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-121">-MaxScaleUnits</span><span class="sxs-lookup"><span data-stu-id="c0ecc-121">-MaxScaleUnits</span></span>
<span data-ttu-id="c0ecc-122">이 ExpressRouteGateway의 최대 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-122">The maximum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="c0ecc-123">유효 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="c0ecc-123">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-124">-MinScaleUnits</span><span class="sxs-lookup"><span data-stu-id="c0ecc-124">-MinScaleUnits</span></span>
<span data-ttu-id="c0ecc-125">이 ExpressRouteGateway의 최소 배율 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-125">The minimum number of scale units for this ExpressRouteGateway.</span></span> <span data-ttu-id="c0ecc-126">유효 범위 > 2</span><span class="sxs-lookup"><span data-stu-id="c0ecc-126">Valid range > 2</span></span>

```yaml
Type: System.UInt32
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-127">-이름</span><span class="sxs-lookup"><span data-stu-id="c0ecc-127">-Name</span></span>
<span data-ttu-id="c0ecc-128">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-128">The resource name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases: ResourceName, ExpressRouteGatewayName, GatewayName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c0ecc-129">-ResourceGroupName</span></span>
<span data-ttu-id="c0ecc-130">업데이트할 ExpressRouteGateway의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-130">The resource group name of the ExpressRouteGateway to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-131">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="c0ecc-131">-ResourceId</span></span>
<span data-ttu-id="c0ecc-132">업데이트 해야 하는 ExpressRouteGateway의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-132">The Id of the ExpressRouteGateway that needs to be updated.</span></span>

```yaml
Type: System.String
Parameter Sets: ByExpressRouteGatewayResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-133">태그</span><span class="sxs-lookup"><span data-stu-id="c0ecc-133">-Tag</span></span>
<span data-ttu-id="c0ecc-134">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-134">A hashtable which represents resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c0ecc-135">-확인</span><span class="sxs-lookup"><span data-stu-id="c0ecc-135">-Confirm</span></span>
<span data-ttu-id="c0ecc-136">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c0ecc-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c0ecc-137">-WhatIf</span></span>
<span data-ttu-id="c0ecc-138">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c0ecc-139">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c0ecc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c0ecc-140">CommonParameters</span></span>
<span data-ttu-id="c0ecc-141">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c0ecc-142">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c0ecc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c0ecc-143">입력</span><span class="sxs-lookup"><span data-stu-id="c0ecc-143">INPUTS</span></span>

### <span data-ttu-id="c0ecc-144">Microsoft. 네트워크. PSVirtualHub</span><span class="sxs-lookup"><span data-stu-id="c0ecc-144">Microsoft.Azure.Commands.Network.Models.PSVirtualHub</span></span>

### <span data-ttu-id="c0ecc-145">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="c0ecc-145">System.String</span></span>

## <span data-ttu-id="c0ecc-146">출력</span><span class="sxs-lookup"><span data-stu-id="c0ecc-146">OUTPUTS</span></span>

### <span data-ttu-id="c0ecc-147">PSExpressRouteGateway에 대 한.</span><span class="sxs-lookup"><span data-stu-id="c0ecc-147">Microsoft.Azure.Commands.Network.Models.PSExpressRouteGateway</span></span>

## <span data-ttu-id="c0ecc-148">상속자</span><span class="sxs-lookup"><span data-stu-id="c0ecc-148">NOTES</span></span>

## <span data-ttu-id="c0ecc-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c0ecc-149">RELATED LINKS</span></span>
