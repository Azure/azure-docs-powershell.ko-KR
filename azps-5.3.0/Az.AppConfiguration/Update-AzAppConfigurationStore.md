---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 8aea57e0c2bea5dbaa2e3233e886c97bfebe4bd4
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98381431"
---
# <span data-ttu-id="073e1-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="073e1-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="073e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="073e1-102">SYNOPSIS</span></span>
<span data-ttu-id="073e1-103">지정된 매개 변수를 사용하여 구성 저장소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="073e1-104">구문</span><span class="sxs-lookup"><span data-stu-id="073e1-104">SYNTAX</span></span>

### <span data-ttu-id="073e1-105">UpdateExpanded(기본값)</span><span class="sxs-lookup"><span data-stu-id="073e1-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="073e1-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="073e1-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="073e1-107">설명</span><span class="sxs-lookup"><span data-stu-id="073e1-107">DESCRIPTION</span></span>
<span data-ttu-id="073e1-108">지정된 매개 변수를 사용하여 구성 저장소를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="073e1-109">예제</span><span class="sxs-lookup"><span data-stu-id="073e1-109">EXAMPLES</span></span>

### <span data-ttu-id="073e1-110">예제 1: 시스템 할당 관리 ID로 앱 구성 저장소의 데이터 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="073e1-110">Example 1: Enable data encryption of the app configuration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="073e1-111">이 명령을 사용하면 시스템 할당 관리 ID를 사용하여 Azure Key Vault에 저장된 키로 데이터 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="073e1-112">자격 증명 모음은 소프트 삭제 및 제거 보호를 사용하도록 설정해야 합니다. 관리 ID에는 get, wrapKey, unwrapKey와 같은 주요 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="073e1-113">예제 2: 사용자 할당 관리 ID로 앱 구성 저장소의 데이터 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="073e1-113">Example 2: Enable data encryption of the app configuration store by user-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $assignedIdentity = New-AzUserAssignedIdentity -ResourceGroupName azpwsh-manual-test -Name assignedIdentity
PS C:\> New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "UserAssigned" -UserAssignedIdentity $assignedIdentity.Id
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $assignedIdentity.PrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test11 -EncryptionKeyIdentifier $key.Id -KeyVaultIdentityClientId $assignedIdentity.ClientId

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="073e1-114">이 명령은 사용자 할당 관리 ID를 사용하여 Azure Key Vault에 저장된 키로 데이터 암호화를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="073e1-115">사용자 할당 ID가 .로 설정되어 있어야 `-UserAssignedIdentity` 합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="073e1-116">자격 증명 모음은 소프트 삭제 및 제거 보호를 사용하도록 설정해야 합니다. 관리 ID에는 get, wrapKey, unwrapKey와 같은 주요 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="073e1-117">예제 3: 앱 구성 저장소의 암호화를 사용하지 않도록 설정</span><span class="sxs-lookup"><span data-stu-id="073e1-117">Example 3: Disable encryption of an app configuration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="073e1-118">이 명령은 앱 구성 저장소의 암호화를 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-118">This command disables encryption of an app configuration store.</span></span>

### <span data-ttu-id="073e1-119">예제 3: 파이프라인에 따라 앱 구성 저장소의 SKU 및 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-119">Example 3: Update sku and tag of an app configuration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="073e1-120">이 명령은 파이프라인에 따라 앱 구성 저장소의 SKU 및 태그를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-120">This command updates sku and tag of an app configuration store by pipeline.</span></span>

## <span data-ttu-id="073e1-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="073e1-121">PARAMETERS</span></span>

### <span data-ttu-id="073e1-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="073e1-122">-AsJob</span></span>
<span data-ttu-id="073e1-123">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="073e1-123">Run the command as a job</span></span>

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

### <span data-ttu-id="073e1-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="073e1-124">-DefaultProfile</span></span>
<span data-ttu-id="073e1-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="073e1-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="073e1-127">데이터를 암호화하는 데 사용되는 키 자격 증명 모음 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="073e1-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="073e1-128">-IdentityType</span></span>
<span data-ttu-id="073e1-129">사용되는 관리 ID의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-129">The type of managed identity used.</span></span>
<span data-ttu-id="073e1-130">'SystemAssignedAndUserAssigned' 형식에는 암시적으로 만든 ID와 사용자 할당 ID 집합이 모두 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="073e1-131">'없음' 형식은 ID를 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-131">The type 'None' will remove any identities.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Support.IdentityType
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="073e1-132">-InputObject</span></span>
<span data-ttu-id="073e1-133">ID 매개 변수를 생성하는 경우 INPUTOBJECT 속성에 대한 NOTES 섹션을 참조하고 해시 테이블을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="073e1-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity
Parameter Sets: UpdateViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="073e1-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="073e1-135">키 자격 증명 모음에 액세스하는 데 사용할 ID의 클라이언트 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="073e1-136">-Name</span><span class="sxs-lookup"><span data-stu-id="073e1-136">-Name</span></span>
<span data-ttu-id="073e1-137">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-137">The name of the configuration store.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="073e1-138">-NoWait</span></span>
<span data-ttu-id="073e1-139">명령을 비동기적으로 실행</span><span class="sxs-lookup"><span data-stu-id="073e1-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="073e1-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="073e1-140">-ResourceGroupName</span></span>
<span data-ttu-id="073e1-141">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-141">The name of the resource group to which the container registry belongs.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="073e1-142">-Sku</span></span>
<span data-ttu-id="073e1-143">구성 저장소의 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="073e1-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="073e1-144">-SubscriptionId</span></span>
<span data-ttu-id="073e1-145">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-145">The Microsoft Azure subscription ID.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-146">-Tag</span><span class="sxs-lookup"><span data-stu-id="073e1-146">-Tag</span></span>
<span data-ttu-id="073e1-147">리소스 ARM 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-147">The ARM resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="073e1-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="073e1-149">리소스와 연결된 사용자 할당 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="073e1-150">사용자 할당 ID 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}' 형식의 리소스 ID로 설정됩니다. ARM</span><span class="sxs-lookup"><span data-stu-id="073e1-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="073e1-151">-Confirm</span><span class="sxs-lookup"><span data-stu-id="073e1-151">-Confirm</span></span>
<span data-ttu-id="073e1-152">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="073e1-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="073e1-153">-WhatIf</span></span>
<span data-ttu-id="073e1-154">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="073e1-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="073e1-155">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="073e1-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="073e1-156">CommonParameters</span></span>
<span data-ttu-id="073e1-157">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="073e1-158">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="073e1-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="073e1-159">입력</span><span class="sxs-lookup"><span data-stu-id="073e1-159">INPUTS</span></span>

### <span data-ttu-id="073e1-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span><span class="sxs-lookup"><span data-stu-id="073e1-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="073e1-161">출력</span><span class="sxs-lookup"><span data-stu-id="073e1-161">OUTPUTS</span></span>

### <span data-ttu-id="073e1-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="073e1-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="073e1-163">참고 사항</span><span class="sxs-lookup"><span data-stu-id="073e1-163">NOTES</span></span>

<span data-ttu-id="073e1-164">별칭</span><span class="sxs-lookup"><span data-stu-id="073e1-164">ALIASES</span></span>

<span data-ttu-id="073e1-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="073e1-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="073e1-166">아래에 설명된 매개 변수를 만들 수 있도록 적절한 속성을 포함하는 해시 테이블을 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="073e1-167">해시 테이블에 대한 자세한 내용은 다음 Get-Help about_Hash_Tables.</span><span class="sxs-lookup"><span data-stu-id="073e1-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="073e1-168">INPUTOBJECT: <IAppConfigurationIdentity> ID 매개 변수</span><span class="sxs-lookup"><span data-stu-id="073e1-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="073e1-169">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="073e1-170">`[GroupName <String>]`: 개인 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="073e1-171">`[Id <String>]`: 리소스 ID 경로</span><span class="sxs-lookup"><span data-stu-id="073e1-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="073e1-172">`[PrivateEndpointConnectionName <String>]`: 개인 엔드포인트 연결 이름</span><span class="sxs-lookup"><span data-stu-id="073e1-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="073e1-173">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="073e1-174">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="073e1-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="073e1-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="073e1-175">RELATED LINKS</span></span>



<span data-ttu-id="073e1-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="073e1-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

