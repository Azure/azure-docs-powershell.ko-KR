---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Synapse.dll-Help.xml
Module Name: Az.Synapse
online version: https://docs.microsoft.com/en-us/powershell/module/az.synapse/new-azsynapseroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Synapse/Synapse/help/New-AzSynapseRoleAssignment.md
ms.openlocfilehash: 6fdb2a51354df01c308629eaedb09cba3a8d2fdf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056058"
---
# <span data-ttu-id="3a21f-101">New-AzSynapseRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="3a21f-101">New-AzSynapseRoleAssignment</span></span>

## <span data-ttu-id="3a21f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a21f-102">SYNOPSIS</span></span>
<span data-ttu-id="3a21f-103">Synapse Analytics 역할 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-103">Creates a Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3a21f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3a21f-104">SYNTAX</span></span>

### <span data-ttu-id="3a21f-105">NewByWorkspaceNameAndNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3a21f-105">NewByWorkspaceNameAndNameParameterSet (Default)</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -SignInName <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a21f-106">NewByWorkspaceNameAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-106">NewByWorkspaceNameAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a21f-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-107">NewByWorkspaceNameAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionId <String> -ObjectId <String> [-AsJob]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a21f-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-108">NewByWorkspaceNameAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceName <String> -RoleDefinitionName <String> -ServicePrincipalName <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a21f-109">NewByWorkspaceObjectAndNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-109">NewByWorkspaceObjectAndNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -SignInName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a21f-110">NewByWorkspaceObjectAndIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-110">NewByWorkspaceObjectAndIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ObjectId <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="3a21f-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-111">NewByWorkspaceObjectAndRoleDefinitionIdAndObjectIdParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionId <String> -ObjectId <String>
 [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a21f-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3a21f-112">NewByWorkspaceObjectAndServicePrincipalNameParameterSet</span></span>
```
New-AzSynapseRoleAssignment -WorkspaceObject <PSSynapseWorkspace> -RoleDefinitionName <String>
 -ServicePrincipalName <String> [-AsJob] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="3a21f-113">설명은</span><span class="sxs-lookup"><span data-stu-id="3a21f-113">DESCRIPTION</span></span>
<span data-ttu-id="3a21f-114">**AzSynapseRoleAssignment** Cmdlet은 Azure Synapse Analytics 역할 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-114">The **New-AzSynapseRoleAssignment** cmdlet creates an Azure Synapse Analytics role assignment.</span></span>

## <span data-ttu-id="3a21f-115">예제의</span><span class="sxs-lookup"><span data-stu-id="3a21f-115">EXAMPLES</span></span>

### <span data-ttu-id="3a21f-116">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a21f-116">Example 1</span></span>
```powershell
PS C:\> New-AzSynapseRoleAssignment -WorkspaceName ContosoWorkspace -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="3a21f-117">이 명령은 principal name이 ContosoName 인 사용자에 게 ContosoRole를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-117">This command assigns ContosoRole to the user whose principal name is ContosoName.</span></span>

### <span data-ttu-id="3a21f-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="3a21f-118">Example 2</span></span>
```powershell
PS C:\> $ws = Get-AzSynapseWorkspace -Name ContosoWorkspace
PS C:\> $ws | New-AzSynapseRoleAssignment -RoleDefinitionName ContosoRole -SignInName ContosoName
```

<span data-ttu-id="3a21f-119">이 명령은 principal name이 파이프라인을 통해 ContosoName 된 사용자에 게 ContosoRole를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-119">This command assigns ContosoRole to the user whose principal name is ContosoName through pipeline.</span></span>

## <span data-ttu-id="3a21f-120">변수</span><span class="sxs-lookup"><span data-stu-id="3a21f-120">PARAMETERS</span></span>

### <span data-ttu-id="3a21f-121">-AsJob</span><span class="sxs-lookup"><span data-stu-id="3a21f-121">-AsJob</span></span>
<span data-ttu-id="3a21f-122">백그라운드에서 cmdlet 실행</span><span class="sxs-lookup"><span data-stu-id="3a21f-122">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="3a21f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a21f-123">-DefaultProfile</span></span>
<span data-ttu-id="3a21f-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a21f-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="3a21f-125">-ObjectId</span></span>
<span data-ttu-id="3a21f-126">사용자, 그룹 또는 서비스 주체의 Azure AD ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-126">The Azure AD ObjectId of the User, Group or Service Principal.</span></span>

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

### <span data-ttu-id="3a21f-127">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="3a21f-127">-RoleDefinitionId</span></span>
<span data-ttu-id="3a21f-128">주도자에 게 지정 된 역할의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-128">Id of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3a21f-129">-RoleDefinitionName</span><span class="sxs-lookup"><span data-stu-id="3a21f-129">-RoleDefinitionName</span></span>
<span data-ttu-id="3a21f-130">주도자에 게 지정 된 역할의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-130">Name of the Role that is assigned to the principal.</span></span>

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

### <span data-ttu-id="3a21f-131">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3a21f-131">-ServicePrincipalName</span></span>
<span data-ttu-id="3a21f-132">서비스 사용자의 ServicePrincipalName.</span><span class="sxs-lookup"><span data-stu-id="3a21f-132">The ServicePrincipalName of the service principal.</span></span>

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

### <span data-ttu-id="3a21f-133">-SignInName</span><span class="sxs-lookup"><span data-stu-id="3a21f-133">-SignInName</span></span>
<span data-ttu-id="3a21f-134">사용자의 전자 메일 주소 또는 사용자 계정 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-134">The email address or the user principal name of the user.</span></span>

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

### <span data-ttu-id="3a21f-135">-WorkspaceName</span><span class="sxs-lookup"><span data-stu-id="3a21f-135">-WorkspaceName</span></span>
<span data-ttu-id="3a21f-136">Synapse 작업 영역의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-136">Name of Synapse workspace.</span></span>

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

### <span data-ttu-id="3a21f-137">-WorkspaceObject</span><span class="sxs-lookup"><span data-stu-id="3a21f-137">-WorkspaceObject</span></span>
<span data-ttu-id="3a21f-138">일반적으로 파이프라인을 통해 전달 되는 작업 영역 입력 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-138">workspace input object, usually passed through the pipeline.</span></span>

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

### <span data-ttu-id="3a21f-139">-확인</span><span class="sxs-lookup"><span data-stu-id="3a21f-139">-Confirm</span></span>
<span data-ttu-id="3a21f-140">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a21f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a21f-141">-WhatIf</span></span>
<span data-ttu-id="3a21f-142">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a21f-143">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a21f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a21f-144">CommonParameters</span></span>
<span data-ttu-id="3a21f-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a21f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a21f-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3a21f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a21f-147">입력</span><span class="sxs-lookup"><span data-stu-id="3a21f-147">INPUTS</span></span>

### <span data-ttu-id="3a21f-148">Synapse. PSSynapseWorkspace/.</span><span class="sxs-lookup"><span data-stu-id="3a21f-148">Microsoft.Azure.Commands.Synapse.Models.PSSynapseWorkspace</span></span>

## <span data-ttu-id="3a21f-149">출력</span><span class="sxs-lookup"><span data-stu-id="3a21f-149">OUTPUTS</span></span>

### <span data-ttu-id="3a21f-150">Synapse. PSRoleAssignmentDetails/.</span><span class="sxs-lookup"><span data-stu-id="3a21f-150">Microsoft.Azure.Commands.Synapse.Models.PSRoleAssignmentDetails</span></span>

## <span data-ttu-id="3a21f-151">상속자</span><span class="sxs-lookup"><span data-stu-id="3a21f-151">NOTES</span></span>

## <span data-ttu-id="3a21f-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a21f-152">RELATED LINKS</span></span>
