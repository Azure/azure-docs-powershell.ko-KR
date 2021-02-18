---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410721"
---
# <span data-ttu-id="fd177-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd177-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="fd177-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fd177-102">SYNOPSIS</span></span>
<span data-ttu-id="fd177-103">키 자격 증명 모음을 사용하여 작업을 수행하도록 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 권한을 부여하거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="fd177-104">구문</span><span class="sxs-lookup"><span data-stu-id="fd177-104">SYNTAX</span></span>

### <span data-ttu-id="fd177-105">ByUserPrincipalName(기본값)</span><span class="sxs-lookup"><span data-stu-id="fd177-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd177-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd177-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="fd177-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd177-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd177-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="fd177-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="fd177-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="fd177-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd177-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="fd177-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="fd177-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="fd177-120">설명</span><span class="sxs-lookup"><span data-stu-id="fd177-120">DESCRIPTION</span></span>
<span data-ttu-id="fd177-121">**Set-AzKeyVaultAccessPolicy** cmdlet은 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 권한을 부여하거나 수정하여 키 자격 증명 모음으로 지정된 작업을 수행할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="fd177-122">다른 사용자, 애플리케이션 또는 보안 그룹이 키 자격 증명 모음에 있는 사용 권한을 수정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="fd177-123">보안 그룹에 대한 사용 권한을 설정하는 경우 이 작업은 해당 보안 그룹의 사용자에만 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="fd177-124">다음 디렉터리는 모두 동일한 Azure 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="fd177-125">키 자격 증명 모음이 있는 Azure 구독의 기본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="fd177-126">권한을 부여하는 사용자 또는 애플리케이션 그룹을 포함하는 Azure 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="fd177-127">이러한 조건이 충족되지 않을 때 이 cmdlet이 작동하지 않는 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="fd177-128">다른 조직의 사용자에게 키 자격 증명 모음을 관리할 수 있는 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="fd177-129">각 조직에는 자체 디렉터리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="fd177-130">Azure 계정에는 여러 개의 감독이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="fd177-131">기본 디렉터리가 다른 디렉터리에 애플리케이션을 등록하는 경우 해당 애플리케이션에 키 자격 증명 모음을 사용할 수 있는 권한을 승인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="fd177-132">애플리케이션은 기본 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-132">The application must be in the default directory.</span></span>
<span data-ttu-id="fd177-133">이 cmdlet에 대해 리소스 그룹을 지정하는 것은 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="fd177-134">서비스 주체에 액세스 정책 권한을 부여하는 경우 매개 변수를 사용해야 `-BypassObjectIdValidation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="fd177-135">예제</span><span class="sxs-lookup"><span data-stu-id="fd177-135">EXAMPLES</span></span>

### <span data-ttu-id="fd177-136">예제 1: 키 자격 증명 모음에 대한 사용자에게 권한 부여 및 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="fd177-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        : create, import, delete, list
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :

PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : True
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             : True
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     : set, delete, get
                                   Permissions to Certificates                :
                                   Permissions to (Key Vault Managed) Storage :

Tags                             :
```

<span data-ttu-id="fd177-137">첫 번째 명령은 Contoso03Vault라는 키 자격 증명 모음을 사용하여 키 및 비밀에 대한 작업을 수행하는 Azure Active Directory의 사용자에 대한 권한을 PattiFuller@contoso.com 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="fd177-138">*PassThru* 매개 변수는 cmdlet에서 업데이트된 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="fd177-139">두 번째 명령은 첫 번째 명령에서 부여된 권한을 수정하여 이제 비밀을 설정하고 삭제하는 것 외에도 비밀을 사용할 PattiFuller@contoso.com 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="fd177-140">이 명령 후에도 키 작업에 대한 사용 권한은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="fd177-141">마지막 명령은 키 작업에 대한 모든 권한을 제거하기 위해 기존 권한을 PattiFuller@contoso.com 추가로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="fd177-142">이 명령 후에도 비밀 작업에 대한 사용 권한은 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="fd177-143">예제 2: 애플리케이션 서비스 주체가 비밀을 읽고 쓸 수 있는 권한 부여</span><span class="sxs-lookup"><span data-stu-id="fd177-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fd177-144">이 명령은 Contoso03Vault라는 키 자격 증명 모음에 대한 애플리케이션에 대한 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="fd177-145">*ServicePrincipalName* 매개 변수는 애플리케이션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="fd177-146">애플리케이션을 Azure Active Directory에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="fd177-147">*ServicePrincipalName* 매개 변수의 값은 애플리케이션의 서비스 주체 이름 또는 애플리케이션 ID GUID가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="fd177-148">이 예제에서는 서비스 주체 이름을 지정하고 이 명령은 비밀을 읽고 쓸 수 있는 애플리케이션 권한을 `http://payroll.contoso.com` 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="fd177-149">예제 3: 개체 ID를 사용하여 애플리케이션에 대한 권한 부여</span><span class="sxs-lookup"><span data-stu-id="fd177-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="fd177-150">이 명령은 비밀을 읽고 쓸 수 있는 권한을 애플리케이션에 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="fd177-151">이 예제에서는 애플리케이션의 서비스 주체의 개체 ID를 사용하여 애플리케이션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="fd177-152">예제 4: 사용자 계정 이름에 대한 권한 부여</span><span class="sxs-lookup"><span data-stu-id="fd177-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="fd177-153">이 명령은 비밀에 액세스하기 위해 지정된 사용자 계정 이름에 대한 권한을 얻게, 나열하고, 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="fd177-154">예제 5: Microsoft.Compute 리소스 공급자가 키 자격 증명 모음에서 비밀을 검색할 수 있도록 설정</span><span class="sxs-lookup"><span data-stu-id="fd177-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="fd177-155">이 명령은 Microsoft.Compute 리소스 공급자가 Contoso03Vault 키 자격 증명 모음에서 검색할 비밀에 대한 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="fd177-156">예제 6: 보안 그룹에 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="fd177-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="fd177-157">첫 번째 명령은 Get-AzADGroup cmdlet을 사용하여 모든 Active Directory 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="fd177-158">출력에서 그룹 **1,** **group2** 및 **group3이라는 3개 그룹이 반환됩니다.**</span><span class="sxs-lookup"><span data-stu-id="fd177-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="fd177-159">여러 그룹에는 이름이 같을 수 있지만 항상 고유한 ObjectId가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="fd177-160">이름이 같은 그룹이 두 개 이상 반환되는 경우 출력의 ObjectId를 사용하여 사용하려는 그룹을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="fd177-161">그런 다음, 이 명령의 출력을 Set-AzKeyVaultAccessPolicy **myownvault라는** 키 자격 증명 모음에 대한 group2에 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="fd177-162">이 예제에서는 동일한 명령줄에서 'group2'라는 그룹을 인라인으로 열고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="fd177-163">반환된 목록에 'group2'라는 그룹이 여러 개 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="fd177-164">이 예제에서는 반환된 목록의 인덱스 0으로 표시된 첫 번째 \[ \] 예제를 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="fd177-165">예제 7: 고객 관리 테넌트 키(BYOK)에 대한 Azure Information Protection 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="fd177-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="fd177-166">이 명령은 Azure Information Protection 테넌트 키로 고객 관리 키(사용자 키 가져오기 또는 "BYOK" 시나리오)를 사용할 수 있도록 Azure Information Protection에 권한을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="fd177-167">이 명령을 실행할 때 사용자 자신의 키 자격 증명 모음 이름을 지정하지만 GUID **00000012-0000-0000-c000-00000000000000으로** *ServicePrincipalName* 매개 변수를 지정하고 예제에서 사용 권한을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="fd177-168">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fd177-168">PARAMETERS</span></span>

### <span data-ttu-id="fd177-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="fd177-169">-ApplicationId</span></span>
<span data-ttu-id="fd177-170">향후 사용을 위해</span><span class="sxs-lookup"><span data-stu-id="fd177-170">For future use.</span></span>

```yaml
Type: System.Nullable`1[System.Guid]
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="fd177-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="fd177-172">Azure Active Directory에 개체가 존재하는지 확인하지 않고 개체 ID를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="fd177-173">다른 Azure 테넌트에서 위임된 보안 그룹을 참조하는 개체 ID에 대한 키 자격 증명 모음에 대한 액세스 권한을 부여하려는 경우 이 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fd177-174">-DefaultProfile</span></span>
<span data-ttu-id="fd177-175">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fd177-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fd177-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="fd177-176">-EmailAddress</span></span>
<span data-ttu-id="fd177-177">권한을 부여할 사용자의 사용자 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fd177-178">이 전자 메일 주소는 현재 구독과 연결된 디렉터리에 있어야하며 고유해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmailAddress, InputObjectByEmailAddress, ResourceIdByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="fd177-179">-EnabledForDeployment</span></span>
<span data-ttu-id="fd177-180">예를 들어 가상 머신을 만들 때 이 키 자격 증명 모음이 리소스 생성에서 참조될 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="fd177-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="fd177-182">Azure 디스크 암호화 서비스를 사용하면 이 키 자격 증명 모음에서 비밀을 얻을 수 있으며 키 래프를 래프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="fd177-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="fd177-184">이 키 자격 증명 모음이 템플릿 배포에서 참조될 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ForVault, InputObjectForVault, ResourceIdForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="fd177-185">-InputObject</span></span>
<span data-ttu-id="fd177-186">Key Vault 개체</span><span class="sxs-lookup"><span data-stu-id="fd177-186">Key Vault Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fd177-187">-ObjectId</span></span>
<span data-ttu-id="fd177-188">권한을 부여할 Azure Active Directory에서 사용자 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: System.String
Parameter Sets: ByObjectId, InputObjectByObjectId, ResourceIdByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="fd177-189">-PassThru</span></span>
<span data-ttu-id="fd177-190">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="fd177-191">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="fd177-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="fd177-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="fd177-193">사용자 또는 서비스 주체에 부여할 인증서 권한의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd177-194">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="fd177-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd177-195">가져오기</span><span class="sxs-lookup"><span data-stu-id="fd177-195">Get</span></span>
- <span data-ttu-id="fd177-196">목록</span><span class="sxs-lookup"><span data-stu-id="fd177-196">List</span></span>
- <span data-ttu-id="fd177-197">삭제</span><span class="sxs-lookup"><span data-stu-id="fd177-197">Delete</span></span>
- <span data-ttu-id="fd177-198">만들기</span><span class="sxs-lookup"><span data-stu-id="fd177-198">Create</span></span>
- <span data-ttu-id="fd177-199">가져오기</span><span class="sxs-lookup"><span data-stu-id="fd177-199">Import</span></span>
- <span data-ttu-id="fd177-200">업데이트</span><span class="sxs-lookup"><span data-stu-id="fd177-200">Update</span></span>
- <span data-ttu-id="fd177-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="fd177-201">Managecontacts</span></span>
- <span data-ttu-id="fd177-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="fd177-202">Getissuers</span></span>
- <span data-ttu-id="fd177-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="fd177-203">Listissuers</span></span>
- <span data-ttu-id="fd177-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="fd177-204">Setissuers</span></span>
- <span data-ttu-id="fd177-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="fd177-205">Deleteissuers</span></span>
- <span data-ttu-id="fd177-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="fd177-206">Manageissuers</span></span>
- <span data-ttu-id="fd177-207">복구</span><span class="sxs-lookup"><span data-stu-id="fd177-207">Recover</span></span>
- <span data-ttu-id="fd177-208">Backup</span><span class="sxs-lookup"><span data-stu-id="fd177-208">Backup</span></span>
- <span data-ttu-id="fd177-209">복원</span><span class="sxs-lookup"><span data-stu-id="fd177-209">Restore</span></span>
- <span data-ttu-id="fd177-210">제거</span><span class="sxs-lookup"><span data-stu-id="fd177-210">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-211">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="fd177-211">-PermissionsToKeys</span></span>
<span data-ttu-id="fd177-212">사용자 또는 서비스 주체에 부여할 키 작업 권한의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd177-213">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="fd177-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd177-214">암호 해독</span><span class="sxs-lookup"><span data-stu-id="fd177-214">Decrypt</span></span>
- <span data-ttu-id="fd177-215">암호화</span><span class="sxs-lookup"><span data-stu-id="fd177-215">Encrypt</span></span>
- <span data-ttu-id="fd177-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="fd177-216">UnwrapKey</span></span>
- <span data-ttu-id="fd177-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="fd177-217">WrapKey</span></span>
- <span data-ttu-id="fd177-218">확인</span><span class="sxs-lookup"><span data-stu-id="fd177-218">Verify</span></span>
- <span data-ttu-id="fd177-219">서명</span><span class="sxs-lookup"><span data-stu-id="fd177-219">Sign</span></span>
- <span data-ttu-id="fd177-220">가져오기</span><span class="sxs-lookup"><span data-stu-id="fd177-220">Get</span></span>
- <span data-ttu-id="fd177-221">목록</span><span class="sxs-lookup"><span data-stu-id="fd177-221">List</span></span>
- <span data-ttu-id="fd177-222">업데이트</span><span class="sxs-lookup"><span data-stu-id="fd177-222">Update</span></span>
- <span data-ttu-id="fd177-223">만들기</span><span class="sxs-lookup"><span data-stu-id="fd177-223">Create</span></span>
- <span data-ttu-id="fd177-224">가져오기</span><span class="sxs-lookup"><span data-stu-id="fd177-224">Import</span></span>
- <span data-ttu-id="fd177-225">삭제</span><span class="sxs-lookup"><span data-stu-id="fd177-225">Delete</span></span>
- <span data-ttu-id="fd177-226">Backup</span><span class="sxs-lookup"><span data-stu-id="fd177-226">Backup</span></span>
- <span data-ttu-id="fd177-227">복원</span><span class="sxs-lookup"><span data-stu-id="fd177-227">Restore</span></span>
- <span data-ttu-id="fd177-228">복구</span><span class="sxs-lookup"><span data-stu-id="fd177-228">Recover</span></span>
- <span data-ttu-id="fd177-229">제거</span><span class="sxs-lookup"><span data-stu-id="fd177-229">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-230">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="fd177-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="fd177-231">사용자 또는 서비스 주체에 부여할 비밀 작업 권한의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="fd177-232">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="fd177-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="fd177-233">가져오기</span><span class="sxs-lookup"><span data-stu-id="fd177-233">Get</span></span>
- <span data-ttu-id="fd177-234">목록</span><span class="sxs-lookup"><span data-stu-id="fd177-234">List</span></span>
- <span data-ttu-id="fd177-235">설정</span><span class="sxs-lookup"><span data-stu-id="fd177-235">Set</span></span>
- <span data-ttu-id="fd177-236">삭제</span><span class="sxs-lookup"><span data-stu-id="fd177-236">Delete</span></span>
- <span data-ttu-id="fd177-237">Backup</span><span class="sxs-lookup"><span data-stu-id="fd177-237">Backup</span></span>
- <span data-ttu-id="fd177-238">복원</span><span class="sxs-lookup"><span data-stu-id="fd177-238">Restore</span></span>
- <span data-ttu-id="fd177-239">복구</span><span class="sxs-lookup"><span data-stu-id="fd177-239">Recover</span></span>
- <span data-ttu-id="fd177-240">제거</span><span class="sxs-lookup"><span data-stu-id="fd177-240">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-241">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="fd177-241">-PermissionsToStorage</span></span>
<span data-ttu-id="fd177-242">사용자 또는 서비스 주체에 부여할 관리되는 저장소 계정 및 SaS 정의 작업 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fd177-243">-ResourceGroupName</span></span>
<span data-ttu-id="fd177-244">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-244">Specifies the name of a resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="fd177-245">-ResourceId</span></span>
<span data-ttu-id="fd177-246">Key Vault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="fd177-246">Key Vault Resource Id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-247">-ServicePrincipalName</span></span>
<span data-ttu-id="fd177-248">권한을 부여할 애플리케이션의 서비스 주체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="fd177-249">AzureActive 디렉터리에서 애플리케이션에 등록된 클라이언트 ID라고도 하는 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="fd177-250">이 매개 변수가 지정하는 서비스 주체 이름이 있는 애플리케이션은 현재 구독을 포함하는 Azure 디렉터리에 등록되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName, ResourceIdByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="fd177-251">-UserPrincipalName</span></span>
<span data-ttu-id="fd177-252">권한을 부여할 사용자의 사용자 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="fd177-253">이 사용자 계정 이름은 현재 구독과 연결된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName, ResourceIdByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="fd177-254">-VaultName</span></span>
<span data-ttu-id="fd177-255">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="fd177-256">이 cmdlet은 이 매개 변수가 지정하는 키 자격 증명 모음에 대한 액세스 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fd177-257">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fd177-257">-Confirm</span></span>
<span data-ttu-id="fd177-258">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fd177-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fd177-259">-WhatIf</span></span>
<span data-ttu-id="fd177-260">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fd177-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fd177-261">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fd177-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fd177-262">CommonParameters</span></span>
<span data-ttu-id="fd177-263">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fd177-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fd177-264">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="fd177-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fd177-265">입력</span><span class="sxs-lookup"><span data-stu-id="fd177-265">INPUTS</span></span>

### <span data-ttu-id="fd177-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="fd177-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="fd177-267">System.String</span><span class="sxs-lookup"><span data-stu-id="fd177-267">System.String</span></span>

## <span data-ttu-id="fd177-268">출력</span><span class="sxs-lookup"><span data-stu-id="fd177-268">OUTPUTS</span></span>

### <span data-ttu-id="fd177-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd177-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="fd177-270">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fd177-270">NOTES</span></span>

## <span data-ttu-id="fd177-271">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fd177-271">RELATED LINKS</span></span>

[<span data-ttu-id="fd177-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="fd177-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="fd177-273">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="fd177-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

