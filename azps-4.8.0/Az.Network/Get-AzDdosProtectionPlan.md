---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94048940"
---
# <span data-ttu-id="4f33a-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4f33a-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="4f33a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f33a-102">SYNOPSIS</span></span>
<span data-ttu-id="4f33a-103">DDoS protection 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="4f33a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4f33a-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f33a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4f33a-105">DESCRIPTION</span></span>
<span data-ttu-id="4f33a-106">Get-AzDdosProtectionPlan cmdlet은 DDoS protection 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="4f33a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4f33a-107">EXAMPLES</span></span>

### <span data-ttu-id="4f33a-108">예제 1: 특정 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f33a-108">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="4f33a-109">이 경우에는 각각 리소스 그룹과 DDoS 보호 계획의 이름에 해당 하는 **ResourceGroupName** 및 **Name** 특성을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="4f33a-110">예제 2: 리소스 그룹에서 모든 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f33a-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzDdosProtectionPlan -ResourceGroupName ResourceGroupName


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="4f33a-111">이 시나리오에서는 DDoS protection 계획 목록을 가져오기 위한 **ResourceGroupName** 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="4f33a-112">예제 3: 구독에서 모든 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f33a-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan


Name              : DdosProtectionPlanName
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/DdosProtectionPlanName
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="4f33a-113">여기서는 구독에서 모든 DDoS 보호 계획 목록을 가져오기 위한 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="4f33a-114">예제 4: 구독에서 모든 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="4f33a-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzDdosProtectionPlan -Name test*


Name              : test1
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test1
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]

Name              : test2
Id                : /subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/ddosProtectionPlans/test2
Etag              : W/"a20e5592-9b51-423b-9758-b00cd322f744"
ProvisioningState : Succeeded
VirtualNetworks   : [
                      {
                        "Id": "/subscriptions/d1dbd366-9871-45ac-84b7-fb318152a9e0/resourceGroups/ResourceGroupName/providers/Microsoft.Network/virtualNetworks/VnetName"
                      }
                    ]
```

<span data-ttu-id="4f33a-115">이 cmdlet은 "test"로 시작 하는 모든 DdosProtectionPlans를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="4f33a-116">변수</span><span class="sxs-lookup"><span data-stu-id="4f33a-116">PARAMETERS</span></span>

### <span data-ttu-id="4f33a-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f33a-117">-DefaultProfile</span></span>
<span data-ttu-id="4f33a-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f33a-119">-이름</span><span class="sxs-lookup"><span data-stu-id="4f33a-119">-Name</span></span>
<span data-ttu-id="4f33a-120">DDoS 보호 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4f33a-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4f33a-121">-ResourceGroupName</span></span>
<span data-ttu-id="4f33a-122">DDoS protection 계획 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="4f33a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f33a-123">CommonParameters</span></span>
<span data-ttu-id="4f33a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f33a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f33a-125">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4f33a-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f33a-126">입력</span><span class="sxs-lookup"><span data-stu-id="4f33a-126">INPUTS</span></span>

### <span data-ttu-id="4f33a-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4f33a-127">System.String</span></span>

## <span data-ttu-id="4f33a-128">출력</span><span class="sxs-lookup"><span data-stu-id="4f33a-128">OUTPUTS</span></span>

### <span data-ttu-id="4f33a-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4f33a-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="4f33a-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4f33a-130">NOTES</span></span>

## <span data-ttu-id="4f33a-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f33a-131">RELATED LINKS</span></span>

[<span data-ttu-id="4f33a-132">새로운 AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4f33a-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="4f33a-133">제거-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="4f33a-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="4f33a-134">새로운 AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f33a-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="4f33a-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f33a-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="4f33a-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="4f33a-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)