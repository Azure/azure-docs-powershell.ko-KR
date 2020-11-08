---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/en-us/powershell/module/az.keyvault/get-azmanagedhsmroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzManagedHsmRoleAssignment.md
ms.openlocfilehash: 20e80617d47cd0a1f0ffb5cdb80d836656cd9abd
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215306"
---
# <span data-ttu-id="f3fe2-101">Get-AzManagedHsmRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f3fe2-101">Get-AzManagedHsmRoleAssignment</span></span>

## <span data-ttu-id="f3fe2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3fe2-102">SYNOPSIS</span></span>
<span data-ttu-id="f3fe2-103">관리 되는 HSM의 역할 할당을 가져오거나 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="f3fe2-104">해당 매개 변수를 사용 하 여 특정 사용자 또는 역할 정의에 대 한 과제를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="f3fe2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="f3fe2-105">SYNTAX</span></span>

### <span data-ttu-id="f3fe2-106">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f3fe2-106">List (Default)</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f3fe2-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="f3fe2-107">GetByName</span></span>
```
Get-AzManagedHsmRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f3fe2-108">설명은</span><span class="sxs-lookup"><span data-stu-id="f3fe2-108">DESCRIPTION</span></span>
<span data-ttu-id="f3fe2-109">명령을 사용 `Get-AzManagedHsmRoleAssignment` 하 여 범위에 적용 되는 모든 역할 과제를 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-109">Use the `Get-AzManagedHsmRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="f3fe2-110">매개 변수 없이이 명령은 관리 되는 HSM에서 생성 된 모든 역할 과제를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="f3fe2-111">이 목록은 주도자, 역할 및 범위에 대 한 필터링 매개 변수를 사용 하 여 필터링 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="f3fe2-112">과제의 주제를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="f3fe2-113">사용자를 지정 하려면 SignInName 또는 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="f3fe2-114">보안 그룹을 지정 하려면 Azure AD ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="f3fe2-115">Azure AD 응용 프로그램을 지정 하려면 ApplicationId 또는 ObjectId 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="f3fe2-116">지정 되는 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용 하 여 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="f3fe2-117">액세스가 허용 되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="f3fe2-118">기본값은 "/"입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-118">It defaults to "/".</span></span>

## <span data-ttu-id="f3fe2-119">예제의</span><span class="sxs-lookup"><span data-stu-id="f3fe2-119">EXAMPLES</span></span>

### <span data-ttu-id="f3fe2-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="f3fe2-120">Example 1</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="f3fe2-121">이 예제에서는 모든 범위에서 "myHsm"의 모든 역할 지정을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="f3fe2-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="f3fe2-122">Example 2</span></span>
```powershell
PS C:\> Get-AzManagedHsmRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="f3fe2-123">이 예제에서는 "/keys" 범위에서 "myHsm"의 모든 역할 지정을 나열 하 고 사용자 로그인 이름으로 결과를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="f3fe2-124">변수</span><span class="sxs-lookup"><span data-stu-id="f3fe2-124">PARAMETERS</span></span>

### <span data-ttu-id="f3fe2-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f3fe2-125">-ApplicationId</span></span>
<span data-ttu-id="f3fe2-126">앱 SPN.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-126">The app SPN.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: SPN, ServicePrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3fe2-127">-DefaultProfile</span></span>
<span data-ttu-id="f3fe2-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3fe2-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="f3fe2-129">-HsmName</span></span>
<span data-ttu-id="f3fe2-130">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="f3fe2-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f3fe2-131">-ObjectId</span></span>
<span data-ttu-id="f3fe2-132">사용자 또는 그룹 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-132">The user or group object id.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="f3fe2-133">-RoleAssignmentName</span></span>
<span data-ttu-id="f3fe2-134">역할 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-134">Name of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f3fe2-135">-RoleDefinitionId</span></span>
<span data-ttu-id="f3fe2-136">주도자가 지정 된 역할 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-136">Role Id the principal is assigned to.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f3fe2-137">-RoleDefinitionName</span></span>
<span data-ttu-id="f3fe2-138">사용자에 게 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-138">Name of the RBAC role to assign the principal with.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: RoleName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-139">-범위</span><span class="sxs-lookup"><span data-stu-id="f3fe2-139">-Scope</span></span>
<span data-ttu-id="f3fe2-140">역할 할당 또는 정의가 적용 되는 범위 (예: '/' 또는 '/keys ' 또는 '/keys/{keyName} ')입니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="f3fe2-141">생략 하면 '/'가 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="f3fe2-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f3fe2-142">-SignInName</span></span>
<span data-ttu-id="f3fe2-143">사용자 SignInName.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-143">The user SignInName.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3fe2-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3fe2-144">CommonParameters</span></span>
<span data-ttu-id="f3fe2-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3fe2-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f3fe2-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3fe2-147">입력</span><span class="sxs-lookup"><span data-stu-id="f3fe2-147">INPUTS</span></span>

### <span data-ttu-id="f3fe2-148">않아야</span><span class="sxs-lookup"><span data-stu-id="f3fe2-148">None</span></span>

## <span data-ttu-id="f3fe2-149">출력</span><span class="sxs-lookup"><span data-stu-id="f3fe2-149">OUTPUTS</span></span>

### <span data-ttu-id="f3fe2-150">Microsoft. KeyVault. PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f3fe2-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="f3fe2-151">상속자</span><span class="sxs-lookup"><span data-stu-id="f3fe2-151">NOTES</span></span>

## <span data-ttu-id="f3fe2-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f3fe2-152">RELATED LINKS</span></span>
