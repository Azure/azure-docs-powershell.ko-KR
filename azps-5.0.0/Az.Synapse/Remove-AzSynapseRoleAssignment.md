---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/remove-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/Remove-AzSynapseRoleAssignment.md
ms.openlocfilehash: 3ac6d0be30075409924c014c27a16b2f4cab21a0
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94311705"
---
# <span data-ttu-id="c75e1-101">Remove-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="c75e1-101">Remove-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="c75e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c75e1-102">SYNOPSIS</span></span>
<span data-ttu-id="c75e1-103">Synapse Analytics 역할 과제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-103">Deletes a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="c75e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c75e1-104">SYNTAX</span></span>

### <span data-ttu-id="c75e1-105">RemoveByWorkspaceNameAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="c75e1-105">RemoveByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-106">RemoveByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-106">RemoveByWorkspaceNameAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleAssignmentId <String> [-PassThru] [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-107">RemoveByWorkspaceNameAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-108">RemoveByWorkspaceNameAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String>
 [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-109">RemoveByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-110">RemoveByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-110">RemoveByWorkspaceObjectAndIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleAssignmentId <String> [-PassThru]
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c75e1-111">RemoveByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-111">RemoveByWorkspaceObjectAndNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c75e1-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-112">RemoveByWorkspaceObjectAndObjectIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c75e1-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-113">RemoveByWorkspaceObjectAndRoleDefinitionIdParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String>
 -ObjectId <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c75e1-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="c75e1-114">RemoveByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
Remove-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-PassThru] [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c75e1-115">설명은</span><span class="sxs-lookup"><span data-stu-id="c75e1-115">DESCRIPTION</span></span>
<span data-ttu-id="c75e1-116">**AzSynapseRoleAssignment** Cmdlet은 Azure Synapse Analytics 역할 할당을 영구적으로 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-116">The **Remove-AzSynapseRoleAssignment** cmdlet permanently deletes an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="c75e1-117">예제의</span><span class="sxs-lookup"><span data-stu-id="c75e1-117">EXAMPLES</span></span>

### <span data-ttu-id="c75e1-118">예제 1</span><span class="sxs-lookup"><span data-stu-id="c75e1-118">Example 1</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="c75e1-119">이 명령은 역할 할당 Id를 사용 하 여 Azure Synapse Analytics 역할 할당을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-119">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id.</span></span>

### <span data-ttu-id="c75e1-120">예제 2</span><span class="sxs-lookup"><span data-stu-id="c75e1-120">Example 2</span></span>
```powershell
PS C:\> Remove-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleAssignmentName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="c75e1-121">이 명령은 역할 이름과 upn (사용자 이름)을 사용 하 여 Azure Synapse Analytics 역할 할당을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-121">This command deletes an Azure Synapse Analytics role assignment with a role name and a user principal name.</span></span>

### <span data-ttu-id="c75e1-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="c75e1-122">Example 3</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | Remove-AzSynapseRoleAssignment -RoleAssignmentId ContosoRoleAssignmentId
```

<span data-ttu-id="c75e1-123">이 명령은 파이프라인을 통해 역할 할당 Id를 사용 하 여 Azure Synapse Analytics 역할 할당을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-123">This command deletes an Azure Synapse Analytics role assignment with a role assignment Id through pipeline.</span></span>

## <span data-ttu-id="c75e1-124">변수</span><span class="sxs-lookup"><span data-stu-id="c75e1-124">PARAMETERS</span></span>

### <span data-ttu-id="c75e1-125">-AsJob</span><span class="sxs-lookup"><span data-stu-id="c75e1-125">-AsJob</span></span>
<span data-ttu-id="c75e1-126">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="c75e1-126">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c75e1-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c75e1-127">-DefaultProfile</span></span>
<span data-ttu-id="c75e1-128">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c75e1-129">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="c75e1-129">-ObjectId</span></span>
<span data-ttu-id="c75e1-130">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-130">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="c75e1-131">-PassThru</span><span class="sxs-lookup"><span data-stu-id="c75e1-131">-PassThru</span></span>
<span data-ttu-id="c75e1-132">이 Cmdlet은 기본적으로 개체를 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-132">This Cmdlet does not return an object by default.</span></span>
<span data-ttu-id="c75e1-133">이 스위치를 지정 하면 성공한 경우 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-133">If this switch is specified, it returns true if successful.</span></span>

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

### <span data-ttu-id="c75e1-134">-RoleAssignmentId</span><span class="sxs-lookup"><span data-stu-id="c75e1-134">-RoleAssignmentId</span></span>
<span data-ttu-id="c75e1-135">역할 할당의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-135">The ID of the role assignment.</span></span>

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

### <span data-ttu-id="c75e1-136">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="c75e1-136">-RoleDefinitionId</span></span>
<span data-ttu-id="c75e1-137">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-137">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="c75e1-138">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="c75e1-138">-RoleDefinitionName</span></span>
<span data-ttu-id="c75e1-139">주도자에 게 지정 된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-139">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="c75e1-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="c75e1-140">-ServicePrincipalName</span></span>
<span data-ttu-id="c75e1-141">서비스 사용자의 ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="c75e1-141">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="c75e1-142">-SignInName</span><span class="sxs-lookup"><span data-stu-id="c75e1-142">-SignInName</span></span>
<span data-ttu-id="c75e1-143">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-143">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="c75e1-144">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="c75e1-144">-WorkspaceName</span></span>
<span data-ttu-id="c75e1-145">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-145">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="c75e1-146">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="c75e1-146">-WorkspaceObject</span></span>
<span data-ttu-id="c75e1-147">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-147">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="c75e1-148">-확인</span><span class="sxs-lookup"><span data-stu-id="c75e1-148">-Confirm</span></span>
<span data-ttu-id="c75e1-149">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-149">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c75e1-150">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c75e1-150">-WhatIf</span></span>
<span data-ttu-id="c75e1-151">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-151">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c75e1-152">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-152">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c75e1-153">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c75e1-153">CommonParameters</span></span>
<span data-ttu-id="c75e1-154">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c75e1-154">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c75e1-155">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="c75e1-155">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c75e1-156">입력</span><span class="sxs-lookup"><span data-stu-id="c75e1-156">INPUTS</span></span>

### <span data-ttu-id="c75e1-157">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="c75e1-157">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="c75e1-158">출력</span><span class="sxs-lookup"><span data-stu-id="c75e1-158">OUTPUTS</span></span>

### <span data-ttu-id="c75e1-159">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="c75e1-159">System.Boolean</span></span>

## <span data-ttu-id="c75e1-160">상속자</span><span class="sxs-lookup"><span data-stu-id="c75e1-160">NOTES</span></span>

## <span data-ttu-id="c75e1-161">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c75e1-161">RELATED LINKS</span></span>
