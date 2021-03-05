---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: 6afbd081eca842e2185428f90a18932e05c3bbe4
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984648"
---
# <span data-ttu-id="652f2-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="652f2-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="652f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="652f2-102">SYNOPSIS</span></span>
<span data-ttu-id="652f2-103">지정된 Event Hubs 네임스페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="652f2-104">구문</span><span class="sxs-lookup"><span data-stu-id="652f2-104">SYNTAX</span></span>

### <span data-ttu-id="652f2-105">네임스페이스ParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="652f2-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="652f2-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="652f2-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="652f2-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="652f2-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="652f2-108">설명</span><span class="sxs-lookup"><span data-stu-id="652f2-108">DESCRIPTION</span></span>
<span data-ttu-id="652f2-109">Set-AzEventHubNamespace cmdlet은 지정된 Event Hubs 네임스페이스의 속성을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="652f2-110">예제</span><span class="sxs-lookup"><span data-stu-id="652f2-110">EXAMPLES</span></span>

### <span data-ttu-id="652f2-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="652f2-111">Example 1</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -Tag @{Tag1='TagValue1'; Tag2='TagValue2'}

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   : {Tag2, TagValue2, Tag1, TagValue1}
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10

```

<span data-ttu-id="652f2-112">네임스페이스 \` MyNamespaceName의 태그를 만든 으로 \` 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="652f2-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="652f2-113">Example 2</span></span>
```powershell
PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName -Location "WestUS" -State Created -EnableAutoInflate -MaximumThroughputUnits 10 

Name                   : MyNamespaceName
Id                     : /subscriptions/{subscriptionId}/resourceGroups/Default-EventHub-WestCentralUS/providers/Microsoft.EventHub/namespaces/MyNamespaceName
ResourceGroup          : Default-EventHub-WestCentralUS
ResourceGroupName      : Default-EventHub-WestCentralUS
Location               : West US
Sku                    : Name : Standard , Capacity : 1 , Tier : Standard
Tags                   :
ProvisioningState      : Succeeded
Status                 : Active
CreatedAt              : 5/24/2019 12:47:27 AM
UpdatedAt              : 5/24/2019 12:48:14 AM
ServiceBusEndpoint     : #########
Enabled                : True
KafkaEnabled           : True
IsAutoInflateEnabled   : True
MaximumThroughputUnits : 10
```

<span data-ttu-id="652f2-114">AutoInflate = 사용 및 \` \` MaximumThroughputUnits = 10으로 네임스페이스 MyNamespaceName의 상태를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="652f2-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="652f2-115">Example 3</span></span>

<span data-ttu-id="652f2-116">지정된 Event Hubs 네임스페이스를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="652f2-117">(자동 재생)</span><span class="sxs-lookup"><span data-stu-id="652f2-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="652f2-118">예제 5: 클러스터에서 ID 관리로 네임스페이스 만들기 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="652f2-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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
CreatedAt                     : 6/12/2020 4:00:29 AM
UpdatedAt                     : 6/14/2020 11:33:12 PM
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
PS C:\> $getnamespace = Get-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -NamespaceName MyNamespaceName

# Create KeyVault
PS C:\>$Keyvault = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Set Access policy on the KeyVault
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName testingnewCluster -ObjectId $getnamespace.Identity.PrincipalId -PermissionsToKeys wrapkey,unwrapkey,get -BypassObjectIdValidation

# Add a key to KeyVault
$key = New-AzKeyVault -ResourceGroupName prod-by3-533-rg -Name testingnewCluster -EnableSoftDelete -EnablePurgeProtection -Location westus

# Update Namespace with KeyVault properties

PS C:\> Set-AzEventHubNamespace -ResourceGroupName MyResourceGroupName -Name MyNamespaceName -Location westus -KeySource Microsoft.KeyVault -KeyProperty @(@($key.Name, $keyvault.VaultUri,""))

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

## <span data-ttu-id="652f2-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="652f2-119">PARAMETERS</span></span>

### <span data-ttu-id="652f2-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="652f2-120">-DefaultProfile</span></span>
<span data-ttu-id="652f2-121">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="652f2-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="652f2-122">-EnableAutoInflate</span></span>
<span data-ttu-id="652f2-123">자동 인플레이트를 사용하도록 설정되어 있는지 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-123">Indicates whether AutoInflate is enabled</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="652f2-124">-EnableKafka</span></span>
<span data-ttu-id="652f2-125">네임스페이스에 대해 Kafka를 사용하도록 설정하거나 사용 안 하게 설정</span><span class="sxs-lookup"><span data-stu-id="652f2-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="652f2-126">-Identity</span><span class="sxs-lookup"><span data-stu-id="652f2-126">-Identity</span></span>
<span data-ttu-id="652f2-127">네임스페이스에 대한 ID 사용 또는 사용 안 림</span><span class="sxs-lookup"><span data-stu-id="652f2-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="652f2-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="652f2-128">-IdentityUserDefined</span></span>
<span data-ttu-id="652f2-129">사용자 정의 ID 또는 없음</span><span class="sxs-lookup"><span data-stu-id="652f2-129">User defined Identity or None</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="652f2-130">-KeyProperty</span></span>
<span data-ttu-id="652f2-131">키 속성 목록, @(@(KeyName, KeyVaultUri, Keyversion),@(KeyName, KeyVaultUri, Keyversion))</span><span class="sxs-lookup"><span data-stu-id="652f2-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String[]]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="652f2-132">-KeySource</span></span>
<span data-ttu-id="652f2-133">키 원본</span><span class="sxs-lookup"><span data-stu-id="652f2-133">Key Source</span></span>

```yaml
Type: System.String
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-134">-Location</span><span class="sxs-lookup"><span data-stu-id="652f2-134">-Location</span></span>
<span data-ttu-id="652f2-135">EventHub 네임스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="652f2-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="652f2-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="652f2-137">자동 인플레이트를 사용하도록 설정하면 0에서 20개까지의 값으로 제한됩니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: AutoInflateParameterSet, IdentityUpdateParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-138">-Name</span><span class="sxs-lookup"><span data-stu-id="652f2-138">-Name</span></span>
<span data-ttu-id="652f2-139">EventHub 네임스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="652f2-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="652f2-140">-ResourceGroupName</span></span>
<span data-ttu-id="652f2-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="652f2-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="652f2-142">-SkuCapacity</span></span>
<span data-ttu-id="652f2-143">1000만 8000원의 10분의 1을 1로 10분의</span><span class="sxs-lookup"><span data-stu-id="652f2-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="652f2-144">-SkuName</span><span class="sxs-lookup"><span data-stu-id="652f2-144">-SkuName</span></span>
<span data-ttu-id="652f2-145">네임스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="652f2-146">-State</span><span class="sxs-lookup"><span data-stu-id="652f2-146">-State</span></span>
<span data-ttu-id="652f2-147">네임스페이스를 사용하지 않도록 설정/사용하도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-147">Disable/Enable Namespace.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.EventHub.Models.NamespaceState]
Parameter Sets: NamespaceParameterSet, AutoInflateParameterSet
Aliases:
Accepted values: Unknown, Active, Disabled

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-148">-Tag</span><span class="sxs-lookup"><span data-stu-id="652f2-148">-Tag</span></span>
<span data-ttu-id="652f2-149">리소스 태그를 나타내는 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-149">Hashtables which represents resource Tag.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="652f2-150">-확인</span><span class="sxs-lookup"><span data-stu-id="652f2-150">-Confirm</span></span>
<span data-ttu-id="652f2-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="652f2-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="652f2-152">-WhatIf</span></span>
<span data-ttu-id="652f2-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="652f2-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="652f2-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="652f2-155">CommonParameters</span></span>
<span data-ttu-id="652f2-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="652f2-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="652f2-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="652f2-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="652f2-158">입력</span><span class="sxs-lookup"><span data-stu-id="652f2-158">INPUTS</span></span>

### <span data-ttu-id="652f2-159">System.String</span><span class="sxs-lookup"><span data-stu-id="652f2-159">System.String</span></span>

### <span data-ttu-id="652f2-160">System.Nullable'1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="652f2-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="652f2-161">System.Nullable'1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span><span class="sxs-lookup"><span data-stu-id="652f2-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="652f2-162">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="652f2-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="652f2-163">출력</span><span class="sxs-lookup"><span data-stu-id="652f2-163">OUTPUTS</span></span>

### <span data-ttu-id="652f2-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span><span class="sxs-lookup"><span data-stu-id="652f2-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="652f2-165">참고 사항</span><span class="sxs-lookup"><span data-stu-id="652f2-165">NOTES</span></span>

## <span data-ttu-id="652f2-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="652f2-166">RELATED LINKS</span></span>
