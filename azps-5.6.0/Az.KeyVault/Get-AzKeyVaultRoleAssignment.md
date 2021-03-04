---
external help file: Microsoft.Azure.PowerShell.Cmdlets.KeyVault.dll-Help.xml
Module Name: Az.KeyVault
online version: https://docs.microsoft.com/powershell/module/az.keyvault/get-azkeyvaultroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/KeyVault/KeyVault/help/Get-AzKeyVaultRoleAssignment.md
ms.openlocfilehash: 7de4753d47ff2a285da6a9d3d60e0f95fcbf6e92
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001456"
---
# <span data-ttu-id="7b956-101">Get-AzKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b956-101">Get-AzKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="7b956-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7b956-102">SYNOPSIS</span></span>
<span data-ttu-id="7b956-103">관리되는 HSM의 역할 할당을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-103">Get or list role assignments of a managed HSM.</span></span> <span data-ttu-id="7b956-104">각 매개 변수를 사용하여 특정 사용자 또는 역할 정의에 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-104">Use respective parameters to list assignments to a specific user or a role definition.</span></span>

## <span data-ttu-id="7b956-105">구문</span><span class="sxs-lookup"><span data-stu-id="7b956-105">SYNTAX</span></span>

### <span data-ttu-id="7b956-106">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="7b956-106">List (Default)</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] [-RoleDefinitionName <String>]
 [-RoleDefinitionId <String>] [-ObjectId <String>] [-SignInName <String>] [-ApplicationId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7b956-107">GetByName</span><span class="sxs-lookup"><span data-stu-id="7b956-107">GetByName</span></span>
```
Get-AzKeyVaultRoleAssignment [-HsmName] <String> [-Scope <String>] -RoleAssignmentName <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7b956-108">설명</span><span class="sxs-lookup"><span data-stu-id="7b956-108">DESCRIPTION</span></span>
<span data-ttu-id="7b956-109">명령을 사용하여 범위에 효과적인 모든 역할 `Get-AzKeyVaultRoleAssignment` 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-109">Use the `Get-AzKeyVaultRoleAssignment` command to list all role assignments that are effective on a scope.</span></span>
<span data-ttu-id="7b956-110">매개 변수가 없는 경우 이 명령은 관리되는 HSM에서 수행한 모든 역할 할당을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-110">Without any parameters, this command returns all the role assignments made under the managed HSM.</span></span>
<span data-ttu-id="7b956-111">이 목록은 주체, 역할 및 범위에 대한 필터링 매개 변수를 사용하여 필터링할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-111">This list can be filtered using filtering parameters for principal, role and scope.</span></span>
<span data-ttu-id="7b956-112">과제의 제목을 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-112">The subject of the assignment must be specified.</span></span>
<span data-ttu-id="7b956-113">사용자를 지정하기 위해 SignInName 또는 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-113">To specify a user, use SignInName or Azure AD ObjectId parameters.</span></span>
<span data-ttu-id="7b956-114">보안 그룹을 지정하기 위해 Azure AD ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-114">To specify a security group, use Azure AD ObjectId parameter.</span></span>
<span data-ttu-id="7b956-115">Azure AD 애플리케이션을 지정하기 위해 ApplicationId 또는 ObjectId 매개 변수를 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-115">And to specify an Azure AD application, use ApplicationId or ObjectId parameters.</span></span>
<span data-ttu-id="7b956-116">할당되는 역할은 RoleDefinitionName 또는 RoleDefinitionId 매개 변수를 사용하여 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-116">The role that is being assigned must be specified using the RoleDefinitionName or RoleDefinitionId parameter.</span></span>
<span data-ttu-id="7b956-117">액세스가 부여되는 범위를 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-117">The scope at which access is being granted may be specified.</span></span> <span data-ttu-id="7b956-118">기본값은 "/"입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-118">It defaults to "/".</span></span>

## <span data-ttu-id="7b956-119">예제</span><span class="sxs-lookup"><span data-stu-id="7b956-119">EXAMPLES</span></span>

### <span data-ttu-id="7b956-120">예제 1</span><span class="sxs-lookup"><span data-stu-id="7b956-120">Example 1</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Administrator  User 1 (user1@microsoft.com)     User       /
Managed HSM Crypto Auditor User 2 (user2@microsoft.com)     User       /keys
Managed HSM Backup         User 2 (user2@microsoft.com)     User       /
Managed HSM Administrator  User 2 (user2@microsoft.com)     User       /
```

<span data-ttu-id="7b956-121">이 예제에서는 모든 범위에서 "myHsm"의 모든 역할 할당을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-121">This example lists all role assignments of "myHsm" on all the scope.</span></span>

### <span data-ttu-id="7b956-122">예제 2</span><span class="sxs-lookup"><span data-stu-id="7b956-122">Example 2</span></span>
```powershell
PS C:\> Get-AzKeyVaultRoleAssignment -HsmName myHsm -SignInName user1@microsoft.com -Scope "/keys"

RoleDefinitionName         DisplayName                      ObjectType Scope
------------------         -----------                      ---------- -----
Managed HSM Crypto Auditor User 1 (user1@microsoft.com)     User       /keys
Managed HSM Backup         User 1 (user1@microsoft.com)     User       /keys
```

<span data-ttu-id="7b956-123">이 예제에서는 "/keys" 범위에서 "myHsm"의 모든 역할 할당을 나열하고 사용자 로그인 이름으로 결과를 필터합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-123">This example lists all role assignments of "myHsm" on "/keys" scope and filters the result by user sign-in name.</span></span>

## <span data-ttu-id="7b956-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="7b956-124">PARAMETERS</span></span>

### <span data-ttu-id="7b956-125">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7b956-125">-ApplicationId</span></span>
<span data-ttu-id="7b956-126">앱 SPN입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-126">The app SPN.</span></span>

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

### <span data-ttu-id="7b956-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7b956-127">-DefaultProfile</span></span>
<span data-ttu-id="7b956-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="7b956-129">-HsmName</span><span class="sxs-lookup"><span data-stu-id="7b956-129">-HsmName</span></span>
<span data-ttu-id="7b956-130">HSM의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-130">Name of the HSM.</span></span>

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

### <span data-ttu-id="7b956-131">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="7b956-131">-ObjectId</span></span>
<span data-ttu-id="7b956-132">사용자 또는 그룹 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-132">The user or group object id.</span></span>

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

### <span data-ttu-id="7b956-133">-RoleAssignmentName</span><span class="sxs-lookup"><span data-stu-id="7b956-133">-RoleAssignmentName</span></span>
<span data-ttu-id="7b956-134">역할 할당의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-134">Name of the role assignment.</span></span>

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

### <span data-ttu-id="7b956-135">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="7b956-135">-RoleDefinitionId</span></span>
<span data-ttu-id="7b956-136">주체가 할당된 역할 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-136">Role Id the principal is assigned to.</span></span>

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

### <span data-ttu-id="7b956-137">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="7b956-137">-RoleDefinitionName</span></span>
<span data-ttu-id="7b956-138">주체에 할당할 RBAC 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-138">Name of the RBAC role to assign the principal with.</span></span>

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

### <span data-ttu-id="7b956-139">-Scope</span><span class="sxs-lookup"><span data-stu-id="7b956-139">-Scope</span></span>
<span data-ttu-id="7b956-140">역할 할당 또는 정의가 적용되는 범위(예: '/' 또는 '/key' 또는 '/key/{keyName}').</span><span class="sxs-lookup"><span data-stu-id="7b956-140">Scope at which the role assignment or definition applies to, e.g., '/' or '/keys' or '/keys/{keyName}'.</span></span>
<span data-ttu-id="7b956-141">'/'는 생략할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-141">'/' is used when omitted.</span></span>

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

### <span data-ttu-id="7b956-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="7b956-142">-SignInName</span></span>
<span data-ttu-id="7b956-143">사용자 SignInName입니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-143">The user SignInName.</span></span>

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

### <span data-ttu-id="7b956-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7b956-144">CommonParameters</span></span>
<span data-ttu-id="7b956-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7b956-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7b956-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="7b956-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7b956-147">입력</span><span class="sxs-lookup"><span data-stu-id="7b956-147">INPUTS</span></span>

### <span data-ttu-id="7b956-148">없음</span><span class="sxs-lookup"><span data-stu-id="7b956-148">None</span></span>

## <span data-ttu-id="7b956-149">출력</span><span class="sxs-lookup"><span data-stu-id="7b956-149">OUTPUTS</span></span>

### <span data-ttu-id="7b956-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7b956-150">Microsoft.Azure.Commands.KeyVault.Models.PSKeyVaultRoleAssignment</span></span>

## <span data-ttu-id="7b956-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7b956-151">NOTES</span></span>

## <span data-ttu-id="7b956-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7b956-152">RELATED LINKS</span></span>
