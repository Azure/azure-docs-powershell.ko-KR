---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 7e216a6d2751ddd24e7d948cb6cca036c2a9b336
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101976075"
---
# <span data-ttu-id="f6deb-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f6deb-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="f6deb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6deb-102">SYNOPSIS</span></span>
<span data-ttu-id="f6deb-103">Synapse Analytics 역할 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="f6deb-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6deb-104">SYNTAX</span></span>

### <span data-ttu-id="f6deb-105">NewByWorkspaceNameAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6deb-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6deb-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6deb-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6deb-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6deb-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6deb-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="f6deb-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6deb-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f6deb-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f6deb-113">설명</span><span class="sxs-lookup"><span data-stu-id="f6deb-113">DESCRIPTION</span></span>
<span data-ttu-id="f6deb-114">**New-AzSynapseRoleAssignment** cmdlet은 Azure Synapse Analytics 역할 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="f6deb-115">예제</span><span class="sxs-lookup"><span data-stu-id="f6deb-115">EXAMPLES</span></span>

### <span data-ttu-id="f6deb-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6deb-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="f6deb-117">이 명령은 ContosoName의 주체 이름이 ContosoName인 사용자에게 ContosoRole을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="f6deb-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="f6deb-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="f6deb-119">이 명령은 파이프라인을 통해 ContosoName 주체 이름이 ContosoName인 사용자에게 ContosoRole을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="f6deb-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f6deb-120">PARAMETERS</span></span>

### <span data-ttu-id="f6deb-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="f6deb-121">-AsJob</span></span>
<span data-ttu-id="f6deb-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="f6deb-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="f6deb-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6deb-123">-DefaultProfile</span></span>
<span data-ttu-id="f6deb-124">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6deb-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f6deb-125">-ObjectId</span></span>
<span data-ttu-id="f6deb-126">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases: Id, PrincipalId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f6deb-127">-RoleDefinitionId</span></span>
<span data-ttu-id="f6deb-128">주체에 할당된 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-128">Id of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="f6deb-129">-RoleDefinitionName</span></span>
<span data-ttu-id="f6deb-130">주체에 할당된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-130">Name of the Role that is assigned to the principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f6deb-131">-ServicePrincipalName</span></span>
<span data-ttu-id="f6deb-132">서비스 주체의 ServicePrincipalName입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-132">The ServicePrincipalName of the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndServicePrincipalNameParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="f6deb-133">-SignInName</span></span>
<span data-ttu-id="f6deb-134">사용자의 전자 메일 주소 또는 사용자 주체 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-134">The email address or the user principal name of the user.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceObjectAndNameParameterSet
Aliases: Email, UserPrincipalName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="f6deb-135">-WorkspaceName</span></span>
<span data-ttu-id="f6deb-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-136">Name of Synapse workspace.</span></span>

```yaml
Type: System.String
Parameter Sets: NewByWorkspaceNameAndNameParameterSet, NewByWorkspaceNameAndIdParameterSet, NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceNameAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="f6deb-137">-WorkspaceObject</span></span>
<span data-ttu-id="f6deb-138">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-138">workspace input object, usually passed through the pipeline.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace
Parameter Sets: NewByWorkspaceObjectAndNameParameterSet, NewByWorkspaceObjectAndIdParameterSet, NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet, NewByWorkspaceObjectAndServicePrincipalNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f6deb-139">-확인</span><span class="sxs-lookup"><span data-stu-id="f6deb-139">-Confirm</span></span>
<span data-ttu-id="f6deb-140">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6deb-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6deb-141">-WhatIf</span></span>
<span data-ttu-id="f6deb-142">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6deb-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6deb-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6deb-144">CommonParameters</span></span>
<span data-ttu-id="f6deb-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6deb-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6deb-146">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="f6deb-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6deb-147">입력</span><span class="sxs-lookup"><span data-stu-id="f6deb-147">INPUTS</span></span>

### <span data-ttu-id="f6deb-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="f6deb-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="f6deb-149">출력</span><span class="sxs-lookup"><span data-stu-id="f6deb-149">OUTPUTS</span></span>

### <span data-ttu-id="f6deb-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="f6deb-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="f6deb-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6deb-151">NOTES</span></span>

## <span data-ttu-id="f6deb-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6deb-152">RELATED LINKS</span></span>
