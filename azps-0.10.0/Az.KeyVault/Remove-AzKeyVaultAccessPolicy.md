---
external help file: Microsoft.Azure.Commands.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
ms.assetid: AE7B103B-23ED-4A66-A0DC-14FB0DF38FA8
online version: https://docs.microsoft.com/en-us/powershell/module/Az.keyvault/remove-Azkeyvaultaccesspolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/KeyVault/KeyVault/help/Remove-AzKeyVaultAccessPolicy.md
ms.openlocfilehash: f5cd00e0ef8e8936a4c87ee313054ae4c084a879
ms.sourcegitcommit: 3d16496984a0b9fd7631aa043726060ddae3624d
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/08/2020
ms.locfileid: "93883273"
---
# <span data-ttu-id="24c8f-101">Remove-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24c8f-101">Remove-AzKeyVaultAccessPolicy</span></span>

## <span data-ttu-id="24c8f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="24c8f-102">SYNOPSIS</span></span>
<span data-ttu-id="24c8f-103">키 자격 증명 모음에서 사용자 또는 응용 프로그램에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-103">Removes all permissions for a user or application from a key vault.</span></span>

## <span data-ttu-id="24c8f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="24c8f-104">SYNTAX</span></span>

### <span data-ttu-id="24c8f-105">ByServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24c8f-105">ByServicePrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -ServicePrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24c8f-106">ByUserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="24c8f-106">ByUserPrincipalName</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 -UserPrincipalName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24c8f-107">ByObjectId</span><span class="sxs-lookup"><span data-stu-id="24c8f-107">ByObjectId</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -ObjectId <String>
 [-ApplicationId <Guid>] [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="24c8f-108">ByEmail</span><span class="sxs-lookup"><span data-stu-id="24c8f-108">ByEmail</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>] -EmailAddress <String>
 [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="24c8f-109">ForVault</span><span class="sxs-lookup"><span data-stu-id="24c8f-109">ForVault</span></span>
```
Remove-AzKeyVaultAccessPolicy [-VaultName] <String> [[-ResourceGroupName] <String>]
 [-EnabledForDeployment] [-EnabledForTemplateDeployment] [-EnabledForDiskEncryption] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="24c8f-110">설명은</span><span class="sxs-lookup"><span data-stu-id="24c8f-110">DESCRIPTION</span></span>
<span data-ttu-id="24c8f-111">**AzKeyVaultAccessPolicy** cmdlet은 사용자 또는 응용 프로그램 또는 모든 사용자 및 응용 프로그램에 대 한 모든 권한을 키 자격 증명 모음에서 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-111">The **Remove-AzKeyVaultAccessPolicy** cmdlet removes all permissions for a user or application or for all users and applications from a key vault.</span></span>
<span data-ttu-id="24c8f-112">모든 권한을 제거 해도 키 자격 증명 모음이 포함 된 Azure 구독 소유자는 해당 키 자격 증명 모음에 대 한 사용 권한을 추가할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-112">Even if you remove all permissions, the owner of the Azure subscription that contains the key vault can add permissions to the key vault.</span></span>

<span data-ttu-id="24c8f-113">이 cmdlet에 대해 리소스 그룹을 지정 하는 것은 선택 사항 이지만 성능 향상을 위해 이러한 작업을 수행 해야 한다는 점에 유의 하세요.</span><span class="sxs-lookup"><span data-stu-id="24c8f-113">Note that although specifying the resource group is optional for this cmdlet, you should do so for better performance.</span></span>

## <span data-ttu-id="24c8f-114">예제의</span><span class="sxs-lookup"><span data-stu-id="24c8f-114">EXAMPLES</span></span>

### <span data-ttu-id="24c8f-115">예제 1: 사용자에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="24c8f-115">Example 1: Remove permissions for a user</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -UserPrincipalName 'PattiFuller@contoso.com'
```

<span data-ttu-id="24c8f-116">이 명령은 사용자가 PattiFuller@contoso.com Contoso03Vault 이라는 키 보관소에 대 한 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-116">This command removes all the permissions that a user PattiFuller@contoso.com has on the key vault named Contoso03Vault.</span></span>

### <span data-ttu-id="24c8f-117">예제 2: 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="24c8f-117">Example 2: Remove permissions for an application</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ServicePrincipalName 'http://payroll.contoso.com'
```

<span data-ttu-id="24c8f-118">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-118">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="24c8f-119">이 예제에서는 Azure Active Directory에 등록 된 서비스 사용자 이름을 사용 하 여 응용 프로그램을 식별 `http://payroll.contoso.com` 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-119">This example identifies the application by using the service principal name registered in Azure Active Directory, `http://payroll.contoso.com`.</span></span>

### <span data-ttu-id="24c8f-120">예제 3: 해당 개체 ID를 사용 하 여 응용 프로그램에 대 한 사용 권한 제거</span><span class="sxs-lookup"><span data-stu-id="24c8f-120">Example 3: Remove permissions for an application by using its object ID</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ObjectID 34595082-9346-41b6-8d6b-295a2808b8db
```

<span data-ttu-id="24c8f-121">이 명령은 Contoso03Vault 이라는 키 보관소에 대 한 응용 프로그램의 모든 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-121">This command removes all the permissions that an application has on the key vault named Contoso03Vault.</span></span>
<span data-ttu-id="24c8f-122">이 예제에서는 서비스 주체의 개체 ID를 기준으로 응용 프로그램을 식별 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-122">This example identifies the application by the object ID of the service principal.</span></span>

### <span data-ttu-id="24c8f-123">예제 4: Microsoft. Compute resource provider에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-123">Example 4: Remove permissions for the Microsoft.Compute resource provider</span></span>
```
PS C:\>Remove-AzKeyVaultAccessPolicy -VaultName 'Contoso03Vault' -ResourceGroupName 'Group14' -EnabledForDeployment
```

<span data-ttu-id="24c8f-124">이 명령은 Contoso03Vault에서 비밀을 가져올 수 있도록 Microsoft. 리소스 공급자에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-124">This command removes permission for the Microsoft.Compute resource provider to get secrets from the Contoso03Vault.</span></span>

## <span data-ttu-id="24c8f-125">변수</span><span class="sxs-lookup"><span data-stu-id="24c8f-125">PARAMETERS</span></span>

### <span data-ttu-id="24c8f-126">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="24c8f-126">-ApplicationId</span></span>
<span data-ttu-id="24c8f-127">나중에 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-127">For future use.</span></span>

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

### <span data-ttu-id="24c8f-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="24c8f-128">-DefaultProfile</span></span>
<span data-ttu-id="24c8f-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="24c8f-129">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="24c8f-130">-EmailAddress</span><span class="sxs-lookup"><span data-stu-id="24c8f-130">-EmailAddress</span></span>
<span data-ttu-id="24c8f-131">액세스 권한을 제거 하려는 사용자의 사용자 전자 메일 주소를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-131">Specifies the user email address of the user whose access you want to remove.</span></span>

```yaml
Type: String
Parameter Sets: ByEmail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="24c8f-132">-EnabledForDeployment</span><span class="sxs-lookup"><span data-stu-id="24c8f-132">-EnabledForDeployment</span></span>
<span data-ttu-id="24c8f-133">이 키 자격 증명 모음이 리소스 만들기에서 참조 되는 경우 (예: 가상 컴퓨터를 만들 때)이 키 보관소에서 비밀을 검색 하도록 Microsoft. a 리소스 공급자를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-133">Enables the Microsoft.Compute resource provider to retrieve secrets from this key vault when this key vault is referenced in resource creation, for example when creating a virtual machine.</span></span>

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

### <span data-ttu-id="24c8f-134">-EnabledForDiskEncryption</span><span class="sxs-lookup"><span data-stu-id="24c8f-134">-EnabledForDiskEncryption</span></span>
<span data-ttu-id="24c8f-135">Azure 디스크 암호화 서비스에서이 키 자격 증명 모음의 비밀 및 래핑 키를 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-135">Enables the Azure disk encryption service to get secrets and unwrap keys from this key vault.</span></span>

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

### <span data-ttu-id="24c8f-136">-EnabledForTemplateDeployment</span><span class="sxs-lookup"><span data-stu-id="24c8f-136">-EnabledForTemplateDeployment</span></span>
<span data-ttu-id="24c8f-137">이 키 자격 증명 모음이 서식 파일 배포에서 참조 되는 경우 Azure 리소스 관리자가이 키 보관소에서 비밀을 가져올 수 있도록 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-137">Enables Azure Resource Manager to get secrets from this key vault when this key vault is referenced in a template deployment.</span></span>

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

### <span data-ttu-id="24c8f-138">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="24c8f-138">-ObjectId</span></span>
<span data-ttu-id="24c8f-139">권한을 제거할 Azure Active Directory에서 사용자 또는 서비스 주체의 개체 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-139">Specifies the object ID of the user or service principal in Azure Active Directory for which to remove permissions.</span></span>

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

### <span data-ttu-id="24c8f-140">-PassThru</span><span class="sxs-lookup"><span data-stu-id="24c8f-140">-PassThru</span></span>
<span data-ttu-id="24c8f-141">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-141">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="24c8f-142">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-142">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="24c8f-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="24c8f-143">-ResourceGroupName</span></span>
<span data-ttu-id="24c8f-144">액세스 정책이 수정 되 고 있는 키 자격 증명 모음과 연결 된 리소스 그룹의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-144">Specifies the name of the resource group associated with the key vault whose access policy is being modified.</span></span>
<span data-ttu-id="24c8f-145">지정 하지 않으면이 cmdlet은 현재 구독의 키 자격 증명 모음을 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-145">If not specified, this cmdlet searches for the key vault in the current subscription.</span></span>

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

### <span data-ttu-id="24c8f-146">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="24c8f-146">-ServicePrincipalName</span></span>
<span data-ttu-id="24c8f-147">해당 사용 권한을 제거 하려는 응용 프로그램의 서비스 사용자 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-147">Specifies the service principal name of the application whose permissions you want to remove.</span></span>
<span data-ttu-id="24c8f-148">Azure Active Directory의 응용 프로그램에 대해 등록 된 응용 프로그램 ID (클라이언트 ID 라고도 함)를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-148">Specify the application ID, also known as client ID, registered for the application in Azure Active Directory.</span></span>

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

### <span data-ttu-id="24c8f-149">-UserPrincipalName</span><span class="sxs-lookup"><span data-stu-id="24c8f-149">-UserPrincipalName</span></span>
<span data-ttu-id="24c8f-150">액세스 권한을 제거 하려는 사용자의 upn (사용자 이름)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-150">Specifies the user principal name of the user whose access you want to remove.</span></span>

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

### <span data-ttu-id="24c8f-151">-VaultName</span><span class="sxs-lookup"><span data-stu-id="24c8f-151">-VaultName</span></span>
<span data-ttu-id="24c8f-152">키 보관소의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-152">Specifies the name of the key vault.</span></span>
<span data-ttu-id="24c8f-153">이 cmdlet은이 매개 변수에서 지정 하는 키 자격 증명에 대 한 사용 권한을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-153">This cmdlet removes permissions for the key vault that this parameter specifies.</span></span>

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

### <span data-ttu-id="24c8f-154">-확인</span><span class="sxs-lookup"><span data-stu-id="24c8f-154">-Confirm</span></span>
<span data-ttu-id="24c8f-155">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-155">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="24c8f-156">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="24c8f-156">-WhatIf</span></span>
<span data-ttu-id="24c8f-157">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-157">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="24c8f-158">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-158">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="24c8f-159">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="24c8f-159">CommonParameters</span></span>
<span data-ttu-id="24c8f-160">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-160">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="24c8f-161">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="24c8f-161">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="24c8f-162">입력</span><span class="sxs-lookup"><span data-stu-id="24c8f-162">INPUTS</span></span>

### <span data-ttu-id="24c8f-163">않아야</span><span class="sxs-lookup"><span data-stu-id="24c8f-163">None</span></span>
<span data-ttu-id="24c8f-164">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="24c8f-164">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="24c8f-165">출력</span><span class="sxs-lookup"><span data-stu-id="24c8f-165">OUTPUTS</span></span>

### <span data-ttu-id="24c8f-166">Microsoft. KeyVault. PSVault</span><span class="sxs-lookup"><span data-stu-id="24c8f-166">Microsoft.Azure.Commands.KeyVault.Models.PSVault</span></span>

## <span data-ttu-id="24c8f-167">상속자</span><span class="sxs-lookup"><span data-stu-id="24c8f-167">NOTES</span></span>

## <span data-ttu-id="24c8f-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="24c8f-168">RELATED LINKS</span></span>

[<span data-ttu-id="24c8f-169">Set-AzKeyVaultAccessPolicy</span><span class="sxs-lookup"><span data-stu-id="24c8f-169">Set-AzKeyVaultAccessPolicy</span></span>](./Set-AzKeyVaultAccessPolicy.md)

