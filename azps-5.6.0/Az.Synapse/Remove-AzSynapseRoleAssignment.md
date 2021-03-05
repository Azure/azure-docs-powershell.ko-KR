---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 4fbc25b919b7fbb3caa972f4e64467dee1df7116
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102008240"
---
# <span data-ttu-id="a16bf-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="a16bf-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="a16bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a16bf-102">SYNOPSIS</span></span>
<span data-ttu-id="a16bf-103">Synapse Analytics 역할 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="a16bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="a16bf-104">SYNTAX</span></span>

### <span data-ttu-id="a16bf-105">RemoveByWorkspaceNameAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a16bf-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a16bf-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a16bf-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a16bf-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="a16bf-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="a16bf-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a16bf-115">설명</span><span class="sxs-lookup"><span data-stu-id="a16bf-115">DESCRIPTION</span></span>
<span data-ttu-id="a16bf-116">**Remove-AzSynapseRoleAssignment** cmdlet은 Azure Synapse Analytics 역할 할당을 영구적으로 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="a16bf-117">예제</span><span class="sxs-lookup"><span data-stu-id="a16bf-117">EXAMPLES</span></span>

### <span data-ttu-id="a16bf-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="a16bf-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="a16bf-119">이 명령은 역할 할당 ID를 사용하여 Azure Synapse Analytics 역할 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="a16bf-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="a16bf-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="a16bf-121">이 명령은 역할 이름 및 사용자 주체 이름이 있는 Azure Synapse Analytics 역할 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="a16bf-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="a16bf-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="a16bf-123">이 명령은 파이프라인을 통해 역할 할당 ID가 있는 Azure Synapse Analytics 역할 할당을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="a16bf-124">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a16bf-124">PARAMETERS</span></span>

### <span data-ttu-id="a16bf-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="a16bf-125">-AsJob</span></span>
<span data-ttu-id="a16bf-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="a16bf-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="a16bf-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a16bf-127">-DefaultProfile</span></span>
<span data-ttu-id="a16bf-128">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a16bf-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="a16bf-129">-ObjectId</span></span>
<span data-ttu-id="a16bf-130">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="a16bf-131">-PassThru</span></span>
<span data-ttu-id="a16bf-132">이 Cmdlet은 기본적으로 개체를 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="a16bf-133">이 스위치가 지정되어 있는 경우 성공하면 true를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="a16bf-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="a16bf-134">-RoleAssignmentId</span></span>
<span data-ttu-id="a16bf-135">역할 할당의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-135">The ID of the role assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceObjectAndIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a16bf-136">-RoleDefinitionId</span></span>
<span data-ttu-id="a16bf-137">주체에 할당된 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-137">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="a16bf-138">-RoleDefinitionName</span></span>
<span data-ttu-id="a16bf-139">주체에 할당된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-139">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="a16bf-140">-ServicePrincipalName</span></span>
<span data-ttu-id="a16bf-141">서비스 주체의 ServicePrincipalName입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-141">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndServicePrincipalNameParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="a16bf-142">-SignInName</span></span>
<span data-ttu-id="a16bf-143">사용자의 전자 메일 주소 또는 사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-143">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="a16bf-144">-WorkspaceName</span></span>
<span data-ttu-id="a16bf-145">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-145">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByWorkspaceNameAndNameParameterSet, RemoveByWorkspaceNameAndIdParameterSet, RemoveByWorkspaceNameAndObjectIdParameterSet, RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet, RemoveByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="a16bf-146">-WorkspaceObject</span></span>
<span data-ttu-id="a16bf-147">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-147">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: RemoveByWorkspaceObjectAndIdParameterSet, RemoveByWorkspaceObjectAndNameParameterSet, RemoveByWorkspaceObjectAndObjectIdParameterSet, RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet, RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a16bf-148">-확인</span><span class="sxs-lookup"><span data-stu-id="a16bf-148">-Confirm</span></span>
<span data-ttu-id="a16bf-149">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a16bf-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a16bf-150">-WhatIf</span></span>
<span data-ttu-id="a16bf-151">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a16bf-152">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a16bf-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a16bf-153">CommonParameters</span></span>
<span data-ttu-id="a16bf-154">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a16bf-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a16bf-155">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a16bf-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a16bf-156">입력</span><span class="sxs-lookup"><span data-stu-id="a16bf-156">INPUTS</span></span>

### <span data-ttu-id="a16bf-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="a16bf-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="a16bf-158">출력</span><span class="sxs-lookup"><span data-stu-id="a16bf-158">OUTPUTS</span></span>

### <span data-ttu-id="a16bf-159">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a16bf-159">System.Boolean</span></span>

## <span data-ttu-id="a16bf-160">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a16bf-160">NOTES</span></span>

## <span data-ttu-id="a16bf-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a16bf-161">RELATED LINKS</span></span>
