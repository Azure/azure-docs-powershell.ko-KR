---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-aznatgateway
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzNatGateway.md
ms.openlocfilehash: f52f6a2872d6f7567a51e1433336ccb8e1629fdb
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93870685"
---
# <span data-ttu-id="47cf5-101">Get-AzNatGateway</span><span class="sxs-lookup"><span data-stu-id="47cf5-101">Get-AzNatGateway</span></span>

## <span data-ttu-id="47cf5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47cf5-102">SYNOPSIS</span></span>
<span data-ttu-id="47cf5-103">리소스 그룹에서 이름 또는 NatGateway Id 또는 리소스 그룹의 모든 Nat 게이트웨이 리소스를 기준으로 Nat 게이트웨이 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-103">Gets a Nat Gateway resource in a resource group by name or NatGateway Id  or all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="47cf5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="47cf5-104">SYNTAX</span></span>

### <span data-ttu-id="47cf5-105">ListParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="47cf5-105">ListParameterSet (Default)</span></span>
```
Get-AzNatGateway [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="47cf5-106">GetByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="47cf5-106">GetByNameParameterSet</span></span>
```
Get-AzNatGateway -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="47cf5-107">GetByResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47cf5-107">GetByResourceIdParameterSet</span></span>
```
Get-AzNatGateway -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="47cf5-108">설명은</span><span class="sxs-lookup"><span data-stu-id="47cf5-108">DESCRIPTION</span></span>
<span data-ttu-id="47cf5-109">리소스 그룹에서 이름 또는 NatGateway Id 또는 리소스 그룹의 모든 Nat 게이트웨이 리소스를 기준으로 Nat 게이트웨이 리소스를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-109">Gets a Nat Gateway resource in a resource group by name OR NatGateway Id OR all Nat Gateway resources in a resource group.</span></span>

## <span data-ttu-id="47cf5-110">예제의</span><span class="sxs-lookup"><span data-stu-id="47cf5-110">EXAMPLES</span></span>

### <span data-ttu-id="47cf5-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="47cf5-111">Example 1</span></span>
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

## <span data-ttu-id="47cf5-112">변수</span><span class="sxs-lookup"><span data-stu-id="47cf5-112">PARAMETERS</span></span>

### <span data-ttu-id="47cf5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47cf5-113">-DefaultProfile</span></span>
<span data-ttu-id="47cf5-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47cf5-115">-이름</span><span class="sxs-lookup"><span data-stu-id="47cf5-115">-Name</span></span>
<span data-ttu-id="47cf5-116">Nat 게이트웨이의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-116">The name of the nat gateway.</span></span>

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

### <span data-ttu-id="47cf5-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47cf5-117">-ResourceGroupName</span></span>
<span data-ttu-id="47cf5-118">Nat 게이트웨이의 리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-118">The resource group name of the nat gateway.</span></span>

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

### <span data-ttu-id="47cf5-119">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="47cf5-119">-ResourceId</span></span>
<span data-ttu-id="47cf5-120">Nat 게이트웨이 Id</span><span class="sxs-lookup"><span data-stu-id="47cf5-120">Nat Gateway Id</span></span>

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

### <span data-ttu-id="47cf5-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47cf5-121">CommonParameters</span></span>
<span data-ttu-id="47cf5-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="47cf5-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47cf5-123">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="47cf5-123">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47cf5-124">입력</span><span class="sxs-lookup"><span data-stu-id="47cf5-124">INPUTS</span></span>

### <span data-ttu-id="47cf5-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="47cf5-125">System.String</span></span>

## <span data-ttu-id="47cf5-126">출력</span><span class="sxs-lookup"><span data-stu-id="47cf5-126">OUTPUTS</span></span>

### <span data-ttu-id="47cf5-127">Microsoft. \* .Patgateway.</span><span class="sxs-lookup"><span data-stu-id="47cf5-127">Microsoft.Azure.Commands.Network.Models.PSNatGateway</span></span>

## <span data-ttu-id="47cf5-128">상속자</span><span class="sxs-lookup"><span data-stu-id="47cf5-128">NOTES</span></span>

## <span data-ttu-id="47cf5-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="47cf5-129">RELATED LINKS</span></span>
