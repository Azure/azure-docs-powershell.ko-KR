---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/new-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/New-AzDdosProtectionPlan.md
ms.openlocfilehash: 39d45085c7f53bfeec6e18f38602fca48a3cefa3
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94213009"
---
# <span data-ttu-id="56c67-101">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="56c67-101">New-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="56c67-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56c67-102">SYNOPSIS</span></span>
<span data-ttu-id="56c67-103">DDoS protection 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-103">Creates a DDoS protection plan.</span></span>

## <span data-ttu-id="56c67-104">구문과</span><span class="sxs-lookup"><span data-stu-id="56c67-104">SYNTAX</span></span>

```
New-AzDdosProtectionPlan -ResourceGroupName <String> -Name <String> -Location <String> [-Tag <Hashtable>]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="56c67-105">설명은</span><span class="sxs-lookup"><span data-stu-id="56c67-105">DESCRIPTION</span></span>
<span data-ttu-id="56c67-106">New-AzDdosProtectionPlan cmdlet은 DDoS protection 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-106">The New-AzDdosProtectionPlan cmdlet creates a DDoS protection plan.</span></span>

## <span data-ttu-id="56c67-107">예제의</span><span class="sxs-lookup"><span data-stu-id="56c67-107">EXAMPLES</span></span>

### <span data-ttu-id="56c67-108">예제 1: DDoS protection 계획 만들기 및 새 가상 네트워크에 연결</span><span class="sxs-lookup"><span data-stu-id="56c67-108">Example 1: Create and associate a DDoS protection plan with a new virtual network</span></span>
```
D:\> $ddosProtectionPlan = New-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName -Location "West US"
D:\> $subnet = New-AzVirtualNetworkSubnetConfig -Name SubnetName -AddressPrefix 10.0.1.0/24
D:\> $vnet = New-AzVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName -Location "West US" -AddressPrefix 10.0.0.0/16 -DnsServer 8.8.8.8 -Subnet $subnet -EnableDdoSProtection -DdosProtectionPlanId $ddosProtectionPlan.Id
```

<span data-ttu-id="56c67-109">먼저 **새로운-AzDdosProtectionPlan** 명령을 사용 하 여 새 DDoS Protection 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-109">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="56c67-110">그런 다음 **new-AzVirtualNetwork** 를 사용 하 여 새 가상 네트워크를 만들고, **DdosProtectionPlanId** 매개 변수에 새로 생성 된 계획의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-110">Then, we create a new virtual network with **New-AzVirtualNetwork** and we specify the ID of the newly created plan in the parameter **DdosProtectionPlanId**.</span></span> <span data-ttu-id="56c67-111">이 경우 가상 네트워크를 계획과 연결 하기 때문에 **EnableDdoSProtection** 매개 변수를 지정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-111">In this case, since we are associating the virtual network with a plan, we can also specify the parameter **EnableDdoSProtection**.</span></span>

### <span data-ttu-id="56c67-112">예제 2: DDoS protection 계획 만들기 및 기존 가상 네트워크에 연결</span><span class="sxs-lookup"><span data-stu-id="56c67-112">Example 2: Create and associate a DDoS protection plan with an existing virtual network</span></span>
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

<span data-ttu-id="56c67-113">먼저 **새로운-AzDdosProtectionPlan** 명령을 사용 하 여 새 DDoS Protection 계획을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-113">First, we create a new DDoS Protection plan with the **New-AzDdosProtectionPlan** command.</span></span>
<span data-ttu-id="56c67-114">두 번째로, 계획과 연결 하려는 가상 네트워크의 업데이트 된 버전을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-114">Second, we get the most updated version of the virtual network we want to associate with the plan.</span></span> <span data-ttu-id="56c67-115">새로 만든 계획의 ID에 대 한 참조를 포함 하는 **Psresourceid** 개체를 사용 하 여 **DdosProtectionPlan** 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-115">We update the property **DdosProtectionPlan** with a **PSResourceId** object containing a reference to the ID of the newly created plan.</span></span> <span data-ttu-id="56c67-116">이 경우 가상 네트워크를 DDoS protection 계획과 연결 하는 경우 **EnableDdosProtection** 플래그를 true로 설정할 수도 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-116">In this case, if we associate the virtual network with a DDoS protection plan, we can also set the flag **EnableDdosProtection** to true.</span></span>
<span data-ttu-id="56c67-117">마지막으로 지역 변수를 **Set-AzVirtualNetwork** 에 파이핑 하 여 새 상태를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-117">Finally, we persist the new state by piping the local variable into **Set-AzVirtualNetwork**.</span></span>

## <span data-ttu-id="56c67-118">변수</span><span class="sxs-lookup"><span data-stu-id="56c67-118">PARAMETERS</span></span>

### <span data-ttu-id="56c67-119">-AsJob</span><span class="sxs-lookup"><span data-stu-id="56c67-119">-AsJob</span></span>
<span data-ttu-id="56c67-120">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="56c67-120">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="56c67-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56c67-121">-DefaultProfile</span></span>
<span data-ttu-id="56c67-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56c67-123">-위치</span><span class="sxs-lookup"><span data-stu-id="56c67-123">-Location</span></span>
<span data-ttu-id="56c67-124">만들려는 DDoS 보호 계획의 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-124">Specifies the location of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="56c67-125">-이름</span><span class="sxs-lookup"><span data-stu-id="56c67-125">-Name</span></span>
<span data-ttu-id="56c67-126">만들려는 DDoS 보호 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-126">Specifies the name of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="56c67-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56c67-127">-ResourceGroupName</span></span>
<span data-ttu-id="56c67-128">만들려는 DDoS protection 계획의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-128">Specifies the resource group of the DDoS protection plan to be created.</span></span>

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

### <span data-ttu-id="56c67-129">태그</span><span class="sxs-lookup"><span data-stu-id="56c67-129">-Tag</span></span>
<span data-ttu-id="56c67-130">리소스 태그를 나타내는 hashtable입니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-130">A hashtable which represents resource tags.</span></span>

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

### <span data-ttu-id="56c67-131">-확인</span><span class="sxs-lookup"><span data-stu-id="56c67-131">-Confirm</span></span>
<span data-ttu-id="56c67-132">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-132">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="56c67-133">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="56c67-133">-WhatIf</span></span>
<span data-ttu-id="56c67-134">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-134">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="56c67-135">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-135">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="56c67-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56c67-136">CommonParameters</span></span>
<span data-ttu-id="56c67-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="56c67-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56c67-138">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="56c67-138">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56c67-139">입력</span><span class="sxs-lookup"><span data-stu-id="56c67-139">INPUTS</span></span>

### <span data-ttu-id="56c67-140">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="56c67-140">System.String</span></span>

### <span data-ttu-id="56c67-141">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="56c67-141">System.Collections.Hashtable</span></span>

## <span data-ttu-id="56c67-142">출력</span><span class="sxs-lookup"><span data-stu-id="56c67-142">OUTPUTS</span></span>

### <span data-ttu-id="56c67-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="56c67-143">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="56c67-144">상속자</span><span class="sxs-lookup"><span data-stu-id="56c67-144">NOTES</span></span>

## <span data-ttu-id="56c67-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56c67-145">RELATED LINKS</span></span>

[<span data-ttu-id="56c67-146">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="56c67-146">Get-AzDdosProtectionPlan</span></span>](./Get-AzDdosProtectionPlan.md)

[<span data-ttu-id="56c67-147">제거-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="56c67-147">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="56c67-148">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56c67-148">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="56c67-149">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56c67-149">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="56c67-150">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="56c67-150">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)