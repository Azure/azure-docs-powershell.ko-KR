---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 5f47237088808fe8966d239f9a0de7c892301db0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226911"
---
# <span data-ttu-id="004b8-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004b8-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="004b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="004b8-102">SYNOPSIS</span></span>
<span data-ttu-id="004b8-103">키 자격 증명 모음을 사용 하 여 작업을 수행 하기 위해 사용자, 응용 프로그램 또는 보안 그룹에 대 한 기존 사용 권한을 부여 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="004b8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="004b8-104">SYNTAX</span></span>

### <span data-ttu-id="004b8-105">ByUserPrincipalName (기본값)</span><span class="sxs-lookup"><span data-stu-id="004b8-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="004b8-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="004b8-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="004b8-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="004b8-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="004b8-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="004b8-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="004b8-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="004b8-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="004b8-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="004b8-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="004b8-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="004b8-120">설명은</span><span class="sxs-lookup"><span data-stu-id="004b8-120">DESCRIPTION</span></span>
<span data-ttu-id="004b8-121">**AzKeyVaultAccessPolicy** cmdlet은 사용자, 응용 프로그램 또는 보안 그룹의 기존 사용 권한을 부여 하거나 수정 하 여 키 자격 증명 모음으로 지정 된 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="004b8-122">다른 사용자, 앱 또는 보안 그룹의 키 자격 증명에 대 한 사용 권한은 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="004b8-123">보안 그룹에 대 한 사용 권한을 설정 하는 경우이 작업은 해당 보안 그룹의 사용자 에게만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="004b8-124">다음 디렉터리는 모두 동일한 Azure 디렉터리 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="004b8-125">키 보관소가 있는 Azure 구독의 기본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="004b8-126">권한을 부여 하는 사용자 또는 응용 프로그램 그룹이 포함 된 Azure 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="004b8-127">이러한 조건이 충족 되지 않고이 cmdlet이 작동 하지 않을 경우 시나리오의 예:</span><span class="sxs-lookup"><span data-stu-id="004b8-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="004b8-128">다른 조직에서 사용자의 키 자격 증명을 관리 하도록 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="004b8-129">각 조직에는 고유한 디렉터리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="004b8-130">Azure 계정에 디렉터리가 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="004b8-131">기본 디렉터리가 아닌 디렉터리에 응용 프로그램을 등록 하는 경우 해당 응용 프로그램에 키 자격 증명 모음을 사용 하도록 허가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="004b8-132">응용 프로그램이 기본 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-132">The application must be in the default directory.</span></span>
<span data-ttu-id="004b8-133">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="004b8-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

> [!NOTE]
> <span data-ttu-id="004b8-134">서비스 사용자를 사용 하 여 액세스 정책 권한을 부여 하는 경우 매개 변수를 사용 해야 합니다 `-BypassObjectIdValidation` .</span><span class="sxs-lookup"><span data-stu-id="004b8-134">When using a service principal to grant access policy permissions, you must use the `-BypassObjectIdValidation` parameter.</span></span>

## <span data-ttu-id="004b8-135">예제의</span><span class="sxs-lookup"><span data-stu-id="004b8-135">EXAMPLES</span></span>

### <span data-ttu-id="004b8-136">예제 1: 키 자격 증명 모음에 대 한 사용 권한을 사용자에 게 부여 하 고 사용 권한을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-136">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="004b8-137">첫 번째 명령은 Azure Active Directory의 사용자에 대 한 사용 권한을 부여 PattiFuller@contoso.com 하 고, Contoso03Vault 이라는 키 보관소를 사용 하 여 키 및 비밀에 대 한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-137">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="004b8-138">*PassThru* 매개 변수는 cmdlet에서 반환 되는 업데이트 된 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-138">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="004b8-139">두 번째 명령은 첫 번째 명령에 부여 된 사용 권한을 수정 하 여 PattiFuller@contoso.com , 이제 암호를 설정 하 고 삭제 하는 것 외에도 비밀을 받을 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-139">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="004b8-140">이 명령 후에는 키 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-140">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="004b8-141">마지막 명령은 PattiFuller@contoso.com 키 작업에 대 한 모든 사용 권한을 제거 하는 기존 권한을 추가로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-141">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="004b8-142">이 명령 후에는 비밀 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-142">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="004b8-143">예제 2: 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 서비스 사용자에 게 권한 부여</span><span class="sxs-lookup"><span data-stu-id="004b8-143">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="004b8-144">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-144">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="004b8-145">*ServicePrincipalName* 매개 변수는 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-145">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="004b8-146">Azure Active Directory에 응용 프로그램을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-146">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="004b8-147">*ServicePrincipalName* 매개 변수 값은 응용 프로그램의 서비스 사용자 이름 또는 응용 프로그램 ID GUID 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-147">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="004b8-148">이 예제에서는 서비스 사용자 이름을 지정 하 `http://payroll.contoso.com` 고, 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-148">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="004b8-149">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="004b8-149">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="004b8-150">이 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-150">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="004b8-151">이 예제에서는 응용 프로그램의 서비스 사용자에 대 한 개체 ID를 사용 하 여 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-151">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="004b8-152">예제 4: 사용자 계정 이름에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="004b8-152">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="004b8-153">이 명령은 비밀에 대 한 액세스에 대 한 지정 된 upn (사용자 이름)의 get, list, set 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-153">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="004b8-154">예제 5: Microsoft에서 키 자격 증명 모음 으로부터 비밀을 검색 하도록 설정 합니다. 계산 리소스 공급자</span><span class="sxs-lookup"><span data-stu-id="004b8-154">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="004b8-155">이 명령은 Contoso03Vault 키 자격 증명 모음에서 Microsoft. a 리소스 공급자가 검색할 수 있는 비밀 정보에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-155">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="004b8-156">예제 6: 보안 그룹에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="004b8-156">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="004b8-157">첫 번째 명령은 Get-AzADGroup cmdlet을 사용 하 여 모든 Active Directory 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-157">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="004b8-158">출력에서 이름이 **group1** , **group2** 및 **group3** 인 3 개의 그룹이 반환 됨을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-158">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="004b8-159">여러 그룹의 이름은 동일 하지만 항상 고유한 ObjectId를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-159">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="004b8-160">동일한 이름을 가진 그룹이 두 개 이상 반환 되는 경우 출력에 ObjectId를 사용 하 여 사용할 항목을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-160">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="004b8-161">그런 다음이 명령의 출력을 Set-AzKeyVaultAccessPolicy와 함께 사용 하 여 **myownvault** 이라는 키 보관소의 group2에 대 한 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-161">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="004b8-162">이 예제에서는 동일한 명령줄에서 ' group2 ' 이라는 그룹을 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-162">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="004b8-163">반환 된 목록에 이름이 ' group2 ' 인 여러 그룹이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-163">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="004b8-164">이 예제에서는 반환 된 목록의 인덱스 0으로 표시 되는 첫 번째 항목을 선택 \[ \] 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-164">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="004b8-165">예제 7: 고객 관리 테 넌 트 키 (BYOK)에 대 한 Azure Information Protection 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="004b8-165">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="004b8-166">이 명령은 사용자가 관리 하는 키 (자체 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테 넌 트 키로 사용 하도록 Azure Information Protection에 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-166">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="004b8-167">이 명령을 실행할 때 고유한 키 보관소 이름을 지정 하면 *ServicePrincipalName* 매개 변수를 GUID **00000012-0000-0000-c 000-000000000000** 에 지정 하 고 예제에서 사용 권한을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-167">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="004b8-168">변수</span><span class="sxs-lookup"><span data-stu-id="004b8-168">PARAMETERS</span></span>

### <span data-ttu-id="004b8-169">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="004b8-169">-ApplicationId</span></span>
<span data-ttu-id="004b8-170">나중에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-170">For future use.</span></span>

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

### <span data-ttu-id="004b8-171">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="004b8-171">-BypassObjectIdValidation</span></span>
<span data-ttu-id="004b8-172">Azure Active Directory에 개체가 있는지 확인 하지 않고 개체 ID를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-172">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="004b8-173">다른 Azure 테 넌 트에서 위임 된 보안 그룹을 참조 하는 개체 ID에 키 자격 증명 모음에 대 한 액세스 권한을 부여 하려는 경우에만이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-173">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="004b8-174">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="004b8-174">-DefaultProfile</span></span>
<span data-ttu-id="004b8-175">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="004b8-175">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="004b8-176">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="004b8-176">-EmailAddress</span></span>
<span data-ttu-id="004b8-177">권한을 부여할 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-177">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="004b8-178">이 전자 메일 주소는 현재 구독과 연결 된 디렉터리에 있어야 하 고 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-178">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="004b8-179">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="004b8-179">-EnabledForDeployment</span></span>
<span data-ttu-id="004b8-180">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-180">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="004b8-181">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="004b8-181">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="004b8-182">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-182">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="004b8-183">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="004b8-183">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="004b8-184">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-184">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="004b8-185">-InputObject</span><span class="sxs-lookup"><span data-stu-id="004b8-185">-InputObject</span></span>
<span data-ttu-id="004b8-186">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="004b8-186">Key Vault Object</span></span>

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

### <span data-ttu-id="004b8-187">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="004b8-187">-ObjectId</span></span>
<span data-ttu-id="004b8-188">사용 권한을 부여할 Azure Active Directory의 사용자 또는 서비스 사용자의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-188">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="004b8-189">-PassThru</span><span class="sxs-lookup"><span data-stu-id="004b8-189">-PassThru</span></span>
<span data-ttu-id="004b8-190">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-190">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="004b8-191">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-191">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="004b8-192">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="004b8-192">-PermissionsToCertificates</span></span>
<span data-ttu-id="004b8-193">사용자 또는 서비스 사용자에 게 부여할 인증서 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-193">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="004b8-194">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-194">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="004b8-195">가져오기</span><span class="sxs-lookup"><span data-stu-id="004b8-195">Get</span></span>
- <span data-ttu-id="004b8-196">목록</span><span class="sxs-lookup"><span data-stu-id="004b8-196">List</span></span>
- <span data-ttu-id="004b8-197">삭제</span><span class="sxs-lookup"><span data-stu-id="004b8-197">Delete</span></span>
- <span data-ttu-id="004b8-198">만드는</span><span class="sxs-lookup"><span data-stu-id="004b8-198">Create</span></span>
- <span data-ttu-id="004b8-199">Import</span><span class="sxs-lookup"><span data-stu-id="004b8-199">Import</span></span>
- <span data-ttu-id="004b8-200">Update</span><span class="sxs-lookup"><span data-stu-id="004b8-200">Update</span></span>
- <span data-ttu-id="004b8-201">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="004b8-201">Managecontacts</span></span>
- <span data-ttu-id="004b8-202">Getissuers</span><span class="sxs-lookup"><span data-stu-id="004b8-202">Getissuers</span></span>
- <span data-ttu-id="004b8-203">Listissuers</span><span class="sxs-lookup"><span data-stu-id="004b8-203">Listissuers</span></span>
- <span data-ttu-id="004b8-204">Setissuers</span><span class="sxs-lookup"><span data-stu-id="004b8-204">Setissuers</span></span>
- <span data-ttu-id="004b8-205">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="004b8-205">Deleteissuers</span></span>
- <span data-ttu-id="004b8-206">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="004b8-206">Manageissuers</span></span>
- <span data-ttu-id="004b8-207">절약할</span><span class="sxs-lookup"><span data-stu-id="004b8-207">Recover</span></span>
- <span data-ttu-id="004b8-208">백업할</span><span class="sxs-lookup"><span data-stu-id="004b8-208">Backup</span></span>
- <span data-ttu-id="004b8-209">복원한</span><span class="sxs-lookup"><span data-stu-id="004b8-209">Restore</span></span>
- <span data-ttu-id="004b8-210">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="004b8-210">Purge</span></span>

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

### <span data-ttu-id="004b8-211">-기능 하는 Sto키</span><span class="sxs-lookup"><span data-stu-id="004b8-211">-PermissionsToKeys</span></span>
<span data-ttu-id="004b8-212">사용자 또는 서비스 사용자에 게 부여할 키 작업 사용 권한의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-212">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="004b8-213">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-213">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="004b8-214">해독은</span><span class="sxs-lookup"><span data-stu-id="004b8-214">Decrypt</span></span>
- <span data-ttu-id="004b8-215">해독할</span><span class="sxs-lookup"><span data-stu-id="004b8-215">Encrypt</span></span>
- <span data-ttu-id="004b8-216">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="004b8-216">UnwrapKey</span></span>
- <span data-ttu-id="004b8-217">WrapKey</span><span class="sxs-lookup"><span data-stu-id="004b8-217">WrapKey</span></span>
- <span data-ttu-id="004b8-218">나타나는지</span><span class="sxs-lookup"><span data-stu-id="004b8-218">Verify</span></span>
- <span data-ttu-id="004b8-219">등록할</span><span class="sxs-lookup"><span data-stu-id="004b8-219">Sign</span></span>
- <span data-ttu-id="004b8-220">가져오기</span><span class="sxs-lookup"><span data-stu-id="004b8-220">Get</span></span>
- <span data-ttu-id="004b8-221">목록</span><span class="sxs-lookup"><span data-stu-id="004b8-221">List</span></span>
- <span data-ttu-id="004b8-222">Update</span><span class="sxs-lookup"><span data-stu-id="004b8-222">Update</span></span>
- <span data-ttu-id="004b8-223">만드는</span><span class="sxs-lookup"><span data-stu-id="004b8-223">Create</span></span>
- <span data-ttu-id="004b8-224">Import</span><span class="sxs-lookup"><span data-stu-id="004b8-224">Import</span></span>
- <span data-ttu-id="004b8-225">삭제</span><span class="sxs-lookup"><span data-stu-id="004b8-225">Delete</span></span>
- <span data-ttu-id="004b8-226">백업할</span><span class="sxs-lookup"><span data-stu-id="004b8-226">Backup</span></span>
- <span data-ttu-id="004b8-227">복원한</span><span class="sxs-lookup"><span data-stu-id="004b8-227">Restore</span></span>
- <span data-ttu-id="004b8-228">절약할</span><span class="sxs-lookup"><span data-stu-id="004b8-228">Recover</span></span>
- <span data-ttu-id="004b8-229">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="004b8-229">Purge</span></span>

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

### <span data-ttu-id="004b8-230">-기능 방법 비밀</span><span class="sxs-lookup"><span data-stu-id="004b8-230">-PermissionsToSecrets</span></span>
<span data-ttu-id="004b8-231">사용자 또는 서비스 사용자에 게 부여할 비밀 작업 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-231">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="004b8-232">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-232">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="004b8-233">가져오기</span><span class="sxs-lookup"><span data-stu-id="004b8-233">Get</span></span>
- <span data-ttu-id="004b8-234">목록</span><span class="sxs-lookup"><span data-stu-id="004b8-234">List</span></span>
- <span data-ttu-id="004b8-235">설치할</span><span class="sxs-lookup"><span data-stu-id="004b8-235">Set</span></span>
- <span data-ttu-id="004b8-236">삭제</span><span class="sxs-lookup"><span data-stu-id="004b8-236">Delete</span></span>
- <span data-ttu-id="004b8-237">백업할</span><span class="sxs-lookup"><span data-stu-id="004b8-237">Backup</span></span>
- <span data-ttu-id="004b8-238">복원한</span><span class="sxs-lookup"><span data-stu-id="004b8-238">Restore</span></span>
- <span data-ttu-id="004b8-239">절약할</span><span class="sxs-lookup"><span data-stu-id="004b8-239">Recover</span></span>
- <span data-ttu-id="004b8-240">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="004b8-240">Purge</span></span>

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

### <span data-ttu-id="004b8-241">-기능 저장 저장소</span><span class="sxs-lookup"><span data-stu-id="004b8-241">-PermissionsToStorage</span></span>
<span data-ttu-id="004b8-242">사용자 또는 서비스 사용자에 게 부여할 관리 되는 저장소 계정 및 SaS 정의 작업 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-242">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="004b8-243">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="004b8-243">-ResourceGroupName</span></span>
<span data-ttu-id="004b8-244">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-244">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="004b8-245">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="004b8-245">-ResourceId</span></span>
<span data-ttu-id="004b8-246">키 자격 증명 모음 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="004b8-246">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="004b8-247">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-247">-ServicePrincipalName</span></span>
<span data-ttu-id="004b8-248">권한을 부여할 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-248">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="004b8-249">클라이언트 ID 라고도 하는 응용 프로그램 ID를 AzureActive Directory의 응용 프로그램에 등록 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-249">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="004b8-250">이 매개 변수에서 지정 하는 서비스 사용자 이름을 사용 하는 응용 프로그램은 현재 구독을 포함 하는 Azure 디렉터리에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-250">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="004b8-251">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="004b8-251">-UserPrincipalName</span></span>
<span data-ttu-id="004b8-252">권한을 부여할 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-252">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="004b8-253">이 사용자 사용자 이름은 현재 구독과 연결 된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-253">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="004b8-254">-VaultName</span><span class="sxs-lookup"><span data-stu-id="004b8-254">-VaultName</span></span>
<span data-ttu-id="004b8-255">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-255">Specifies the name of a key vault.</span></span>
<span data-ttu-id="004b8-256">이 cmdlet은이 매개 변수에서 지정 하는 키 보관소에 대 한 액세스 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-256">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="004b8-257">-확인</span><span class="sxs-lookup"><span data-stu-id="004b8-257">-Confirm</span></span>
<span data-ttu-id="004b8-258">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-258">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="004b8-259">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="004b8-259">-WhatIf</span></span>
<span data-ttu-id="004b8-260">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-260">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="004b8-261">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-261">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="004b8-262">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="004b8-262">CommonParameters</span></span>
<span data-ttu-id="004b8-263">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="004b8-263">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="004b8-264">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="004b8-264">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="004b8-265">입력</span><span class="sxs-lookup"><span data-stu-id="004b8-265">INPUTS</span></span>

### <span data-ttu-id="004b8-266">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="004b8-266">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="004b8-267">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="004b8-267">System.String</span></span>

## <span data-ttu-id="004b8-268">출력</span><span class="sxs-lookup"><span data-stu-id="004b8-268">OUTPUTS</span></span>

### <span data-ttu-id="004b8-269">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="004b8-269">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="004b8-270">상속자</span><span class="sxs-lookup"><span data-stu-id="004b8-270">NOTES</span></span>

## <span data-ttu-id="004b8-271">관련 링크</span><span class="sxs-lookup"><span data-stu-id="004b8-271">RELATED LINKS</span></span>

[<span data-ttu-id="004b8-272">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="004b8-272">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="004b8-273">제거-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="004b8-273">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

