---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: b2881c735caae8f644676b1ee19cb0d80725c13a
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98370623"
---
# <span data-ttu-id="4b2ec-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="4b2ec-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="4b2ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4b2ec-102">SYNOPSIS</span></span>
<span data-ttu-id="4b2ec-103">Get-AzPolicyAlias 정의되고 주어진 매개 변수 값과 일치하는 Azure 공급자 리소스 유형을 검색하고 출력합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="4b2ec-104">매개 변수가 제공되지 않는 경우 별칭을 포함하는 모든 공급자 리소스 종류가 출력됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="4b2ec-105">-ListAvailable 스위치는 별칭이 없는 리소스를 포함하여 일치하는 모든 리소스 유형을 나열하여 이 동작을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="4b2ec-106">구문</span><span class="sxs-lookup"><span data-stu-id="4b2ec-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4b2ec-107">설명</span><span class="sxs-lookup"><span data-stu-id="4b2ec-107">DESCRIPTION</span></span>
<span data-ttu-id="4b2ec-108">**Get-AzPolicyAlias** cmdlet은 정책 별칭 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="4b2ec-109">정책 별칭은 Azure Policy에서 리소스 종류 속성을 참조하는 데 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="4b2ec-110">리소스 형식 또는 해당 별칭의 다양한 속성을 일치하여 목록의 항목을 제한하는 매개 변수가 제공됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="4b2ec-111">대상 문자열에 대소문자 무관한 비교를 사용하여 포함된 경우 지정한 일치 값이 일치합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="4b2ec-112">예제</span><span class="sxs-lookup"><span data-stu-id="4b2ec-112">EXAMPLES</span></span>

### <span data-ttu-id="4b2ec-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="4b2ec-113">Example 1</span></span>
```powershell
PS C:\> Get-AzPolicyAlias

Namespace                     ResourceType                                   Aliases
---------                     ------------                                   -------
Microsoft.AnalysisServices    servers                                        {Microsoft.AnalysisServices/servers/state, Microsoft.AnalysisServices/s...
Microsoft.Authorization       roleAssignments                                {Microsoft.Authorization/roleAssignments/roleDefinitionId, Microsoft.Au...
Microsoft.Authorization       roleDefinitions                                {Microsoft.Authorization/roleDefinitions/type, Microsoft.Authorization/...

...                           ...                                            ...

Microsoft.Web                 hostingEnvironments                            {Microsoft.Web/hostingEnvironments/clusterSettings[*].name, Microsoft.W...
Microsoft.Web                 sites/config                                   {Microsoft.Web/sites/config/httpLoggingEnabled, Microsoft.Web/sites/con...
Microsoft.GuestConfiguration  guestConfigurationAssignments                  {Microsoft.GuestConfiguration/guestConfigurationAssignments/complianceS...


PS C:\>
```

<span data-ttu-id="4b2ec-114">별칭이 있는 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="4b2ec-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="4b2ec-115">Example 2</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ListAvailable

Namespace                                ResourceType                                                        Aliases
---------                                ------------                                                        -------

...                                      ...                                                                 ...

Microsoft.AlertsManagement               operations                                                          {}
Microsoft.AnalysisServices               servers                                                             {Microsoft.AnalysisServices/servers/sta...
Microsoft.AnalysisServices               locations                                                           {}

...                                      ...                                                                 ...


PS C:\>
```

<span data-ttu-id="4b2ec-116">별칭이 없는 리소스를 포함하여 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="4b2ec-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="4b2ec-117">Example 3</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...
Microsoft.Compute disks                              {Microsoft.Compute/imagePublisher, Microsoft.Compute/imageOffer, Microsoft.Compute/imageSku, Mi...


PS C:\>
```

<span data-ttu-id="4b2ec-118">네임스페이스가 'compute'과 일치하고 별칭을 포함하는 모든 공급자 리소스 유형을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="4b2ec-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="4b2ec-119">Example 4</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual'

Namespace         ResourceType                           Aliases
---------         ------------                           -------
Microsoft.Compute virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Micro...
Microsoft.Compute virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualM...
Microsoft.Compute virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleS...
Microsoft.Compute virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/...
Microsoft.Network virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGateway...
Microsoft.Network virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetworks...
Microsoft.Network virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql     servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers/vi...


PS C:\>
```

<span data-ttu-id="4b2ec-120">리소스 종류가 'virtual'과 일치하고 별칭을 포함하는 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="4b2ec-121">예제 5</span><span class="sxs-lookup"><span data-stu-id="4b2ec-121">Example 5</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ResourceTypeMatch 'virtual' -ListAvailable

Namespace                    ResourceType                                               Aliases
---------                    ------------                                               -------

...                          ...                                                        ...

Microsoft.KeyVault           locations/deleteVirtualNetworkOrSubnets                    {}
Microsoft.Network            virtualNetworks                                            {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id,...
Microsoft.Network            virtualNetworkGateways                                     {Microsoft.Network/virtualNetworkGateways/sku.name, Microsof...
Microsoft.Network            locations/virtualNetworkAvailableEndpointServices          {}

...                          ...                                                        ...


PS C:\>
```

<span data-ttu-id="4b2ec-122">별칭이 없는 리소스를 포함하여 리소스 종류가 '가상'에 일치하는 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="4b2ec-123">예제 6</span><span class="sxs-lookup"><span data-stu-id="4b2ec-123">Example 6</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -NamespaceMatch 'compute' -ResourceTypeMatch 'virtual'

Namespace         ResourceType                       Aliases
---------         ------------                       -------
Microsoft.Compute virtualMachines                    {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Microsoft...
Microsoft.Compute virtualMachines/extensions         {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtualMachi...
Microsoft.Compute virtualMachineScaleSets            {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineScaleSets/...
Microsoft.Compute virtualMachineScaleSets/extensions {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compute/virt...


PS C:\>
```

<span data-ttu-id="4b2ec-124">네임스페이스가 'compute'과 일치하고 리소스 종류가 'virtual'과 일치하고 별칭을 포함하는 모든 공급자 리소스 유형을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="4b2ec-125">참고: -NamespaceMatch 및 -ResourceTypeMatch는 배타적 일치를 제공하는 반면 다른 일치는 포괄적입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="4b2ec-126">예제 7</span><span class="sxs-lookup"><span data-stu-id="4b2ec-126">Example 7</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="4b2ec-127">'virtual'에 일치하는 별칭을 포함하는 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="4b2ec-128">예제 8</span><span class="sxs-lookup"><span data-stu-id="4b2ec-128">Example 8</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -AliasMatch 'virtual' -PathMatch 'network'

Namespace            ResourceType                           Aliases
---------            ------------                           -------
Microsoft.Compute    virtualMachines                        {Microsoft.Compute/licenseType, Microsoft.Compute/virtualMachines/availabilitySet.id, Mi...
Microsoft.Compute    virtualMachines/extensions             {Microsoft.Compute/virtualMachines/extensions/provisioningState, Microsoft.Compute/virtu...
Microsoft.Compute    virtualMachineScaleSets                {Microsoft.Compute/VirtualMachineScaleSets/sku.name, Microsoft.Compute/VirtualMachineSca...
Microsoft.Compute    virtualMachineScaleSets/extensions     {Microsoft.Compute/virtualMachineScaleSets/extensions/provisioningState, Microsoft.Compu...
Microsoft.DocumentDB databaseAccounts                       {Microsoft.DocumentDB/databaseAccounts/sku.name, Microsoft.DocumentDB/databaseAccounts/v...
Microsoft.HDInsight  clusters                               {Microsoft.HDInsight/clusters/clusterVersion, Microsoft.HDInsight/clusters/osType, Micro...
Microsoft.KeyVault   vaults                                 {Microsoft.KeyVault/vaults/sku.name, Microsoft.KeyVault/vaults/sku.family, Microsoft.Key...
Microsoft.Network    virtualNetworks                        {Microsoft.Network/virtualNetworks/subnets[*].routeTable.id, Microsoft.Network/virtualNe...
Microsoft.Network    networkInterfaces                      {Microsoft.Network/networkInterfaces/ipconfigurations[*].subnet.id, Microsoft.Network/ne...
Microsoft.Network    networkSecurityGroups                  {Microsoft.Network/networkSecurityGroups/securityRules[*].protocol, Microsoft.Network/ne...
Microsoft.Network    virtualNetworkGateways                 {Microsoft.Network/virtualNetworkGateways/sku.name, Microsoft.Network/virtualNetworkGate...
Microsoft.Network    virtualNetworks/subnets                {Microsoft.Network/virtualNetworks/subnets/routeTable.id, Microsoft.Network/virtualNetwo...
Microsoft.Network    virtualNetworks/virtualNetworkPeerings {Microsoft.Network/virtualNetworks/virtualNetworkPeerings/remoteVirtualNetwork.id}
Microsoft.Sql        servers/virtualNetworkRules            {Microsoft.Sql/servers/virtualNetworkRules/virtualNetworkSubnetId, Microsoft.Sql/servers...
Microsoft.Storage    storageAccounts                        {Microsoft.Storage/storageAccounts/accountType, Microsoft.Storage/storageAccounts/sku.na...


PS C:\>
```

<span data-ttu-id="4b2ec-129">'virtual'와 일치하는 별칭을 포함하는 모든 공급자 리소스 종류 또는 경로가 '네트워크'와 일치하는 별칭을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="4b2ec-130">예제 9</span><span class="sxs-lookup"><span data-stu-id="4b2ec-130">Example 9</span></span>
```powershell
PS C:\> Get-AzPolicyAlias -ApiVersionMatch 'alpha'

Namespace          ResourceType        Aliases
---------          ------------        -------
Microsoft.Cache    Redis               {Microsoft.Cache/Redis/sku.name, Microsoft.Cache/Redis/sku.family, Microsoft.Cache/Redis/sku.capacity, Micros...
Microsoft.Cache    Redis/firewallrules {Microsoft.Cache/Redis/firewallrules/startIP, Microsoft.Cache/Redis/firewallrules/endIP}
Microsoft.Security alerts              {Microsoft.Security/alerts/state}
Microsoft.Security pricings            {Microsoft.Security/pricings/pricingTier}
Microsoft.Security complianceResults   {Microsoft.Security/complianceResults/resourceStatus}


PS C:\>
```

<span data-ttu-id="4b2ec-131">알파 API 버전 또는 알파 API 버전이 있는 별칭을 포함하는 모든 공급자 리소스 종류를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="4b2ec-132">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4b2ec-132">PARAMETERS</span></span>

### <span data-ttu-id="4b2ec-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-133">-AliasMatch</span></span>
<span data-ttu-id="4b2ec-134">이름이 이 값과 일치하는 별칭이 있는 출력 항목에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-134">Includes in the output items with aliases whose name matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Alias

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="4b2ec-135">-ApiVersion</span></span>
<span data-ttu-id="4b2ec-136">설정되면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="4b2ec-137">지정하지 않으면 API 버전이 사용 가능한 최신 버전으로 자동으로 결정됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-137">If not specified, the API version is automatically determined as the latest available.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-138">-ApiVersionMatch</span></span>
<span data-ttu-id="4b2ec-139">리소스 종류 또는 별칭에 일치하는 API 버전이 있는 출력 항목에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4b2ec-140">-DefaultProfile</span></span>
<span data-ttu-id="4b2ec-141">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="4b2ec-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="4b2ec-142">-ListAvailable</span></span>
<span data-ttu-id="4b2ec-143">별칭을 포함 또는 포함하지 않고 일치하는 항목을 출력에 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-143">Includes in the output matching items with and without aliases.</span></span>


```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: ShowAll

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-144">-LocationMatch</span></span>
<span data-ttu-id="4b2ec-145">리소스 종류에 일치하는 위치가 있는 출력 항목에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-145">Includes in the output items whose resource types have a matching location.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Location

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-146">-NamespaceMatch</span></span>
<span data-ttu-id="4b2ec-147">네임스페이스가 이 값과 일치하는 항목으로 출력을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-147">Limits the output to items whose namespace matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name, Namespace

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-148">-PathMatch</span></span>
<span data-ttu-id="4b2ec-149">이 값과 일치하는 경로를 포함하는 별칭이 있는 출력 항목에 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Path

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="4b2ec-150">-Pre</span></span>
<span data-ttu-id="4b2ec-151">설정하면 사용할 버전을 자동으로 결정할 때 cmdlet이 릴리스 전 API 버전을 사용해야 한다고 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="4b2ec-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="4b2ec-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="4b2ec-153">리소스 종류가 이 값과 일치하는 항목으로 출력을 제한합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-153">Limits the output to items whose resource type matches this value.</span></span>


```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceType, Resource

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4b2ec-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4b2ec-154">CommonParameters</span></span>
<span data-ttu-id="4b2ec-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4b2ec-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4b2ec-157">입력</span><span class="sxs-lookup"><span data-stu-id="4b2ec-157">INPUTS</span></span>

### <span data-ttu-id="4b2ec-158">없음</span><span class="sxs-lookup"><span data-stu-id="4b2ec-158">None</span></span>

## <span data-ttu-id="4b2ec-159">출력</span><span class="sxs-lookup"><span data-stu-id="4b2ec-159">OUTPUTS</span></span>

### <span data-ttu-id="4b2ec-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span><span class="sxs-lookup"><span data-stu-id="4b2ec-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="4b2ec-161">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4b2ec-161">NOTES</span></span>

* <span data-ttu-id="4b2ec-162">별칭 또는 다른 속성을 확장하기 위해 출력을 `select -ExpandProperty <property>` 에 파이프합니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="4b2ec-163">예를 들어: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="4b2ec-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="4b2ec-164">추가 속성은 출력에서 사용할 수 있으며 출력을 에 파이핑하여 표시할 수 `Format-List` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4b2ec-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="4b2ec-165">예를 들어: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="4b2ec-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="4b2ec-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4b2ec-166">RELATED LINKS</span></span>
