---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: 0feaa59a6af5610a7dbdef555c8baebdba9abe54
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102006379"
---
# <span data-ttu-id="7409a-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="7409a-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="7409a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7409a-102">SYNOPSIS</span></span>
<span data-ttu-id="7409a-103">리소스 그룹의 이름 또는 NatGateway ID 또는 리소스 그룹의 모든 Nat Gateway 리소스를 리소스 그룹에서 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="7409a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7409a-104">SYNTAX</span></span>

### <span data-ttu-id="7409a-105">ListParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7409a-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7409a-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="7409a-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7409a-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7409a-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7409a-108">설명</span><span class="sxs-lookup"><span data-stu-id="7409a-108">DESCRIPTION</span></span>
<span data-ttu-id="7409a-109">리소스 그룹의 이름 또는 NatGateway ID 또는 리소스 그룹의 모든 Nat Gateway 리소스를 이름으로 리소스 그룹에서 Nat Gateway 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="7409a-110">예제</span><span class="sxs-lookup"><span data-stu-id="7409a-110">EXAMPLES</span></span>

### <span data-ttu-id="7409a-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7409a-111">Example 1</span></span>
```powershell
PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : []
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : ng1
Etag                  : W/"bdf98e30-d6c6-4af2-8f62-10d1fdaa6e84"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/ng1


PS C:> Get-AzNatGateway -ResourceGroupName "natgateway_test" -Name "nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway

PS C:> Get-AzNatGateway -ResourceId "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway"


IdleTimeoutInMinutes  : 4
ProvisioningState     : Succeeded
Sku                   : Microsoft.Azure.Commands.Network.Models.PSNatGatewaySku
PublicIpAddresses     : {/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip}
PublicIpPrefixes      : {}
SkuText               : {
                          "Name": "Standard"
                        }
PublicIpAddressesText : [
                          {
                            "Id": "/subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/publicIPAddresses/Test_Pip"
                          }
                        ]
PublicIpPrefixesText  : []
ResourceGroupName     : natgateway_test
Location              : eastus2
ResourceGuid          :
Type                  : Microsoft.Network/natGateways
Tag                   :
TagsTable             :
Name                  : nat_gateway
Etag                  : W/"178470d2-7b86-4ddd-b954-e0cd3ab30a90"
Id                    : /subscriptions/<subid>/resourceGroups/natgateway_test/providers/Microsoft.Network/natGateways/nat_gateway
```

## <span data-ttu-id="7409a-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7409a-112">PARAMETERS</span></span>

### <span data-ttu-id="7409a-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7409a-113">-DefaultProfile</span></span>
<span data-ttu-id="7409a-114">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7409a-115">-Name</span><span class="sxs-lookup"><span data-stu-id="7409a-115">-Name</span></span>
<span data-ttu-id="7409a-116">nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-116">The name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases: ResourceName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7409a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7409a-117">-ResourceGroupName</span></span>
<span data-ttu-id="7409a-118">nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-118">The resource group name of the nat gateway.</span></span>

```yaml
Type: System.String
Parameter Sets: ListParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7409a-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="7409a-119">-ResourceId</span></span>
<span data-ttu-id="7409a-120">Nat Gateway Id</span><span class="sxs-lookup"><span data-stu-id="7409a-120">Nat Gateway Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7409a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7409a-121">CommonParameters</span></span>
<span data-ttu-id="7409a-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7409a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7409a-123">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7409a-123">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7409a-124">입력</span><span class="sxs-lookup"><span data-stu-id="7409a-124">INPUTS</span></span>

### <span data-ttu-id="7409a-125">System.String</span><span class="sxs-lookup"><span data-stu-id="7409a-125">System.String</span></span>

## <span data-ttu-id="7409a-126">출력</span><span class="sxs-lookup"><span data-stu-id="7409a-126">OUTPUTS</span></span>

### <span data-ttu-id="7409a-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span><span class="sxs-lookup"><span data-stu-id="7409a-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="7409a-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7409a-128">NOTES</span></span>

## <span data-ttu-id="7409a-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7409a-129">RELATED LINKS</span></span>
