---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: f7ec596a73c3659584d1e0b80c899b4bf9aad8d2
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982352"
---
# <span data-ttu-id="42c8c-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c8c-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="42c8c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="42c8c-102">SYNOPSIS</span></span>
<span data-ttu-id="42c8c-103">개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="42c8c-104">구문</span><span class="sxs-lookup"><span data-stu-id="42c8c-104">SYNTAX</span></span>

### <span data-ttu-id="42c8c-105">모두</span><span class="sxs-lookup"><span data-stu-id="42c8c-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="42c8c-106">설명</span><span class="sxs-lookup"><span data-stu-id="42c8c-106">DESCRIPTION</span></span>

<span data-ttu-id="42c8c-107">**New-AzPrivateEndpoint** cmdlet은 개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="42c8c-108">예제</span><span class="sxs-lookup"><span data-stu-id="42c8c-108">EXAMPLES</span></span>

### <span data-ttu-id="42c8c-109">예제 1: 개인 엔드포인트 만들기</span><span class="sxs-lookup"><span data-stu-id="42c8c-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="42c8c-110">다음 예제에서는 가상 네트워크의 지정된 서브넷에 특정 개인 링크 서비스 ID가 있는 개인 엔드포인트를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="42c8c-111">매개 변수</span><span class="sxs-lookup"><span data-stu-id="42c8c-111">PARAMETERS</span></span>

### <span data-ttu-id="42c8c-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="42c8c-112">-AsJob</span></span>

<span data-ttu-id="42c8c-113">백그라운드에서 작업으로 cmdlet을 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="42c8c-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="42c8c-114">-ByManualRequest</span></span>

<span data-ttu-id="42c8c-115">수동 요청을 사용하여 연결을 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="42c8c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="42c8c-116">-DefaultProfile</span></span>

<span data-ttu-id="42c8c-117">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="42c8c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="42c8c-118">-Force</span></span>

<span data-ttu-id="42c8c-119">리소스를 덮어 덮어 우기 위해 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="42c8c-120">-Location</span><span class="sxs-lookup"><span data-stu-id="42c8c-120">-Location</span></span>

<span data-ttu-id="42c8c-121">개인 엔드포인트의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="42c8c-122">[Get-AzLocation을 사용하여](/powershell/module/az.resources/get-azlocation) 이 매개 변수에 대한 유효한 값을 확인할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="42c8c-123">-Name</span><span class="sxs-lookup"><span data-stu-id="42c8c-123">-Name</span></span>

<span data-ttu-id="42c8c-124">개인 엔드포인트의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="42c8c-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="42c8c-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="42c8c-126">개인 엔드포인트를 연결하는 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="42c8c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="42c8c-127">-ResourceGroupName</span></span>

<span data-ttu-id="42c8c-128">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="42c8c-129">-서브넷</span><span class="sxs-lookup"><span data-stu-id="42c8c-129">-Subnet</span></span>

<span data-ttu-id="42c8c-130">개인 엔드포인트의 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="42c8c-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="42c8c-131">-Tag</span></span>

<span data-ttu-id="42c8c-132">해시 테이블의 형태로 키 값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="42c8c-133">예: @{key0='value0';key1=$null;key2='value2'}</span><span class="sxs-lookup"><span data-stu-id="42c8c-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="42c8c-134">-확인</span><span class="sxs-lookup"><span data-stu-id="42c8c-134">-Confirm</span></span>

<span data-ttu-id="42c8c-135">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="42c8c-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="42c8c-136">-WhatIf</span></span>

<span data-ttu-id="42c8c-137">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="42c8c-138">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="42c8c-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="42c8c-139">CommonParameters</span></span>

<span data-ttu-id="42c8c-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="42c8c-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="42c8c-141">자세한 내용은 를 [about_CommonParameters.](/powershell/module/microsoft.powershell.core/about/about_commonparameters)</span><span class="sxs-lookup"><span data-stu-id="42c8c-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="42c8c-142">입력</span><span class="sxs-lookup"><span data-stu-id="42c8c-142">INPUTS</span></span>

### <span data-ttu-id="42c8c-143">System.String</span><span class="sxs-lookup"><span data-stu-id="42c8c-143">System.String</span></span>

### <span data-ttu-id="42c8c-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span><span class="sxs-lookup"><span data-stu-id="42c8c-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="42c8c-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span><span class="sxs-lookup"><span data-stu-id="42c8c-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="42c8c-146">출력</span><span class="sxs-lookup"><span data-stu-id="42c8c-146">OUTPUTS</span></span>

### <span data-ttu-id="42c8c-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c8c-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="42c8c-148">참고 사항</span><span class="sxs-lookup"><span data-stu-id="42c8c-148">NOTES</span></span>

## <span data-ttu-id="42c8c-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="42c8c-149">RELATED LINKS</span></span>

[<span data-ttu-id="42c8c-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c8c-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="42c8c-151">Remove-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="42c8c-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="42c8c-152">New-AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="42c8c-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)