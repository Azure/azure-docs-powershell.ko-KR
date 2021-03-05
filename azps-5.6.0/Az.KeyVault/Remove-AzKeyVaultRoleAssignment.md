---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/remove-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: f93adbf99667c2854557e71af8091012ea82bb74
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102015195"
---
# <span data-ttu-id="d76ab-101">Remove-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d76ab-101">Remove-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="d76ab-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d76ab-102">SYNOPSIS</span></span>
<span data-ttu-id="d76ab-103">특정 범위에서 특정 역할에 할당된 지정된 주체에 대한 역할 할당을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="d76ab-104">구문</span><span class="sxs-lookup"><span data-stu-id="d76ab-104">SYNTAX</span></span>

### <span data-ttu-id="d76ab-105">DefinitionNameSignInName(기본값)</span><span class="sxs-lookup"><span data-stu-id="d76ab-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="d76ab-106">DefinitionNameApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="d76ab-107">DefinitionNameObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="d76ab-108">DefinitionIdApplicationId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="d76ab-109">DefinitionIdObjectId</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="d76ab-110">DefinitionIdSignInName</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d76ab-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d76ab-111">RemoveByNameParameterSet</span></span>
```
Remove-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d76ab-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="d76ab-112">InputObject</span></span>
```
Remove-AzKeyVaultRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d76ab-113">설명</span><span class="sxs-lookup"><span data-stu-id="d76ab-113">DESCRIPTION</span></span>
<span data-ttu-id="d76ab-114">cmdlet을 사용하여 주어진 범위 및 주어진 역할의 모든 주체에 대한 액세스를 `Remove-AzKeyVaultRoleAssignment` 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-114">Use the `Remove-AzKeyVaultRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="d76ab-115">할당의 개체(예: 주체)를 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="d76ab-116">주체는 사용자일 수 있습니다(SignInName 또는 ObjectId 매개 변수를 사용하여 사용자를 식별), 보안 그룹(ObjectId 매개 변수를 사용하여 그룹을 식별) 또는 서비스 주체(ApplicationId 또는 ObjectId 매개 변수를 사용하여 ServicePrincipal을 식별합니다).</span><span class="sxs-lookup"><span data-stu-id="d76ab-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="d76ab-117">주체가 할당된 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="d76ab-118">예제</span><span class="sxs-lookup"><span data-stu-id="d76ab-118">EXAMPLES</span></span>

### <span data-ttu-id="d76ab-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="d76ab-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="d76ab-120">이 예제에서는 "/keys" 범위에서 "관리되는 HSM 정책 관리자" 역할을 user1@microsoft.com 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="d76ab-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="d76ab-121">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzKeyVaultRoleAssignment
```

<span data-ttu-id="d76ab-122">이 예제에서는 모든 범위에서 ""의 모든 역할을 user1@microsoft.com 해지합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="d76ab-123">매개 변수</span><span class="sxs-lookup"><span data-stu-id="d76ab-123">PARAMETERS</span></span>

### <span data-ttu-id="d76ab-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d76ab-124">-ApplicationId</span></span>
<span data-ttu-id="d76ab-125">앱 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-125">The app SPN.</span></span>

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

### <span data-ttu-id="d76ab-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d76ab-126">-DefaultProfile</span></span>
<span data-ttu-id="d76ab-127">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d76ab-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="d76ab-128">-HsmName</span></span>
<span data-ttu-id="d76ab-129">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="d76ab-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d76ab-130">-InputObject</span></span>
<span data-ttu-id="d76ab-131">역할 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-131">Role assignment object.</span></span>

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

### <span data-ttu-id="d76ab-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="d76ab-132">-ObjectId</span></span>
<span data-ttu-id="d76ab-133">사용자 또는 그룹 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-133">The user or group object id.</span></span>

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

### <span data-ttu-id="d76ab-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="d76ab-134">-PassThru</span></span>
<span data-ttu-id="d76ab-135">HSM이 복원되면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="d76ab-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="d76ab-136">-RoleAssignmentName</span></span>
<span data-ttu-id="d76ab-137">역할 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="d76ab-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d76ab-138">-RoleDefinitionId</span></span>
<span data-ttu-id="d76ab-139">주체가 할당된 역할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="d76ab-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="d76ab-140">-RoleDefinitionName</span></span>
<span data-ttu-id="d76ab-141">주체에 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="d76ab-142">-Scope</span><span class="sxs-lookup"><span data-stu-id="d76ab-142">-Scope</span></span>
<span data-ttu-id="d76ab-143">역할 할당 또는 정의가 적용되는 범위(예: '/' 또는 '/key' 또는 '/key/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="d76ab-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="d76ab-144">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="d76ab-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="d76ab-145">-SignInName</span></span>
<span data-ttu-id="d76ab-146">사용자 SignInName입니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-146">The user SignInName.</span></span>

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

### <span data-ttu-id="d76ab-147">-확인</span><span class="sxs-lookup"><span data-stu-id="d76ab-147">-Confirm</span></span>
<span data-ttu-id="d76ab-148">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d76ab-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d76ab-149">-WhatIf</span></span>
<span data-ttu-id="d76ab-150">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d76ab-151">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d76ab-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d76ab-152">CommonParameters</span></span>
<span data-ttu-id="d76ab-153">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="d76ab-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d76ab-154">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="d76ab-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d76ab-155">입력</span><span class="sxs-lookup"><span data-stu-id="d76ab-155">INPUTS</span></span>

### <span data-ttu-id="d76ab-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d76ab-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="d76ab-157">출력</span><span class="sxs-lookup"><span data-stu-id="d76ab-157">OUTPUTS</span></span>

### <span data-ttu-id="d76ab-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="d76ab-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="d76ab-159">참고 사항</span><span class="sxs-lookup"><span data-stu-id="d76ab-159">NOTES</span></span>

## <span data-ttu-id="d76ab-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d76ab-160">RELATED LINKS</span></span>
