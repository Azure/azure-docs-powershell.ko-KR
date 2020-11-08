---
external help file: Microsoft.Azure.PowerShell.Cmdlets.EventHub.dll-Help.xml
Module Name: Az.EventHub
online version: https://docs.microsoft.com/en-us/powershell/module/az.eventhub/set-azeventhubnamespace
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/EventHub/EventHub/help/Set-AzEventHubNamespace.md
ms.openlocfilehash: f13a92bef4bfbafc67beec6d99cf02d8d1d63c31
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217435"
---
# <span data-ttu-id="df072-101">Set-AzEventHubNamespace</span><span class="sxs-lookup"><span data-stu-id="df072-101">Set-AzEventHubNamespace</span></span>

## <span data-ttu-id="df072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df072-102">SYNOPSIS</span></span>
<span data-ttu-id="df072-103">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-103">Updates the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="df072-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df072-104">SYNTAX</span></span>

### <span data-ttu-id="df072-105">NamespaceParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="df072-105">NamespaceParameterSet (Default)</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>] [-EnableKafka]
 [-Identity] [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df072-106">AutoInflateParameterSet</span><span class="sxs-lookup"><span data-stu-id="df072-106">AutoInflateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-State] <NamespaceState>] [[-Tag] <Hashtable>]
 [-EnableAutoInflate] [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity]
 [-IdentityUserDefined <String>] [-KeySource <String>]
 [-KeyProperty <System.Collections.Generic.List`1[System.String[]]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="df072-107">IdentityUpdateParameterSet</span><span class="sxs-lookup"><span data-stu-id="df072-107">IdentityUpdateParameterSet</span></span>
```
Set-AzEventHubNamespace [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [[-SkuName] <String>] [[-SkuCapacity] <Int32>] [[-Tag] <Hashtable>] [-EnableAutoInflate]
 [-MaximumThroughputUnits <Int32>] [-EnableKafka] [-Identity] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="df072-108">설명은</span><span class="sxs-lookup"><span data-stu-id="df072-108">DESCRIPTION</span></span>
<span data-ttu-id="df072-109">Set-AzEventHubNamespace cmdlet은 지정 된 이벤트 허브 네임 스페이스의 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-109">The Set-AzEventHubNamespace cmdlet updates the properties of the specified Event Hubs namespace.</span></span>

## <span data-ttu-id="df072-110">예제의</span><span class="sxs-lookup"><span data-stu-id="df072-110">EXAMPLES</span></span>

### <span data-ttu-id="df072-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="df072-111">Example 1</span></span>
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

<span data-ttu-id="df072-112">네임 스페이스 MyNamespaceName의 태그 \` \` 를 생성으로 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-112">Updates the Tags for namespace \`MyNamespaceName\` to Created .</span></span>

### <span data-ttu-id="df072-113">예제 2</span><span class="sxs-lookup"><span data-stu-id="df072-113">Example 2</span></span>
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

<span data-ttu-id="df072-114">\` \` Autoinflate = Enabled 및 MaximumThroughputUnits = 10 인 네임 스페이스 MyNamespaceName의 상태를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-114">Updates the state of namespace \`MyNamespaceName\` with AutoInflate = enabled and MaximumThroughputUnits = 10</span></span>

### <span data-ttu-id="df072-115">예제 3</span><span class="sxs-lookup"><span data-stu-id="df072-115">Example 3</span></span>

<span data-ttu-id="df072-116">지정 된 이벤트 허브 네임 스페이스를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-116">Updates the specified Event Hubs namespace.</span></span> <span data-ttu-id="df072-117">생성</span><span class="sxs-lookup"><span data-stu-id="df072-117">(autogenerated)</span></span>

```powershell <!-- Aladdin Generated Example --> 
Set-AzEventHubNamespace -Location 'WestUS' -Name MyNamespaceName -ResourceGroupName MyResourceGroupName -SkuName Basic
```

### <span data-ttu-id="df072-118">예제 5: 클러스터에서 Id 관리를 사용 하 여 네임 스페이스 만들기 및 업데이트</span><span class="sxs-lookup"><span data-stu-id="df072-118">Example 5: Creating and updating Namespace with Manage Identity in a cluster</span></span> 
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

## <span data-ttu-id="df072-119">변수</span><span class="sxs-lookup"><span data-stu-id="df072-119">PARAMETERS</span></span>

### <span data-ttu-id="df072-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df072-120">-DefaultProfile</span></span>
<span data-ttu-id="df072-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="df072-122">-EnableAutoInflate</span><span class="sxs-lookup"><span data-stu-id="df072-122">-EnableAutoInflate</span></span>
<span data-ttu-id="df072-123">자동 팽창 사용 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="df072-123">Indicates whether AutoInflate is enabled</span></span>

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

### <span data-ttu-id="df072-124">-EnableKafka</span><span class="sxs-lookup"><span data-stu-id="df072-124">-EnableKafka</span></span>
<span data-ttu-id="df072-125">네임 스페이스의 Kafka을 사용 하거나 사용 하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="df072-125">enabling or disabling Kafka for namespace</span></span>

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

### <span data-ttu-id="df072-126">-Id</span><span class="sxs-lookup"><span data-stu-id="df072-126">-Identity</span></span>
<span data-ttu-id="df072-127">네임 스페이스에 대 한 Id 사용 또는 사용 안 함</span><span class="sxs-lookup"><span data-stu-id="df072-127">enabling or disabling Identity for namespace</span></span>

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

### <span data-ttu-id="df072-128">-IdentityUserDefined</span><span class="sxs-lookup"><span data-stu-id="df072-128">-IdentityUserDefined</span></span>
<span data-ttu-id="df072-129">사용자 정의 Id 또는 없음</span><span class="sxs-lookup"><span data-stu-id="df072-129">User defined Identity or None</span></span>

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

### <span data-ttu-id="df072-130">-KeyProperty</span><span class="sxs-lookup"><span data-stu-id="df072-130">-KeyProperty</span></span>
<span data-ttu-id="df072-131">키 속성 목록 (@ (@ (KeyName, KeyVaultUri, Keyversion), @ (KeyName, KeyVaultUri, Keyversion))</span><span class="sxs-lookup"><span data-stu-id="df072-131">List of Key Properties, @(@(KeyName,KeyVaultUri,Keyversion),@(KeyName,KeyVaultUri,Keyversion))</span></span>

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

### <span data-ttu-id="df072-132">-KeySource</span><span class="sxs-lookup"><span data-stu-id="df072-132">-KeySource</span></span>
<span data-ttu-id="df072-133">키 원본</span><span class="sxs-lookup"><span data-stu-id="df072-133">Key Source</span></span>

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

### <span data-ttu-id="df072-134">-위치</span><span class="sxs-lookup"><span data-stu-id="df072-134">-Location</span></span>
<span data-ttu-id="df072-135">EventHub 네임 스페이스 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-135">EventHub Namespace Location.</span></span>

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

### <span data-ttu-id="df072-136">-MaximumThroughputUnits</span><span class="sxs-lookup"><span data-stu-id="df072-136">-MaximumThroughputUnits</span></span>
<span data-ttu-id="df072-137">자동 팽창을 사용 하는 경우 처리량 단위의 상한 값은 0 ~ 20 개의 처리량 단위 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-137">Upper limit of throughput units when AutoInflate is enabled, value should be within 0 to 20 throughput units.</span></span>

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

### <span data-ttu-id="df072-138">-이름</span><span class="sxs-lookup"><span data-stu-id="df072-138">-Name</span></span>
<span data-ttu-id="df072-139">EventHub 네임 스페이스 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-139">EventHub Namespace Name.</span></span>

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

### <span data-ttu-id="df072-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="df072-140">-ResourceGroupName</span></span>
<span data-ttu-id="df072-141">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-141">Resource Group Name.</span></span>

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

### <span data-ttu-id="df072-142">-SkuCapacity</span><span class="sxs-lookup"><span data-stu-id="df072-142">-SkuCapacity</span></span>
<span data-ttu-id="df072-143">Eventhub 처리량 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-143">The eventhub throughput units.</span></span>

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

### <span data-ttu-id="df072-144">-서 비 Uname</span><span class="sxs-lookup"><span data-stu-id="df072-144">-SkuName</span></span>
<span data-ttu-id="df072-145">네임 스페이스 Sku 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-145">Namespace Sku Name.</span></span>

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

### <span data-ttu-id="df072-146">-상태</span><span class="sxs-lookup"><span data-stu-id="df072-146">-State</span></span>
<span data-ttu-id="df072-147">네임 스페이스를 사용 하거나 사용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df072-147">Disable/Enable Namespace.</span></span>

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

### <span data-ttu-id="df072-148">태그</span><span class="sxs-lookup"><span data-stu-id="df072-148">-Tag</span></span>
<span data-ttu-id="df072-149">리소스 태그를 나타내는 Hashtables입니다.</span><span class="sxs-lookup"><span data-stu-id="df072-149">Hashtables which represents resource Tag.</span></span>

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

### <span data-ttu-id="df072-150">-확인</span><span class="sxs-lookup"><span data-stu-id="df072-150">-Confirm</span></span>
<span data-ttu-id="df072-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="df072-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="df072-152">-WhatIf</span></span>
<span data-ttu-id="df072-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="df072-153">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="df072-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df072-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="df072-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df072-155">CommonParameters</span></span>
<span data-ttu-id="df072-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df072-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df072-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="df072-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df072-158">입력</span><span class="sxs-lookup"><span data-stu-id="df072-158">INPUTS</span></span>

### <span data-ttu-id="df072-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="df072-159">System.String</span></span>

### <span data-ttu-id="df072-160">시스템 Null 허용 ' 1 [[b77a5c561934e089, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="df072-160">System.Nullable\`1[[System.Int32, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="df072-161">시스템 Null 허용 ' 1 [[NamespaceState, [Microsoft Azure. 1.4.3.0., Microsoft Azure. PowerShell, Version =, Culture = 중립, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="df072-161">System.Nullable\`1[[Microsoft.Azure.Commands.EventHub.Models.NamespaceState, Microsoft.Azure.PowerShell.Cmdlets.EventHub, Version=1.4.3.0, Culture=neutral, PublicKeyToken=null]]</span></span>

### <span data-ttu-id="df072-162">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="df072-162">System.Collections.Hashtable</span></span>

## <span data-ttu-id="df072-163">출력</span><span class="sxs-lookup"><span data-stu-id="df072-163">OUTPUTS</span></span>

### <span data-ttu-id="df072-164">PSNamespaceAttributes (.).</span><span class="sxs-lookup"><span data-stu-id="df072-164">Microsoft.Azure.Commands.EventHub.Models.PSNamespaceAttributes</span></span>

## <span data-ttu-id="df072-165">상속자</span><span class="sxs-lookup"><span data-stu-id="df072-165">NOTES</span></span>

## <span data-ttu-id="df072-166">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df072-166">RELATED LINKS</span></span>
