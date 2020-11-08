---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: 636FAD5B-8C39-4E5C-8978-6845C6B89BC0
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/set-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Set-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: a774c438f9be25dc55f48c5121031956374a2cb7
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "94047369"
---
# <span data-ttu-id="4744e-101">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4744e-101">Set-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="4744e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4744e-102">SYNOPSIS</span></span>
<span data-ttu-id="4744e-103">키 자격 증명 모음을 사용 하 여 작업을 수행 하기 위해 사용자, 응용 프로그램 또는 보안 그룹에 대 한 기존 사용 권한을 부여 하거나 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-103">Grants or modifies existing permissions for a user, application, or security group to perform operations with a key vault.</span></span>

## <span data-ttu-id="4744e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4744e-104">SYNTAX</span></span>

### <span data-ttu-id="4744e-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4744e-105">ByServicePrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4744e-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4744e-106">ByUserPrincipalName</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4744e-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="4744e-107">ByObjectId</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>]
 [-PermissionsToCertificates <String[]>] [-PermissionsToStorage <String[]>] [-BypassObjectIdValidation]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4744e-108">ByEmailAddress</span><span class="sxs-lookup"><span data-stu-id="4744e-108">ByEmailAddress</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PermissionsToKeys <String[]>] [-PermissionsToSecrets <String[]>] [-PermissionsToCertificates <String[]>]
 [-PermissionsToStorage <String[]>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="4744e-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="4744e-109">ForVault</span></span>
```
Set-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4744e-110">설명은</span><span class="sxs-lookup"><span data-stu-id="4744e-110">DESCRIPTION</span></span>
<span data-ttu-id="4744e-111">**AzKeyVaultAccessPolicy** cmdlet은 사용자, 응용 프로그램 또는 보안 그룹의 기존 사용 권한을 부여 하거나 수정 하 여 키 자격 증명 모음으로 지정 된 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-111">The **Set-AzKeyVaultAccessPolicy** cmdlet grants or modifies existing permissions for a user, application, or security group to perform the specified operations with a key vault.</span></span> <span data-ttu-id="4744e-112">다른 사용자, 앱 또는 보안 그룹의 키 자격 증명에 대 한 사용 권한은 수정 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-112">It does not modify the permissions that other users, applications, or security groups have on the key vault.</span></span>

<span data-ttu-id="4744e-113">보안 그룹에 대 한 사용 권한을 설정 하는 경우이 작업은 해당 보안 그룹의 사용자 에게만 적용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-113">If you are setting permissions for a security group, this operation affects only users in that security group.</span></span>

<span data-ttu-id="4744e-114">다음 디렉터리는 모두 동일한 Azure 디렉터리 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-114">The following directories must all be the same Azure directory:</span></span>
- <span data-ttu-id="4744e-115">키 보관소가 있는 Azure 구독의 기본 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-115">The default directory of the Azure subscription in which the key vault resides.</span></span>
- <span data-ttu-id="4744e-116">권한을 부여 하는 사용자 또는 응용 프로그램 그룹이 포함 된 Azure 디렉터리입니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-116">The Azure directory that contains the user or application group that you are granting permissions to.</span></span>

<span data-ttu-id="4744e-117">이러한 조건이 충족 되지 않고이 cmdlet이 작동 하지 않을 경우 시나리오의 예:</span><span class="sxs-lookup"><span data-stu-id="4744e-117">Examples of scenarios when these conditions are not met and this cmdlet will not work are:</span></span>

- <span data-ttu-id="4744e-118">다른 조직에서 사용자의 키 자격 증명을 관리 하도록 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-118">Authorizing a user from a different organization to manage your key vault.</span></span>
<span data-ttu-id="4744e-119">각 조직에는 고유한 디렉터리가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-119">Each organization has its own directory.</span></span>
- <span data-ttu-id="4744e-120">Azure 계정에 디렉터리가 여러 개 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-120">Your Azure account has multiple directories.</span></span>
<span data-ttu-id="4744e-121">기본 디렉터리가 아닌 디렉터리에 응용 프로그램을 등록 하는 경우 해당 응용 프로그램에 키 자격 증명 모음을 사용 하도록 허가할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-121">If you register an application in a directory other than the default directory, you cannot authorize that application to use your key vault.</span></span>
<span data-ttu-id="4744e-122">응용 프로그램이 기본 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-122">The application must be in the default directory.</span></span>

<span data-ttu-id="4744e-123">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="4744e-123">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="4744e-124">예제의</span><span class="sxs-lookup"><span data-stu-id="4744e-124">EXAMPLES</span></span>

### <span data-ttu-id="4744e-125">예제 1: 키 자격 증명 모음에 대 한 사용 권한을 사용자에 게 부여 하 고 사용 권한을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-125">Example 1: Grant permissions to a user for a key vault and modify the permissions</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys create,import,delete,list -PermissionsToSecrets set,delete
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets set,delete,get -PassThru
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToKeys @() -PassThru
```

<span data-ttu-id="4744e-126">첫 번째 명령은 Azure Active Directory의 사용자에 대 한 사용 권한을 부여 PattiFuller@contoso.com 하 고, Contoso03Vault 이라는 키 보관소를 사용 하 여 키 및 비밀에 대 한 작업을 수행 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-126">The first command grants permissions for a user in your Azure Active Directory, PattiFuller@contoso.com, to perform operations on keys and secrets with a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="4744e-127">두 번째 명령은 첫 번째 명령에 부여 된 사용 권한을 수정 하 여 PattiFuller@contoso.com , 이제 암호를 설정 하 고 삭제 하는 것 외에도 비밀을 받을 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-127">The second command modifies the permissions that were granted to PattiFuller@contoso.com in the first command, to now allow getting secrets in addition to setting and deleting them.</span></span> <span data-ttu-id="4744e-128">이 명령 후에는 키 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-128">The permissions to key operations remain unchanged after this command.</span></span> <span data-ttu-id="4744e-129">*PassThru* 매개 변수는 cmdlet에서 반환 되는 업데이트 된 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-129">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

<span data-ttu-id="4744e-130">마지막 명령은 PattiFuller@contoso.com 키 작업에 대 한 모든 사용 권한을 제거 하는 기존 권한을 추가로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-130">The final command further modifies the existing permissions for PattiFuller@contoso.com to remove all permissions to key operations.</span></span> <span data-ttu-id="4744e-131">이 명령 후에는 비밀 작업에 대 한 사용 권한이 변경 되지 않고 그대로 유지 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-131">The permissions to secret operations remain unchanged after this command.</span></span> <span data-ttu-id="4744e-132">*PassThru* 매개 변수는 cmdlet에서 반환 되는 업데이트 된 개체를 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-132">The *PassThru* parameter results in the updated object being returned by the cmdlet.</span></span>

### <span data-ttu-id="4744e-133">예제 2: 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 서비스 사용자에 게 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4744e-133">Example 2: Grant permissions for an application service principal to read and write secrets</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com' -PermissionsToSecrets Get,Set
```

<span data-ttu-id="4744e-134">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-134">This command grants permissions for an application for a key vault named Contoso03Vault.</span></span>

<span data-ttu-id="4744e-135">*ServicePrincipalName* 매개 변수는 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-135">The *ServicePrincipalName* parameter specifies the application.</span></span> <span data-ttu-id="4744e-136">Azure Active Directory에 응용 프로그램을 등록 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-136">The application must be registered in your Azure Active Directory.</span></span> <span data-ttu-id="4744e-137">*ServicePrincipalName* 매개 변수 값은 응용 프로그램의 서비스 사용자 이름 또는 응용 프로그램 ID GUID 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-137">The value of the *ServicePrincipalName* parameter must be either the service principal name of the application or the application ID GUID.</span></span>

<span data-ttu-id="4744e-138">이 예제에서는 서비스 사용자 이름을 지정 하 `http://payroll.contoso.com` 고, 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-138">This example specifies the service principal name `http://payroll.contoso.com`, and the command grants the application permissions to read and write secrets.</span></span>

### <span data-ttu-id="4744e-139">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4744e-139">Example 3: Grant permissions for an application using its object ID</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectId 34595082-9346-41b6-8d6b-295a2808b8db -PermissionsToSecrets Get,Set
```

<span data-ttu-id="4744e-140">이 명령은 비밀 정보를 읽고 쓸 수 있도록 응용 프로그램 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-140">This command grants the application permissions to read and write secrets.</span></span>

<span data-ttu-id="4744e-141">이 예제에서는 응용 프로그램의 서비스 사용자에 대 한 개체 ID를 사용 하 여 응용 프로그램을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-141">This example specifies the application using the object ID of the service principal of the application.</span></span>

### <span data-ttu-id="4744e-142">예제 4: 사용자 계정 이름에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4744e-142">Example 4: Grant permissions for a user principal name</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com' -PermissionsToSecrets Get,List,Set
```

<span data-ttu-id="4744e-143">이 명령은 비밀에 대 한 액세스에 대 한 지정 된 upn (사용자 이름)의 get, list, set 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-143">This command grants get, list, and set permissions for the specified user principal name for access to secrets.</span></span>

### <span data-ttu-id="4744e-144">예제 5: Microsoft의 키 자격 증명 모음에서 비밀을 검색할 수 있도록 설정 합니다. 리소스 공급자</span><span class="sxs-lookup"><span data-stu-id="4744e-144">Example 5: Enable secrets to be retrieved from a key vault vault by the Microsoft.Compute resource provider</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="4744e-145">이 명령은 Contoso03Vault 키 자격 증명 모음에서 Microsoft. a 리소스 공급자가 검색할 수 있는 비밀 정보에 대 한 사용 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-145">This command grants the permissions for secrets to be retrieved from the Contoso03Vault key vault by the Microsoft.Compute resource provider.</span></span>

### <span data-ttu-id="4744e-146">예제 6: 보안 그룹에 대 한 사용 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4744e-146">Example 6: Grant permissions to a security group</span></span>
```
PS C:\>Get-AzADGroup
PS C:\> Set-AzKeyVaultAccessPolicy -VaultName 'myownvault' -ObjectId (Get-AzADGroup -SearchString 'group2')[0].Id -PermissionsToKeys All -PermissionsToSecrets All
DisplayName                    Type                           ObjectId
-----------                    ----                           --------
group1                                                        96a0daa6-9841-4a9c-bdeb-e7062276c688
group2                                                        b8a401eb-63ad-4a30-b0e1-a7461969fe54
group3                                                        da07a6be-2c1e-4e42-934d-ceb57cf652b4
```

<span data-ttu-id="4744e-147">첫 번째 명령은 Get-AzADGroup cmdlet을 사용 하 여 모든 Active Directory 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-147">The first command uses the Get-AzADGroup cmdlet to get all Active Directory groups.</span></span> <span data-ttu-id="4744e-148">출력에서 이름이 **group1** , **group2** 및 **group3** 인 3 개의 그룹이 반환 됨을 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-148">From the output, you see 3 groups returned, named **group1** , **group2** , and **group3**.</span></span> <span data-ttu-id="4744e-149">여러 그룹의 이름은 동일 하지만 항상 고유한 ObjectId를 가질 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-149">Multiple groups can have the same name but always have a unique ObjectId.</span></span> <span data-ttu-id="4744e-150">동일한 이름을 가진 그룹이 두 개 이상 반환 되는 경우 출력에 ObjectId를 사용 하 여 사용할 항목을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-150">When more than one group that has the same name is returned, use the ObjectId in the output to identify the one you want to use.</span></span>

<span data-ttu-id="4744e-151">그런 다음이 명령의 출력을 Set-AzKeyVaultAccessPolicy와 함께 사용 하 여 **myownvault** 이라는 키 보관소의 group2에 대 한 사용 권한을 부여할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-151">You then use the output of this command with Set-AzKeyVaultAccessPolicy to grant permissions to group2 for your key vault, named **myownvault**.</span></span> <span data-ttu-id="4744e-152">이 예제에서는 동일한 명령줄에서 ' group2 ' 이라는 그룹을 열거 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-152">This example enumerates the groups named 'group2' inline in the same command line.</span></span>

<span data-ttu-id="4744e-153">반환 된 목록에 이름이 ' group2 ' 인 여러 그룹이 있을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-153">There may be multiple groups in the returned list that are named 'group2'.</span></span>
<span data-ttu-id="4744e-154">이 예제에서는 반환 된 목록의 인덱스 0으로 표시 되는 첫 번째 항목을 선택 \[ \] 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-154">This example picks the first one, indicated by index \[0\] in the returned list.</span></span>

### <span data-ttu-id="4744e-155">예제 7: 고객 관리 테 넌 트 키 (BYOK)에 대 한 Azure Information Protection 액세스 권한 부여</span><span class="sxs-lookup"><span data-stu-id="4744e-155">Example 7: Grant Azure Information Protection access to the customer-managed tenant key (BYOK)</span></span>
```
PS C:\>Set-AzKeyVaultAccessPolicy -VaultName 'Contoso04Vault' -ServicePrincipalName 00000012-0000-0000-c000-000000000000 -PermissionsToKeys decrypt,sign,get
```

<span data-ttu-id="4744e-156">이 명령은 사용자가 관리 하는 키 (자체 키 가져오기 또는 "BYOK" 시나리오)를 Azure Information Protection 테 넌 트 키로 사용 하도록 Azure Information Protection에 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-156">This command authorizes Azure Information Protection to use a customer-managed key (the bring your own key, or "BYOK" scenario) as the Azure Information Protection tenant key.</span></span>

<span data-ttu-id="4744e-157">이 명령을 실행할 때 고유한 키 보관소 이름을 지정 하면 *ServicePrincipalName* 매개 변수를 GUID **00000012-0000-0000-c 000-000000000000** 에 지정 하 고 예제에서 사용 권한을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-157">When you run this command, specify your own key vault name but you must specify the *ServicePrincipalName* parameter with the GUID **00000012-0000-0000-c000-000000000000** and specify the permissions in the example.</span></span>

## <span data-ttu-id="4744e-158">변수</span><span class="sxs-lookup"><span data-stu-id="4744e-158">PARAMETERS</span></span>

### <span data-ttu-id="4744e-159">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="4744e-159">-ApplicationId</span></span>
<span data-ttu-id="4744e-160">나중에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-160">For future use.</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-161">-BypassObjectIdValidation</span><span class="sxs-lookup"><span data-stu-id="4744e-161">-BypassObjectIdValidation</span></span>
<span data-ttu-id="4744e-162">Azure Active Directory에 개체가 있는지 확인 하지 않고 개체 ID를 지정할 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-162">Enables you to specify an object ID without validating that the object exists in Azure Active Directory.</span></span>

<span data-ttu-id="4744e-163">다른 Azure 테 넌 트에서 위임 된 보안 그룹을 참조 하는 개체 ID에 키 자격 증명 모음에 대 한 액세스 권한을 부여 하려는 경우에만이 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-163">Use this parameter only if you want to grant access to your key vault to an object ID that refers to a delegated security group from another Azure tenant.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-164">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4744e-164">-DefaultProfile</span></span>
<span data-ttu-id="4744e-165">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="4744e-165">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-166">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="4744e-166">-EmailAddress</span></span>
<span data-ttu-id="4744e-167">권한을 부여할 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-167">Specifies the user email address of the user to whom to grant permissions.</span></span>

<span data-ttu-id="4744e-168">이 전자 메일 주소는 현재 구독과 연결 된 디렉터리에 있어야 하 고 고유 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-168">This email address must exist in the directory associated with the current subscription and be unique.</span></span>

```yaml
Type: String
Parameter Sets: ByEmailAddress
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-169">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="4744e-169">-EnabledForDeployment</span></span>
<span data-ttu-id="4744e-170">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-170">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-171">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="4744e-171">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="4744e-172">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-172">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-173">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="4744e-173">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="4744e-174">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-174">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-175">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="4744e-175">-ObjectId</span></span>
<span data-ttu-id="4744e-176">사용 권한을 부여할 Azure Active Directory의 사용자 또는 서비스 사용자의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-176">Specifies the object ID of the user or service principal in Azure Active Directory for which to grant permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-177">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4744e-177">-PassThru</span></span>
<span data-ttu-id="4744e-178">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-178">Returns an object representing the item with which you are working.</span></span>

<span data-ttu-id="4744e-179">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-179">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-180">-PermissionsToCertificates</span><span class="sxs-lookup"><span data-stu-id="4744e-180">-PermissionsToCertificates</span></span>
<span data-ttu-id="4744e-181">사용자 또는 서비스 사용자에 게 부여할 인증서 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-181">Specifies an array of certificate permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="4744e-182">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-182">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="4744e-183">가져오기</span><span class="sxs-lookup"><span data-stu-id="4744e-183">Get</span></span>
- <span data-ttu-id="4744e-184">목록</span><span class="sxs-lookup"><span data-stu-id="4744e-184">List</span></span>
- <span data-ttu-id="4744e-185">삭제</span><span class="sxs-lookup"><span data-stu-id="4744e-185">Delete</span></span>
- <span data-ttu-id="4744e-186">만드는</span><span class="sxs-lookup"><span data-stu-id="4744e-186">Create</span></span>
- <span data-ttu-id="4744e-187">Import</span><span class="sxs-lookup"><span data-stu-id="4744e-187">Import</span></span>
- <span data-ttu-id="4744e-188">Update</span><span class="sxs-lookup"><span data-stu-id="4744e-188">Update</span></span>
- <span data-ttu-id="4744e-189">Managecontacts</span><span class="sxs-lookup"><span data-stu-id="4744e-189">Managecontacts</span></span>
- <span data-ttu-id="4744e-190">Getissuers</span><span class="sxs-lookup"><span data-stu-id="4744e-190">Getissuers</span></span>
- <span data-ttu-id="4744e-191">Listissuers</span><span class="sxs-lookup"><span data-stu-id="4744e-191">Listissuers</span></span>
- <span data-ttu-id="4744e-192">Setissuers</span><span class="sxs-lookup"><span data-stu-id="4744e-192">Setissuers</span></span>
- <span data-ttu-id="4744e-193">Deleteissuers</span><span class="sxs-lookup"><span data-stu-id="4744e-193">Deleteissuers</span></span>
- <span data-ttu-id="4744e-194">Manageissuers</span><span class="sxs-lookup"><span data-stu-id="4744e-194">Manageissuers</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, create, import, update, managecontacts, getissuers, listissuers, setissuers, deleteissuers, manageissuers, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-195">-기능 하는 Sto키</span><span class="sxs-lookup"><span data-stu-id="4744e-195">-PermissionsToKeys</span></span>
<span data-ttu-id="4744e-196">사용자 또는 서비스 사용자에 게 부여할 키 작업 사용 권한의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-196">Specifies an array of key operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="4744e-197">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-197">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="4744e-198">해독은</span><span class="sxs-lookup"><span data-stu-id="4744e-198">Decrypt</span></span>
- <span data-ttu-id="4744e-199">해독할</span><span class="sxs-lookup"><span data-stu-id="4744e-199">Encrypt</span></span>
- <span data-ttu-id="4744e-200">UnwrapKey</span><span class="sxs-lookup"><span data-stu-id="4744e-200">UnwrapKey</span></span>
- <span data-ttu-id="4744e-201">WrapKey</span><span class="sxs-lookup"><span data-stu-id="4744e-201">WrapKey</span></span>
- <span data-ttu-id="4744e-202">나타나는지</span><span class="sxs-lookup"><span data-stu-id="4744e-202">Verify</span></span>
- <span data-ttu-id="4744e-203">등록할</span><span class="sxs-lookup"><span data-stu-id="4744e-203">Sign</span></span>
- <span data-ttu-id="4744e-204">가져오기</span><span class="sxs-lookup"><span data-stu-id="4744e-204">Get</span></span>
- <span data-ttu-id="4744e-205">목록</span><span class="sxs-lookup"><span data-stu-id="4744e-205">List</span></span>
- <span data-ttu-id="4744e-206">Update</span><span class="sxs-lookup"><span data-stu-id="4744e-206">Update</span></span>
- <span data-ttu-id="4744e-207">만드는</span><span class="sxs-lookup"><span data-stu-id="4744e-207">Create</span></span>
- <span data-ttu-id="4744e-208">Import</span><span class="sxs-lookup"><span data-stu-id="4744e-208">Import</span></span>
- <span data-ttu-id="4744e-209">삭제</span><span class="sxs-lookup"><span data-stu-id="4744e-209">Delete</span></span>
- <span data-ttu-id="4744e-210">백업할</span><span class="sxs-lookup"><span data-stu-id="4744e-210">Backup</span></span>
- <span data-ttu-id="4744e-211">복원한</span><span class="sxs-lookup"><span data-stu-id="4744e-211">Restore</span></span>
- <span data-ttu-id="4744e-212">절약할</span><span class="sxs-lookup"><span data-stu-id="4744e-212">Recover</span></span>
- <span data-ttu-id="4744e-213">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="4744e-213">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: decrypt, encrypt, unwrapKey, wrapKey, verify, sign, get, list, update, create, import, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-214">-기능 방법 비밀</span><span class="sxs-lookup"><span data-stu-id="4744e-214">-PermissionsToSecrets</span></span>
<span data-ttu-id="4744e-215">사용자 또는 서비스 사용자에 게 부여할 비밀 작업 권한 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-215">Specifies an array of secret operation permissions to grant to a user or service principal.</span></span>

<span data-ttu-id="4744e-216">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-216">The acceptable values for this parameter:</span></span>

- <span data-ttu-id="4744e-217">가져오기</span><span class="sxs-lookup"><span data-stu-id="4744e-217">Get</span></span>
- <span data-ttu-id="4744e-218">목록</span><span class="sxs-lookup"><span data-stu-id="4744e-218">List</span></span>
- <span data-ttu-id="4744e-219">설치할</span><span class="sxs-lookup"><span data-stu-id="4744e-219">Set</span></span>
- <span data-ttu-id="4744e-220">삭제</span><span class="sxs-lookup"><span data-stu-id="4744e-220">Delete</span></span>
- <span data-ttu-id="4744e-221">백업할</span><span class="sxs-lookup"><span data-stu-id="4744e-221">Backup</span></span>
- <span data-ttu-id="4744e-222">복원한</span><span class="sxs-lookup"><span data-stu-id="4744e-222">Restore</span></span>
- <span data-ttu-id="4744e-223">절약할</span><span class="sxs-lookup"><span data-stu-id="4744e-223">Recover</span></span>
- <span data-ttu-id="4744e-224">지우시겠습니까</span><span class="sxs-lookup"><span data-stu-id="4744e-224">Purge</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, set, delete, backup, restore, recover, purge, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-225">-기능 저장 저장소</span><span class="sxs-lookup"><span data-stu-id="4744e-225">-PermissionsToStorage</span></span>
<span data-ttu-id="4744e-226">사용자 또는 서비스 사용자에 게 부여할 관리 되는 저장소 계정 및 SaS 정의 작업 사용 권한을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-226">Specifies managed storage account and SaS-definition operation permissions to grant to a user or service principal.</span></span>

```yaml
Type: String[]
Parameter Sets: ByServicePrincipalName, ByUserPrincipalName, ByObjectId, ByEmailAddress
Aliases:
Accepted values: get, list, delete, set, update, regeneratekey, getsas, listsas, deletesas, setsas, all

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-227">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4744e-227">-ResourceGroupName</span></span>
<span data-ttu-id="4744e-228">리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-228">Specifies the name of a resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-229">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="4744e-229">-ServicePrincipalName</span></span>
<span data-ttu-id="4744e-230">권한을 부여할 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-230">Specifies the service principal name of the application to which to grant permissions.</span></span>

<span data-ttu-id="4744e-231">클라이언트 ID 라고도 하는 응용 프로그램 ID를 AzureActive Directory의 응용 프로그램에 등록 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-231">Specify the application ID, also known as client ID, registered for the application in AzureActive Directory.</span></span> <span data-ttu-id="4744e-232">이 매개 변수에서 지정 하는 서비스 사용자 이름을 사용 하는 응용 프로그램은 현재 구독을 포함 하는 Azure 디렉터리에 등록 되어 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-232">The application with the service principal name that this parameter specifies must be registered in the Azure directory that contains your current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-233">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="4744e-233">-UserPrincipalName</span></span>
<span data-ttu-id="4744e-234">권한을 부여할 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-234">Specifies the user principal name of the user to whom to grant permissions.</span></span>

<span data-ttu-id="4744e-235">이 사용자 사용자 이름은 현재 구독과 연결 된 디렉터리에 있어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-235">This user principal name must exist in the directory associated with the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-236">-VaultName</span><span class="sxs-lookup"><span data-stu-id="4744e-236">-VaultName</span></span>
<span data-ttu-id="4744e-237">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-237">Specifies the name of a key vault.</span></span>

<span data-ttu-id="4744e-238">이 cmdlet은이 매개 변수에서 지정 하는 키 보관소에 대 한 액세스 정책을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-238">This cmdlet modifies the access policy for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-239">-확인</span><span class="sxs-lookup"><span data-stu-id="4744e-239">-Confirm</span></span>
<span data-ttu-id="4744e-240">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-240">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-241">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4744e-241">-WhatIf</span></span>
<span data-ttu-id="4744e-242">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-242">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4744e-243">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-243">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4744e-244">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4744e-244">CommonParameters</span></span>
<span data-ttu-id="4744e-245">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4744e-245">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4744e-246">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4744e-246">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4744e-247">입력</span><span class="sxs-lookup"><span data-stu-id="4744e-247">INPUTS</span></span>

### <span data-ttu-id="4744e-248">문자열, Guid, String [], 스위치</span><span class="sxs-lookup"><span data-stu-id="4744e-248">String, Guid, String[], Switch</span></span>

## <span data-ttu-id="4744e-249">출력</span><span class="sxs-lookup"><span data-stu-id="4744e-249">OUTPUTS</span></span>

### <span data-ttu-id="4744e-250">Microsoft. KeyVault. PSVault</span><span class="sxs-lookup"><span data-stu-id="4744e-250">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="4744e-251">상속자</span><span class="sxs-lookup"><span data-stu-id="4744e-251">NOTES</span></span>

## <span data-ttu-id="4744e-252">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4744e-252">RELATED LINKS</span></span>

[<span data-ttu-id="4744e-253">Get-AzKeyVault</span><span class="sxs-lookup"><span data-stu-id="4744e-253">Get-AzKeyVault</span></span>](./Get-AzKeyVault.md)

[<span data-ttu-id="4744e-254">제거-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="4744e-254">Remove-AzKeyVaultAccessPolicy</span></span>](./Remove-AzKeyVaultAccessPolicy.md)

