---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/new-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/New-AzEventHubNamespace.md
ms.openlocfilehash: 7abc847bebf5baeea1bf12db6d930bd2daa34d7f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101952635"
---
# <span data-ttu-id="2ade9-101">New-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="2ade9-101">New-AzEventHubNamespace</span></span>

## <span data-ttu-id="2ade9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2ade9-102">SYNOPSIS</span></span>
<span data-ttu-id="2ade9-103">Event Hubs 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-103">Creates an Event Hubs namespace.</span></span>

## <span data-ttu-id="2ade9-104">구문</span><span class="sxs-lookup"><span data-stu-id="2ade9-104">SYNTAX</span></span>

### <span data-ttu-id="2ade9-105">네임스페이스ParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="2ade9-105">NamespaceParameterSet (Default)</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableKafka] [-ZoneRedundant]
 [[-ClusterARMId] <String>] [-Identity] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2ade9-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="2ade9-106">AutoInflateParameterSet</span></span>
```
New-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [[-MaximumThroughputUnits] <Int32>] [-EnableKafka] [-ZoneRedundant] [[-ClusterARMId] <String>] [-Identity]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2ade9-107">설명</span><span class="sxs-lookup"><span data-stu-id="2ade9-107">DESCRIPTION</span></span>
<span data-ttu-id="2ade9-108">New-AzEventHubNamespace cmdlet은 Event Hubs 형식의 새 네임스페이스를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-108">The New-AzEventHubNamespace cmdlet creates a new namespace of type Event Hubs.</span></span>

## <span data-ttu-id="2ade9-109">예제</span><span class="sxs-lookup"><span data-stu-id="2ade9-109">EXAMPLES</span></span>
### <span data-ttu-id="2ade9-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="2ade9-110">Example 1</span></span>                                           
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/14/2020 9:02:16 PM
UpdatedAt                     : 6/14/2020 9:03:04 PM
ServiceBusEndpoint            : https://testingnew2018.servicebus.windows.net:443/
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : False
MaximumThroughputUnits        : 0
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="2ade9-111">리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 지정된 지리적 위치 MyLocation에서 Event Hubs 네임스페이스 MyNamespaceName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-111">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\`.</span></span>

### <span data-ttu-id="2ade9-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="2ade9-112">Example 2</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -MaximumThroughputUnits 10

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="2ade9-113">지정된 지리적 위치 MyLocation에서 Event Hubs 네임스페이스 \` \` \` MyNamespaceName을 만듭니다. 리소스 그룹 \` \` MyResourceGroupName 및 \` AutoInflate에서 MaximumThroughputUnits 10을 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-113">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` and AutoInflate is enabled with MaximumThroughputUnits 10.</span></span>

### <span data-ttu-id="2ade9-114">예제 3: Kafka 사용 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="2ade9-114">Example 3: Kafka enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -EnableKafka

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="2ade9-115">Kafka 및 AutoInflate를 사용하도록 설정된 리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 지정된 지리적 위치 MyLocation에서 Event Hubs 네임스페이스 MyNamespaceName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-115">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="2ade9-116">예제 4: ZoneRedundant 사용 네임스페이스</span><span class="sxs-lookup"><span data-stu-id="2ade9-116">Example 4: ZoneRedundant enabled namespace</span></span>
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation -EnableAutoInflate -ZoneRedundant

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : True
ClusterArmId                  :
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          :
Identity.TenantId             :
Identity.Type                 :
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :
```

<span data-ttu-id="2ade9-117">Kafka 및 AutoInflate를 사용하도록 설정된 리소스 그룹 \` \` \` \` \` MyResourceGroupName에서 지정된 지리적 위치 MyLocation에서 Event Hubs 네임스페이스 MyNamespaceName을 \` 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-117">Creates an Event Hubs namespace \`MyNamespaceName\` in the specified geographic location \`MyLocation\`, in resource group \`MyResourceGroupName\` with Kafka and  AutoInflate enabled.</span></span>

### <span data-ttu-id="2ade9-118">예제 5: 클러스터에서 ID 관리로 네임스페이스 만들기</span><span class="sxs-lookup"><span data-stu-id="2ade9-118">Example 5: Creating Namespace with Manage Identity in a cluster</span></span> 
```powershell
PS C:\> New-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location MyLocation --EnableAutoInflate -MaximumThroughputUnits 12 -EnableKafka -ZoneRedundant -Identity

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 5/24/2019 12:47:27 AM
UpdatedAt                     : 5/24/2019 12:48:14 AM
ServiceBusEndpoint            : #########
Enabled                       : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 12
ZoneRedundant                 : True
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity.PrincipalId          : ##########
Identity.TenantId             : ##########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          :
Encryption.KeyVaultProperties :


# Get created namespace
PS C:\>$getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
PS C:\> $key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperties @(@($key.Name, $keyvault.VaultUri,""))

Name                          : MyNamespaceName
Id                            : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName             : Default-EventHub-WestCentralUS
Location                      : West US
Sku                           : Name : Standard , Capacity : 1 , Tier : Standard
Tags                          :
ProvisioningState             : Succeeded
Status                        : Active
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
ServiceBusEndpoint            : #########
Enabled                       : True
KafkaEnabled                  : True
IsAutoInflateEnabled          : True
MaximumThroughputUnits        : 10
ZoneRedundant                 : False
ClusterArmId                  : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/clusters/TestCluster
Identity                      : Microsoft.Azure.Commands.EventHub.Models.PSIdentityAttributes
Identity.PrincipalId          : #########
Identity.TenantId             : #########
Identity.Type                 : SystemAssigned
Encryption                    : Microsoft.Azure.Commands.EventHub.Models.PSEncryptionAttributes
Encryption.KeySource          : MicrosoftKeyVault
Encryption.KeyVaultProperties : {testkey, https://myvaultname.vault.azure.net, }
```

## <span data-ttu-id="2ade9-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="2ade9-119">PARAMETERS</span></span>

### <span data-ttu-id="2ade9-120">-ClusterARMId</span><span class="sxs-lookup"><span data-stu-id="2ade9-120">-ClusterARMId</span></span>
<span data-ttu-id="2ade9-121">네임스페이스를 만들 클러스터의 ARM ID</span><span class="sxs-lookup"><span data-stu-id="2ade9-121">ARM ID of Cluster where namespace is to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2ade9-122">-DefaultProfile</span></span>
<span data-ttu-id="2ade9-123">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2ade9-124">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="2ade9-124">-EnableAutoInflate</span></span>
<span data-ttu-id="2ade9-125">자동 인플레이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-125">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-126">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="2ade9-126">-EnableKafka</span></span>
<span data-ttu-id="2ade9-127">네임스페이스에 대해 Kafka를 사용하도록 설정하거나 사용 안 하게 설정</span><span class="sxs-lookup"><span data-stu-id="2ade9-127">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="2ade9-128">-Identity</span><span class="sxs-lookup"><span data-stu-id="2ade9-128">-Identity</span></span>
<span data-ttu-id="2ade9-129">네임스페이스에 대한 ID 사용 또는 사용 안 림</span><span class="sxs-lookup"><span data-stu-id="2ade9-129">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="2ade9-130">-Location</span><span class="sxs-lookup"><span data-stu-id="2ade9-130">-Location</span></span>
<span data-ttu-id="2ade9-131">EventHub 네임스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-131">EventHub Namespace Location.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-132">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="2ade9-132">-MaximumThroughputUnits</span></span>
<span data-ttu-id="2ade9-133">자동 인플레이트를 사용하도록 설정하면 0에서 20개까지의 값으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-133">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet
Aliases:

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-134">-Name</span><span class="sxs-lookup"><span data-stu-id="2ade9-134">-Name</span></span>
<span data-ttu-id="2ade9-135">EventHub 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-135">EventHub Namespace Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: NamespaceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2ade9-136">-ResourceGroupName</span></span>
<span data-ttu-id="2ade9-137">리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="2ade9-137">Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-138">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="2ade9-138">-SkuCapacity</span></span>
<span data-ttu-id="2ade9-139">1000만 8000원의 10분의 1을 1로 10분의</span><span class="sxs-lookup"><span data-stu-id="2ade9-139">The eventhub throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-140">-SkuName</span><span class="sxs-lookup"><span data-stu-id="2ade9-140">-SkuName</span></span>
<span data-ttu-id="2ade9-141">네임스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-141">Namespace Sku Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Basic, Standard, Premium

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-142">-Tag</span><span class="sxs-lookup"><span data-stu-id="2ade9-142">-Tag</span></span>
<span data-ttu-id="2ade9-143">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-143">Hashtables which represents resource Tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2ade9-144">-ZoneRedundant</span><span class="sxs-lookup"><span data-stu-id="2ade9-144">-ZoneRedundant</span></span>
<span data-ttu-id="2ade9-145">네임스페이스에 대해 영역 중복을 사용하도록 설정하거나 사용 안 하게 설정</span><span class="sxs-lookup"><span data-stu-id="2ade9-145">enabling or disabling Zone Redundant for namespace</span></span>

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

### <span data-ttu-id="2ade9-146">-확인</span><span class="sxs-lookup"><span data-stu-id="2ade9-146">-Confirm</span></span>
<span data-ttu-id="2ade9-147">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-147">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2ade9-148">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2ade9-148">-WhatIf</span></span>
<span data-ttu-id="2ade9-149">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-149">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2ade9-150">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-150">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2ade9-151">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2ade9-151">CommonParameters</span></span>
<span data-ttu-id="2ade9-152">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2ade9-152">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2ade9-153">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="2ade9-153">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2ade9-154">입력</span><span class="sxs-lookup"><span data-stu-id="2ade9-154">INPUTS</span></span>

### <span data-ttu-id="2ade9-155">System.String</span><span class="sxs-lookup"><span data-stu-id="2ade9-155">System.String</span></span>

### <span data-ttu-id="2ade9-156">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="2ade9-156">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="2ade9-157">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="2ade9-157">System.Collections.Hashtable</span></span>

## <span data-ttu-id="2ade9-158">출력</span><span class="sxs-lookup"><span data-stu-id="2ade9-158">OUTPUTS</span></span>

### <span data-ttu-id="2ade9-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="2ade9-159">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="2ade9-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2ade9-160">NOTES</span></span>

## <span data-ttu-id="2ade9-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2ade9-161">RELATED LINKS</span></span>
