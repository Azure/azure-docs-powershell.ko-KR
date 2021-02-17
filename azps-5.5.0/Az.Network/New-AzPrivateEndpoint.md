---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100184388"
---
# <span data-ttu-id="59f69-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59f69-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="59f69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59f69-102">SYNOPSIS</span></span>
<span data-ttu-id="59f69-103">개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="59f69-104">구문</span><span class="sxs-lookup"><span data-stu-id="59f69-104">SYNTAX</span></span>

### <span data-ttu-id="59f69-105">모두</span><span class="sxs-lookup"><span data-stu-id="59f69-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="59f69-106">설명</span><span class="sxs-lookup"><span data-stu-id="59f69-106">DESCRIPTION</span></span>

<span data-ttu-id="59f69-107">**New-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="59f69-108">예제</span><span class="sxs-lookup"><span data-stu-id="59f69-108">EXAMPLES</span></span>

### <span data-ttu-id="59f69-109">예제 1: 개인 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="59f69-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="59f69-110">다음 예제에서는 가상 네트워크의 지정된 서브넷에 특정 개인 링크 서비스 ID를 사용하여 개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="59f69-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="59f69-111">PARAMETERS</span></span>

### <span data-ttu-id="59f69-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="59f69-112">-AsJob</span></span>

<span data-ttu-id="59f69-113">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="59f69-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="59f69-114">-ByManualRequest</span></span>

<span data-ttu-id="59f69-115">수동 요청을 사용하여 연결을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="59f69-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59f69-116">-DefaultProfile</span></span>

<span data-ttu-id="59f69-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59f69-118">-Force</span><span class="sxs-lookup"><span data-stu-id="59f69-118">-Force</span></span>

<span data-ttu-id="59f69-119">리소스를 덮어치기 위한 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="59f69-120">-Location</span><span class="sxs-lookup"><span data-stu-id="59f69-120">-Location</span></span>

<span data-ttu-id="59f69-121">개인 엔드포인트의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="59f69-122">[Get-AzLocation을 사용하여](/powershell/module/az.resources/get-azlocation) 이 매개 변수에 대한 유효한 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="59f69-123">-Name</span><span class="sxs-lookup"><span data-stu-id="59f69-123">-Name</span></span>

<span data-ttu-id="59f69-124">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="59f69-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="59f69-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="59f69-126">개인 엔드포인트를 연결할 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-126">The resource ID to connect the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f69-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="59f69-127">-ResourceGroupName</span></span>

<span data-ttu-id="59f69-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="59f69-129">-Subnet</span><span class="sxs-lookup"><span data-stu-id="59f69-129">-Subnet</span></span>

<span data-ttu-id="59f69-130">개인 엔드포인트의 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-130">The subnet of the private endpoint.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Network.Models.PSSubnet
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="59f69-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="59f69-131">-Tag</span></span>

<span data-ttu-id="59f69-132">해시 테이블 형식의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="59f69-133">예: @{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="59f69-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="59f69-134">-Confirm</span><span class="sxs-lookup"><span data-stu-id="59f69-134">-Confirm</span></span>

<span data-ttu-id="59f69-135">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="59f69-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="59f69-136">-WhatIf</span></span>

<span data-ttu-id="59f69-137">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="59f69-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="59f69-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="59f69-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59f69-139">CommonParameters</span></span>

<span data-ttu-id="59f69-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="59f69-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59f69-141">자세한 내용은 [다음](/powershell/module/microsoft.powershell.core/about/about_commonparameters)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="59f69-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="59f69-142">입력</span><span class="sxs-lookup"><span data-stu-id="59f69-142">INPUTS</span></span>

### <span data-ttu-id="59f69-143">System.String</span><span class="sxs-lookup"><span data-stu-id="59f69-143">System.String</span></span>

### <span data-ttu-id="59f69-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="59f69-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="59f69-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="59f69-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="59f69-146">출력</span><span class="sxs-lookup"><span data-stu-id="59f69-146">OUTPUTS</span></span>

### <span data-ttu-id="59f69-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59f69-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="59f69-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="59f69-148">NOTES</span></span>

## <span data-ttu-id="59f69-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59f69-149">RELATED LINKS</span></span>

[<span data-ttu-id="59f69-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59f69-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="59f69-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="59f69-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="59f69-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="59f69-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)