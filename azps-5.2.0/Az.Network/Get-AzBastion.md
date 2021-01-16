---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Network.dll-Help.xml
Module Name: Az.Network
online version: https://docs.microsoft.com/en-us/powershell/module/az.network/get-azbastion
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Network/Network/help/Get-AzBastion.md
ms.openlocfilehash: eedb6c593ecb430916815ea9a68eae387ebe92fe
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98338102"
---
# <span data-ttu-id="0884c-101">Get-AzBastion</span><span class="sxs-lookup"><span data-stu-id="0884c-101">Get-AzBastion</span></span>

## <span data-ttu-id="0884c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0884c-102">SYNOPSIS</span></span>
<span data-ttu-id="0884c-103">배스션 리소스 또는 배스션 리소스를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-103">Gets a Bastion resource or Bastion resources.</span></span>

## <span data-ttu-id="0884c-104">구문</span><span class="sxs-lookup"><span data-stu-id="0884c-104">SYNTAX</span></span>

### <span data-ttu-id="0884c-105">ListBySubscriptionId(기본값)</span><span class="sxs-lookup"><span data-stu-id="0884c-105">ListBySubscriptionId (Default)</span></span>
```
Get-AzBastion [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0884c-106">ListByResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0884c-106">ListByResourceGroupName</span></span>
```
Get-AzBastion [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0884c-107">ByResourceGroupNameByName</span><span class="sxs-lookup"><span data-stu-id="0884c-107">ByResourceGroupNameByName</span></span>
```
Get-AzBastion -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0884c-108">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="0884c-108">ByResourceId</span></span>
```
Get-AzBastion -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0884c-109">설명</span><span class="sxs-lookup"><span data-stu-id="0884c-109">DESCRIPTION</span></span>
<span data-ttu-id="0884c-110">**Get-Bastion** cmdlet은 리소스 그룹 또는 하위 작업에서 하나 이상의 Bastion을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-110">The **Get-Bastion** cmdlet gets one or more bastions in a resource group or subscritption.</span></span>

## <span data-ttu-id="0884c-111">예제</span><span class="sxs-lookup"><span data-stu-id="0884c-111">EXAMPLES</span></span>

### <span data-ttu-id="0884c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="0884c-112">Example 1</span></span>
```powershell
Get-AzBastion

ResourceGroupName    : abagarwaProd-PPTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : abagarwaProd-PPTest-vnet-bastion
Etag                 : W/"55702e34-348f-4b79-bf44-9c306623b7c7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/abagarwaProd-PPTest/providers/Microsoft.Network/bastionHosts/abagarwaProd-PPTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-f594cc74-c21e-44c3-ad5e-5bb93933965f.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"7ae27d14-9260-4e2d-8c48-47e9628a3e3b\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/virtualNetworks/BastionTest-vnet/subnets/default"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/publicIPAddresses/BastionTest-vnet-ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionTest
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  : {}
TagsTable            :
Name                 : BastionTest-vnet-bastion
Etag                 : W/"7ae27d14-9260-4e2d-8c48-47e9628a3e3b"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionTest/providers/Microsoft.Network/bastionHosts/BastionTest-vnet-bastion

IpConfigurations     : {IpConf}
DnsName              : bst-32359e0c-d6a5-45f1-b196-2f9a4b4b77e8.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"bd537319-3379-4caf-a8dc-be4506f9dd3a\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/virtualNetworks/ps7070/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/publicIPAddresses/ps2217"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps1621
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps5581
Etag                 : W/"bd537319-3379-4caf-a8dc-be4506f9dd3a"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps1621/providers/Microsoft.Network/bastionHosts/ps5581

IpConfigurations     : {IpConf}
DnsName              : bst-aee29973-3b60-44c1-a1de-bd8636e79127.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"42f723dd-f1de-4fd0-b307-3fe82f0b50f7\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/virtualNetworks/ps5766/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/publicIPAddresses/ps2773"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : ps3151
Location             : westcentralus
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : ps8815
Etag                 : W/"42f723dd-f1de-4fd0-b307-3fe82f0b50f7"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3151/providers/Microsoft.Network/bastionHosts/ps8815

IpConfigurations     : {IpConf}
DnsName              : bst-746c229d-f144-4699-a7ea-303a15a70457.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"0b11e3e7-330b-4727-b073-dfe458429fcf\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/bastionHosts/ps7790/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/virtualNetworks/ps7582/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/ps3429/providers/Microsoft.Network/publicIPAddresses/ps8199"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
```

### <span data-ttu-id="0884c-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="0884c-113">Example 2</span></span>
```powershell
Get-AzBastion -ResourceGroupName "BastionPowershellTest" -Name "testBastion"

IpConfigurations     : {IpConf}
DnsName              : bst-0597f607-ab71-46c2-ab2a-777bfa887aff.bastion.azure.com
ProvisioningState    : Succeeded
IpConfigurationsText : [
                         {
                           "Name": "IpConf",
                           "Etag": "W/\"4d023823-3ea8-439a-ac00-20f16fb0c9b2\"",
                           "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion/bastionHostIpConfigurations/IpConf",
                           "Subnet": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/virtualNetworks/TestVnet/subnets/AzureBastionSubnet"
                           },
                           "PublicIpAddress": {
                             "Id": "/subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/publicIPAddresses/Test-Ip"
                           },
                           "ProvisioningState": "Succeeded",
                           "PrivateIpAllocationMethod": "Dynamic"
                         }
                       ]
ResourceGroupName    : BastionPowershellTest
Location             : westeurope
ResourceGuid         :
Type                 : Microsoft.Network/bastionHosts
Tag                  :
TagsTable            :
Name                 : testBastion
Etag                 : W/"4d023823-3ea8-439a-ac00-20f16fb0c9b2"
Id                   : /subscriptions/359a08a9-ff1b-463c-92d7-6df8d946f25c/resourceGroups/BastionPowershellTest/providers/Microsoft.Network/bastionHosts/testBastion
```

## <span data-ttu-id="0884c-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="0884c-114">PARAMETERS</span></span>

### <span data-ttu-id="0884c-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="0884c-115">-Confirm</span></span>
<span data-ttu-id="0884c-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0884c-117">-DefaultProfile</span></span>
<span data-ttu-id="0884c-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-119">-Name</span><span class="sxs-lookup"><span data-stu-id="0884c-119">-Name</span></span>
<span data-ttu-id="0884c-120">배스션 리소스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-120">The bastion resource name.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases: ResourceName, BastionName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0884c-121">-ResourceGroupName</span></span>
<span data-ttu-id="0884c-122">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-122">The resource group name.</span></span>

```yaml
Type: String
Parameter Sets: ListByResourceGroupName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: ByResourceGroupNameByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0884c-123">-ResourceId</span></span>
<span data-ttu-id="0884c-124">Bastion Azure 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="0884c-124">The bastion Azure resource Id</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0884c-125">-WhatIf</span></span>
<span data-ttu-id="0884c-126">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="0884c-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0884c-127">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0884c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0884c-128">CommonParameters</span></span>
<span data-ttu-id="0884c-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="0884c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0884c-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="0884c-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0884c-131">입력</span><span class="sxs-lookup"><span data-stu-id="0884c-131">INPUTS</span></span>

### <span data-ttu-id="0884c-132">없음</span><span class="sxs-lookup"><span data-stu-id="0884c-132">None</span></span>

## <span data-ttu-id="0884c-133">출력</span><span class="sxs-lookup"><span data-stu-id="0884c-133">OUTPUTS</span></span>

### <span data-ttu-id="0884c-134">Microsoft.Azure.Commands.Network.Models.PSBastion</span><span class="sxs-lookup"><span data-stu-id="0884c-134">Microsoft.Azure.Commands.Network.Models.PSBastion</span></span>

### <span data-ttu-id="0884c-135">System.Collections.Generic.IEnumerable'1[[Microsoft.Azure.Commands.Network.Models.PSBastion, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.13.0.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="0884c-135">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.Network.Models.PSBastion, Microsoft.Azure.PowerShell.Cmdlets.Network, Version=1.13.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="0884c-136">참고 사항</span><span class="sxs-lookup"><span data-stu-id="0884c-136">NOTES</span></span>

## <span data-ttu-id="0884c-137">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0884c-137">RELATED LINKS</span></span>
[<span data-ttu-id="0884c-138">New-AzBastion</span><span class="sxs-lookup"><span data-stu-id="0884c-138">New-AzBastion</span></span>](./New-AzBastion.md)

[<span data-ttu-id="0884c-139">Remove-AzBastion</span><span class="sxs-lookup"><span data-stu-id="0884c-139">Remove-AzBastion</span></span>](./Remove-AzBastion.md)
