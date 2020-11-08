---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: df298b41ea1efa4915cb7556b9fd07b1d8f3e2de
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94218830"
---
# <span data-ttu-id="24a73-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24a73-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="24a73-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24a73-102">SYNOPSIS</span></span>
<span data-ttu-id="24a73-103">개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="24a73-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24a73-104">SYNTAX</span></span>

### <span data-ttu-id="24a73-105">모든</span><span class="sxs-lookup"><span data-stu-id="24a73-105">All</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24a73-106">설명은</span><span class="sxs-lookup"><span data-stu-id="24a73-106">DESCRIPTION</span></span>

<span data-ttu-id="24a73-107">**AzPrivateEndpoint** cmdlet은 개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-107">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="24a73-108">예제의</span><span class="sxs-lookup"><span data-stu-id="24a73-108">EXAMPLES</span></span>

### <span data-ttu-id="24a73-109">예제 1: 개인 끝점 만들기</span><span class="sxs-lookup"><span data-stu-id="24a73-109">Example 1: Create a private endpoint</span></span>

<span data-ttu-id="24a73-110">다음 예제에서는 가상 네트워크의 지정 된 서브넷에서 특정 개인 링크 서비스 ID를 사용 하 여 개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-110">The following example creates a private endpoint with a specific private link service ID in the specified subnet in a virtual network.</span></span>

```powershell
$virtualNetwork = Get-AzVirtualNetwork -ResourceName 'myVirtualNetwork' -ResourceGroupName 'myResourceGroup'
$subnet = $virtualNetwork | Select-Object -ExpandProperty subnets | Where-Object Name -eq 'mySubnet'
$plsConnection= New-AzPrivateLinkServiceConnection -Name 'MyPLSConnections' -PrivateLinkServiceId '/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/myResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService' -RequestMessage 'Please Approve my request'
New-AzPrivateEndpoint -Name 'MyPrivateEndpoint' -ResourceGroup 'myResourceGroup' -Location 'centralus' -PrivateLinkServiceConnection $plsConnection -Subnet $subnet
```

## <span data-ttu-id="24a73-111">변수</span><span class="sxs-lookup"><span data-stu-id="24a73-111">PARAMETERS</span></span>

### <span data-ttu-id="24a73-112">-AsJob</span><span class="sxs-lookup"><span data-stu-id="24a73-112">-AsJob</span></span>

<span data-ttu-id="24a73-113">백그라운드에서 cmdlet을 작업으로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-113">Run cmdlet as a job in the background.</span></span>

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

### <span data-ttu-id="24a73-114">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="24a73-114">-ByManualRequest</span></span>

<span data-ttu-id="24a73-115">수동 요청을 사용 하 여 연결을 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-115">Use manual request to establish the connection.</span></span>

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

### <span data-ttu-id="24a73-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24a73-116">-DefaultProfile</span></span>

<span data-ttu-id="24a73-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="24a73-118">-Force</span><span class="sxs-lookup"><span data-stu-id="24a73-118">-Force</span></span>

<span data-ttu-id="24a73-119">리소스 덮어쓰기 확인을 묻지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-119">Do not ask for confirmation to overwrite a resource.</span></span>

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

### <span data-ttu-id="24a73-120">-위치</span><span class="sxs-lookup"><span data-stu-id="24a73-120">-Location</span></span>

<span data-ttu-id="24a73-121">개인 끝점의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-121">Specifies a location for the private endpoint.</span></span> <span data-ttu-id="24a73-122">이 매개 변수에 대 한 유효한 값을 확인 하려면 [Get-AzLocation](/powershell/module/az.resources/get-azlocation) 을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-122">Use [Get-AzLocation](/powershell/module/az.resources/get-azlocation) to determine valid values for this parameter.</span></span>

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

### <span data-ttu-id="24a73-123">-이름</span><span class="sxs-lookup"><span data-stu-id="24a73-123">-Name</span></span>

<span data-ttu-id="24a73-124">개인 끝점의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-124">Name of the private endpoint.</span></span>

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

### <span data-ttu-id="24a73-125">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="24a73-125">-PrivateLinkServiceConnection</span></span>

<span data-ttu-id="24a73-126">개인 끝점을 연결할 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-126">The resource ID to connect the private endpoint.</span></span>

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

### <span data-ttu-id="24a73-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24a73-127">-ResourceGroupName</span></span>

<span data-ttu-id="24a73-128">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="24a73-129">-서브넷</span><span class="sxs-lookup"><span data-stu-id="24a73-129">-Subnet</span></span>

<span data-ttu-id="24a73-130">개인 끝점의 서브넷입니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-130">The subnet of the private endpoint.</span></span>

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

### <span data-ttu-id="24a73-131">태그</span><span class="sxs-lookup"><span data-stu-id="24a73-131">-Tag</span></span>

<span data-ttu-id="24a73-132">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-132">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="24a73-133">예를 들어 @ {key0 = ' value0 ', key1 = $null, key2 = ' value2 = ' 2, 2,.</span><span class="sxs-lookup"><span data-stu-id="24a73-133">For example: @{key0='value0';key1=$null;key2='value2'}</span></span>

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

### <span data-ttu-id="24a73-134">-확인</span><span class="sxs-lookup"><span data-stu-id="24a73-134">-Confirm</span></span>

<span data-ttu-id="24a73-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24a73-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24a73-136">-WhatIf</span></span>

<span data-ttu-id="24a73-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24a73-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24a73-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24a73-139">CommonParameters</span></span>

<span data-ttu-id="24a73-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24a73-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24a73-141">자세한 내용은 [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="24a73-141">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="24a73-142">입력</span><span class="sxs-lookup"><span data-stu-id="24a73-142">INPUTS</span></span>

### <span data-ttu-id="24a73-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="24a73-143">System.String</span></span>

### <span data-ttu-id="24a73-144">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="24a73-144">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="24a73-145">PSPrivateLinkServiceConnection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="24a73-145">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="24a73-146">출력</span><span class="sxs-lookup"><span data-stu-id="24a73-146">OUTPUTS</span></span>

### <span data-ttu-id="24a73-147">PSPrivateEndpoint에 대 한.</span><span class="sxs-lookup"><span data-stu-id="24a73-147">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="24a73-148">상속자</span><span class="sxs-lookup"><span data-stu-id="24a73-148">NOTES</span></span>

## <span data-ttu-id="24a73-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24a73-149">RELATED LINKS</span></span>

[<span data-ttu-id="24a73-150">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24a73-150">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="24a73-151">제거-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="24a73-151">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="24a73-152">새로운 AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="24a73-152">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)