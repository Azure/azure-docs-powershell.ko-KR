---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/get-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Get-AzSynapseRoleAssignment.md
ms.openlocfilehash: bf96dc0818b978c6c759d363c9d3e2637f27b704
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94309409"
---
# <span data-ttu-id="09d64-101">Get-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="09d64-101">Get-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="09d64-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="09d64-102">SYNOPSIS</span></span>
<span data-ttu-id="09d64-103">Synapse Analytics 역할 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-103">Gets a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="09d64-104">구문과</span><span class="sxs-lookup"><span data-stu-id="09d64-104">SYNTAX</span></span>

### <span data-ttu-id="09d64-105">GetByWorkspaceNameAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="09d64-105">GetByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-SignInName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-106">GetByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-106">GetByWorkspaceNameAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>] [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-107">GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> [-ObjectId <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-108">GetByWorkspaceNameAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-109">GetByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceName <String> [-RoleDefinitionName <String>]
 [-ServicePrincipalName <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-110">GetByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-110">GetByWorkspaceObjectAndNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -SignInName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-111">GetByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-111">GetByWorkspaceObjectAndIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-112">GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 [-ObjectId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-113">GetByWorkspaceObjectAndAssignmentIdParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="09d64-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="09d64-114">GetByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Get-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> [-RoleDefinitionName <String>]
 -ServicePrincipalName <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="09d64-115">설명은</span><span class="sxs-lookup"><span data-stu-id="09d64-115">DESCRIPTION</span></span>
<span data-ttu-id="09d64-116">**AzSynapseRoleAssignment** Cmdlet은 Azure Synapse Analytics 역할 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-116">The **Get-AzSynapseRoleAssignment** cmdlet gets a Azure Synapse Analytics Role Assignment.</span></span>
<span data-ttu-id="09d64-117">역할 정의 또는 사용자 계정 이름을 지정 하지 않으면이 cmdlet은 모든 역할 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-117">If you do not specify a role definition or a user principal name, this cmdlet gets all role assignment.</span></span>

## <span data-ttu-id="09d64-118">예제의</span><span class="sxs-lookup"><span data-stu-id="09d64-118">EXAMPLES</span></span>

### <span data-ttu-id="09d64-119">예제 1</span><span class="sxs-lookup"><span data-stu-id="09d64-119">Example 1</span></span>
```powershell
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace
```

<span data-ttu-id="09d64-120">이 명령은 모든 역할 과제를 작업 영역 아래에 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-120">This command gets all role assignments under a workspace.</span></span>

### <span data-ttu-id="09d64-121">예제 2</span><span class="sxs-lookup"><span data-stu-id="09d64-121">Example 2</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole
```

<span data-ttu-id="09d64-122">이 명령은 role name ContosoRole를 사용 하 여 작업 영역 ContosoWorkspace에서 모든 역할 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-122">This command gets all role assignments under workspace ContosoWorkspace with role name ContosoRole.</span></span>

### <span data-ttu-id="09d64-123">예제 3</span><span class="sxs-lookup"><span data-stu-id="09d64-123">Example 3</span></span>
```powershells
PS C:\> Get-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="09d64-124">이 명령은 역할 이름 ContosoRole 및 upn (사용자 이름)을 사용 하 여 작업 영역 ContosoWorkspace에 역할 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-124">This command gets a role assignment under workspace ContosoWorkspace with role name ContosoRole and user principal name ContosoName.</span></span>

### <span data-ttu-id="09d64-125">예제 4</span><span class="sxs-lookup"><span data-stu-id="09d64-125">Example 4</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Get-AzSynapseRoleAssignment
```

<span data-ttu-id="09d64-126">이 명령은 파이프라인을 통해 작업 영역 아래에 있는 모든 역할 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-126">This command gets all role assignments under a workspace through pipeline.</span></span>

## <span data-ttu-id="09d64-127">변수</span><span class="sxs-lookup"><span data-stu-id="09d64-127">PARAMETERS</span></span>

### <span data-ttu-id="09d64-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="09d64-128">-DefaultProfile</span></span>
<span data-ttu-id="09d64-129">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-129">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="09d64-130">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="09d64-130">-ObjectId</span></span>
<span data-ttu-id="09d64-131">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-131">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-132">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="09d64-132">-RoleAssignmentId</span></span>
<span data-ttu-id="09d64-133">역할 할당의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-133">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-134">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="09d64-134">-RoleDefinitionId</span></span>
<span data-ttu-id="09d64-135">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-135">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-136">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="09d64-136">-RoleDefinitionName</span></span>
<span data-ttu-id="09d64-137">주도자에 게 지정 된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-137">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet, GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-138">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="09d64-138">-ServicePrincipalName</span></span>
<span data-ttu-id="09d64-139">서비스 사용자의 ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="09d64-139">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-140">-SignInName</span><span class="sxs-lookup"><span data-stu-id="09d64-140">-SignInName</span></span>
<span data-ttu-id="09d64-141">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-141">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-142">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="09d64-142">-WorkspaceName</span></span>
<span data-ttu-id="09d64-143">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-143">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByWorkspaceNameAndNameParameterSet, GetByWorkspaceNameAndIdParameterSet, GetByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceNameAndAssignmentIdParameterSet, GetByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-144">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="09d64-144">-WorkspaceObject</span></span>
<span data-ttu-id="09d64-145">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-145">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: GetByWorkspaceObjectAndNameParameterSet, GetByWorkspaceObjectAndIdParameterSet, GetByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, GetByWorkspaceObjectAndAssignmentIdParameterSet, GetByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="09d64-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="09d64-146">CommonParameters</span></span>
<span data-ttu-id="09d64-147">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="09d64-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="09d64-148">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="09d64-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="09d64-149">입력</span><span class="sxs-lookup"><span data-stu-id="09d64-149">INPUTS</span></span>

### <span data-ttu-id="09d64-150">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="09d64-150">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="09d64-151">출력</span><span class="sxs-lookup"><span data-stu-id="09d64-151">OUTPUTS</span></span>

### <span data-ttu-id="09d64-152">Synapse. PSRoleAssignmentDetails/.</span><span class="sxs-lookup"><span data-stu-id="09d64-152">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="09d64-153">상속자</span><span class="sxs-lookup"><span data-stu-id="09d64-153">NOTES</span></span>

## <span data-ttu-id="09d64-154">관련 링크</span><span class="sxs-lookup"><span data-stu-id="09d64-154">RELATED LINKS</span></span>
