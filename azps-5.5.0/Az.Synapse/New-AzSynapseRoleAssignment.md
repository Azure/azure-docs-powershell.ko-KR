---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100190596"
---
# <span data-ttu-id="9a814-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="9a814-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="9a814-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a814-102">SYNOPSIS</span></span>
<span data-ttu-id="9a814-103">Synapse Analytics 역할 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="9a814-104">구문</span><span class="sxs-lookup"><span data-stu-id="9a814-104">SYNTAX</span></span>

### <span data-ttu-id="9a814-105">NewByWorkspaceNameAndNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="9a814-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a814-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a814-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a814-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a814-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a814-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="9a814-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="9a814-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="9a814-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="9a814-113">설명</span><span class="sxs-lookup"><span data-stu-id="9a814-113">DESCRIPTION</span></span>
<span data-ttu-id="9a814-114">**New-AzSynapseRoleAssignment** cmdlet은 Azure Synapse Analytics 역할 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="9a814-115">예제</span><span class="sxs-lookup"><span data-stu-id="9a814-115">EXAMPLES</span></span>

### <span data-ttu-id="9a814-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="9a814-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="9a814-117">이 명령은 보안 주체 이름이 ContosoName인 사용자에게 ContosoRole을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="9a814-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="9a814-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="9a814-119">이 명령은 파이프라인을 통해 보안 주체 이름이 ContosoName인 사용자에게 ContosoRole을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="9a814-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="9a814-120">PARAMETERS</span></span>

### <span data-ttu-id="9a814-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="9a814-121">-AsJob</span></span>
<span data-ttu-id="9a814-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="9a814-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="9a814-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a814-123">-DefaultProfile</span></span>
<span data-ttu-id="9a814-124">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="9a814-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="9a814-125">-ObjectId</span></span>
<span data-ttu-id="9a814-126">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="9a814-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="9a814-127">-RoleDefinitionId</span></span>
<span data-ttu-id="9a814-128">보안 주체에 할당된 역할의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="9a814-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="9a814-129">-RoleDefinitionName</span></span>
<span data-ttu-id="9a814-130">보안 주체에 할당된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="9a814-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="9a814-131">-ServicePrincipalName</span></span>
<span data-ttu-id="9a814-132">서비스 주체의 ServicePrincipalName입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="9a814-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="9a814-133">-SignInName</span></span>
<span data-ttu-id="9a814-134">사용자의 이메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="9a814-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="9a814-135">-WorkspaceName</span></span>
<span data-ttu-id="9a814-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="9a814-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="9a814-137">-WorkspaceObject</span></span>
<span data-ttu-id="9a814-138">일반적으로 파이프라인을 통해 전달되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="9a814-139">-Confirm</span><span class="sxs-lookup"><span data-stu-id="9a814-139">-Confirm</span></span>
<span data-ttu-id="9a814-140">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9a814-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9a814-141">-WhatIf</span></span>
<span data-ttu-id="9a814-142">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="9a814-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="9a814-143">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9a814-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a814-144">CommonParameters</span></span>
<span data-ttu-id="9a814-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="9a814-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a814-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="9a814-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a814-147">입력</span><span class="sxs-lookup"><span data-stu-id="9a814-147">INPUTS</span></span>

### <span data-ttu-id="9a814-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span><span class="sxs-lookup"><span data-stu-id="9a814-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="9a814-149">출력</span><span class="sxs-lookup"><span data-stu-id="9a814-149">OUTPUTS</span></span>

### <span data-ttu-id="9a814-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span><span class="sxs-lookup"><span data-stu-id="9a814-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="9a814-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="9a814-151">NOTES</span></span>

## <span data-ttu-id="9a814-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9a814-152">RELATED LINKS</span></span>
