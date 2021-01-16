---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 9e2dd07ac0346cacb99bbcc2e05d47b57ac8ccd6
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98493460"
---
# <span data-ttu-id="66bb9-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66bb9-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="66bb9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="66bb9-102">SYNOPSIS</span></span>
<span data-ttu-id="66bb9-103">특정 범위에서 특정 역할에 할당된 지정된 보안 주체에 대한 역할 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="66bb9-104">구문</span><span class="sxs-lookup"><span data-stu-id="66bb9-104">SYNTAX</span></span>

### <span data-ttu-id="66bb9-105">DefinitionNameSignInName(기본값)</span><span class="sxs-lookup"><span data-stu-id="66bb9-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="66bb9-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="66bb9-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="66bb9-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="66bb9-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="66bb9-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="66bb9-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="66bb9-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="66bb9-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="66bb9-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="66bb9-113">설명</span><span class="sxs-lookup"><span data-stu-id="66bb9-113">DESCRIPTION</span></span>
<span data-ttu-id="66bb9-114">cmdlet을 사용하여 주어진 범위 및 주어진 역할의 모든 보안 주체에 `Remove-AzKeyVaultRoleAssignment` 대한 액세스를 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="66bb9-115">할당의 개체입니다. 예: 보안 주체는 반드시 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="66bb9-116">보안 주체는 사용자(SignInName 또는 ObjectId 매개 변수를 사용하여 사용자 식별), 보안 그룹(ObjectId 매개 변수를 사용하여 그룹 식별) 또는 서비스 주체(ApplicationId 또는 ObjectId 매개 변수를 사용하여 ServicePrincipal 식별)일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="66bb9-117">보안 주체에 할당된 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="66bb9-118">예제</span><span class="sxs-lookup"><span data-stu-id="66bb9-118">EXAMPLES</span></span>

### <span data-ttu-id="66bb9-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="66bb9-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="66bb9-120">이 예제에서는 "/keys" 범위에서 ""의 "관리되는 HSM 정책 user1@microsoft.com 관리자" 역할을 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="66bb9-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="66bb9-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="66bb9-122">이 예제에서는 모든 범위에서 user1@microsoft.com ""의 모든 역할을 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="66bb9-123">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="66bb9-123">PARAMETERS</span></span>

### <span data-ttu-id="66bb9-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="66bb9-124">-ApplicationId</span></span>
<span data-ttu-id="66bb9-125">앱 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-125">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameApplicationId, DefinitionIdApplicationId
Aliases: SPN, ServicePrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="66bb9-126">-DefaultProfile</span></span>
<span data-ttu-id="66bb9-127">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="66bb9-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="66bb9-128">-HsmName</span></span>
<span data-ttu-id="66bb9-129">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-129">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId, DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName, RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="66bb9-130">-InputObject</span></span>
<span data-ttu-id="66bb9-131">역할 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-131">Role assignment object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment
Parameter Sets: InputObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="66bb9-132">-ObjectId</span></span>
<span data-ttu-id="66bb9-133">사용자 또는 그룹 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-133">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameObjectId, DefinitionIdObjectId
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="66bb9-134">-PassThru</span></span>
<span data-ttu-id="66bb9-135">HSM이 복원되면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="66bb9-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="66bb9-136">-RoleAssignmentName</span></span>
<span data-ttu-id="66bb9-137">역할 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-137">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="66bb9-138">-RoleDefinitionId</span></span>
<span data-ttu-id="66bb9-139">보안 주체가 할당된 역할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-139">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionIdApplicationId, DefinitionIdObjectId, DefinitionIdSignInName
Aliases: RoleId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="66bb9-140">-RoleDefinitionName</span></span>
<span data-ttu-id="66bb9-141">보안 주체에 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-141">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionNameApplicationId, DefinitionNameObjectId
Aliases: RoleName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="66bb9-142">-Scope</span></span>
<span data-ttu-id="66bb9-143">역할 할당 또는 정의가 적용되는 범위입니다(예: '/' 또는 '/keys' 또는 '/keys/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="66bb9-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="66bb9-144">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="66bb9-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="66bb9-145">-SignInName</span></span>
<span data-ttu-id="66bb9-146">사용자 SignInName입니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-146">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: DefinitionNameSignInName, DefinitionIdSignInName
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="66bb9-147">-Confirm</span><span class="sxs-lookup"><span data-stu-id="66bb9-147">-Confirm</span></span>
<span data-ttu-id="66bb9-148">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="66bb9-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="66bb9-149">-WhatIf</span></span>
<span data-ttu-id="66bb9-150">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="66bb9-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="66bb9-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="66bb9-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="66bb9-152">CommonParameters</span></span>
<span data-ttu-id="66bb9-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="66bb9-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="66bb9-154">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="66bb9-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="66bb9-155">입력</span><span class="sxs-lookup"><span data-stu-id="66bb9-155">INPUTS</span></span>

### <span data-ttu-id="66bb9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66bb9-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="66bb9-157">출력</span><span class="sxs-lookup"><span data-stu-id="66bb9-157">OUTPUTS</span></span>

### <span data-ttu-id="66bb9-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="66bb9-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="66bb9-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="66bb9-159">NOTES</span></span>

## <span data-ttu-id="66bb9-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="66bb9-160">RELATED LINKS</span></span>
