---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/remove-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Remove-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 87110fe779e128e8ef5d5d6de0504ec9fdca1b25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93537539"
---
# <span data-ttu-id="611c8-101">Remove-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="611c8-101">Remove-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="611c8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="611c8-102">SYNOPSIS</span></span>
<span data-ttu-id="611c8-103">DDoS 보호 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-103">Removes a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="611c8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="611c8-104">SYNTAX</span></span>

```
Remove-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="611c8-105">설명은</span><span class="sxs-lookup"><span data-stu-id="611c8-105">DESCRIPTION</span></span>
<span data-ttu-id="611c8-106">Remove-AzureRmDdosProtectionPlan cmdlet은 DDoS protection 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-106">The Remove-AzureRmDdosProtectionPlan cmdlet removes a DDoS protection plan.</span></span>

## <span data-ttu-id="611c8-107">예제의</span><span class="sxs-lookup"><span data-stu-id="611c8-107">EXAMPLES</span></span>

### <span data-ttu-id="611c8-108">예제 1: 빈 DDoS 보호 계획 제거</span><span class="sxs-lookup"><span data-stu-id="611c8-108">Example 1: Remove an empty DDoS protection plan</span></span>
```
D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="611c8-109">이 경우 지정 된 대로 DDoS protection 계획을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-109">In this case, we remove a DDoS protection plan as specified.</span></span>

### <span data-ttu-id="611c8-110">예제 2: 가상 네트워크와 연결 된 DDoS protection 계획 제거</span><span class="sxs-lookup"><span data-stu-id="611c8-110">Example 2: Remove a DDoS protection plan associated with a virtual network</span></span>
```
D:\> $vnet = Get-AzureRmVirtualNetwork -Name VnetName -ResourceGroupName ResourceGroupName
D:\> $vnet.DdosProtectionPlan = $null
D:\> $vnet.EnableDdosProtection = $false
D:\> $vnet | Set-AzureRmVirtualNetwork


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


D:\> Remove-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlan
```

<span data-ttu-id="611c8-111">DDoS 보호 계획은 가상 네트워크와 연결 되어 있는 경우 삭제할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-111">DDoS protection plans cannot be deleted if they are associated with a virtual network.</span></span> <span data-ttu-id="611c8-112">따라서 첫 번째 단계는 두 개체의 연관을 해제 하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-112">So the first step is to disassociate both objects.</span></span> <span data-ttu-id="611c8-113">여기서는 계획과 연결 된 가상 네트워크의 업데이트 버전을 **DdosProtectionPlan** 속성을 빈 값으로 설정 하 고 플래그 **EnableDdosProtection** (이 플래그는 계획 없이는 true 일 수 없습니다).</span><span class="sxs-lookup"><span data-stu-id="611c8-113">Here, we get the most updated version of the virtual network associated with the plan, and we set the property **DdosProtectionPlan** to an empty value and the flag **EnableDdosProtection** (this flag cannot be true without a plan).</span></span>
<span data-ttu-id="611c8-114">그런 다음 지역 변수를 **Set-AzureRmVirtualNetwork** 에 파이핑 하 여 새 상태를 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-114">Then, we persist the new state by piping the local variable into **Set-AzureRmVirtualNetwork**.</span></span> <span data-ttu-id="611c8-115">이 시점에서 계획이 더 이상 가상 네트워크에 연결 되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-115">At this point, the plan is no longer associated with the virtual network.</span></span>
<span data-ttu-id="611c8-116">이 계획이 계획에 연결 된 마지막 DDoS 경우 Remove-AzureRmDdosProtectionPlan 명령을 사용 하 여 보호 계획을 제거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-116">If this is the last one associated with the plan, we can remove the DDoS protection plan by using the command Remove-AzureRmDdosProtectionPlan.</span></span>

## <span data-ttu-id="611c8-117">변수</span><span class="sxs-lookup"><span data-stu-id="611c8-117">PARAMETERS</span></span>

### <span data-ttu-id="611c8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="611c8-118">-DefaultProfile</span></span>
<span data-ttu-id="611c8-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="611c8-120">-이름</span><span class="sxs-lookup"><span data-stu-id="611c8-120">-Name</span></span>
<span data-ttu-id="611c8-121">제거할 DDoS 보호 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-121">Specifies the name of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="611c8-122">-PassThru</span><span class="sxs-lookup"><span data-stu-id="611c8-122">-PassThru</span></span>
<span data-ttu-id="611c8-123">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-123">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="611c8-124">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-124">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="611c8-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="611c8-125">-ResourceGroupName</span></span>
<span data-ttu-id="611c8-126">제거할 DDoS protection 계획의 리소스 그룹을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-126">Specifies the resource group of the DDoS protection plan to be removed.</span></span>

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

### <span data-ttu-id="611c8-127">-확인</span><span class="sxs-lookup"><span data-stu-id="611c8-127">-Confirm</span></span>
<span data-ttu-id="611c8-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="611c8-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="611c8-129">-WhatIf</span></span>
<span data-ttu-id="611c8-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-130">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="611c8-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="611c8-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="611c8-132">CommonParameters</span></span>
<span data-ttu-id="611c8-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="611c8-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="611c8-134">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="611c8-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="611c8-135">입력</span><span class="sxs-lookup"><span data-stu-id="611c8-135">INPUTS</span></span>

### <span data-ttu-id="611c8-136">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="611c8-136">System.String</span></span>

## <span data-ttu-id="611c8-137">출력</span><span class="sxs-lookup"><span data-stu-id="611c8-137">OUTPUTS</span></span>

### <span data-ttu-id="611c8-138">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="611c8-138">System.Boolean</span></span>

## <span data-ttu-id="611c8-139">상속자</span><span class="sxs-lookup"><span data-stu-id="611c8-139">NOTES</span></span>

## <span data-ttu-id="611c8-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="611c8-140">RELATED LINKS</span></span>

[<span data-ttu-id="611c8-141">새로운 AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="611c8-141">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="611c8-142">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="611c8-142">Get-AzureRmDdosProtectionPlan</span></span>](./Get-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="611c8-143">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="611c8-143">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="611c8-144">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="611c8-144">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="611c8-145">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="611c8-145">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
