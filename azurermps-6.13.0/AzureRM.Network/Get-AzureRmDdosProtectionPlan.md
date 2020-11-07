---
external help file: Microsoft.Azure.Commands.Network.dll-Help.xml
Module Name: AzureRM.Network
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.network/get-azuredosprotectionplan
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Network/Commands.Network/help/Get-AzureRmDdosProtectionPlan.md
ms.openlocfilehash: 2d1942dd5c069660d062922a069cc88b505748fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703443"
---
# <span data-ttu-id="5d032-101">Get-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5d032-101">Get-AzureRmDdosProtectionPlan</span></span>

## <span data-ttu-id="5d032-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d032-102">SYNOPSIS</span></span>
<span data-ttu-id="5d032-103">DDoS protection 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-103">Gets a DDoS protection plan.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="5d032-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5d032-104">SYNTAX</span></span>

### <span data-ttu-id="5d032-105">GetByNameAndGroup</span><span class="sxs-lookup"><span data-stu-id="5d032-105">GetByNameAndGroup</span></span>
```
Get-AzureRmDdosProtectionPlan -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5d032-106">목록</span><span class="sxs-lookup"><span data-stu-id="5d032-106">List</span></span>
```
Get-AzureRmDdosProtectionPlan [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5d032-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5d032-107">DESCRIPTION</span></span>
<span data-ttu-id="5d032-108">Get-AzureRmDdosProtectionPlan cmdlet은 DDoS protection 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-108">The Get-AzureRmDdosProtectionPlan cmdlet gets a DDoS protection plan.</span></span>

## <span data-ttu-id="5d032-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5d032-109">EXAMPLES</span></span>

### <span data-ttu-id="5d032-110">예제 1: 특정 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d032-110">Example 1: Get a specific DDoS protection plan</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName -Name DdosProtectionPlanName


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

<span data-ttu-id="5d032-111">이 경우에는 각각 리소스 그룹과 DDoS 보호 계획의 이름에 해당 하는 **ResourceGroupName** 및 **Name** 특성을 모두 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-111">In this case, we need to specify both **ResourceGroupName** and **Name** attributes, which correspond to the resource group and the name of the DDoS protection plan, respectively.</span></span>

### <span data-ttu-id="5d032-112">예제 2: 리소스 그룹에서 모든 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d032-112">Example 2: Get all DDoS protection plans in a resource group</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan -ResourceGroupName ResourceGroupName


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

<span data-ttu-id="5d032-113">이 시나리오에서는 DDoS protection 계획 목록을 가져오기 위한 **ResourceGroupName** 매개 변수만 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-113">In this scenario, we only specify the parameter **ResourceGroupName** to get a list of DDoS protection plans.</span></span>

### <span data-ttu-id="5d032-114">예제 2: 구독에서 모든 DDoS 보호 계획 가져오기</span><span class="sxs-lookup"><span data-stu-id="5d032-114">Example 2: Get all DDoS protection plans in a subscription</span></span>
```
D:\> Get-AzureRmDdosProtectionPlan


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

<span data-ttu-id="5d032-115">여기서는 구독에서 모든 DDoS 보호 계획 목록을 가져오기 위한 매개 변수를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-115">Here, we do not specify any parameters to get a list of all DDoS protection plans in a subscription.</span></span>

## <span data-ttu-id="5d032-116">변수</span><span class="sxs-lookup"><span data-stu-id="5d032-116">PARAMETERS</span></span>

### <span data-ttu-id="5d032-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d032-117">-DefaultProfile</span></span>
<span data-ttu-id="5d032-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5d032-119">-이름</span><span class="sxs-lookup"><span data-stu-id="5d032-119">-Name</span></span>
<span data-ttu-id="5d032-120">DDoS 보호 계획의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-120">Specifies the name of the DDoS protection plan.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d032-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d032-121">-ResourceGroupName</span></span>
<span data-ttu-id="5d032-122">DDoS protection 계획 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-122">Specifies the name of the DDoS protection plan resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndGroup
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d032-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d032-123">CommonParameters</span></span>
<span data-ttu-id="5d032-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5d032-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d032-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5d032-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d032-126">입력</span><span class="sxs-lookup"><span data-stu-id="5d032-126">INPUTS</span></span>

### <span data-ttu-id="5d032-127">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5d032-127">System.String</span></span>

## <span data-ttu-id="5d032-128">출력</span><span class="sxs-lookup"><span data-stu-id="5d032-128">OUTPUTS</span></span>

### <span data-ttu-id="5d032-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5d032-129">Microsoft.Azure.Commands.Network.Models.PSDdosProtectionPlan</span></span>

## <span data-ttu-id="5d032-130">상속자</span><span class="sxs-lookup"><span data-stu-id="5d032-130">NOTES</span></span>

## <span data-ttu-id="5d032-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d032-131">RELATED LINKS</span></span>

[<span data-ttu-id="5d032-132">새로운 AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5d032-132">New-AzureRmDdosProtectionPlan</span></span>](./New-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="5d032-133">제거-AzureRmDdosProtectionPlan</span><span class="sxs-lookup"><span data-stu-id="5d032-133">Remove-AzureRmDdosProtectionPlan</span></span>](./Remove-AzureRmDdosProtectionPlan.md)

[<span data-ttu-id="5d032-134">새로운 AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d032-134">New-AzureRmVirtualNetwork</span></span>](./New-AzureRmVirtualNetwork.md)

[<span data-ttu-id="5d032-135">Set-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d032-135">Set-AzureRmVirtualNetwork</span></span>](./Set-AzureRmVirtualNetwork.md)

[<span data-ttu-id="5d032-136">Get-AzureRmVirtualNetwork</span><span class="sxs-lookup"><span data-stu-id="5d032-136">Get-AzureRmVirtualNetwork</span></span>](./Get-AzureRmVirtualNetwork.md)
