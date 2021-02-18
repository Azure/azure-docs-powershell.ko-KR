---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: e19565aa8ae249acf61fce67f0a2b54e20143758
ms.sourcegitcommit: 0c61b7f42dec507e576c92e0a516c6655e9f50fc
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/14/2021
ms.locfileid: "100410160"
---
# <span data-ttu-id="86ae2-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86ae2-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="86ae2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="86ae2-102">SYNOPSIS</span></span>
<span data-ttu-id="86ae2-103">키 자격 증명 모음에서 사용자 또는 애플리케이션에 대한 모든 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="86ae2-104">구문</span><span class="sxs-lookup"><span data-stu-id="86ae2-104">SYNTAX</span></span>

### <span data-ttu-id="86ae2-105">ByUserPrincipalName(기본값)</span><span class="sxs-lookup"><span data-stu-id="86ae2-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="86ae2-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ae2-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="86ae2-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="86ae2-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="86ae2-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="86ae2-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="86ae2-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="86ae2-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="86ae2-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="86ae2-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="86ae2-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="86ae2-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="86ae2-120">설명</span><span class="sxs-lookup"><span data-stu-id="86ae2-120">DESCRIPTION</span></span>
<span data-ttu-id="86ae2-121">**Remove-AzKeyVaultAccessPolicy** cmdlet은 사용자 또는 애플리케이션 또는 키 자격 증명 모음의 모든 사용자 및 애플리케이션에 대한 모든 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="86ae2-122">모든 권한을 제거한 경우에도 키 자격 증명 모음이 포함된 Azure 구독의 소유자는 키 자격 증명 모음에 권한을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="86ae2-123">이 cmdlet에 대해 리소스 그룹을 지정하는 것은 선택 사항이지만 성능을 향상하기 위해 이 작업을 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="86ae2-124">예제</span><span class="sxs-lookup"><span data-stu-id="86ae2-124">EXAMPLES</span></span>

### <span data-ttu-id="86ae2-125">예제 1: 사용자에 대한 권한 제거</span><span class="sxs-lookup"><span data-stu-id="86ae2-125">Example 1: Remove permissions for a user</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PassThru

Vault Name                       : Contoso03Vault
Resource Group Name              : myrg
Location                         : westus
Resource ID                      : /subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx/resourceGroups/myrg/providers
                                   /Microsoft.KeyVault/vaults/contoso03vault
Vault URI                        : https://contoso03vault.vault.azure.net/
Tenant ID                        : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
SKU                              : Standard
Enabled For Deployment?          : False
Enabled For Template Deployment? : False
Enabled For Disk Encryption?     : False
Soft Delete Enabled?             :
Access Policies                  :
                                   Tenant ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Object ID                                  : xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxxx
                                   Application ID                             :
                                   Display Name                               : User Name (username@microsoft.com)
                                   Permissions to Keys                        :
                                   Permissions to Secrets                     :
                                   Permissions to Certificates                : get, create
                                   Permissions to (Key Vault Managed) Storage :


Network Rule Set                 :
                                   Default Action                             : Allow
                                   Bypass                                     : AzureServices
                                   IP Rules                                   :
                                   Virtual Network Rules                      :

Tags                             :
```

<span data-ttu-id="86ae2-126">이 명령은 Contoso03Vault라는 키 자격 증명 모음에 대해 사용자가 가지는 모든 권한을 PattiFuller@contoso.com 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="86ae2-127">-PassThru를 지정하면 KeyVault 개체가 반환됩니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="86ae2-128">예제 2: 애플리케이션에 대한 권한 제거</span><span class="sxs-lookup"><span data-stu-id="86ae2-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="86ae2-129">이 명령은 Contoso03Vault라는 키 자격 증명 모음에 애플리케이션이 가지는 모든 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="86ae2-130">이 예제에서는 Azure Active Directory에 등록된 서비스 주체 이름을 사용하여 애플리케이션을 `http://payroll.contoso.com` 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="86ae2-131">예제 3: 개체 ID를 사용하여 애플리케이션에 대한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="86ae2-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="86ae2-132">이 명령은 Contoso03Vault라는 키 자격 증명 모음에 애플리케이션이 가지는 모든 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="86ae2-133">이 예제에서는 서비스 주체의 개체 ID로 애플리케이션을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="86ae2-134">예제 4: Microsoft.Compute 리소스 공급자에 대한 권한 제거</span><span class="sxs-lookup"><span data-stu-id="86ae2-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="86ae2-135">이 명령은 Contoso03Vault에서 비밀을 얻을 수 있는 Microsoft.Compute 리소스 공급자에 대한 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="86ae2-136">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="86ae2-136">PARAMETERS</span></span>

### <span data-ttu-id="86ae2-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="86ae2-137">-ApplicationId</span></span>
<span data-ttu-id="86ae2-138">사용 권한을 제거해야 하는 애플리케이션의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="86ae2-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="86ae2-139">-DefaultProfile</span></span>
<span data-ttu-id="86ae2-140">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="86ae2-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="86ae2-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="86ae2-141">-EmailAddress</span></span>
<span data-ttu-id="86ae2-142">액세스 권한을 제거하려는 사용자의 사용자 전자 메일 주소를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-142">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: ByEmail, InputObjectByEmail, ResourceIdByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ae2-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="86ae2-143">-EnabledForDeployment</span></span>
<span data-ttu-id="86ae2-144">지정된 경우 리소스 생성 시 참조될 때 Microsoft.Compute 리소스 공급자가 이 키 자격 증명 모음에서 비밀 검색을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="86ae2-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="86ae2-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="86ae2-146">지정된 경우 Azure Disk Encryption을 통해 이 키 자격 증명 모음에서 비밀 검색을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="86ae2-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="86ae2-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="86ae2-148">지정한 경우 템플릿에서 참조할 때 Azure Resource Manager가 이 키 자격 증명 모음에서 비밀 검색을 사용하지 않도록 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="86ae2-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="86ae2-149">-InputObject</span></span>
<span data-ttu-id="86ae2-150">Key Vault 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-150">Key Vault object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="86ae2-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="86ae2-151">-ObjectId</span></span>
<span data-ttu-id="86ae2-152">권한을 제거할 Azure Active Directory에서 사용자 또는 서비스 주체의 개체 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="86ae2-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="86ae2-153">-PassThru</span></span>
<span data-ttu-id="86ae2-154">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="86ae2-155">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="86ae2-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="86ae2-156">-ResourceGroupName</span></span>
<span data-ttu-id="86ae2-157">액세스 정책을 수정하는 키 자격 증명 모음과 연결된 리소스 그룹의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="86ae2-158">지정하지 않으면 이 cmdlet은 현재 구독에서 키 자격 증명 모음을 검색합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ae2-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="86ae2-159">-ResourceId</span></span>
<span data-ttu-id="86ae2-160">KeyVault 리소스 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-160">KeyVault Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdByObjectId, ResourceIdByServicePrincipalName, ResourceIdByUserPrincipalName, ResourceIdByEmail, ResourceIdForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="86ae2-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-161">-ServicePrincipalName</span></span>
<span data-ttu-id="86ae2-162">사용 권한을 제거하려는 애플리케이션의 서비스 주체 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="86ae2-163">Azure Active Directory에서 애플리케이션에 등록된 클라이언트 ID라고도 하는 애플리케이션 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="86ae2-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="86ae2-164">-UserPrincipalName</span></span>
<span data-ttu-id="86ae2-165">액세스 권한을 제거하려는 사용자의 사용자 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="86ae2-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="86ae2-166">-VaultName</span></span>
<span data-ttu-id="86ae2-167">키 자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="86ae2-168">이 cmdlet은 이 매개 변수가 지정하는 키 자격 증명 모음에 대한 권한을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: System.String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="86ae2-169">-Confirm</span><span class="sxs-lookup"><span data-stu-id="86ae2-169">-Confirm</span></span>
<span data-ttu-id="86ae2-170">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="86ae2-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="86ae2-171">-WhatIf</span></span>
<span data-ttu-id="86ae2-172">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="86ae2-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="86ae2-173">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="86ae2-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="86ae2-174">CommonParameters</span></span>
<span data-ttu-id="86ae2-175">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="86ae2-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="86ae2-176">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="86ae2-176">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="86ae2-177">입력</span><span class="sxs-lookup"><span data-stu-id="86ae2-177">INPUTS</span></span>

### <span data-ttu-id="86ae2-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ae2-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="86ae2-179">System.String</span><span class="sxs-lookup"><span data-stu-id="86ae2-179">System.String</span></span>

## <span data-ttu-id="86ae2-180">출력</span><span class="sxs-lookup"><span data-stu-id="86ae2-180">OUTPUTS</span></span>

### <span data-ttu-id="86ae2-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="86ae2-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="86ae2-182">참고 사항</span><span class="sxs-lookup"><span data-stu-id="86ae2-182">NOTES</span></span>

## <span data-ttu-id="86ae2-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="86ae2-183">RELATED LINKS</span></span>

[<span data-ttu-id="86ae2-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="86ae2-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

