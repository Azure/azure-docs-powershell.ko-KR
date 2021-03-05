---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ae55bf782f627c17cd73cbb075fd9f0d36ae6081
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001275"
---
# <span data-ttu-id="97e91-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="97e91-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="97e91-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="97e91-102">SYNOPSIS</span></span>
<span data-ttu-id="97e91-103">지정된 범위의 지정된 주체에 지정된 RBAC 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="97e91-104">구문</span><span class="sxs-lookup"><span data-stu-id="97e91-104">SYNTAX</span></span>

### <span data-ttu-id="97e91-105">DefinitionNameSignInName(기본값)</span><span class="sxs-lookup"><span data-stu-id="97e91-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e91-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="97e91-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e91-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="97e91-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e91-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="97e91-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e91-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="97e91-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="97e91-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="97e91-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="97e91-111">설명</span><span class="sxs-lookup"><span data-stu-id="97e91-111">DESCRIPTION</span></span>
<span data-ttu-id="97e91-112">명령을 `New-AzKeyVaultRoleAssignment` 사용하여 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="97e91-113">적절한 범위에서 적절한 RBAC 역할을 할당하여 액세스가 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="97e91-114">과제의 제목을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="97e91-115">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="97e91-116">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="97e91-117">Azure AD 애플리케이션을 지정하기 위해 ApplicationId 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="97e91-118">할당되는 역할은 RoleDefinitionName pr RoleDefinitionId 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="97e91-119">액세스가 부여되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="97e91-120">기본값은 선택한 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="97e91-121">예제</span><span class="sxs-lookup"><span data-stu-id="97e91-121">EXAMPLES</span></span>

### <span data-ttu-id="97e91-122">예제 1</span><span class="sxs-lookup"><span data-stu-id="97e91-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="97e91-123">이 예제에서는 "관리되는 HSM 정책 관리자"를 사용자 "에 최상위 범위에 user1@microsoft.com 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="97e91-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="97e91-124">PARAMETERS</span></span>

### <span data-ttu-id="97e91-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="97e91-125">-ApplicationId</span></span>
<span data-ttu-id="97e91-126">앱 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-126">The app SPN.</span></span>

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

### <span data-ttu-id="97e91-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="97e91-127">-DefaultProfile</span></span>
<span data-ttu-id="97e91-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="97e91-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="97e91-129">-HsmName</span></span>
<span data-ttu-id="97e91-130">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-130">Name of the HSM.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="97e91-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="97e91-131">-ObjectId</span></span>
<span data-ttu-id="97e91-132">사용자 또는 그룹 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-132">The user or group object id.</span></span>

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

### <span data-ttu-id="97e91-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="97e91-133">-RoleDefinitionId</span></span>
<span data-ttu-id="97e91-134">주체가 할당된 역할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="97e91-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="97e91-135">-RoleDefinitionName</span></span>
<span data-ttu-id="97e91-136">주체에 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="97e91-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="97e91-137">-Scope</span></span>
<span data-ttu-id="97e91-138">역할 할당 또는 정의가 적용되는 범위(예: '/' 또는 '/key' 또는 '/key/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="97e91-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="97e91-139">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="97e91-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="97e91-140">-SignInName</span></span>
<span data-ttu-id="97e91-141">사용자 SignInName입니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-141">The user SignInName.</span></span>

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

### <span data-ttu-id="97e91-142">-확인</span><span class="sxs-lookup"><span data-stu-id="97e91-142">-Confirm</span></span>
<span data-ttu-id="97e91-143">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="97e91-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="97e91-144">-WhatIf</span></span>
<span data-ttu-id="97e91-145">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="97e91-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="97e91-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="97e91-147">CommonParameters</span></span>
<span data-ttu-id="97e91-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="97e91-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="97e91-149">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="97e91-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="97e91-150">입력</span><span class="sxs-lookup"><span data-stu-id="97e91-150">INPUTS</span></span>

### <span data-ttu-id="97e91-151">없음</span><span class="sxs-lookup"><span data-stu-id="97e91-151">None</span></span>

## <span data-ttu-id="97e91-152">출력</span><span class="sxs-lookup"><span data-stu-id="97e91-152">OUTPUTS</span></span>

### <span data-ttu-id="97e91-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="97e91-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="97e91-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="97e91-154">NOTES</span></span>

## <span data-ttu-id="97e91-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="97e91-155">RELATED LINKS</span></span>
