---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintArtifact.md
ms.openlocfilehash: 7a6910e18b966c49ee6c766f06fddc88f903914f
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496197"
---
# <span data-ttu-id="ffc44-101">New-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="ffc44-101">New-AzBlueprintArtifact</span></span>

## <span data-ttu-id="ffc44-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ffc44-102">SYNOPSIS</span></span>
<span data-ttu-id="ffc44-103">새 아티팩트를 만들고 청사진 정의 내에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-103">Create a new artifact and save it within a blueprint definition.</span></span>

## <span data-ttu-id="ffc44-104">구문</span><span class="sxs-lookup"><span data-stu-id="ffc44-104">SYNTAX</span></span>

### <span data-ttu-id="ffc44-105">CreateTemplateArtifact(기본값)</span><span class="sxs-lookup"><span data-stu-id="ffc44-105">CreateTemplateArtifact (Default)</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc44-106">CreateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="ffc44-106">CreateArtifactByInputFile</span></span>
```
New-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc44-107">CreateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="ffc44-107">CreateRoleAssignmentArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="ffc44-108">CreatePolicyArtifact</span><span class="sxs-lookup"><span data-stu-id="ffc44-108">CreatePolicyArtifact</span></span>
```
New-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ffc44-109">설명</span><span class="sxs-lookup"><span data-stu-id="ffc44-109">DESCRIPTION</span></span>
<span data-ttu-id="ffc44-110">새 아티팩트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-110">Create a new artifact.</span></span> <span data-ttu-id="ffc44-111">아티팩트를 만드는 두 가지 방법은 아티팩트 JSON을 입력 파일로 또는 아티팩트에 대한 인라인 매개 변수를 제공하는 것입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-111">There are two ways to create an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="ffc44-112">JSON 메서드는 인라인 매개 변수 메서드를 제공해야 하는 아티팩트 형식이 필요하지는 않은 반면 사용자는 -Type 매개 변수를 통해 아티팩트의 형식을 제공해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="ffc44-113">예제</span><span class="sxs-lookup"><span data-stu-id="ffc44-113">EXAMPLES</span></span>

### <span data-ttu-id="ffc44-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="ffc44-114">Example 1</span></span>
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

<span data-ttu-id="ffc44-115">아티팩트 JSON 파일을 통해 새 아티팩트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-115">Create a new artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="ffc44-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="ffc44-116">Example 2</span></span>
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

<span data-ttu-id="ffc44-117">인라인 매개 변수를 통해 새 아티팩트를 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-117">Create a new artifact through inline parameters.</span></span>

### <span data-ttu-id="ffc44-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="ffc44-118">Example 3</span></span>
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

<span data-ttu-id="ffc44-119">템플릿 파일을 사용하여 새 아티팩트를 ARM 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-119">Create a new artifact through an ARM template file.</span></span>

## <span data-ttu-id="ffc44-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="ffc44-120">PARAMETERS</span></span>

### <span data-ttu-id="ffc44-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="ffc44-121">-ArtifactFile</span></span>
<span data-ttu-id="ffc44-122">디스크의 JSON 형식인 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="ffc44-123">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="ffc44-123">-Blueprint</span></span>
<span data-ttu-id="ffc44-124">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-124">Blueprint object.</span></span>

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

### <span data-ttu-id="ffc44-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ffc44-125">-DefaultProfile</span></span>
<span data-ttu-id="ffc44-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="ffc44-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="ffc44-127">-DependsOn</span></span>
<span data-ttu-id="ffc44-128">현재 아티팩트를 만들기 전에 만들어야 하는 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="ffc44-129">-Description</span><span class="sxs-lookup"><span data-stu-id="ffc44-129">-Description</span></span>
<span data-ttu-id="ffc44-130">아티팩트에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="ffc44-131">-Name</span><span class="sxs-lookup"><span data-stu-id="ffc44-131">-Name</span></span>
<span data-ttu-id="ffc44-132">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="ffc44-132">Name of the artifact</span></span>

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

### <span data-ttu-id="ffc44-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ffc44-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="ffc44-134">정책 정의의 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="ffc44-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="ffc44-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="ffc44-136">정책 정의 아티팩트에 전달할 매개 변수의 해시가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="ffc44-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ffc44-137">-ResourceGroupName</span></span>
<span data-ttu-id="ffc44-138">아티팩트가 있을 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="ffc44-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="ffc44-139">-RoleDefinitionId</span></span>
<span data-ttu-id="ffc44-140">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="ffc44-140">List of role definition</span></span>

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

### <span data-ttu-id="ffc44-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="ffc44-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="ffc44-142">역할 정의 주체 ID 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="ffc44-143">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="ffc44-143">-TemplateFile</span></span>
<span data-ttu-id="ffc44-144">디스크의 ARM 템플릿 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="ffc44-145">-TemplateParameterFile</span><span class="sxs-lookup"><span data-stu-id="ffc44-145">-TemplateParameterFile</span></span>
<span data-ttu-id="ffc44-146">디스크에 ARM 템플릿 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="ffc44-147">-Type</span><span class="sxs-lookup"><span data-stu-id="ffc44-147">-Type</span></span>
<span data-ttu-id="ffc44-148">아티팩트의 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-148">Type of the artifact.</span></span>
<span data-ttu-id="ffc44-149">지원되는 세 가지 유형은 RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact입니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="ffc44-150">-Confirm</span><span class="sxs-lookup"><span data-stu-id="ffc44-150">-Confirm</span></span>
<span data-ttu-id="ffc44-151">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ffc44-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ffc44-152">-WhatIf</span></span>
<span data-ttu-id="ffc44-153">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="ffc44-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ffc44-154">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ffc44-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ffc44-155">CommonParameters</span></span>
<span data-ttu-id="ffc44-156">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ffc44-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ffc44-157">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="ffc44-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ffc44-158">입력</span><span class="sxs-lookup"><span data-stu-id="ffc44-158">INPUTS</span></span>

### <span data-ttu-id="ffc44-159">System.String</span><span class="sxs-lookup"><span data-stu-id="ffc44-159">System.String</span></span>

### <span data-ttu-id="ffc44-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="ffc44-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="ffc44-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="ffc44-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="ffc44-162">System.Collections.Generic.List'1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="ffc44-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="ffc44-163">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="ffc44-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="ffc44-164">System.String[]</span><span class="sxs-lookup"><span data-stu-id="ffc44-164">System.String[]</span></span>

## <span data-ttu-id="ffc44-165">출력</span><span class="sxs-lookup"><span data-stu-id="ffc44-165">OUTPUTS</span></span>

### <span data-ttu-id="ffc44-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span><span class="sxs-lookup"><span data-stu-id="ffc44-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="ffc44-167">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ffc44-167">NOTES</span></span>

## <span data-ttu-id="ffc44-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ffc44-168">RELATED LINKS</span></span>
