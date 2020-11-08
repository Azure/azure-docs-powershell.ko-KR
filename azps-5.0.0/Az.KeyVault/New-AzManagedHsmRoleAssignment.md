---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 3b02bf3471546c9b6bc68d0ded109133341d20bc
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215303"
---
# <span data-ttu-id="c9a1d-101">New-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c9a1d-101">New-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="c9a1d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9a1d-102">SYNOPSIS</span></span>
<span data-ttu-id="c9a1d-103">지정 된 범위에서 지정한 RBAC 역할을 지정 된 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="c9a1d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c9a1d-104">SYNTAX</span></span>

### <span data-ttu-id="c9a1d-105">DefinitionNameSignInName (기본값)</span><span class="sxs-lookup"><span data-stu-id="c9a1d-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1d-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-106">DefinitionNameApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1d-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-107">DefinitionNameObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1d-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-108">DefinitionIdApplicationId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1d-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-109">DefinitionIdObjectId</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c9a1d-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="c9a1d-110">DefinitionIdSignInName</span></span>
```
New-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c9a1d-111">설명은</span><span class="sxs-lookup"><span data-stu-id="c9a1d-111">DESCRIPTION</span></span>
<span data-ttu-id="c9a1d-112">명령을 사용 `New-AzManagedHsmRoleAssignment` 하 여 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-112">Use the `New-AzManagedHsmRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="c9a1d-113">올바른 범위에서 적절 한 RBAC 역할을 할당 하 여 액세스 권한을 부여 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="c9a1d-114">과제의 주제를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="c9a1d-115">사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="c9a1d-116">보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="c9a1d-117">Azure AD 응용 프로그램을 지정 하려면 ApplicationId 또는 ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="c9a1d-118">RoleDefinitionName pr RoleDefinitionId 매개 변수를 사용 하 여 할당 되는 역할을 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="c9a1d-119">액세스가 허용 되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="c9a1d-120">선택한 구독이 기본값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="c9a1d-121">예제의</span><span class="sxs-lookup"><span data-stu-id="c9a1d-121">EXAMPLES</span></span>

### <span data-ttu-id="c9a1d-122">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9a1d-122">Example 1</span></span>
```powershell
PS C:\> New-AzManagedHsmRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="c9a1d-123">이 예제에서는 "관리 되는 HSM 정책 관리자" 역할을 user1@microsoft.com 최상위 범위에서 "" 사용자에 게 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="c9a1d-124">변수</span><span class="sxs-lookup"><span data-stu-id="c9a1d-124">PARAMETERS</span></span>

### <span data-ttu-id="c9a1d-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-125">-ApplicationId</span></span>
<span data-ttu-id="c9a1d-126">앱 SPN.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-126">The app SPN.</span></span>

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

### <span data-ttu-id="c9a1d-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9a1d-127">-DefaultProfile</span></span>
<span data-ttu-id="c9a1d-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9a1d-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="c9a1d-129">-HsmName</span></span>
<span data-ttu-id="c9a1d-130">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="c9a1d-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-131">-ObjectId</span></span>
<span data-ttu-id="c9a1d-132">사용자 또는 그룹 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-132">The user or group object id.</span></span>

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

### <span data-ttu-id="c9a1d-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c9a1d-133">-RoleDefinitionId</span></span>
<span data-ttu-id="c9a1d-134">주도자가 지정 된 역할 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="c9a1d-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c9a1d-135">-RoleDefinitionName</span></span>
<span data-ttu-id="c9a1d-136">사용자에 게 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="c9a1d-137">-범위</span><span class="sxs-lookup"><span data-stu-id="c9a1d-137">-Scope</span></span>
<span data-ttu-id="c9a1d-138">역할 할당 또는 정의가 적용 되는 범위 (예: '/' 또는 '/keys ' 또는 '/keys/{keyName} ')입니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="c9a1d-139">생략 하면 '/'가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="c9a1d-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="c9a1d-140">-SignInName</span></span>
<span data-ttu-id="c9a1d-141">사용자 SignInName.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-141">The user SignInName.</span></span>

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

### <span data-ttu-id="c9a1d-142">-확인</span><span class="sxs-lookup"><span data-stu-id="c9a1d-142">-Confirm</span></span>
<span data-ttu-id="c9a1d-143">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c9a1d-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c9a1d-144">-WhatIf</span></span>
<span data-ttu-id="c9a1d-145">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c9a1d-146">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c9a1d-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9a1d-147">CommonParameters</span></span>
<span data-ttu-id="c9a1d-148">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9a1d-149">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c9a1d-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9a1d-150">입력</span><span class="sxs-lookup"><span data-stu-id="c9a1d-150">INPUTS</span></span>

### <span data-ttu-id="c9a1d-151">않아야</span><span class="sxs-lookup"><span data-stu-id="c9a1d-151">None</span></span>

## <span data-ttu-id="c9a1d-152">출력</span><span class="sxs-lookup"><span data-stu-id="c9a1d-152">OUTPUTS</span></span>

### <span data-ttu-id="c9a1d-153">Microsoft. KeyVault. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c9a1d-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c9a1d-154">상속자</span><span class="sxs-lookup"><span data-stu-id="c9a1d-154">NOTES</span></span>

## <span data-ttu-id="c9a1d-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9a1d-155">RELATED LINKS</span></span>
