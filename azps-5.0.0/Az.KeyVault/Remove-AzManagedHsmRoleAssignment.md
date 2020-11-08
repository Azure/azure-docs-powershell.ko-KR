---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/remove-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Remove-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 038049af40d84b678da12a57918328b3b0725127
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215288"
---
# <span data-ttu-id="b7e9f-101">Remove-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b7e9f-101">Remove-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="b7e9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b7e9f-102">SYNOPSIS</span></span>
<span data-ttu-id="b7e9f-103">특정 범위에서 특정 역할에 할당 된 지정 된 주체에 대 한 역할 할당을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-103">Removes a role assignment to the specified principal who is assigned to a particular role at a particular scope.</span></span>

## <span data-ttu-id="b7e9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b7e9f-104">SYNTAX</span></span>

### <span data-ttu-id="b7e9f-105">DefinitionNameSignInName (기본값)</span><span class="sxs-lookup"><span data-stu-id="b7e9f-105">DefinitionNameSignInName (Default)</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-106">DefinitionNameApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-107">DefinitionNameObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-108">DefinitionIdApplicationId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-109">DefinitionIdObjectId</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="b7e9f-110">DefinitionIdSignInName</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-111">RemoveByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="b7e9f-111">RemoveByNameParameterSet</span></span>
```
Remove-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-PassThru]
 -RoleAssignmentName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="b7e9f-112">InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e9f-112">InputObject</span></span>
```
Remove-AzManagedHsmRoleAssignment [-Scope <String>] [-PassThru] -InputObject <PSKeyVaultRoleAssignment>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b7e9f-113">설명은</span><span class="sxs-lookup"><span data-stu-id="b7e9f-113">DESCRIPTION</span></span>
<span data-ttu-id="b7e9f-114">Cmdlet을 사용 `Remove-AzManagedHsmRoleAssignment` 하 여 지정 된 범위 및 지정 된 역할에 대 한 모든 주체에 대 한 액세스 권한을 취소 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-114">Use the `Remove-AzManagedHsmRoleAssignment` cmdlet to revoke access to any principal at given scope and given role.</span></span> <span data-ttu-id="b7e9f-115">과제의 개체 즉, 주체를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-115">The object of the assignment i.e. the principal MUST be specified.</span></span> <span data-ttu-id="b7e9f-116">Principal은 사용자 (SignInName 또는 ObjectId 매개 변수를 사용 하 여 사용자를 식별), 보안 그룹 (그룹을 식별 하는 데 ObjectId 매개 변수 사용) 또는 서비스 주체 (ApplicationId 또는 ObjectId 매개 변수를 사용 하 여 ServicePrincipal 식별) 일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-116">The principal can be a user (use SignInName or ObjectId parameters to identify a user), security group (use ObjectId parameter to identify a group) or service principal (use ApplicationId or ObjectId parameters to identify a ServicePrincipal.</span></span> <span data-ttu-id="b7e9f-117">사용자가 할당 하는 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용 하 여 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-117">The role that the principal is assigned to MUST be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>

## <span data-ttu-id="b7e9f-118">예제의</span><span class="sxs-lookup"><span data-stu-id="b7e9f-118">EXAMPLES</span></span>

### <span data-ttu-id="b7e9f-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="b7e9f-119">Example 1</span></span>
```powershell
PS C:\> Remove-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com -Scope "/keys"
```

<span data-ttu-id="b7e9f-120">이 예제에서는 "/keys" 범위에서 "관리 되는 HSM 정책 관리자" 역할을 해지 user1@microsoft.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-120">This example revokes "Managed HSM Policy Administrator" role of "user1@microsoft.com" at "/keys" scope.</span></span>

### <span data-ttu-id="b7e9f-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="b7e9f-121">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com | Remove-AzManagedHsmRoleAssignment
```

<span data-ttu-id="b7e9f-122">이 예제에서는 모든 범위에서 ""의 모든 역할을 해지 user1@microsoft.com 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-122">This example revokes all roles of "user1@microsoft.com" at all scopes.</span></span>

## <span data-ttu-id="b7e9f-123">변수</span><span class="sxs-lookup"><span data-stu-id="b7e9f-123">PARAMETERS</span></span>

### <span data-ttu-id="b7e9f-124">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-124">-ApplicationId</span></span>
<span data-ttu-id="b7e9f-125">앱 SPN.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-125">The app SPN.</span></span>

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

### <span data-ttu-id="b7e9f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b7e9f-126">-DefaultProfile</span></span>
<span data-ttu-id="b7e9f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b7e9f-128">-HsmName</span><span class="sxs-lookup"><span data-stu-id="b7e9f-128">-HsmName</span></span>
<span data-ttu-id="b7e9f-129">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-129">Name of the HSM.</span></span>

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

### <span data-ttu-id="b7e9f-130">-InputObject</span><span class="sxs-lookup"><span data-stu-id="b7e9f-130">-InputObject</span></span>
<span data-ttu-id="b7e9f-131">역할 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-131">Role assignment object.</span></span>

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

### <span data-ttu-id="b7e9f-132">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-132">-ObjectId</span></span>
<span data-ttu-id="b7e9f-133">사용자 또는 그룹 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-133">The user or group object id.</span></span>

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

### <span data-ttu-id="b7e9f-134">-PassThru</span><span class="sxs-lookup"><span data-stu-id="b7e9f-134">-PassThru</span></span>
<span data-ttu-id="b7e9f-135">HSM이 복원 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-135">Return true when the HSM is restored.</span></span>

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

### <span data-ttu-id="b7e9f-136">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="b7e9f-136">-RoleAssignmentName</span></span>
<span data-ttu-id="b7e9f-137">역할 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-137">Name of the role assignment.</span></span>

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

### <span data-ttu-id="b7e9f-138">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="b7e9f-138">-RoleDefinitionId</span></span>
<span data-ttu-id="b7e9f-139">주도자가 지정 된 역할 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-139">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="b7e9f-140">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="b7e9f-140">-RoleDefinitionName</span></span>
<span data-ttu-id="b7e9f-141">사용자에 게 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-141">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="b7e9f-142">-범위</span><span class="sxs-lookup"><span data-stu-id="b7e9f-142">-Scope</span></span>
<span data-ttu-id="b7e9f-143">역할 할당 또는 정의가 적용 되는 범위 (예: '/' 또는 '/keys ' 또는 '/keys/{keyName} ')입니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-143">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="b7e9f-144">생략 하면 '/'가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-144">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="b7e9f-145">-SignInName</span><span class="sxs-lookup"><span data-stu-id="b7e9f-145">-SignInName</span></span>
<span data-ttu-id="b7e9f-146">사용자 SignInName.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-146">The user SignInName.</span></span>

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

### <span data-ttu-id="b7e9f-147">-확인</span><span class="sxs-lookup"><span data-stu-id="b7e9f-147">-Confirm</span></span>
<span data-ttu-id="b7e9f-148">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-148">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b7e9f-149">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b7e9f-149">-WhatIf</span></span>
<span data-ttu-id="b7e9f-150">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-150">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="b7e9f-151">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-151">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b7e9f-152">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b7e9f-152">CommonParameters</span></span>
<span data-ttu-id="b7e9f-153">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-153">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b7e9f-154">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b7e9f-154">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b7e9f-155">입력</span><span class="sxs-lookup"><span data-stu-id="b7e9f-155">INPUTS</span></span>

### <span data-ttu-id="b7e9f-156">Microsoft. KeyVault. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b7e9f-156">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b7e9f-157">출력</span><span class="sxs-lookup"><span data-stu-id="b7e9f-157">OUTPUTS</span></span>

### <span data-ttu-id="b7e9f-158">Microsoft. KeyVault. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="b7e9f-158">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="b7e9f-159">상속자</span><span class="sxs-lookup"><span data-stu-id="b7e9f-159">NOTES</span></span>

## <span data-ttu-id="b7e9f-160">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b7e9f-160">RELATED LINKS</span></span>
