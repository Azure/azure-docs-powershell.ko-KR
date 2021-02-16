---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azddosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzDdosProtectionPlan.md
ms.openlocfilehash: a94ed627d50b8523157d52d3a9c2bf1f8ab29229
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100189801"
---
# <span data-ttu-id="fca1e-101">Get-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fca1e-101">Get-AzDdosProtectionPlan</span></span>

## <span data-ttu-id="fca1e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fca1e-102">SYNOPSIS</span></span>
<span data-ttu-id="fca1e-103">DDoS 보호 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-103">Gets a DDoS protection plan.</span></span>

## <span data-ttu-id="fca1e-104">구문</span><span class="sxs-lookup"><span data-stu-id="fca1e-104">SYNTAX</span></span>

```
Get-AzDdosProtectionPlan [-ResourceGroupName <String>] [-Name <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fca1e-105">설명</span><span class="sxs-lookup"><span data-stu-id="fca1e-105">DESCRIPTION</span></span>
<span data-ttu-id="fca1e-106">Get-AzDdosProtectionPlan cmdlet은 DDoS 보호 계획을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-106">The Get-AzDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="fca1e-107">예제</span><span class="sxs-lookup"><span data-stu-id="fca1e-107">EXAMPLES</span></span>

### <span data-ttu-id="fca1e-108">예제 1: 특정 DDoS 보호 계획 얻기</span><span class="sxs-lookup"><span data-stu-id="fca1e-108">Example 1: Get a specific DDoS protection plan</span></span>
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

<span data-ttu-id="fca1e-109">이 경우 리소스 그룹 및 DDoS 보호 계획의 이름에 해당하는 **ResourceGroupName** 및 **Name** 특성을 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-109">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="fca1e-110">예제 2: 리소스 그룹의 모든 DDoS 보호 계획 얻기</span><span class="sxs-lookup"><span data-stu-id="fca1e-110">Example 2: Get all DDoS protection plans in a resource group</span></span>
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

<span data-ttu-id="fca1e-111">이 시나리오에서는 **ResourceGroupName** 매개 변수만 지정하여 DDoS 보호 계획 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-111">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="fca1e-112">예제 3: 구독에서 모든 DDoS 보호 계획 확인</span><span class="sxs-lookup"><span data-stu-id="fca1e-112">Example 3: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="fca1e-113">여기서는 구독의 모든 DDoS 보호 계획 목록을 표시하는 매개 변수를 지정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-113">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

### <span data-ttu-id="fca1e-114">예제 4: 구독의 모든 DDoS 보호 계획 확인</span><span class="sxs-lookup"><span data-stu-id="fca1e-114">Example 4: Get all DDoS protection plans in a subscription</span></span>
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

<span data-ttu-id="fca1e-115">이 cmdlet은 "test"로 시작하는 모든 DdosProtectionPlans를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-115">This cmdlet returns all DdosProtectionPlans that start with "test".</span></span>

## <span data-ttu-id="fca1e-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fca1e-116">PARAMETERS</span></span>

### <span data-ttu-id="fca1e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fca1e-117">-DefaultProfile</span></span>
<span data-ttu-id="fca1e-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="fca1e-119">-Name</span><span class="sxs-lookup"><span data-stu-id="fca1e-119">-Name</span></span>
<span data-ttu-id="fca1e-120">DDoS 보호 계획의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-120">Specifies the name of the DDoS protection plan.</span></span>

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

### <span data-ttu-id="fca1e-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fca1e-121">-ResourceGroupName</span></span>
<span data-ttu-id="fca1e-122">DDoS 보호 계획 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-122">Specifies the name of the DDoS protection plan resource group.</span></span>

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

### <span data-ttu-id="fca1e-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fca1e-123">CommonParameters</span></span>
<span data-ttu-id="fca1e-124">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fca1e-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fca1e-125">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fca1e-125">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fca1e-126">입력</span><span class="sxs-lookup"><span data-stu-id="fca1e-126">INPUTS</span></span>

### <span data-ttu-id="fca1e-127">System.String</span><span class="sxs-lookup"><span data-stu-id="fca1e-127">System.String</span></span>

## <span data-ttu-id="fca1e-128">출력</span><span class="sxs-lookup"><span data-stu-id="fca1e-128">OUTPUTS</span></span>

### <span data-ttu-id="fca1e-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fca1e-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="fca1e-130">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fca1e-130">NOTES</span></span>

## <span data-ttu-id="fca1e-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fca1e-131">RELATED LINKS</span></span>

[<span data-ttu-id="fca1e-132">New-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fca1e-132">New-AzDdosProtectionPlan</span></span>](./New-AzDdosProtectionPlan.md)

[<span data-ttu-id="fca1e-133">Remove-AzDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="fca1e-133">Remove-AzDdosProtectionPlan</span></span>](./Remove-AzDdosProtectionPlan.md)

[<span data-ttu-id="fca1e-134">New-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fca1e-134">New-AzVirtualNetwork</span></span>](./New-AzVirtualNetwork.md)

[<span data-ttu-id="fca1e-135">Set-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fca1e-135">Set-AzVirtualNetwork</span></span>](./Set-AzVirtualNetwork.md)

[<span data-ttu-id="fca1e-136">Get-AzVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="fca1e-136">Get-AzVirtualNetwork</span></span>](./Get-AzVirtualNetwork.md)