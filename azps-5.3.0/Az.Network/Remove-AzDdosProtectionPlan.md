---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/remove-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Remove-AzDdosProtectionPlan.md
ms.openlocfilehash: c565c78e7f95e02d3449a04f0a53f4b84ef7a9f5
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491768"
---
# <span data-ttu-id="7b7f0-101">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="7b7f0-101">Remove-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="7b7f0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b7f0-102">SYNOPSIS</span></span>
<span data-ttu-id="7b7f0-103">DDoS 보호 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-103">Removes a DDoS protection plan.</span></span>

## <span data-ttu-id="7b7f0-104">구문</span><span class="sxs-lookup"><span data-stu-id="7b7f0-104">SYNTAX</span></span>

```
Remove-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7b7f0-105">설명</span><span class="sxs-lookup"><span data-stu-id="7b7f0-105">DESCRIPTION</span></span>
<span data-ttu-id="7b7f0-106">Remove-AzDdosProtectionPlan cmdlet은 DDoS 보호 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-106">The Remove-AzDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="7b7f0-107">예제</span><span class="sxs-lookup"><span data-stu-id="7b7f0-107">EXAMPLES</span></span>

### <span data-ttu-id="7b7f0-108">예제 1: 빈 DDoS 보호 계획 제거</span><span class="sxs-lookup"><span data-stu-id="7b7f0-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="7b7f0-109">이 경우 지정된 DDoS 보호 계획을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="7b7f0-110">예제 2: 가상 네트워크와 연결된 DDoS 보호 계획 제거</span><span class="sxs-lookup"><span data-stu-id="7b7f0-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"65947351-747e-4686-aa8b-c40da58f6c8b"
ResourceGuid           : fcb7bc1e-ee0d-4005-b3f1-feda76e3756c
ProvisioningState      : Succeeded
Tags                   :
AddressSpace           : {
                           "AddressPrefixes": [
                             "10.0.0.0/16"
                           ]
                         }
DhcpOptions            : {
                           "DnsServers": [
                             "8.8.8.8"
                           ]
                         }
Subnets                : [
                           {
                             "Name": "SubnetName",
                             "Etag": "W/\"65947351-747e-4686-aa8b-c40da58f6c8b\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : false
DdosProtectionPlan     : null
EnableVmProtection     : false


D:\> Remove-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="7b7f0-111">DDoS 보호 계획은 가상 네트워크에 연결된 경우 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="7b7f0-112">따라서 첫 번째 단계는 두 개체를 모두 분해하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="7b7f0-113">여기서는 계획과 연결된 가상 네트워크의 가장 업데이트된 버전을 얻게 됐고 **DdosProtectionPlan** 속성을 빈 값으로 설정하고 **EnableDdosProtection** 플래그를 설정했습니다(계획이 없는 경우 이 플래그는 true일 수 없습니다).</span><span class="sxs-lookup"><span data-stu-id="7b7f0-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="7b7f0-114">그런 다음 로컬 변수를 **Set-AzVirtualNetwork로** 파이핑하여 새 상태를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-114">Then, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span> <span data-ttu-id="7b7f0-115">이 시점에서 계획은 더 이상 가상 네트워크와 연결하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="7b7f0-116">계획과 연결된 마지막 계획인 경우 Remove-AzDdosProtectionPlan 명령을 사용하여 DDoS 보호 계획을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzDdosProtectionPlan.</span></span>

## <span data-ttu-id="7b7f0-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7b7f0-117">PARAMETERS</span></span>

### <span data-ttu-id="7b7f0-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b7f0-118">-DefaultProfile</span></span>
<span data-ttu-id="7b7f0-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b7f0-120">-Name</span><span class="sxs-lookup"><span data-stu-id="7b7f0-120">-Name</span></span>
<span data-ttu-id="7b7f0-121">제거할 DDoS 보호 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="7b7f0-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="7b7f0-122">-PassThru</span></span>
<span data-ttu-id="7b7f0-123">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="7b7f0-124">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="7b7f0-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7b7f0-125">-ResourceGroupName</span></span>
<span data-ttu-id="7b7f0-126">제거할 DDoS 보호 계획의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="7b7f0-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="7b7f0-127">-Confirm</span></span>
<span data-ttu-id="7b7f0-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="7b7f0-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7b7f0-129">-WhatIf</span></span>
<span data-ttu-id="7b7f0-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="7b7f0-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7b7f0-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="7b7f0-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b7f0-132">CommonParameters</span></span>
<span data-ttu-id="7b7f0-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b7f0-134">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="7b7f0-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b7f0-135">입력</span><span class="sxs-lookup"><span data-stu-id="7b7f0-135">INPUTS</span></span>

### <span data-ttu-id="7b7f0-136">System.String</span><span class="sxs-lookup"><span data-stu-id="7b7f0-136">System.String</span></span>

## <span data-ttu-id="7b7f0-137">출력</span><span class="sxs-lookup"><span data-stu-id="7b7f0-137">OUTPUTS</span></span>

### <span data-ttu-id="7b7f0-138">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="7b7f0-138">System.Boolean</span></span>

## <span data-ttu-id="7b7f0-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b7f0-139">NOTES</span></span>

## <span data-ttu-id="7b7f0-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b7f0-140">RELATED LINKS</span></span>

[<span data-ttu-id="7b7f0-141">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="7b7f0-141">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="7b7f0-142">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="7b7f0-142">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="7b7f0-143">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7b7f0-143">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="7b7f0-144">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7b7f0-144">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="7b7f0-145">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="7b7f0-145">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)