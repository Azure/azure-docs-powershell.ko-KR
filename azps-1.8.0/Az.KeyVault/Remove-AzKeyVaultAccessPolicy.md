---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a0cf20ad9fafbae2ed6902226e396b3d732cee5c
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93883265"
---
# <span data-ttu-id="e4683-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4683-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="e4683-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4683-102">SYNOPSIS</span></span>
<span data-ttu-id="e4683-103">키 자격 증명 모음에서 사용자 또는 응용 프로그램에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="e4683-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e4683-104">SYNTAX</span></span>

### <span data-ttu-id="e4683-105">ByUserPrincipalName (기본값)</span><span class="sxs-lookup"><span data-stu-id="e4683-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -UserPrincipalName <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="e4683-106">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4683-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-107">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e4683-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="e4683-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="e4683-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="e4683-110">InputObjectByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="e4683-113">InputObjectByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="e4683-114">InputObjectForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-115">ResourceIdByObjectId</span><span class="sxs-lookup"><span data-stu-id="e4683-115">ResourceIdByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ObjectId <String> [-ApplicationId <Guid>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-116">ResourceIdByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-116">ResourceIdByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-117">ResourceIdByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-117">ResourceIdByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-118">ResourceIdByEmail</span><span class="sxs-lookup"><span data-stu-id="e4683-118">ResourceIdByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e4683-119">ResourceIdForVault</span><span class="sxs-lookup"><span data-stu-id="e4683-119">ResourceIdForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-ResourceId] <String> [-EnabledForDeployment] [-EnabledForTemplateDeployment]
 [-EnabledForDiskEncryption] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e4683-120">설명은</span><span class="sxs-lookup"><span data-stu-id="e4683-120">DESCRIPTION</span></span>
<span data-ttu-id="e4683-121">**AzKeyVaultAccessPolicy** cmdlet은 사용자 또는 응용 프로그램 또는 모든 사용자 및 응용 프로그램에 대 한 모든 권한을 키 자격 증명 모음에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-121">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="e4683-122">모든 권한을 제거 해도 키 자격 증명 모음이 포함 된 Azure 구독 소유자는 해당 키 자격 증명 모음에 대 한 사용 권한을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-122">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>
<span data-ttu-id="e4683-123">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="e4683-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="e4683-124">예제의</span><span class="sxs-lookup"><span data-stu-id="e4683-124">EXAMPLES</span></span>

### <span data-ttu-id="e4683-125">예제 1: 사용자에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="e4683-125">Example 1: Remove permissions for a user</span></span>
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

<span data-ttu-id="e4683-126">이 명령은 사용자가 PattiFuller@contoso.com Contoso03Vault 이라는 키 보관소에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-126">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>  <span data-ttu-id="e4683-127">-PassThru를 지정 하면 KeyVault 개체가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-127">If -PassThru is specified, the KeyVault object is returned.</span></span>

### <span data-ttu-id="e4683-128">예제 2: 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="e4683-128">Example 2: Remove permissions for an application</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="e4683-129">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-129">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="e4683-130">이 예제에서는 Azure Active Directory에 등록 된 서비스 사용자 이름을 사용 하 여 응용 프로그램을 식별 `http://payroll.contoso.com` 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-130">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="e4683-131">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="e4683-131">Example 3: Remove permissions for an application by using its object ID</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="e4683-132">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-132">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="e4683-133">이 예제에서는 서비스 주체의 개체 ID를 기준으로 응용 프로그램을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-133">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="e4683-134">예제 4: Microsoft. Compute resource provider에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-134">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```powershell
PS C:\> Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="e4683-135">이 명령은 Contoso03Vault에서 비밀을 가져올 수 있도록 Microsoft. 리소스 공급자에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-135">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="e4683-136">변수</span><span class="sxs-lookup"><span data-stu-id="e4683-136">PARAMETERS</span></span>

### <span data-ttu-id="e4683-137">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="e4683-137">-ApplicationId</span></span>
<span data-ttu-id="e4683-138">사용 권한을 제거할 응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-138">Specifies the ID of application whose permissions should be removed</span></span>

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

### <span data-ttu-id="e4683-139">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4683-139">-DefaultProfile</span></span>
<span data-ttu-id="e4683-140">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e4683-140">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e4683-141">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="e4683-141">-EmailAddress</span></span>
<span data-ttu-id="e4683-142">액세스 권한을 제거 하려는 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-142">Specifies the user email address of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="e4683-143">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="e4683-143">-EnabledForDeployment</span></span>
<span data-ttu-id="e4683-144">지정 된 경우 리소스 생성 시 참조 되는 리소스 공급자에서이 키 보관소의 비밀을 검색 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-144">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

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

### <span data-ttu-id="e4683-145">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="e4683-145">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="e4683-146">지정 된 경우 Azure 디스크 암호화를 통해이 키 보관소의 비밀 검색을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-146">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

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

### <span data-ttu-id="e4683-147">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="e4683-147">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="e4683-148">지정 하면 템플릿에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소의 비밀을 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-148">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

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

### <span data-ttu-id="e4683-149">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4683-149">-InputObject</span></span>
<span data-ttu-id="e4683-150">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="e4683-150">Key Vault object.</span></span>

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

### <span data-ttu-id="e4683-151">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="e4683-151">-ObjectId</span></span>
<span data-ttu-id="e4683-152">권한을 제거할 Azure Active Directory에서 사용자 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-152">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="e4683-153">-PassThru</span><span class="sxs-lookup"><span data-stu-id="e4683-153">-PassThru</span></span>
<span data-ttu-id="e4683-154">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-154">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="e4683-155">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-155">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="e4683-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4683-156">-ResourceGroupName</span></span>
<span data-ttu-id="e4683-157">액세스 정책이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-157">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="e4683-158">지정 하지 않으면이 cmdlet은 현재 구독의 키 자격 증명 모음을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-158">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="e4683-159">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e4683-159">-ResourceId</span></span>
<span data-ttu-id="e4683-160">KeyVault 리소스 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-160">KeyVault Resource Id.</span></span>

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

### <span data-ttu-id="e4683-161">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-161">-ServicePrincipalName</span></span>
<span data-ttu-id="e4683-162">해당 사용 권한을 제거 하려는 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-162">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="e4683-163">Azure Active Directory의 응용 프로그램에 대해 등록 된 응용 프로그램 ID (클라이언트 ID 라고도 함)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-163">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="e4683-164">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="e4683-164">-UserPrincipalName</span></span>
<span data-ttu-id="e4683-165">액세스 권한을 제거 하려는 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-165">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="e4683-166">-VaultName</span><span class="sxs-lookup"><span data-stu-id="e4683-166">-VaultName</span></span>
<span data-ttu-id="e4683-167">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-167">Specifies the name of the key vault.</span></span>
<span data-ttu-id="e4683-168">이 cmdlet은이 매개 변수에서 지정 하는 키 자격 증명에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-168">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="e4683-169">-확인</span><span class="sxs-lookup"><span data-stu-id="e4683-169">-Confirm</span></span>
<span data-ttu-id="e4683-170">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-170">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e4683-171">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e4683-171">-WhatIf</span></span>
<span data-ttu-id="e4683-172">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-172">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e4683-173">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-173">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e4683-174">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4683-174">CommonParameters</span></span>
<span data-ttu-id="e4683-175">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e4683-175">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4683-176">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4683-176">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4683-177">입력</span><span class="sxs-lookup"><span data-stu-id="e4683-177">INPUTS</span></span>

### <span data-ttu-id="e4683-178">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4683-178">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

### <span data-ttu-id="e4683-179">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e4683-179">System.String</span></span>

## <span data-ttu-id="e4683-180">출력</span><span class="sxs-lookup"><span data-stu-id="e4683-180">OUTPUTS</span></span>

### <span data-ttu-id="e4683-181">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="e4683-181">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="e4683-182">상속자</span><span class="sxs-lookup"><span data-stu-id="e4683-182">NOTES</span></span>

## <span data-ttu-id="e4683-183">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e4683-183">RELATED LINKS</span></span>

[<span data-ttu-id="e4683-184">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="e4683-184">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

