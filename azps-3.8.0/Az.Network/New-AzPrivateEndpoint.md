---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azprivateendpoint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzPrivateEndpoint.md
ms.openlocfilehash: 6e83def7c4956e4936e8e3c55f96aab1da0d451d
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94041770"
---
# <span data-ttu-id="b553d-101">New-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b553d-101">New-AzPrivateEndpoint</span></span>

## <span data-ttu-id="b553d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b553d-102">SYNOPSIS</span></span>
<span data-ttu-id="b553d-103">개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-103">Creates a private endpoint.</span></span>

## <span data-ttu-id="b553d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b553d-104">SYNTAX</span></span>

```
New-AzPrivateEndpoint -Name <String> -ResourceGroupName <String> -Location <String> -Subnet <PSSubnet>
 -PrivateLinkServiceConnection <PSPrivateLinkServiceConnection[]> [-ByManualRequest] [-Tag <Hashtable>]
 [-Force] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b553d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b553d-105">DESCRIPTION</span></span>
<span data-ttu-id="b553d-106">**AzPrivateEndpoint** cmdlet은 개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-106">The **New-AzPrivateEndpoint** cmdlet creates a private endpoint.</span></span>

## <span data-ttu-id="b553d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b553d-107">EXAMPLES</span></span>

### <span data-ttu-id="b553d-108">1: 개인 끝점 만들기</span><span class="sxs-lookup"><span data-stu-id="b553d-108">1: Create a private endpoint</span></span>
```
$virtualNetwork = Get-AzVirtualNetwork -ResourceName MyVirtualNetwork -ResourceGroupName TestResourceGroup
$plsConnection= New-AzPrivateLinkServiceConnection -Name MyPLSConnections -PrivateLinkServiceId "/subscriptions/00000000-0000-0000-0000-000000000000/resourceGroups/TestResourceGroup/providers/Microsoft.Network/privateLinkServices/privateLinkService" -RequestMessage "Please Approve my request"
New-AzPrivateEndpoint -Name MyPrivateEndpoint -ResourceGroup TestResourceGroup -Location centralus -PrivateLinkServiceConnection $plsConnection -Subnet $virtualNetwork.Subnets[0]
```

<span data-ttu-id="b553d-109">이 예제에서는 가상 네트워크의 특정 서브넷에 특정 개인 링크 서비스 id가 포함 된 개인 끝점을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-109">This example creates a private endpoint with specific private link service id in a specific subnet in a virtual network.</span></span>

## <span data-ttu-id="b553d-110">변수</span><span class="sxs-lookup"><span data-stu-id="b553d-110">PARAMETERS</span></span>

### <span data-ttu-id="b553d-111">-AsJob</span><span class="sxs-lookup"><span data-stu-id="b553d-111">-AsJob</span></span>
<span data-ttu-id="b553d-112">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="b553d-112">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="b553d-113">-ByManualRequest</span><span class="sxs-lookup"><span data-stu-id="b553d-113">-ByManualRequest</span></span>
<span data-ttu-id="b553d-114">수동 요청을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-114">Using manual request.</span></span>

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

### <span data-ttu-id="b553d-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b553d-115">-DefaultProfile</span></span>
<span data-ttu-id="b553d-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b553d-117">-Force</span><span class="sxs-lookup"><span data-stu-id="b553d-117">-Force</span></span>
<span data-ttu-id="b553d-118">리소스를 덮어쓰려고 할 때 확인 메시지 표시 안 함</span><span class="sxs-lookup"><span data-stu-id="b553d-118">Do not ask for confirmation if you want to overwrite a resource</span></span>

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

### <span data-ttu-id="b553d-119">-위치</span><span class="sxs-lookup"><span data-stu-id="b553d-119">-Location</span></span>
<span data-ttu-id="b553d-120">location.</span><span class="sxs-lookup"><span data-stu-id="b553d-120">location.</span></span>

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

### <span data-ttu-id="b553d-121">-이름</span><span class="sxs-lookup"><span data-stu-id="b553d-121">-Name</span></span>
<span data-ttu-id="b553d-122">자원 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-122">The resource name.</span></span>

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

### <span data-ttu-id="b553d-123">-PrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b553d-123">-PrivateLinkServiceConnection</span></span>
<span data-ttu-id="b553d-124">개인 링크 서비스 연결.</span><span class="sxs-lookup"><span data-stu-id="b553d-124">The private link service connection.</span></span>

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

### <span data-ttu-id="b553d-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b553d-125">-ResourceGroupName</span></span>
<span data-ttu-id="b553d-126">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-126">The resource group name.</span></span>

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

### <span data-ttu-id="b553d-127">-서브넷</span><span class="sxs-lookup"><span data-stu-id="b553d-127">-Subnet</span></span>
<span data-ttu-id="b553d-128">개인 끝점의 서브넷</span><span class="sxs-lookup"><span data-stu-id="b553d-128">The subnet of the private endpoint</span></span>

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

### <span data-ttu-id="b553d-129">태그</span><span class="sxs-lookup"><span data-stu-id="b553d-129">-Tag</span></span>
<span data-ttu-id="b553d-130">해시 테이블 형태의 키-값 쌍입니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-130">Key-value pairs in the form of a hash table.</span></span> <span data-ttu-id="b553d-131">예: @ {key0 = "value0"; key1 = $null; key2 = "value2"}</span><span class="sxs-lookup"><span data-stu-id="b553d-131">For example: @{key0="value0";key1=$null;key2="value2"}</span></span>

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

### <span data-ttu-id="b553d-132">-확인</span><span class="sxs-lookup"><span data-stu-id="b553d-132">-Confirm</span></span>
<span data-ttu-id="b553d-133">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b553d-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b553d-134">-WhatIf</span></span>
<span data-ttu-id="b553d-135">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b553d-136">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b553d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b553d-137">CommonParameters</span></span>
<span data-ttu-id="b553d-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b553d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b553d-139">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b553d-139">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b553d-140">입력</span><span class="sxs-lookup"><span data-stu-id="b553d-140">INPUTS</span></span>

### <span data-ttu-id="b553d-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="b553d-141">System.String</span></span>

### <span data-ttu-id="b553d-142">Microsoft. 네트워크 모델. PSSubnet</span><span class="sxs-lookup"><span data-stu-id="b553d-142">Microsoft.Azure.Commands.Network.Models.PSSubnet</span></span>

### <span data-ttu-id="b553d-143">PSPrivateLinkServiceConnection [] (으)로</span><span class="sxs-lookup"><span data-stu-id="b553d-143">Microsoft.Azure.Commands.Network.Models.PSPrivateLinkServiceConnection[]</span></span>

## <span data-ttu-id="b553d-144">출력</span><span class="sxs-lookup"><span data-stu-id="b553d-144">OUTPUTS</span></span>

### <span data-ttu-id="b553d-145">PSPrivateEndpoint에 대 한.</span><span class="sxs-lookup"><span data-stu-id="b553d-145">Microsoft.Azure.Commands.Network.Models.PSPrivateEndpoint</span></span>

## <span data-ttu-id="b553d-146">상속자</span><span class="sxs-lookup"><span data-stu-id="b553d-146">NOTES</span></span>

## <span data-ttu-id="b553d-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b553d-147">RELATED LINKS</span></span>

[<span data-ttu-id="b553d-148">Get-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b553d-148">Get-AzPrivateEndpoint</span></span>](./Get-AzPrivateEndpoint.md)

[<span data-ttu-id="b553d-149">제거-AzPrivateEndpoint</span><span class="sxs-lookup"><span data-stu-id="b553d-149">Remove-AzPrivateEndpoint</span></span>](./Remove-AzPrivateEndpoint.md)

[<span data-ttu-id="b553d-150">새로운 AzPrivateLinkServiceConnection</span><span class="sxs-lookup"><span data-stu-id="b553d-150">New-AzPrivateLinkServiceConnection</span></span>](./New-AzPrivateLinkServiceConnection.md)