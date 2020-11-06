---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: AzureRM.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.keyvault/remove-azurermkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/KeyVault/Commands.KeyVault/help/Remove-AzureRmKeyVaultAccessPolicy.md
ms.openlocfilehash: ca175d0873b74d8b13d1755f3d0986580c5853ea
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93531709"
---
# <span data-ttu-id="a5010-101">Remove-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5010-101">Remove-AzureRmKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="a5010-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5010-102">SYNOPSIS</span></span>
<span data-ttu-id="a5010-103">키 자격 증명 모음에서 사용자 또는 응용 프로그램에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-103">Removes all permissions for a user or application from a key vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a5010-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5010-104">SYNTAX</span></span>

### <span data-ttu-id="a5010-105">ByUserPrincipalName (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5010-105">ByUserPrincipalName (Default)</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5010-106">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="a5010-106">ByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5010-107">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5010-107">ByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a5010-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="a5010-108">ByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="a5010-109">ForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-110">InputObjectByObjectId</span><span class="sxs-lookup"><span data-stu-id="a5010-110">InputObjectByObjectId</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ObjectId <String> [-ApplicationId <Guid>]
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-111">InputObjectByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5010-111">InputObjectByServicePrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -ServicePrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-112">InputObjectByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5010-112">InputObjectByUserPrincipalName</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -UserPrincipalName <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-113">InputObjectByEmail</span><span class="sxs-lookup"><span data-stu-id="a5010-113">InputObjectByEmail</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> -EmailAddress <String> [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5010-114">InputObjectForVault</span><span class="sxs-lookup"><span data-stu-id="a5010-114">InputObjectForVault</span></span>
```
Remove-AzureRmKeyVaultAccessPolicy [-InputObject] <PSKeyVault> [-EnabledForDeployment]
 [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5010-115">설명은</span><span class="sxs-lookup"><span data-stu-id="a5010-115">DESCRIPTION</span></span>
<span data-ttu-id="a5010-116">**AzureRmKeyVaultAccessPolicy** cmdlet은 사용자 또는 응용 프로그램 또는 모든 사용자 및 응용 프로그램에 대 한 모든 권한을 키 자격 증명 모음에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-116">The **Remove-AzureRmKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="a5010-117">모든 권한을 제거 해도 키 자격 증명 모음이 포함 된 Azure 구독 소유자는 해당 키 자격 증명 모음에 대 한 사용 권한을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-117">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="a5010-118">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5010-118">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="a5010-119">예제의</span><span class="sxs-lookup"><span data-stu-id="a5010-119">EXAMPLES</span></span>

### <span data-ttu-id="a5010-120">예제 1: 사용자에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="a5010-120">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="a5010-121">이 명령은 사용자가 PattiFuller@contoso.com Contoso03Vault 이라는 키 보관소에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-121">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="a5010-122">예제 2: 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="a5010-122">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="a5010-123">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-123">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="a5010-124">이 예제에서는 Azure Active Directory에 등록 된 서비스 사용자 이름을 사용 하 여 응용 프로그램을 식별 http://payroll.contoso.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-124">This example identifies the application by using the service principal name registered in Azure Active Directory, http://payroll.contoso.com.</span></span>

### <span data-ttu-id="a5010-125">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="a5010-125">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="a5010-126">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-126">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="a5010-127">이 예제에서는 서비스 주체의 개체 ID를 기준으로 응용 프로그램을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-127">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="a5010-128">예제 4: Microsoft. Compute resource provider에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-128">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzureRmKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="a5010-129">이 명령은 Contoso03Vault에서 비밀을 가져올 수 있도록 Microsoft. 리소스 공급자에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-129">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="a5010-130">변수</span><span class="sxs-lookup"><span data-stu-id="a5010-130">PARAMETERS</span></span>

### <span data-ttu-id="a5010-131">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a5010-131">-ApplicationId</span></span>
<span data-ttu-id="a5010-132">사용 권한을 제거할 응용 프로그램의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-132">Specifies the ID of application whose permissions should be removed</span></span>

```yaml
Type: Guid
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5010-133">-DefaultProfile</span></span>
<span data-ttu-id="a5010-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a5010-134">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-135">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="a5010-135">-EmailAddress</span></span>
<span data-ttu-id="a5010-136">액세스 권한을 제거 하려는 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-136">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail, InputObjectByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-137">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="a5010-137">-EnabledForDeployment</span></span>
<span data-ttu-id="a5010-138">지정 된 경우 리소스 생성 시 참조 되는 리소스 공급자에서이 키 보관소의 비밀을 검색 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-138">If specified, disables the retrieval of secrets from this key vault by the Microsoft.Compute resource provider when referenced in resource creation.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-139">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="a5010-139">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="a5010-140">지정 된 경우 Azure 디스크 암호화를 통해이 키 보관소의 비밀 검색을 사용 하지 않도록 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-140">If specified, disables the retrieval of secrets from this key vault by Azure Disk Encryption.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-141">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="a5010-141">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="a5010-142">지정 하면 템플릿에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소의 비밀을 검색할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-142">If specified, disables the retrieval of secrets from this key vault by Azure Resource Manager when referenced in templates.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: ForVault, InputObjectForVault
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-143">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a5010-143">-InputObject</span></span>
<span data-ttu-id="a5010-144">키 자격 증명 모음 개체</span><span class="sxs-lookup"><span data-stu-id="a5010-144">Key Vault object.</span></span>

```yaml
Type: PSKeyVault
Parameter Sets: InputObjectByObjectId, InputObjectByServicePrincipalName, InputObjectByUserPrincipalName, InputObjectByEmail, InputObjectForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-145">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a5010-145">-ObjectId</span></span>
<span data-ttu-id="a5010-146">권한을 제거할 Azure Active Directory에서 사용자 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-146">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

```yaml
Type: String
Parameter Sets: ByObjectId, InputObjectByObjectId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-147">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a5010-147">-PassThru</span></span>
<span data-ttu-id="a5010-148">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-148">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="a5010-149">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-149">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="a5010-150">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5010-150">-ResourceGroupName</span></span>
<span data-ttu-id="a5010-151">액세스 정책이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-151">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="a5010-152">지정 하지 않으면이 cmdlet은 현재 구독의 키 자격 증명 모음을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-152">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-153">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5010-153">-ServicePrincipalName</span></span>
<span data-ttu-id="a5010-154">해당 사용 권한을 제거 하려는 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-154">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="a5010-155">Azure Active Directory의 응용 프로그램에 대해 등록 된 응용 프로그램 ID (클라이언트 ID 라고도 함)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-155">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

```yaml
Type: String
Parameter Sets: ByServicePrincipalName, InputObjectByServicePrincipalName
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-156">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="a5010-156">-UserPrincipalName</span></span>
<span data-ttu-id="a5010-157">액세스 권한을 제거 하려는 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-157">Specifies the user principal name of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, InputObjectByUserPrincipalName
Aliases: UPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-158">-VaultName</span><span class="sxs-lookup"><span data-stu-id="a5010-158">-VaultName</span></span>
<span data-ttu-id="a5010-159">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-159">Specifies the name of the key vault.</span></span>
<span data-ttu-id="a5010-160">이 cmdlet은이 매개 변수에서 지정 하는 키 자격 증명에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-160">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

```yaml
Type: String
Parameter Sets: ByUserPrincipalName, ByObjectId, ByServicePrincipalName, ByEmail, ForVault
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a5010-161">-확인</span><span class="sxs-lookup"><span data-stu-id="a5010-161">-Confirm</span></span>
<span data-ttu-id="a5010-162">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-162">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5010-163">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5010-163">-WhatIf</span></span>
<span data-ttu-id="a5010-164">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-164">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5010-165">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-165">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5010-166">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5010-166">CommonParameters</span></span>
<span data-ttu-id="a5010-167">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-167">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5010-168">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a5010-168">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5010-169">입력</span><span class="sxs-lookup"><span data-stu-id="a5010-169">INPUTS</span></span>

### <span data-ttu-id="a5010-170">않아야</span><span class="sxs-lookup"><span data-stu-id="a5010-170">None</span></span>
<span data-ttu-id="a5010-171">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5010-171">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="a5010-172">출력</span><span class="sxs-lookup"><span data-stu-id="a5010-172">OUTPUTS</span></span>

### <span data-ttu-id="a5010-173">Microsoft. KeyVault. 모델. PSKeyVault</span><span class="sxs-lookup"><span data-stu-id="a5010-173">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVault</span></span>

## <span data-ttu-id="a5010-174">상속자</span><span class="sxs-lookup"><span data-stu-id="a5010-174">NOTES</span></span>

## <span data-ttu-id="a5010-175">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5010-175">RELATED LINKS</span></span>

[<span data-ttu-id="a5010-176">Set-AzureRmKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="a5010-176">Set-AzureRmKeyVaultAccessPolicy</span></span>](./Set-AzureRmKeyVaultAccessPolicy.md)

