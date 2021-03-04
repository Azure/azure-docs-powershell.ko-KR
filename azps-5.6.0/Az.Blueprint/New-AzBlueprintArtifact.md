---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 82d0d3667371485d079785dbdb2f87eb8284aa94
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101954859"
---
# <span data-ttu-id="76bda-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="76bda-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="76bda-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="76bda-102">SYNOPSIS</span></span>
<span data-ttu-id="76bda-103">새 아티팩트를 만들고 청사진 정의 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="76bda-104">구문</span><span class="sxs-lookup"><span data-stu-id="76bda-104">SYNTAX</span></span>

### <span data-ttu-id="76bda-105">CreateTemplateArtifact(기본값)</span><span class="sxs-lookup"><span data-stu-id="76bda-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76bda-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="76bda-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76bda-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="76bda-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="76bda-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="76bda-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="76bda-109">설명</span><span class="sxs-lookup"><span data-stu-id="76bda-109">DESCRIPTION</span></span>
<span data-ttu-id="76bda-110">새 아티팩트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-110">Create a new artifact.</span></span> <span data-ttu-id="76bda-111">아티팩트를 만드는 두 가지 방법은 아티팩트 JSON을 입력 파일로 또는 아티팩트에 대한 인라인 매개 변수를 제공하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="76bda-112">JSON 메서드는 인라인 매개 변수 메서드를 제공해야 하는 아티팩트 형식을 요구하지는 않는 반면 사용자가 -Type 매개 변수를 통해 아티팩트 형식을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="76bda-113">예제</span><span class="sxs-lookup"><span data-stu-id="76bda-113">EXAMPLES</span></span>

### <span data-ttu-id="76bda-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="76bda-114">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Name PolicyStorage -Blueprint $bp -ArtifactFile C:\PolicyAssignmentStorageTag.json

DisplayName        :
Description        : Apply storage tag and the parameter also used by the template to resource groups
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/PolicyAssignmentStorageTag
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : PolicyAssignmentStorageTag
```

<span data-ttu-id="76bda-115">아티팩트 JSON 파일을 통해 새 아티팩트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="76bda-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="76bda-116">Example 2</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type PolicyAssignmentArtifact -Name "ApplyTag-RG" -Blueprint $bp -PolicyDefinitionId "/providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71" -PolicyDefinitionParameter @{tagName="[parameters('tagName')]"; tagValue="[parameters('tagValue')]"} -ResourceGroupName storageRG

DisplayName        : ApplyTag-RG
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/49c88fc8-6fd1-46fd-a676-f12d1d3a4c71
Parameters         : {[tagValue, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagName,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : storageRG
Id                 : /subscriptions/28cbf98f-381d-4425-9ac4-cf342dab9753/providers/Microsoft.Blueprint/blueprints/AppNetwork/
                     artifacts/ApplyTag-RG
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : ApplyTag-RG
```

<span data-ttu-id="76bda-117">인라인 매개 변수를 통해 새 아티팩트를 생성합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="76bda-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="76bda-118">Example 3</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> New-AzBlueprintArtifact -Type TemplateArtifact -Name storage-account -Blueprint $bp -TemplateFile C:\StorageAccountArmTemplate.json -ResourceGroup "storageRG" -TemplateParameterFile C:\Workspace\BlueprintTemplates\RestTemplatesSomeInline\StorageAccountParameters.json

DisplayName   : storage-account
Description   :
DependsOn     :
Template      : {$schema, contentVersion, parameters, variables...}
Parameters    : {}
ResourceGroup : storageRG
Id            : /subscriptions/{subscriptionId}/providers/Microsoft.Blueprint/blueprints/AppNetwork/artifacts/storage-account
Type          : Microsoft.Blueprint/blueprints/artifacts
Name          : storage-account
```

<span data-ttu-id="76bda-119">템플릿 파일을 통해 새 아티팩트를 ARM 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="76bda-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="76bda-120">PARAMETERS</span></span>

### <span data-ttu-id="76bda-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="76bda-121">-ArtifactFile</span></span>
<span data-ttu-id="76bda-122">디스크의 JSON 형식의 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="76bda-123">-Blueprint</span></span>
<span data-ttu-id="76bda-124">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="76bda-125">-DefaultProfile</span></span>
<span data-ttu-id="76bda-126">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="76bda-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="76bda-127">-DependsOn</span></span>
<span data-ttu-id="76bda-128">현재 아티팩트를 만들기 전에 만들어야 하는 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-129">-Description</span><span class="sxs-lookup"><span data-stu-id="76bda-129">-Description</span></span>
<span data-ttu-id="76bda-130">아티팩트에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-131">-Name</span><span class="sxs-lookup"><span data-stu-id="76bda-131">-Name</span></span>
<span data-ttu-id="76bda-132">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="76bda-132">Name of the artifact</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="76bda-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="76bda-134">정책 정의의 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="76bda-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="76bda-136">정책 정의 아티팩트에 전달할 매개 변수의 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="76bda-137">-ResourceGroupName</span></span>
<span data-ttu-id="76bda-138">아티팩트가 언더에 있을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="76bda-139">-RoleDefinitionId</span></span>
<span data-ttu-id="76bda-140">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="76bda-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="76bda-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="76bda-142">역할 정의 주체 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="76bda-143">-TemplateFile</span></span>
<span data-ttu-id="76bda-144">디스크의 ARM 템플릿 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="76bda-145">-TemplateParameterFile</span></span>
<span data-ttu-id="76bda-146">디스크의 ARM 템플릿 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: CreateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-147">-Type</span><span class="sxs-lookup"><span data-stu-id="76bda-147">-Type</span></span>
<span data-ttu-id="76bda-148">아티팩트의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-148">Type of the artifact.</span></span>
<span data-ttu-id="76bda-149">지원되는 3가지 유형은 RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact입니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: CreateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="76bda-150">-확인</span><span class="sxs-lookup"><span data-stu-id="76bda-150">-Confirm</span></span>
<span data-ttu-id="76bda-151">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="76bda-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="76bda-152">-WhatIf</span></span>
<span data-ttu-id="76bda-153">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="76bda-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="76bda-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="76bda-155">CommonParameters</span></span>
<span data-ttu-id="76bda-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="76bda-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="76bda-157">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="76bda-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="76bda-158">입력</span><span class="sxs-lookup"><span data-stu-id="76bda-158">INPUTS</span></span>

### <span data-ttu-id="76bda-159">System.String</span><span class="sxs-lookup"><span data-stu-id="76bda-159">System.String</span></span>

### <span data-ttu-id="76bda-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="76bda-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="76bda-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="76bda-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="76bda-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="76bda-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="76bda-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="76bda-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="76bda-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="76bda-164">System.String[]</span></span>

## <span data-ttu-id="76bda-165">출력</span><span class="sxs-lookup"><span data-stu-id="76bda-165">OUTPUTS</span></span>

### <span data-ttu-id="76bda-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="76bda-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="76bda-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="76bda-167">NOTES</span></span>

## <span data-ttu-id="76bda-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="76bda-168">RELATED LINKS</span></span>
