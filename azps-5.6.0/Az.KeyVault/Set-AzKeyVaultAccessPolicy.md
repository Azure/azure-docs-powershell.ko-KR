---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 77f6ac36f756e89859d38a0c608139dfe28c9667
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954587"
---
# <span data-ttu-id="99880-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="99880-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="99880-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="99880-102">SYNOPSIS</span></span>
<span data-ttu-id="99880-103">키 자격 증명 모음을 사용하여 작업을 수행하도록 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 사용 권한을 부여하거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="99880-104">구문</span><span class="sxs-lookup"><span data-stu-id="99880-104">SYNTAX</span></span>

### <span data-ttu-id="99880-105">ByUserPrincipalName(기본값)</span><span class="sxs-lookup"><span data-stu-id="99880-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="99880-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="99880-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="99880-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="99880-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="99880-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="99880-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="99880-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="99880-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="99880-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="99880-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="99880-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="99880-120">설명</span><span class="sxs-lookup"><span data-stu-id="99880-120">DESCRIPTION</span></span>
<span data-ttu-id="99880-121">**Set-AzKeyVaultAccessPolicy** cmdlet은 키 자격 증명 모음을 사용하여 지정된 작업을 수행하기 위해 사용자, 애플리케이션 또는 보안 그룹에 대한 기존 권한을 부여하거나 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="99880-122">다른 사용자, 애플리케이션 또는 보안 그룹이 키 자격 증명 모음에 있는 권한을 수정하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="99880-123">보안 그룹에 대한 사용 권한을 설정하는 경우 이 작업은 해당 보안 그룹의 사용자에만 영향을 미치게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="99880-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="99880-124">다음 디렉터리는 모두 동일한 Azure 디렉터리가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="99880-125">키 자격 증명 모음이 있는 Azure 구독의 기본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="99880-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="99880-126">권한을 부여하는 사용자 또는 애플리케이션 그룹을 포함하는 Azure 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="99880-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="99880-127">이러한 조건을 충족하지 못하고 이 cmdlet이 작동하지 않는 시나리오의 예는 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="99880-128">다른 조직의 사용자가 키 자격 증명 모음을 관리할 수 있도록 권한을 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="99880-129">각 조직에는 자체 디렉터리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="99880-130">Azure 계정에는 여러 개의 감독이 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="99880-131">기본 디렉터리가 다른 디렉터리에 애플리케이션을 등록하는 경우 해당 애플리케이션이 키 자격 증명 모음을 사용할 수 있도록 권한을 승인할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="99880-132">애플리케이션은 기본 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-132">The application must be in the default directory.</span></span>
<span data-ttu-id="99880-133">이 cmdlet에서는 리소스 그룹을 지정하는 것이 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="99880-134">서비스 주체를 사용하여 액세스 정책 권한을 부여하는 경우 매개 변수를 사용해야 `-BypassObjectIdValidation` 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="99880-135">예제</span><span class="sxs-lookup"><span data-stu-id="99880-135">EXAMPLES</span></span>

### <span data-ttu-id="99880-136">예제 1: 키 자격 증명 모음에 대한 사용자에게 권한 부여 및 사용 권한 수정</span><span class="sxs-lookup"><span data-stu-id="99880-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="99880-137">첫 번째 명령은 Azure Active Directory의 사용자에게 Contoso03Vault라는 키 자격 증명 모음을 사용하여 키 및 비밀에 대한 작업을 수행할 수 있는 권한을 PattiFuller@contoso.com 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="99880-138">*PassThru 매개* 변수는 cmdlet에서 업데이트된 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="99880-139">두 번째 명령은 첫 번째 명령에서 부여된 권한을 수정하여 이제 비밀을 설정하고 삭제하는 것 외에도 비밀을 지울 PattiFuller@contoso.com 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="99880-140">키 작업에 대한 사용 권한은 이 명령 이후에 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="99880-141">최종 명령은 키 작업에 대한 모든 권한을 제거하기 위한 기존 권한을 PattiFuller@contoso.com 추가로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="99880-142">비밀 작업에 대한 사용 권한은 이 명령 후에 변경되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="99880-143">예제 2: 애플리케이션 서비스 주체가 비밀을 읽고 쓸 수 있는 권한 부여</span><span class="sxs-lookup"><span data-stu-id="99880-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="99880-144">이 명령은 Contoso03Vault라는 키 자격 증명 모음에 대한 애플리케이션에 대한 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="99880-145">*ServicePrincipalName 매개 변수는* 애플리케이션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="99880-146">애플리케이션을 Azure Active Directory에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="99880-147">*ServicePrincipalName* 매개 변수의 값은 애플리케이션의 서비스 주체 이름 또는 애플리케이션 ID GUID가 되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="99880-148">이 예제에서는 서비스 주체 이름을 지정하며 명령은 비밀을 읽고 쓸 수 있는 애플리케이션 권한을 `http://payroll.contoso.com` 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="99880-149">예제 3: 개체 ID를 사용하여 애플리케이션에 대한 권한 부여</span><span class="sxs-lookup"><span data-stu-id="99880-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="99880-150">이 명령은 애플리케이션에게 비밀을 읽고 쓸 수 있는 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="99880-151">이 예제에서는 애플리케이션의 서비스 주체의 개체 ID를 사용하여 애플리케이션을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="99880-152">예제 4: 사용자 주체 이름에 대한 권한 부여</span><span class="sxs-lookup"><span data-stu-id="99880-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="99880-153">이 명령은 비밀에 대한 액세스에 대해 지정된 사용자 주체 이름에 대한 권한을 얻게, 나열하고, 설정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="99880-154">예제 5: Microsoft.Compute 리소스 공급자가 키 자격 증명 모음에서 비밀을 검색하도록 설정</span><span class="sxs-lookup"><span data-stu-id="99880-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="99880-155">이 명령은 Microsoft.Compute 리소스 공급자가 Contoso03Vault 키 자격 증명 모음에서 검색할 수 있는 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="99880-156">예제 6: 보안 그룹에 권한 부여</span><span class="sxs-lookup"><span data-stu-id="99880-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="99880-157">첫 번째 명령은 Get-AzADGroup cmdlet을 사용하여 모든 Active Directory 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="99880-158">출력에서 **그룹1, group2** 및 **group3이라는** 3개 그룹이 **반환됩니다.**</span><span class="sxs-lookup"><span data-stu-id="99880-158">From the output, you see 3 groups returned, named **group1**, **group2**, and **group3**.</span></span> <span data-ttu-id="99880-159">여러 그룹에는 이름이 같지만 항상 고유한 ObjectId가 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="99880-160">이름이 같은 두 개 이상의 그룹이 반환되는 경우 출력의 ObjectId를 사용하여 사용할 그룹을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="99880-161">그런 다음 이 명령의 출력을 Set-AzKeyVaultAccessPolicy **myownvault라는** 키 자격 증명 모음에 대한 group2에 대한 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="99880-162">이 예제에서는 동일한 명령줄에 'group2' 인라인이라는 그룹을 열소합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="99880-163">반환된 목록에 'group2'라는 그룹이 여러 개 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="99880-164">이 예제에서는 반환된 목록에서 인덱스 0으로 표시된 첫 번째를 \[ \] 선택합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="99880-165">예제 7: BYOK(고객 관리 테넌트 키에 대한 Azure Information Protection 액세스 권한 부여)</span><span class="sxs-lookup"><span data-stu-id="99880-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="99880-166">이 명령은 Azure Information Protection에서 고객 관리 키(사용자 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테넌트 키로 사용할 수 있도록 권한을 Azure Information Protection에 권한을 줍니다.</span><span class="sxs-lookup"><span data-stu-id="99880-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="99880-167">이 명령을 실행할 때 사용자 지정 키 자격 증명 모음 이름을 지정하지만 GUID **000000012-0000-c0000-000000000000000으로** *ServicePrincipalName* 매개 변수를 지정하고 예제에서 사용 권한을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="99880-168">매개 변수</span><span class="sxs-lookup"><span data-stu-id="99880-168">PARAMETERS</span></span>

### <span data-ttu-id="99880-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="99880-169">-ApplicationId</span></span>
<span data-ttu-id="99880-170">향후 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-170">For future use.</span></span>

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

### <span data-ttu-id="99880-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="99880-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="99880-172">Azure Active Directory에 개체가 존재하는지 확인하지 않고 개체 ID를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="99880-173">다른 Azure 테넌트에서 위임된 보안 그룹을 참조하는 개체 ID에 대한 키 자격 증명 모음에 대한 액세스 권한을 부여하려는 경우만 이 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="99880-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="99880-174">-DefaultProfile</span></span>
<span data-ttu-id="99880-175">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="99880-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="99880-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="99880-176">-EmailAddress</span></span>
<span data-ttu-id="99880-177">권한을 부여할 사용자의 사용자 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="99880-178">이 전자 메일 주소는 현재 구독과 연결된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="99880-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="99880-179">-EnabledForDeployment</span></span>
<span data-ttu-id="99880-180">가상 머신을 만들 때와 같은 리소스 만들기에서 이 키 자격 증명 모음을 참조할 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="99880-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="99880-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="99880-182">Azure 디스크 암호화 서비스를 사용하여 이 키 자격 증명 모음에서 비밀을 얻고 키를 래프 래프할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="99880-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="99880-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="99880-184">이 키 자격 증명 모음이 템플릿 배포에서 참조될 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀을 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="99880-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="99880-185">-InputObject</span></span>
<span data-ttu-id="99880-186">Key Vault 개체</span><span class="sxs-lookup"><span data-stu-id="99880-186">Key Vault Object</span></span>

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

### <span data-ttu-id="99880-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="99880-187">-ObjectId</span></span>
<span data-ttu-id="99880-188">권한을 부여할 Azure Active Directory의 사용자 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="99880-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="99880-189">-PassThru</span></span>
<span data-ttu-id="99880-190">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="99880-191">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="99880-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="99880-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="99880-193">사용자 또는 서비스 주체에 부여할 인증서 사용 권한 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="99880-194">이 매개 변수에 대해 허용되는 값:</span><span class="sxs-lookup"><span data-stu-id="99880-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="99880-195">모두</span><span class="sxs-lookup"><span data-stu-id="99880-195">All</span></span>
- <span data-ttu-id="99880-196">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-196">Get</span></span>
- <span data-ttu-id="99880-197">목록</span><span class="sxs-lookup"><span data-stu-id="99880-197">List</span></span>
- <span data-ttu-id="99880-198">삭제</span><span class="sxs-lookup"><span data-stu-id="99880-198">Delete</span></span>
- <span data-ttu-id="99880-199">만들기</span><span class="sxs-lookup"><span data-stu-id="99880-199">Create</span></span>
- <span data-ttu-id="99880-200">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-200">Import</span></span>
- <span data-ttu-id="99880-201">업데이트</span><span class="sxs-lookup"><span data-stu-id="99880-201">Update</span></span>
- <span data-ttu-id="99880-202">관리contacts</span><span class="sxs-lookup"><span data-stu-id="99880-202">Managecontacts</span></span>
- <span data-ttu-id="99880-203">Getissuers</span><span class="sxs-lookup"><span data-stu-id="99880-203">Getissuers</span></span>
- <span data-ttu-id="99880-204">Listissuers</span><span class="sxs-lookup"><span data-stu-id="99880-204">Listissuers</span></span>
- <span data-ttu-id="99880-205">Setissuers</span><span class="sxs-lookup"><span data-stu-id="99880-205">Setissuers</span></span>
- <span data-ttu-id="99880-206">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="99880-206">Deleteissuers</span></span>
- <span data-ttu-id="99880-207">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="99880-207">Manageissuers</span></span>
- <span data-ttu-id="99880-208">복구</span><span class="sxs-lookup"><span data-stu-id="99880-208">Recover</span></span>
- <span data-ttu-id="99880-209">백업</span><span class="sxs-lookup"><span data-stu-id="99880-209">Backup</span></span>
- <span data-ttu-id="99880-210">복원</span><span class="sxs-lookup"><span data-stu-id="99880-210">Restore</span></span>
- <span data-ttu-id="99880-211">제거</span><span class="sxs-lookup"><span data-stu-id="99880-211">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, backup, restore

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99880-212">-PermissionsToKeys</span><span class="sxs-lookup"><span data-stu-id="99880-212">-PermissionsToKeys</span></span>
<span data-ttu-id="99880-213">사용자 또는 서비스 주체에 부여할 키 작업 권한의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-213">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="99880-214">이 매개 변수에 대해 허용되는 값:</span><span class="sxs-lookup"><span data-stu-id="99880-214">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="99880-215">모두</span><span class="sxs-lookup"><span data-stu-id="99880-215">All</span></span>
- <span data-ttu-id="99880-216">암호 해독</span><span class="sxs-lookup"><span data-stu-id="99880-216">Decrypt</span></span>
- <span data-ttu-id="99880-217">암호화</span><span class="sxs-lookup"><span data-stu-id="99880-217">Encrypt</span></span>
- <span data-ttu-id="99880-218">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="99880-218">UnwrapKey</span></span>
- <span data-ttu-id="99880-219">WrapKey</span><span class="sxs-lookup"><span data-stu-id="99880-219">WrapKey</span></span>
- <span data-ttu-id="99880-220">확인</span><span class="sxs-lookup"><span data-stu-id="99880-220">Verify</span></span>
- <span data-ttu-id="99880-221">서명</span><span class="sxs-lookup"><span data-stu-id="99880-221">Sign</span></span>
- <span data-ttu-id="99880-222">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-222">Get</span></span>
- <span data-ttu-id="99880-223">목록</span><span class="sxs-lookup"><span data-stu-id="99880-223">List</span></span>
- <span data-ttu-id="99880-224">업데이트</span><span class="sxs-lookup"><span data-stu-id="99880-224">Update</span></span>
- <span data-ttu-id="99880-225">만들기</span><span class="sxs-lookup"><span data-stu-id="99880-225">Create</span></span>
- <span data-ttu-id="99880-226">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-226">Import</span></span>
- <span data-ttu-id="99880-227">삭제</span><span class="sxs-lookup"><span data-stu-id="99880-227">Delete</span></span>
- <span data-ttu-id="99880-228">백업</span><span class="sxs-lookup"><span data-stu-id="99880-228">Backup</span></span>
- <span data-ttu-id="99880-229">복원</span><span class="sxs-lookup"><span data-stu-id="99880-229">Restore</span></span>
- <span data-ttu-id="99880-230">복구</span><span class="sxs-lookup"><span data-stu-id="99880-230">Recover</span></span>
- <span data-ttu-id="99880-231">제거</span><span class="sxs-lookup"><span data-stu-id="99880-231">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99880-232">-PermissionsToSecrets</span><span class="sxs-lookup"><span data-stu-id="99880-232">-PermissionsToSecrets</span></span>
<span data-ttu-id="99880-233">사용자 또는 서비스 주체에 부여할 비밀 작업 사용 권한 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-233">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="99880-234">이 매개 변수에 대해 허용되는 값:</span><span class="sxs-lookup"><span data-stu-id="99880-234">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="99880-235">모두</span><span class="sxs-lookup"><span data-stu-id="99880-235">All</span></span>
- <span data-ttu-id="99880-236">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-236">Get</span></span>
- <span data-ttu-id="99880-237">목록</span><span class="sxs-lookup"><span data-stu-id="99880-237">List</span></span>
- <span data-ttu-id="99880-238">설정</span><span class="sxs-lookup"><span data-stu-id="99880-238">Set</span></span>
- <span data-ttu-id="99880-239">삭제</span><span class="sxs-lookup"><span data-stu-id="99880-239">Delete</span></span>
- <span data-ttu-id="99880-240">백업</span><span class="sxs-lookup"><span data-stu-id="99880-240">Backup</span></span>
- <span data-ttu-id="99880-241">복원</span><span class="sxs-lookup"><span data-stu-id="99880-241">Restore</span></span>
- <span data-ttu-id="99880-242">복구</span><span class="sxs-lookup"><span data-stu-id="99880-242">Recover</span></span>
- <span data-ttu-id="99880-243">제거</span><span class="sxs-lookup"><span data-stu-id="99880-243">Purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, set, delete, backup, restore, recover, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99880-244">-PermissionsToStorage</span><span class="sxs-lookup"><span data-stu-id="99880-244">-PermissionsToStorage</span></span>
<span data-ttu-id="99880-245">사용자 또는 서비스 주체에 부여할 관리 저장소 계정 및 SaS-definition 작업 권한을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-245">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="99880-246">이 매개 변수에 대해 허용되는 값:</span><span class="sxs-lookup"><span data-stu-id="99880-246">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="99880-247">모든</span><span class="sxs-lookup"><span data-stu-id="99880-247">all</span></span>
- <span data-ttu-id="99880-248">가져오기</span><span class="sxs-lookup"><span data-stu-id="99880-248">get</span></span>
- <span data-ttu-id="99880-249">목록</span><span class="sxs-lookup"><span data-stu-id="99880-249">list</span></span>
- <span data-ttu-id="99880-250">delete</span><span class="sxs-lookup"><span data-stu-id="99880-250">delete</span></span>
- <span data-ttu-id="99880-251">집합</span><span class="sxs-lookup"><span data-stu-id="99880-251">set</span></span>
- <span data-ttu-id="99880-252">업데이트</span><span class="sxs-lookup"><span data-stu-id="99880-252">update</span></span>
- <span data-ttu-id="99880-253">regeneratekey</span><span class="sxs-lookup"><span data-stu-id="99880-253">regeneratekey</span></span>
- <span data-ttu-id="99880-254">getsas</span><span class="sxs-lookup"><span data-stu-id="99880-254">getsas</span></span>
- <span data-ttu-id="99880-255">listsas</span><span class="sxs-lookup"><span data-stu-id="99880-255">listsas</span></span>
- <span data-ttu-id="99880-256">deletesas</span><span class="sxs-lookup"><span data-stu-id="99880-256">deletesas</span></span>
- <span data-ttu-id="99880-257">setas</span><span class="sxs-lookup"><span data-stu-id="99880-257">setsas</span></span>
- <span data-ttu-id="99880-258">복구</span><span class="sxs-lookup"><span data-stu-id="99880-258">recover</span></span>
- <span data-ttu-id="99880-259">Backup</span><span class="sxs-lookup"><span data-stu-id="99880-259">backup</span></span>
- <span data-ttu-id="99880-260">복원</span><span class="sxs-lookup"><span data-stu-id="99880-260">restore</span></span>
- <span data-ttu-id="99880-261">제거</span><span class="sxs-lookup"><span data-stu-id="99880-261">purge</span></span>

```yaml
Type: System.String[]
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmailAddress, InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmailAddress, ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmailAddress
Aliases:
Accepted values: all, get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, recover, backup, restore, purge

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="99880-262">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="99880-262">-ResourceGroupName</span></span>
<span data-ttu-id="99880-263">리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-263">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="99880-264">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="99880-264">-ResourceId</span></span>
<span data-ttu-id="99880-265">Key Vault 리소스 ID</span><span class="sxs-lookup"><span data-stu-id="99880-265">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="99880-266">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-266">-ServicePrincipalName</span></span>
<span data-ttu-id="99880-267">권한을 부여할 애플리케이션의 서비스 주체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-267">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="99880-268">AzureActive Directory에서 애플리케이션에 등록된 클라이언트 ID라고도 하는 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-268">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="99880-269">이 매개 변수가 지정하는 서비스 주체 이름이 있는 애플리케이션은 현재 구독을 포함하는 Azure 디렉터리에 등록해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-269">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="99880-270">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="99880-270">-UserPrincipalName</span></span>
<span data-ttu-id="99880-271">권한을 부여할 사용자의 사용자 주체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-271">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="99880-272">이 사용자 주체 이름은 현재 구독과 연결된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-272">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="99880-273">-VaultName</span><span class="sxs-lookup"><span data-stu-id="99880-273">-VaultName</span></span>
<span data-ttu-id="99880-274">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-274">Specifies the name of a key vault.</span></span>
<span data-ttu-id="99880-275">이 cmdlet은 이 매개 변수가 지정하는 키 자격 증명 모음에 대한 액세스 정책을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-275">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="99880-276">-확인</span><span class="sxs-lookup"><span data-stu-id="99880-276">-Confirm</span></span>
<span data-ttu-id="99880-277">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="99880-277">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="99880-278">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="99880-278">-WhatIf</span></span>
<span data-ttu-id="99880-279">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="99880-279">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="99880-280">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="99880-280">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="99880-281">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="99880-281">CommonParameters</span></span>
<span data-ttu-id="99880-282">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="99880-282">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="99880-283">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="99880-283">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="99880-284">입력</span><span class="sxs-lookup"><span data-stu-id="99880-284">INPUTS</span></span>

### <span data-ttu-id="99880-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="99880-285">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="99880-286">System.String</span><span class="sxs-lookup"><span data-stu-id="99880-286">System.String</span></span>

## <span data-ttu-id="99880-287">출력</span><span class="sxs-lookup"><span data-stu-id="99880-287">OUTPUTS</span></span>

### <span data-ttu-id="99880-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="99880-288">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="99880-289">참고 사항</span><span class="sxs-lookup"><span data-stu-id="99880-289">NOTES</span></span>

## <span data-ttu-id="99880-290">관련 링크</span><span class="sxs-lookup"><span data-stu-id="99880-290">RELATED LINKS</span></span>

[<span data-ttu-id="99880-291">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="99880-291">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="99880-292">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="99880-292">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

