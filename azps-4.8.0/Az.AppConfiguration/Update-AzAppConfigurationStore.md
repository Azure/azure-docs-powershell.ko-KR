---
external help file: ''
Module Name: Az.AppConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.appconfiguration/update-azappconfigurationstore
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AppConfiguration/help/Update-AzAppConfigurationStore.md
ms.openlocfilehash: 944241dc7434646272c7149d81b380996e71db8f
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056573"
---
# <span data-ttu-id="01257-101">Update-AzAppConfigurationStore</span><span class="sxs-lookup"><span data-stu-id="01257-101">Update-AzAppConfigurationStore</span></span>

## <span data-ttu-id="01257-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01257-102">SYNOPSIS</span></span>
<span data-ttu-id="01257-103">지정 된 매개 변수를 사용 하 여 구성 저장소를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-103">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="01257-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01257-104">SYNTAX</span></span>

### <span data-ttu-id="01257-105">UpdateExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="01257-105">UpdateExpanded (Default)</span></span>
```
Update-AzAppConfigurationStore -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-EncryptionKeyIdentifier <String>] [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>]
 [-Sku <String>] [-Tag <Hashtable>] [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="01257-106">UpdateViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="01257-106">UpdateViaIdentityExpanded</span></span>
```
Update-AzAppConfigurationStore -InputObject <IAppConfigurationIdentity> [-EncryptionKeyIdentifier <String>]
 [-IdentityType <IdentityType>] [-KeyVaultIdentityClientId <String>] [-Sku <String>] [-Tag <Hashtable>]
 [-UserAssignedIdentity <String[]>] [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

## <span data-ttu-id="01257-107">설명은</span><span class="sxs-lookup"><span data-stu-id="01257-107">DESCRIPTION</span></span>
<span data-ttu-id="01257-108">지정 된 매개 변수를 사용 하 여 구성 저장소를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-108">Updates a configuration store with the specified parameters.</span></span>

## <span data-ttu-id="01257-109">예제의</span><span class="sxs-lookup"><span data-stu-id="01257-109">EXAMPLES</span></span>

### <span data-ttu-id="01257-110">예제 1: 시스템에서 할당 한 관리 되는 id에 따라 app conifguration store의 데이터 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="01257-110">Example 1: Enable data encryption of the app conifguration store by system-assigned managed identity</span></span>
```powershell
PS C:\> $key = Add-AzKeyVaultKey -VaultName kv-Name -Name key-Name -Destination 'Software'
PS C:\> $systemAssignedAppStore = New-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -Location $env.location -Sku 'standard' -IdentityType "SystemAssigned"
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName kv-Name -ObjectId $systemAssignedAppStore.IdentityPrincipalId -PermissionsToKeys get,unwrapKey,wrapKey -PassThru
PS C:\> Update-AzAppConfigurationStore -Name appconfig-test11 -ResourceGroupName azpwsh-manual-test -EncryptionKeyIdentifier $key.Id

Location Name             Type
-------- ----             ----
eastus   appconfig-test01 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="01257-111">이 명령은 시스템 할당 관리 id를 사용 하 여 Azure Key Vault에 저장 된 키로 데이터 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-111">This command enables data encryption by a key stored in Azure Key Vault using a system-assigned managed identity.</span></span>
<span data-ttu-id="01257-112">자격 증명 모음에는 소프트 삭제 및 제거 보호가 설정 되어 있어야 하며, 관리 되는 id에는 get, wrapKey, unwrapKey 키 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-112">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="01257-113">예제 2: 사용자가 할당 한 관리 되는 id로 app conifguration store의 데이터 암호화 사용</span><span class="sxs-lookup"><span data-stu-id="01257-113">Example 2: Enable data encryption of the app conifguration store by user-assigned managed identity</span></span>
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

<span data-ttu-id="01257-114">이 명령은 사용자가 할당 한 관리 id를 사용 하 여 Azure Key Vault에 저장 된 키로 데이터 암호화를 사용 하도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-114">This command enables data encryption by a key stored in Azure Key Vault using a user-assigned managed identity.</span></span>
<span data-ttu-id="01257-115">사용자 지정 id는로 설정 되어 있어야 합니다 `-UserAssignedIdentity` .</span><span class="sxs-lookup"><span data-stu-id="01257-115">The user-assigned identity must have been set with `-UserAssignedIdentity`.</span></span>
<span data-ttu-id="01257-116">자격 증명 모음에는 소프트 삭제 및 제거 보호가 설정 되어 있어야 하며, 관리 되는 id에는 get, wrapKey, unwrapKey 키 권한이 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-116">The vault must have enabled soft-delete and purge-protection, and the managed identity must have these key permissions: get, wrapKey, unwrapKey.</span></span>

### <span data-ttu-id="01257-117">예제 3: app conifguration store의 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-117">Example 3: Disable encryption of an app conifguration store.</span></span>
```powershell
PS C:\> $appConf = Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -EncryptionKeyIdentifier $null

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="01257-118">이 명령은 app conifguration store의 암호화를 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-118">This command disables encryption of an app conifguration store.</span></span>

### <span data-ttu-id="01257-119">예제 3: 파이프라인을 기준으로 앱 conifguration 저장소의 sku 및 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-119">Example 3: Update sku and tag of an app conifguration store by pipeline.</span></span>
```powershell
PS C:\> Get-AzAppConfigurationStore -ResourceGroupName azpwsh-manual-test -Name appconfig-test10 | Update-AzAppConfigurationStore -Sku 'standard' -Tag @{'key'='update'}

Location Name             Type
-------- ----             ----
eastus   appconfig-test10 Microsoft.AppConfiguration/configurationStores
```

<span data-ttu-id="01257-120">이 명령은 파이프라인 별로 app conifguration store의 sku 및 태그를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-120">This command updates sku and tag of an app conifguration store by pipeline.</span></span>

## <span data-ttu-id="01257-121">변수</span><span class="sxs-lookup"><span data-stu-id="01257-121">PARAMETERS</span></span>

### <span data-ttu-id="01257-122">-AsJob</span><span class="sxs-lookup"><span data-stu-id="01257-122">-AsJob</span></span>
<span data-ttu-id="01257-123">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="01257-123">Run the command as a job</span></span>

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

### <span data-ttu-id="01257-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01257-124">-DefaultProfile</span></span>
<span data-ttu-id="01257-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="01257-126">-EncryptionKeyIdentifier</span><span class="sxs-lookup"><span data-stu-id="01257-126">-EncryptionKeyIdentifier</span></span>
<span data-ttu-id="01257-127">데이터를 암호화 하는 데 사용 되는 키 보관소 키의 URI입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-127">The URI of the key vault key used to encrypt data.</span></span>

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

### <span data-ttu-id="01257-128">-IdentityType</span><span class="sxs-lookup"><span data-stu-id="01257-128">-IdentityType</span></span>
<span data-ttu-id="01257-129">사용 되는 관리 되는 id의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-129">The type of managed identity used.</span></span>
<span data-ttu-id="01257-130">' SystemAssignedAndUserAssigned ' 형식에는 암시적으로 만들어진 id와 사용자 지정 id 집합이 모두 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="01257-130">The type 'SystemAssignedAndUserAssigned' includes both an implicitly created identity and a set of user-assigned identities.</span></span>
<span data-ttu-id="01257-131">' 없음 ' 형식은 id를 모두 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-131">The type 'None' will remove any identities.</span></span>

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

### <span data-ttu-id="01257-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="01257-132">-InputObject</span></span>
<span data-ttu-id="01257-133">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="01257-133">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="01257-134">-KeyVaultIdentityClientId</span><span class="sxs-lookup"><span data-stu-id="01257-134">-KeyVaultIdentityClientId</span></span>
<span data-ttu-id="01257-135">키 자격 증명 모음에 액세스 하는 데 사용 되는 id의 클라이언트 id입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-135">The client id of the identity which will be used to access key vault.</span></span>

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

### <span data-ttu-id="01257-136">-이름</span><span class="sxs-lookup"><span data-stu-id="01257-136">-Name</span></span>
<span data-ttu-id="01257-137">구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-137">The name of the configuration store.</span></span>

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

### <span data-ttu-id="01257-138">-NoWait</span><span class="sxs-lookup"><span data-stu-id="01257-138">-NoWait</span></span>
<span data-ttu-id="01257-139">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="01257-139">Run the command asynchronously</span></span>

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

### <span data-ttu-id="01257-140">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01257-140">-ResourceGroupName</span></span>
<span data-ttu-id="01257-141">컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-141">The name of the resource group to which the container registry belongs.</span></span>

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

### <span data-ttu-id="01257-142">-Sku</span><span class="sxs-lookup"><span data-stu-id="01257-142">-Sku</span></span>
<span data-ttu-id="01257-143">구성 저장소의 SKU 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-143">The SKU name of the configuration store.</span></span>

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

### <span data-ttu-id="01257-144">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="01257-144">-SubscriptionId</span></span>
<span data-ttu-id="01257-145">Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-145">The Microsoft Azure subscription ID.</span></span>

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

### <span data-ttu-id="01257-146">태그</span><span class="sxs-lookup"><span data-stu-id="01257-146">-Tag</span></span>
<span data-ttu-id="01257-147">ARM 리소스 태그입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-147">The ARM resource tags.</span></span>

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

### <span data-ttu-id="01257-148">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="01257-148">-UserAssignedIdentity</span></span>
<span data-ttu-id="01257-149">리소스와 연결 된 사용자 할당 id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-149">The list of user-assigned identities associated with the resource.</span></span>
<span data-ttu-id="01257-150">사용자 할당 id 사전 키는 '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName} ' 형식의 리소스 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-150">The user-assigned identity dictionary keys will be ARM resource ids in the form: '/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.ManagedIdentity/userAssignedIdentities/{identityName}'.</span></span>

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

### <span data-ttu-id="01257-151">-확인</span><span class="sxs-lookup"><span data-stu-id="01257-151">-Confirm</span></span>
<span data-ttu-id="01257-152">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-152">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="01257-153">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="01257-153">-WhatIf</span></span>
<span data-ttu-id="01257-154">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="01257-154">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="01257-155">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="01257-155">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="01257-156">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01257-156">CommonParameters</span></span>
<span data-ttu-id="01257-157">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-157">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01257-158">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="01257-158">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01257-159">입력</span><span class="sxs-lookup"><span data-stu-id="01257-159">INPUTS</span></span>

### <span data-ttu-id="01257-160">Microsoft. p p. p. p i d.</span><span class="sxs-lookup"><span data-stu-id="01257-160">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.IAppConfigurationIdentity</span></span>

## <span data-ttu-id="01257-161">출력</span><span class="sxs-lookup"><span data-stu-id="01257-161">OUTPUTS</span></span>

### <span data-ttu-id="01257-162">Api20200601. IConfigurationStore에 대 한 Microsoft.</span><span class="sxs-lookup"><span data-stu-id="01257-162">Microsoft.Azure.PowerShell.Cmdlets.AppConfiguration.Models.Api20200601.IConfigurationStore</span></span>

## <span data-ttu-id="01257-163">상속자</span><span class="sxs-lookup"><span data-stu-id="01257-163">NOTES</span></span>

<span data-ttu-id="01257-164">별칭과</span><span class="sxs-lookup"><span data-stu-id="01257-164">ALIASES</span></span>

<span data-ttu-id="01257-165">복합 매개 변수 속성</span><span class="sxs-lookup"><span data-stu-id="01257-165">COMPLEX PARAMETER PROPERTIES</span></span>

<span data-ttu-id="01257-166">아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="01257-166">To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="01257-167">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="01257-167">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>


<span data-ttu-id="01257-168">INPUTOBJECT <IAppConfigurationIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="01257-168">INPUTOBJECT <IAppConfigurationIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="01257-169">`[ConfigStoreName <String>]`: 구성 저장소의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-169">`[ConfigStoreName <String>]`: The name of the configuration store.</span></span>
  - <span data-ttu-id="01257-170">`[GroupName <String>]`: 비공개 링크 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-170">`[GroupName <String>]`: The name of the private link resource group.</span></span>
  - <span data-ttu-id="01257-171">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="01257-171">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="01257-172">`[PrivateEndpointConnectionName <String>]`: 개인 끝점 연결 이름</span><span class="sxs-lookup"><span data-stu-id="01257-172">`[PrivateEndpointConnectionName <String>]`: Private endpoint connection name</span></span>
  - <span data-ttu-id="01257-173">`[ResourceGroupName <String>]`: 컨테이너 레지스트리가 속한 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-173">`[ResourceGroupName <String>]`: The name of the resource group to which the container registry belongs.</span></span>
  - <span data-ttu-id="01257-174">`[SubscriptionId <String>]`: Microsoft Azure 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="01257-174">`[SubscriptionId <String>]`: The Microsoft Azure subscription ID.</span></span>

## <span data-ttu-id="01257-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01257-175">RELATED LINKS</span></span>



<span data-ttu-id="01257-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0) 
 [새로운 AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span><span class="sxs-lookup"><span data-stu-id="01257-176">[Set-AzKeyVaultAccessPolicy](https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy?view=azps-4.4.0)
[New-AzUserAssignedIdentity](https://docs.microsoft.com/en-us/powershell/module/az.managedserviceidentity/new-azuserassignedidentity?view=azps-4.4.0)</span></span>

