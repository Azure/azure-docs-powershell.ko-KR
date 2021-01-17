---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372709"
---
# <span data-ttu-id="fc2f3-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc2f3-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="fc2f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc2f3-102">SYNOPSIS</span></span>
<span data-ttu-id="fc2f3-103">DDoS 보호 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="fc2f3-104">구문</span><span class="sxs-lookup"><span data-stu-id="fc2f3-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fc2f3-105">설명</span><span class="sxs-lookup"><span data-stu-id="fc2f3-105">DESCRIPTION</span></span>
<span data-ttu-id="fc2f3-106">New-AzDdosProtectionPlan cmdlet은 DDoS 보호 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="fc2f3-107">예제</span><span class="sxs-lookup"><span data-stu-id="fc2f3-107">EXAMPLES</span></span>

### <span data-ttu-id="fc2f3-108">예제 1: 새 가상 네트워크와 DDoS 보호 계획 만들기 및 연결</span><span class="sxs-lookup"><span data-stu-id="fc2f3-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="fc2f3-109">먼저 **New-AzDdosProtectionPlan** 명령을 사용하여 새 DDoS Protection 계획을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="fc2f3-110">그런 다음 **New-AzVirtualNetwork를** 사용하여 새 가상 네트워크를 만들고 새로 만든 계획의 ID를 **DdosProtectionPlanId** 매개 변수에 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="fc2f3-111">이 경우 가상 네트워크를 계획과 연결하기 때문에 **EnableDdoSProtection** 매개 변수를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="fc2f3-112">예제 2: DDoS 보호 계획 만들기 및 기존 가상 네트워크와 연결</span><span class="sxs-lookup"><span data-stu-id="fc2f3-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $vnet = Get-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = New-Object Microsoft.Azure.Commands.Network.Models.PSResourceId
D:\> $vnet.DdosProtectionPlan.Id = $ddosProtectionPlan.Id
D:\> $vnet.EnableDdosProtection = $true
D:\> $vnet | Set-AzVirtualNetwork


Name                   : VnetName
ResourceGroupName      : ResourceGroupName
Location               : westus
Id                     : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName
Etag                   : W/"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb"
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
                             "Etag": "W/\"fbf41754-3c13-43fd-bb5b-fcc37d5e1cbb\"",
                             "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName/subnets/SubnetName",
                             "AddressPrefix": "10.0.1.0/24",
                             "IpConfigurations": [],
                             "ResourceNavigationLinks": [],
                             "ServiceEndpoints": [],
                             "ProvisioningState": "Succeeded"
                           }
                         ]
VirtualNetworkPeerings : []
EnableDdosProtection   : true
DdosProtectionPlan     : {
                           "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName"
                         }
EnableVmProtection     : false
```

<span data-ttu-id="fc2f3-113">먼저 **New-AzDdosProtectionPlan** 명령을 사용하여 새 DDoS Protection 계획을 작성합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="fc2f3-114">둘째, 계획과 연결하려는 가상 네트워크의 가장 업데이트된 버전을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="fc2f3-115">새로 만든 계획의 ID에 대한 참조를 포함하는 **PSResourceId** 개체로 **DdosProtectionPlan** 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="fc2f3-116">이 경우 가상 네트워크를 DDoS 보호 계획과 연결하면 **EnableDdosProtection 플래그를 true로** 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="fc2f3-117">마지막으로 로컬 변수를 **Set-AzVirtualNetwork에** 파이핑하여 새 상태를 유지합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="fc2f3-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fc2f3-118">PARAMETERS</span></span>

### <span data-ttu-id="fc2f3-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="fc2f3-119">-AsJob</span></span>
<span data-ttu-id="fc2f3-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="fc2f3-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="fc2f3-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc2f3-121">-DefaultProfile</span></span>
<span data-ttu-id="fc2f3-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fc2f3-123">-Location</span><span class="sxs-lookup"><span data-stu-id="fc2f3-123">-Location</span></span>
<span data-ttu-id="fc2f3-124">만들 DDoS 보호 계획의 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc2f3-125">-Name</span><span class="sxs-lookup"><span data-stu-id="fc2f3-125">-Name</span></span>
<span data-ttu-id="fc2f3-126">만들 DDoS 보호 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc2f3-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc2f3-127">-ResourceGroupName</span></span>
<span data-ttu-id="fc2f3-128">만들 DDoS 보호 계획의 리소스 그룹을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="fc2f3-129">-Tag</span><span class="sxs-lookup"><span data-stu-id="fc2f3-129">-Tag</span></span>
<span data-ttu-id="fc2f3-130">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="fc2f3-131">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fc2f3-131">-Confirm</span></span>
<span data-ttu-id="fc2f3-132">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fc2f3-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fc2f3-133">-WhatIf</span></span>
<span data-ttu-id="fc2f3-134">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fc2f3-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fc2f3-135">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fc2f3-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc2f3-136">CommonParameters</span></span>
<span data-ttu-id="fc2f3-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc2f3-138">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fc2f3-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc2f3-139">입력</span><span class="sxs-lookup"><span data-stu-id="fc2f3-139">INPUTS</span></span>

### <span data-ttu-id="fc2f3-140">System.String</span><span class="sxs-lookup"><span data-stu-id="fc2f3-140">System.String</span></span>

### <span data-ttu-id="fc2f3-141">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="fc2f3-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="fc2f3-142">출력</span><span class="sxs-lookup"><span data-stu-id="fc2f3-142">OUTPUTS</span></span>

### <span data-ttu-id="fc2f3-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc2f3-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="fc2f3-144">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fc2f3-144">NOTES</span></span>

## <span data-ttu-id="fc2f3-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fc2f3-145">RELATED LINKS</span></span>

[<span data-ttu-id="fc2f3-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc2f3-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="fc2f3-147">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fc2f3-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="fc2f3-148">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc2f3-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fc2f3-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc2f3-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="fc2f3-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fc2f3-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)