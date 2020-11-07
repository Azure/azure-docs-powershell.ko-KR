---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/set-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: 55cdc385c5cdf291db15399f4fd587b9b10ce308
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93883290"
---
# <span data-ttu-id="9eecd-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9eecd-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="9eecd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9eecd-102">SYNOPSIS</span></span>
<span data-ttu-id="9eecd-103">키 자격 증명 모음을 사용 하 여 작업을 수행 하기 위해 사용자, 응용 프로그램 또는 보안 그룹에 대 한 기존 사용 권한을 부여 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="9eecd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9eecd-104">SYNTAX</span></span>

### <span data-ttu-id="9eecd-105">ByUserPrincipalName (기본값)</span><span class="sxs-lookup"><span data-stu-id="9eecd-105">ByUserPrincipalName (Default)</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="9eecd-106">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-107">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9eecd-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="9eecd-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="9eecd-110">InputObjectByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-111">InputObjectByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-112">InputObjectByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -UserPrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-113">InputObjectByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9eecd-113">InputObjectByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="9eecd-114">InputObjectForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVaultIdentityItem> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="9eecd-115">ResourceIdByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>]
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-116">ResourceIdByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9eecd-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-117">ResourceIdByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-118">ResourceIdByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="9eecd-118">ResourceIdByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PermissionsToKeys <String[]>]
 [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9eecd-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="9eecd-119">ResourceIdForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9eecd-120">설명은</span><span class="sxs-lookup"><span data-stu-id="9eecd-120">DESCRIPTION</span></span>
<span data-ttu-id="9eecd-121">**AzKeyVaultAccessPolicy** cmdlet은 사용자, 응용 프로그램 또는 보안 그룹의 기존 사용 권한을 부여 하거나 수정 하 여 키 자격 증명 모음으로 지정 된 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-121">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="9eecd-122">다른 사용자, 앱 또는 보안 그룹의 키 자격 증명에 대 한 사용 권한은 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-122">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>
<span data-ttu-id="9eecd-123">보안 그룹에 대 한 사용 권한을 설정 하는 경우이 작업은 해당 보안 그룹의 사용자 에게만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-123">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>
<span data-ttu-id="9eecd-124">다음 디렉터리는 모두 동일한 Azure 디렉터리 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-124">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="9eecd-125">키 보관소가 있는 Azure 구독의 기본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-125">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="9eecd-126">권한을 부여 하는 사용자 또는 응용 프로그램 그룹이 포함 된 Azure 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-126">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>
<span data-ttu-id="9eecd-127">이러한 조건이 충족 되지 않고이 cmdlet이 작동 하지 않을 경우 시나리오의 예:</span><span class="sxs-lookup"><span data-stu-id="9eecd-127">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>
- <span data-ttu-id="9eecd-128">다른 조직에서 사용자의 키 자격 증명을 관리 하도록 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-128">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="9eecd-129">각 조직에는 고유한 디렉터리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-129">Each organization has its own directory.</span></span>
- <span data-ttu-id="9eecd-130">Azure 계정에 디렉터리가 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-130">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="9eecd-131">기본 디렉터리가 아닌 디렉터리에 응용 프로그램을 등록 하는 경우 해당 응용 프로그램에 키 자격 증명 모음을 사용 하도록 허가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-131">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="9eecd-132">응용 프로그램이 기본 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-132">The application must be in the default directory.</span></span>
<span data-ttu-id="9eecd-133">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="9eecd-133">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="9eecd-134">예제의</span><span class="sxs-lookup"><span data-stu-id="9eecd-134">EXAMPLES</span></span>

### <span data-ttu-id="9eecd-135">예제 1: 키 자격 증명 모음에 대 한 사용 권한을 사용자에 게 부여 하 고 사용 권한을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-135">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
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

<span data-ttu-id="9eecd-136">첫 번째 명령은 Azure Active Directory의 사용자에 대 한 사용 권한을 부여 PattiFuller@contoso.com 하 고, Contoso03Vault 이라는 키 보관소를 사용 하 여 키 및 비밀에 대 한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-136">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span> <span data-ttu-id="9eecd-137">*PassThru* 매개 변수는 cmdlet에서 반환 되는 업데이트 된 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-137">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>
<span data-ttu-id="9eecd-138">두 번째 명령은 첫 번째 명령에 부여 된 사용 권한을 수정 하 여 PattiFuller@contoso.com , 이제 암호를 설정 하 고 삭제 하는 것 외에도 비밀을 받을 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-138">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="9eecd-139">이 명령 후에는 키 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-139">The permissions to key operations remain unchanged after this command.</span></span>
<span data-ttu-id="9eecd-140">마지막 명령은 PattiFuller@contoso.com 키 작업에 대 한 모든 사용 권한을 제거 하는 기존 권한을 추가로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-140">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="9eecd-141">이 명령 후에는 비밀 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-141">The permissions to secret operations remain unchanged after this command.</span></span>

### <span data-ttu-id="9eecd-142">예제 2: 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 서비스 사용자에 게 권한 부여</span><span class="sxs-lookup"><span data-stu-id="9eecd-142">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="9eecd-143">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-143">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>
<span data-ttu-id="9eecd-144">*ServicePrincipalName* 매개 변수는 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-144">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="9eecd-145">Azure Active Directory에 응용 프로그램을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-145">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="9eecd-146">*ServicePrincipalName* 매개 변수 값은 응용 프로그램의 서비스 사용자 이름 또는 응용 프로그램 ID GUID 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-146">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>
<span data-ttu-id="9eecd-147">이 예제에서는 서비스 사용자 이름을 지정 하 `http://payroll.contoso.com` 고, 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-147">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="9eecd-148">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="9eecd-148">Example 3: Grant permissions for an application using its object ID</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="9eecd-149">이 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-149">This command grants the application permissions to read and write secrets.</span></span>
<span data-ttu-id="9eecd-150">이 예제에서는 응용 프로그램의 서비스 사용자에 대 한 개체 ID를 사용 하 여 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-150">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="9eecd-151">예제 4: 사용자 계정 이름에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="9eecd-151">Example 4: Grant permissions for a user principal name</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="9eecd-152">이 명령은 비밀에 대 한 액세스에 대 한 지정 된 upn (사용자 이름)의 get, list, set 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-152">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="9eecd-153">예제 5: Microsoft에서 키 자격 증명 모음 으로부터 비밀을 검색 하도록 설정 합니다. 계산 리소스 공급자</span><span class="sxs-lookup"><span data-stu-id="9eecd-153">Example 5: Enable secrets to be retrieved from a key vault by the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="9eecd-154">이 명령은 Contoso03Vault 키 자격 증명 모음에서 Microsoft. a 리소스 공급자가 검색할 수 있는 비밀 정보에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-154">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="9eecd-155">예제 6: 보안 그룹에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="9eecd-155">Example 6: Grant permissions to a security group</span></span>
```powershell
PS C:\> Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys get, set -PermissionsToSecrets get, set
```

<span data-ttu-id="9eecd-156">첫 번째 명령은 Get-AzADGroup cmdlet을 사용 하 여 모든 Active Directory 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-156">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="9eecd-157">출력에서 이름이 **group1** , **group2** 및 **group3** 인 3 개의 그룹이 반환 됨을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-157">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="9eecd-158">여러 그룹의 이름은 동일 하지만 항상 고유한 ObjectId를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-158">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="9eecd-159">동일한 이름을 가진 그룹이 두 개 이상 반환 되는 경우 출력에 ObjectId를 사용 하 여 사용할 항목을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-159">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>
<span data-ttu-id="9eecd-160">그런 다음이 명령의 출력을 Set-AzKeyVaultAccessPolicy와 함께 사용 하 여 **myownvault** 이라는 키 보관소의 group2에 대 한 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-160">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="9eecd-161">이 예제에서는 동일한 명령줄에서 ' group2 ' 이라는 그룹을 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-161">This example enumerates the groups named 'group2' inline in the same command line.</span></span>
<span data-ttu-id="9eecd-162">반환 된 목록에 이름이 ' group2 ' 인 여러 그룹이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-162">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="9eecd-163">이 예제에서는 반환 된 목록의 인덱스 0으로 표시 되는 첫 번째 항목을 선택 \[ \] 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-163">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="9eecd-164">예제 7: 고객 관리 테 넌 트 키 (BYOK)에 대 한 Azure Information Protection 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="9eecd-164">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```powershell
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="9eecd-165">이 명령은 사용자가 관리 하는 키 (자체 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테 넌 트 키로 사용 하도록 Azure Information Protection에 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-165">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>
<span data-ttu-id="9eecd-166">이 명령을 실행할 때 고유한 키 보관소 이름을 지정 하면 *ServicePrincipalName* 매개 변수를 GUID **00000012-0000-0000-c 000-000000000000** 에 지정 하 고 예제에서 사용 권한을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-166">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="9eecd-167">변수</span><span class="sxs-lookup"><span data-stu-id="9eecd-167">PARAMETERS</span></span>

### <span data-ttu-id="9eecd-168">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="9eecd-168">-ApplicationId</span></span>
<span data-ttu-id="9eecd-169">나중에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-169">For future use.</span></span>

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

### <span data-ttu-id="9eecd-170">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="9eecd-170">-BypassObjectIdValidation</span></span>
<span data-ttu-id="9eecd-171">Azure Active Directory에 개체가 있는지 확인 하지 않고 개체 ID를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-171">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>
<span data-ttu-id="9eecd-172">다른 Azure 테 넌 트에서 위임 된 보안 그룹을 참조 하는 개체 ID에 키 자격 증명 모음에 대 한 액세스 권한을 부여 하려는 경우에만이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-172">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

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

### <span data-ttu-id="9eecd-173">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9eecd-173">-DefaultProfile</span></span>
<span data-ttu-id="9eecd-174">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="9eecd-174">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="9eecd-175">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="9eecd-175">-EmailAddress</span></span>
<span data-ttu-id="9eecd-176">권한을 부여할 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-176">Specifies the user email address of the user to whom to grant permissions.</span></span>
<span data-ttu-id="9eecd-177">이 전자 메일 주소는 현재 구독과 연결 된 디렉터리에 있어야 하 고 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-177">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

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

### <span data-ttu-id="9eecd-178">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="9eecd-178">-EnabledForDeployment</span></span>
<span data-ttu-id="9eecd-179">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-179">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="9eecd-180">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="9eecd-180">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="9eecd-181">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-181">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="9eecd-182">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="9eecd-182">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="9eecd-183">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-183">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="9eecd-184">-InputObject</span><span class="sxs-lookup"><span data-stu-id="9eecd-184">-InputObject</span></span>
<span data-ttu-id="9eecd-185">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="9eecd-185">Key Vault Object</span></span>

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

### <span data-ttu-id="9eecd-186">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9eecd-186">-ObjectId</span></span>
<span data-ttu-id="9eecd-187">사용 권한을 부여할 Azure Active Directory의 사용자 또는 서비스 사용자의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-187">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

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

### <span data-ttu-id="9eecd-188">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9eecd-188">-PassThru</span></span>
<span data-ttu-id="9eecd-189">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-189">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="9eecd-190">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-190">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="9eecd-191">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="9eecd-191">-PermissionsToCertificates</span></span>
<span data-ttu-id="9eecd-192">사용자 또는 서비스 사용자에 게 부여할 인증서 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-192">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="9eecd-193">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-193">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="9eecd-194">가져오기</span><span class="sxs-lookup"><span data-stu-id="9eecd-194">Get</span></span>
- <span data-ttu-id="9eecd-195">목록</span><span class="sxs-lookup"><span data-stu-id="9eecd-195">List</span></span>
- <span data-ttu-id="9eecd-196">삭제</span><span class="sxs-lookup"><span data-stu-id="9eecd-196">Delete</span></span>
- <span data-ttu-id="9eecd-197">만드는</span><span class="sxs-lookup"><span data-stu-id="9eecd-197">Create</span></span>
- <span data-ttu-id="9eecd-198">Import</span><span class="sxs-lookup"><span data-stu-id="9eecd-198">Import</span></span>
- <span data-ttu-id="9eecd-199">Update</span><span class="sxs-lookup"><span data-stu-id="9eecd-199">Update</span></span>
- <span data-ttu-id="9eecd-200">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="9eecd-200">Managecontacts</span></span>
- <span data-ttu-id="9eecd-201">Getissuers</span><span class="sxs-lookup"><span data-stu-id="9eecd-201">Getissuers</span></span>
- <span data-ttu-id="9eecd-202">Listissuers</span><span class="sxs-lookup"><span data-stu-id="9eecd-202">Listissuers</span></span>
- <span data-ttu-id="9eecd-203">Setissuers</span><span class="sxs-lookup"><span data-stu-id="9eecd-203">Setissuers</span></span>
- <span data-ttu-id="9eecd-204">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="9eecd-204">Deleteissuers</span></span>
- <span data-ttu-id="9eecd-205">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="9eecd-205">Manageissuers</span></span>
- <span data-ttu-id="9eecd-206">절약할</span><span class="sxs-lookup"><span data-stu-id="9eecd-206">Recover</span></span>
- <span data-ttu-id="9eecd-207">백업할</span><span class="sxs-lookup"><span data-stu-id="9eecd-207">Backup</span></span>
- <span data-ttu-id="9eecd-208">복원한</span><span class="sxs-lookup"><span data-stu-id="9eecd-208">Restore</span></span>
- <span data-ttu-id="9eecd-209">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="9eecd-209">Purge</span></span>

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

### <span data-ttu-id="9eecd-210">-기능 하는 Sto키</span><span class="sxs-lookup"><span data-stu-id="9eecd-210">-PermissionsToKeys</span></span>
<span data-ttu-id="9eecd-211">사용자 또는 서비스 사용자에 게 부여할 키 작업 사용 권한의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-211">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="9eecd-212">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-212">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="9eecd-213">해독은</span><span class="sxs-lookup"><span data-stu-id="9eecd-213">Decrypt</span></span>
- <span data-ttu-id="9eecd-214">해독할</span><span class="sxs-lookup"><span data-stu-id="9eecd-214">Encrypt</span></span>
- <span data-ttu-id="9eecd-215">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="9eecd-215">UnwrapKey</span></span>
- <span data-ttu-id="9eecd-216">WrapKey</span><span class="sxs-lookup"><span data-stu-id="9eecd-216">WrapKey</span></span>
- <span data-ttu-id="9eecd-217">나타나는지</span><span class="sxs-lookup"><span data-stu-id="9eecd-217">Verify</span></span>
- <span data-ttu-id="9eecd-218">등록할</span><span class="sxs-lookup"><span data-stu-id="9eecd-218">Sign</span></span>
- <span data-ttu-id="9eecd-219">가져오기</span><span class="sxs-lookup"><span data-stu-id="9eecd-219">Get</span></span>
- <span data-ttu-id="9eecd-220">목록</span><span class="sxs-lookup"><span data-stu-id="9eecd-220">List</span></span>
- <span data-ttu-id="9eecd-221">Update</span><span class="sxs-lookup"><span data-stu-id="9eecd-221">Update</span></span>
- <span data-ttu-id="9eecd-222">만드는</span><span class="sxs-lookup"><span data-stu-id="9eecd-222">Create</span></span>
- <span data-ttu-id="9eecd-223">Import</span><span class="sxs-lookup"><span data-stu-id="9eecd-223">Import</span></span>
- <span data-ttu-id="9eecd-224">삭제</span><span class="sxs-lookup"><span data-stu-id="9eecd-224">Delete</span></span>
- <span data-ttu-id="9eecd-225">백업할</span><span class="sxs-lookup"><span data-stu-id="9eecd-225">Backup</span></span>
- <span data-ttu-id="9eecd-226">복원한</span><span class="sxs-lookup"><span data-stu-id="9eecd-226">Restore</span></span>
- <span data-ttu-id="9eecd-227">절약할</span><span class="sxs-lookup"><span data-stu-id="9eecd-227">Recover</span></span>
- <span data-ttu-id="9eecd-228">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="9eecd-228">Purge</span></span>

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

### <span data-ttu-id="9eecd-229">-기능 방법 비밀</span><span class="sxs-lookup"><span data-stu-id="9eecd-229">-PermissionsToSecrets</span></span>
<span data-ttu-id="9eecd-230">사용자 또는 서비스 사용자에 게 부여할 비밀 작업 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-230">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>
<span data-ttu-id="9eecd-231">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-231">The acceptable values for this parameter:</span></span>
- <span data-ttu-id="9eecd-232">가져오기</span><span class="sxs-lookup"><span data-stu-id="9eecd-232">Get</span></span>
- <span data-ttu-id="9eecd-233">목록</span><span class="sxs-lookup"><span data-stu-id="9eecd-233">List</span></span>
- <span data-ttu-id="9eecd-234">설치할</span><span class="sxs-lookup"><span data-stu-id="9eecd-234">Set</span></span>
- <span data-ttu-id="9eecd-235">삭제</span><span class="sxs-lookup"><span data-stu-id="9eecd-235">Delete</span></span>
- <span data-ttu-id="9eecd-236">백업할</span><span class="sxs-lookup"><span data-stu-id="9eecd-236">Backup</span></span>
- <span data-ttu-id="9eecd-237">복원한</span><span class="sxs-lookup"><span data-stu-id="9eecd-237">Restore</span></span>
- <span data-ttu-id="9eecd-238">절약할</span><span class="sxs-lookup"><span data-stu-id="9eecd-238">Recover</span></span>
- <span data-ttu-id="9eecd-239">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="9eecd-239">Purge</span></span>

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

### <span data-ttu-id="9eecd-240">-기능 저장 저장소</span><span class="sxs-lookup"><span data-stu-id="9eecd-240">-PermissionsToStorage</span></span>
<span data-ttu-id="9eecd-241">사용자 또는 서비스 사용자에 게 부여할 관리 되는 저장소 계정 및 SaS 정의 작업 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-241">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

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

### <span data-ttu-id="9eecd-242">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9eecd-242">-ResourceGroupName</span></span>
<span data-ttu-id="9eecd-243">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-243">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="9eecd-244">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="9eecd-244">-ResourceId</span></span>
<span data-ttu-id="9eecd-245">키 자격 증명 모음 리소스 Id</span><span class="sxs-lookup"><span data-stu-id="9eecd-245">Key Vault Resource Id</span></span>

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

### <span data-ttu-id="9eecd-246">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-246">-ServicePrincipalName</span></span>
<span data-ttu-id="9eecd-247">권한을 부여할 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-247">Specifies the service principal name of the application to which to grant permissions.</span></span>
<span data-ttu-id="9eecd-248">클라이언트 ID 라고도 하는 응용 프로그램 ID를 AzureActive Directory의 응용 프로그램에 등록 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-248">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="9eecd-249">이 매개 변수에서 지정 하는 서비스 사용자 이름을 사용 하는 응용 프로그램은 현재 구독을 포함 하는 Azure 디렉터리에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-249">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

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

### <span data-ttu-id="9eecd-250">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="9eecd-250">-UserPrincipalName</span></span>
<span data-ttu-id="9eecd-251">권한을 부여할 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-251">Specifies the user principal name of the user to whom to grant permissions.</span></span>
<span data-ttu-id="9eecd-252">이 사용자 사용자 이름은 현재 구독과 연결 된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-252">This user principal name must exist in the directory associated with the current subscription.</span></span>

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

### <span data-ttu-id="9eecd-253">-VaultName</span><span class="sxs-lookup"><span data-stu-id="9eecd-253">-VaultName</span></span>
<span data-ttu-id="9eecd-254">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-254">Specifies the name of a key vault.</span></span>
<span data-ttu-id="9eecd-255">이 cmdlet은이 매개 변수에서 지정 하는 키 보관소에 대 한 액세스 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-255">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="9eecd-256">-확인</span><span class="sxs-lookup"><span data-stu-id="9eecd-256">-Confirm</span></span>
<span data-ttu-id="9eecd-257">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-257">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9eecd-258">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9eecd-258">-WhatIf</span></span>
<span data-ttu-id="9eecd-259">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-259">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9eecd-260">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-260">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9eecd-261">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9eecd-261">CommonParameters</span></span>
<span data-ttu-id="9eecd-262">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9eecd-262">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9eecd-263">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9eecd-263">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9eecd-264">입력</span><span class="sxs-lookup"><span data-stu-id="9eecd-264">INPUTS</span></span>

### <span data-ttu-id="9eecd-265">Microsoft. KeyVault. PSKeyVaultIdentityItem</span><span class="sxs-lookup"><span data-stu-id="9eecd-265">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultIdentityItem</span></span>

### <span data-ttu-id="9eecd-266">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="9eecd-266">System.String</span></span>

## <span data-ttu-id="9eecd-267">출력</span><span class="sxs-lookup"><span data-stu-id="9eecd-267">OUTPUTS</span></span>

### <span data-ttu-id="9eecd-268">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="9eecd-268">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="9eecd-269">상속자</span><span class="sxs-lookup"><span data-stu-id="9eecd-269">NOTES</span></span>

## <span data-ttu-id="9eecd-270">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9eecd-270">RELATED LINKS</span></span>

[<span data-ttu-id="9eecd-271">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="9eecd-271">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="9eecd-272">제거-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="9eecd-272">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

