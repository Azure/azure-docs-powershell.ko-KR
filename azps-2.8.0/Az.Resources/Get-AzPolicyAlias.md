---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyalias
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAlias.md
ms.openlocfilehash: baf810316aeec781a0d1ae31b941f260e219d439
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93871850"
---
# <span data-ttu-id="9dc60-101">Get-AzPolicyAlias</span><span class="sxs-lookup"><span data-stu-id="9dc60-101">Get-AzPolicyAlias</span></span>

## <span data-ttu-id="9dc60-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9dc60-102">SYNOPSIS</span></span>
<span data-ttu-id="9dc60-103">Get-AzPolicyAlias 별칭을 정의 하 고 지정 된 매개 변수 값과 일치 하는 Azure 공급자 리소스 형식을 검색 하 고 출력 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-103">Get-AzPolicyAlias retrieves and outputs Azure provider resource types that have aliases defined and match the given parameter values.</span></span> <span data-ttu-id="9dc60-104">매개 변수를 제공 하지 않으면 별칭을 포함 하는 모든 공급자 리소스 형식이 출력 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-104">If no parameters are provided, all provider resource types that contain an alias will be output.</span></span>
<span data-ttu-id="9dc60-105">-ListAvailable 스위치는 별칭이 없는 항목을 포함 하 여 일치 하는 리소스 종류를 모두 나열 하 여이 동작을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-105">The -ListAvailable switch modifies this behavior by listing all matching resource types including those without aliases.</span></span>

## <span data-ttu-id="9dc60-106">구문과</span><span class="sxs-lookup"><span data-stu-id="9dc60-106">SYNTAX</span></span>

```
Get-AzPolicyAlias [-NamespaceMatch <String>] [-ResourceTypeMatch <String>] [-AliasMatch <String>]
 [-PathMatch <String>] [-ApiVersionMatch <String>] [-LocationMatch <String>] [-ListAvailable]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9dc60-107">설명은</span><span class="sxs-lookup"><span data-stu-id="9dc60-107">DESCRIPTION</span></span>
<span data-ttu-id="9dc60-108">**Get-AzPolicyAlias** cmdlet은 정책 별칭 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-108">The **Get-AzPolicyAlias** cmdlet gets a listing of policy aliases.</span></span>
<span data-ttu-id="9dc60-109">정책 별칭은 Azure Policy에서 리소스 종류 속성을 참조 하는 데 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-109">Policy aliases are used by Azure Policy to refer to resource type properties.</span></span>
<span data-ttu-id="9dc60-110">리소스 종류의 다양 한 속성 또는 별칭을 일치 시켜 목록의 항목을 제한 하는 매개 변수가 제공 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-110">Parameters are provided that limit items in the listing by matching various properties of the resource type or its aliases.</span></span>
<span data-ttu-id="9dc60-111">대상 문자열에 대/소문자를 구분 하지 않는 비교를 사용 하는 경우 지정 된 match 값이 일치 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-111">A given match value matches if the target string contains it using case insensitive comparison.</span></span>

## <span data-ttu-id="9dc60-112">예제의</span><span class="sxs-lookup"><span data-stu-id="9dc60-112">EXAMPLES</span></span>

### <span data-ttu-id="9dc60-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="9dc60-113">Example 1</span></span>
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

<span data-ttu-id="9dc60-114">별칭이 있는 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-114">Lists all provider resource types that have an alias.</span></span>

### <span data-ttu-id="9dc60-115">예제 2</span><span class="sxs-lookup"><span data-stu-id="9dc60-115">Example 2</span></span>
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

<span data-ttu-id="9dc60-116">별칭 없이 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-116">Lists all provider resource types, including those without aliases.</span></span>

### <span data-ttu-id="9dc60-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="9dc60-117">Example 3</span></span>
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

<span data-ttu-id="9dc60-118">네임 스페이스가 ' compute '와 일치 하 고 별칭을 포함 하는 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-118">Lists all provider resource types whose namespace matches 'compute' and contain an alias.</span></span>

### <span data-ttu-id="9dc60-119">예제 4</span><span class="sxs-lookup"><span data-stu-id="9dc60-119">Example 4</span></span>
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

<span data-ttu-id="9dc60-120">리소스 종류가 ' virtual '와 일치 하 고 별칭을 포함 하는 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-120">Lists all provider resource types whose resource type matches 'virtual' and contain an alias.</span></span>

### <span data-ttu-id="9dc60-121">예제 5</span><span class="sxs-lookup"><span data-stu-id="9dc60-121">Example 5</span></span>
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

<span data-ttu-id="9dc60-122">별칭 없이 리소스 종류가 ' virtual '와 일치 하는 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-122">Lists all provider resource types whose resource type matches 'virtual', including those without aliases.</span></span>

### <span data-ttu-id="9dc60-123">예제 6</span><span class="sxs-lookup"><span data-stu-id="9dc60-123">Example 6</span></span>
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

<span data-ttu-id="9dc60-124">네임 스페이스가 ' compute ' 및 리소스 형식이 일치 하는 모든 공급자 리소스 형식을 나열 하 고 별칭을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-124">Lists all provider resource types whose namespace matches 'compute' and resource type matches 'virtual' and contain an alias.</span></span>
<span data-ttu-id="9dc60-125">참고:-NamespaceMatch 및-ResourceTypeMatch는 단독으로 일치 하는 항목을 제공 하는 반면 나머지는 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-125">Note: -NamespaceMatch and -ResourceTypeMatch provide exclusive matches, whereas the others are inclusive.</span></span>

### <span data-ttu-id="9dc60-126">예제 7</span><span class="sxs-lookup"><span data-stu-id="9dc60-126">Example 7</span></span>
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

<span data-ttu-id="9dc60-127">' Virtual ' 별칭을 포함 하는 모든 공급자 리소스 형식을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-127">Lists all provider resource types that contain an alias matching 'virtual'.</span></span>

### <span data-ttu-id="9dc60-128">예제 8</span><span class="sxs-lookup"><span data-stu-id="9dc60-128">Example 8</span></span>
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

<span data-ttu-id="9dc60-129">' Virtual ' 별칭을 포함 하는 모든 공급자 리소스 형식 또는 경로가 ' 네트워크 '와 일치 하는 별칭이 나열 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-129">Lists all provider resource types that contain an alias matching 'virtual' or an alias with a path matching 'network'.</span></span>

### <span data-ttu-id="9dc60-130">예제 9</span><span class="sxs-lookup"><span data-stu-id="9dc60-130">Example 9</span></span>
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

<span data-ttu-id="9dc60-131">Alpha api 버전이 있는 모든 공급자 리소스 형식을 나열 하거나 alpha api 버전이 포함 된 별칭을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-131">Lists all provider resource types with alpha api version or containing an alias with an alpha api version.</span></span>

## <span data-ttu-id="9dc60-132">변수</span><span class="sxs-lookup"><span data-stu-id="9dc60-132">PARAMETERS</span></span>

### <span data-ttu-id="9dc60-133">-AliasMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-133">-AliasMatch</span></span>
<span data-ttu-id="9dc60-134">해당 이름이이 값과 일치 하는 별칭을 사용 하 여 출력 항목에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-134">Includes in the output items with aliases whose name matches this value.</span></span>


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

### <span data-ttu-id="9dc60-135">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="9dc60-135">-ApiVersion</span></span>
<span data-ttu-id="9dc60-136">설정 되 면 사용할 리소스 공급자 API의 버전을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-136">When set, indicates the version of the resource provider API to use.</span></span> <span data-ttu-id="9dc60-137">지정 하지 않으면 API 버전이 최신 버전으로 자동 결정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-137">If not specified, the API version is automatically determined as the latest available.</span></span>


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

### <span data-ttu-id="9dc60-138">-ApiVersionMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-138">-ApiVersionMatch</span></span>
<span data-ttu-id="9dc60-139">리소스 형식이 나 별칭에 일치 하는 api 버전이 있는 출력 항목을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-139">Includes in the output items whose resource types or aliases have a matching api version.</span></span>


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

### <span data-ttu-id="9dc60-140">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9dc60-140">-DefaultProfile</span></span>
<span data-ttu-id="9dc60-141">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-141">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>


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

### <span data-ttu-id="9dc60-142">-ListAvailable</span><span class="sxs-lookup"><span data-stu-id="9dc60-142">-ListAvailable</span></span>
<span data-ttu-id="9dc60-143">별칭을 포함 하거나 제외 하 고 일치 하는 출력 항목에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-143">Includes in the output matching items with and without aliases.</span></span>


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

### <span data-ttu-id="9dc60-144">-LocationMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-144">-LocationMatch</span></span>
<span data-ttu-id="9dc60-145">리소스 종류가 일치 하는 위치를 갖는 출력 항목에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-145">Includes in the output items whose resource types have a matching location.</span></span>


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

### <span data-ttu-id="9dc60-146">-NamespaceMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-146">-NamespaceMatch</span></span>
<span data-ttu-id="9dc60-147">해당 네임 스페이스가이 값과 일치 하는 항목으로 출력을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-147">Limits the output to items whose namespace matches this value.</span></span>


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

### <span data-ttu-id="9dc60-148">-PathMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-148">-PathMatch</span></span>
<span data-ttu-id="9dc60-149">이 값과 일치 하는 경로가 포함 된 별칭을 사용 하 여 출력 항목에 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-149">Includes in the output items with aliases containing a path that matches this value.</span></span>


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

### <span data-ttu-id="9dc60-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="9dc60-150">-Pre</span></span>
<span data-ttu-id="9dc60-151">설정 하는 경우 cmdlet에서 사용할 버전을 자동으로 결정할 때 시험판 API 버전을 사용 해야 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-151">When set, indicates that the cmdlet should use pre-release API versions when automatically determining which version to use.</span></span>


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

### <span data-ttu-id="9dc60-152">-ResourceTypeMatch</span><span class="sxs-lookup"><span data-stu-id="9dc60-152">-ResourceTypeMatch</span></span>
<span data-ttu-id="9dc60-153">리소스 종류가이 값과 일치 하는 항목으로 출력을 제한 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-153">Limits the output to items whose resource type matches this value.</span></span>


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

### <span data-ttu-id="9dc60-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9dc60-154">CommonParameters</span></span>
<span data-ttu-id="9dc60-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9dc60-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9dc60-156">자세한 내용은 [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="9dc60-156">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9dc60-157">입력</span><span class="sxs-lookup"><span data-stu-id="9dc60-157">INPUTS</span></span>

### <span data-ttu-id="9dc60-158">않아야</span><span class="sxs-lookup"><span data-stu-id="9dc60-158">None</span></span>

## <span data-ttu-id="9dc60-159">출력</span><span class="sxs-lookup"><span data-stu-id="9dc60-159">OUTPUTS</span></span>

### <span data-ttu-id="9dc60-160">Microsoft. PsResourceProviderAlias 구현.</span><span class="sxs-lookup"><span data-stu-id="9dc60-160">Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.PsResourceProviderAlias</span></span>

## <span data-ttu-id="9dc60-161">상속자</span><span class="sxs-lookup"><span data-stu-id="9dc60-161">NOTES</span></span>

* <span data-ttu-id="9dc60-162">별칭 또는 기타 속성을 확장 하려면 출력을로 파이프 합니다 `select -ExpandProperty <property>` .</span><span class="sxs-lookup"><span data-stu-id="9dc60-162">To expand the Aliases or any other property, pipe the output to `select -ExpandProperty <property>`.</span></span> <span data-ttu-id="9dc60-163">예를 들어: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span><span class="sxs-lookup"><span data-stu-id="9dc60-163">For example: `Get-AzPolicyAlias -NamespaceMatch 'Microsoft.Cache' -ApiVersionMatch 'alpha' | select -ExpandProperty Aliases | select -Property Name -ExpandProperty Paths`</span></span>

* <span data-ttu-id="9dc60-164">출력에서 사용할 수 있는 추가 속성은 출력에 파이핑 하 여 표시할 수 있습니다 `Format-List` .</span><span class="sxs-lookup"><span data-stu-id="9dc60-164">Additional properties are available in the output and can be displayed by piping the output to `Format-List`.</span></span> <span data-ttu-id="9dc60-165">예를 들어: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span><span class="sxs-lookup"><span data-stu-id="9dc60-165">For example: `Get-AzPolicyAlias -NamespaceMatch 'Web' -ResourceTypeMatch site -PathMatch cert | Format-List`</span></span>

## <span data-ttu-id="9dc60-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9dc60-166">RELATED LINKS</span></span>
