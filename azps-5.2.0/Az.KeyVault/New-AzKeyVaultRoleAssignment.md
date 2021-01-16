---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/new-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/New-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: ee90ab1b4ba22f1a5c40427f7fc435c75cef992d
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336974"
---
# <span data-ttu-id="c4046-101">New-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c4046-101">New-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c4046-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c4046-102">SYNOPSIS</span></span>
<span data-ttu-id="c4046-103">지정된 범위에서 지정된 보안 주체에 지정된 RBAC 역할을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-103">Assigns the specified RBAC role to the specified principal, at the specified scope.</span></span>

## <span data-ttu-id="c4046-104">구문</span><span class="sxs-lookup"><span data-stu-id="c4046-104">SYNTAX</span></span>

### <span data-ttu-id="c4046-105">DefinitionNameSignInName(기본값)</span><span class="sxs-lookup"><span data-stu-id="c4046-105">DefinitionNameSignInName (Default)</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4046-106">DefinitionNameApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4046-106">DefinitionNameApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4046-107">DefinitionNameObjectId</span><span class="sxs-lookup"><span data-stu-id="c4046-107">DefinitionNameObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionName <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4046-108">DefinitionIdApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4046-108">DefinitionIdApplicationId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ApplicationId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4046-109">DefinitionIdObjectId</span><span class="sxs-lookup"><span data-stu-id="c4046-109">DefinitionIdObjectId</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -ObjectId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c4046-110">DefinitionIdSignInName</span><span class="sxs-lookup"><span data-stu-id="c4046-110">DefinitionIdSignInName</span></span>
```
New-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleDefinitionId <String>
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c4046-111">설명</span><span class="sxs-lookup"><span data-stu-id="c4046-111">DESCRIPTION</span></span>
<span data-ttu-id="c4046-112">이 명령을 `New-AzKeyVaultRoleAssignment` 사용하여 액세스 권한을 부여합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-112">Use the `New-AzKeyVaultRoleAssignment` command to grant access.</span></span>
<span data-ttu-id="c4046-113">액세스 권한은 적절한 범위에서 적절한 RBAC 역할을 할당하여 부여됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-113">Access is granted by assigning the appropriate RBAC role to them at the right scope.</span></span>
<span data-ttu-id="c4046-114">과제의 제목을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-114">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="c4046-115">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-115">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="c4046-116">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-116">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="c4046-117">Azure AD 애플리케이션을 지정하기 위해 ApplicationId 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-117">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="c4046-118">할당되는 역할은 RoleDefinitionName pr RoleDefinitionId 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-118">The role that is being assigned must be specified using the RoleDefinitionName pr RoleDefinitionId parameter.</span></span> <span data-ttu-id="c4046-119">액세스 권한이 부여되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-119">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="c4046-120">기본적으로 선택한 구독으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-120">It defaults to the selected subscription.</span></span>

## <span data-ttu-id="c4046-121">예제</span><span class="sxs-lookup"><span data-stu-id="c4046-121">EXAMPLES</span></span>

### <span data-ttu-id="c4046-122">예제 1</span><span class="sxs-lookup"><span data-stu-id="c4046-122">Example 1</span></span>
```powershell
PS C:\> New-AzKeyVaultRoleAssignment -HsmName myHsm -RoleDefinitionName "Managed HSM Policy Administrator" -SignInName user1@microsoft.com

RoleDefinitionName               DisplayName                    ObjectType Scope
------------------               -----------                    ---------- -----
Managed HSM Policy Administrator User 1 (user1@microsoft.com)   User       /
```

<span data-ttu-id="c4046-123">이 예제에서는 최상위 범위에서 "Managed HSM Policy Administrator" 역할을 사용자 user1@microsoft.com "에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-123">This example assigns role "Managed HSM Policy Administrator" to user "user1@microsoft.com" at top scope.</span></span>

## <span data-ttu-id="c4046-124">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c4046-124">PARAMETERS</span></span>

### <span data-ttu-id="c4046-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="c4046-125">-ApplicationId</span></span>
<span data-ttu-id="c4046-126">앱 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-126">The app SPN.</span></span>

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

### <span data-ttu-id="c4046-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c4046-127">-DefaultProfile</span></span>
<span data-ttu-id="c4046-128">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c4046-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="c4046-129">-HsmName</span></span>
<span data-ttu-id="c4046-130">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="c4046-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c4046-131">-ObjectId</span></span>
<span data-ttu-id="c4046-132">사용자 또는 그룹 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-132">The user or group object id.</span></span>

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

### <span data-ttu-id="c4046-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c4046-133">-RoleDefinitionId</span></span>
<span data-ttu-id="c4046-134">보안 주체가 할당된 역할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-134">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="c4046-135">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c4046-135">-RoleDefinitionName</span></span>
<span data-ttu-id="c4046-136">보안 주체에 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-136">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="c4046-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="c4046-137">-Scope</span></span>
<span data-ttu-id="c4046-138">역할 할당 또는 정의가 적용되는 범위입니다(예: '/' 또는 '/keys' 또는 '/keys/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="c4046-138">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="c4046-139">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-139">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="c4046-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="c4046-140">-SignInName</span></span>
<span data-ttu-id="c4046-141">사용자 SignInName입니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-141">The user SignInName.</span></span>

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

### <span data-ttu-id="c4046-142">-Confirm</span><span class="sxs-lookup"><span data-stu-id="c4046-142">-Confirm</span></span>
<span data-ttu-id="c4046-143">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c4046-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c4046-144">-WhatIf</span></span>
<span data-ttu-id="c4046-145">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="c4046-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c4046-146">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c4046-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c4046-147">CommonParameters</span></span>
<span data-ttu-id="c4046-148">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c4046-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c4046-149">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="c4046-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c4046-150">입력</span><span class="sxs-lookup"><span data-stu-id="c4046-150">INPUTS</span></span>

### <span data-ttu-id="c4046-151">없음</span><span class="sxs-lookup"><span data-stu-id="c4046-151">None</span></span>

## <span data-ttu-id="c4046-152">출력</span><span class="sxs-lookup"><span data-stu-id="c4046-152">OUTPUTS</span></span>

### <span data-ttu-id="c4046-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c4046-153">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="c4046-154">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c4046-154">NOTES</span></span>

## <span data-ttu-id="c4046-155">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c4046-155">RELATED LINKS</span></span>
