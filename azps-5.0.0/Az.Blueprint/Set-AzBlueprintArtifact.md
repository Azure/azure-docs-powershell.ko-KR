---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216092"
---
# <span data-ttu-id="16c51-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="16c51-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="16c51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16c51-102">SYNOPSIS</span></span>
<span data-ttu-id="16c51-103">청사진 정의의 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="16c51-104">구문과</span><span class="sxs-lookup"><span data-stu-id="16c51-104">SYNTAX</span></span>

### <span data-ttu-id="16c51-105">UpdateTemplateArtifact (기본값)</span><span class="sxs-lookup"><span data-stu-id="16c51-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c51-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="16c51-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c51-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="16c51-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="16c51-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="16c51-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="16c51-109">설명은</span><span class="sxs-lookup"><span data-stu-id="16c51-109">DESCRIPTION</span></span>
<span data-ttu-id="16c51-110">아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-110">Update an artifact.</span></span> <span data-ttu-id="16c51-111">아티팩트를 입력 파일로 업데이트 하거나 아티팩트에 대 한 인라인 매개 변수를 제공 하는 등 두 가지 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="16c51-112">JSON 메서드에는 인라인 매개 변수 메서드를 제공할 아티팩트의 형식이 필요 하지 않지만 사용자는 아티팩트를 통해 형식의 매개 변수를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="16c51-113">예제의</span><span class="sxs-lookup"><span data-stu-id="16c51-113">EXAMPLES</span></span>

### <span data-ttu-id="16c51-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="16c51-114">Example 1</span></span>
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

<span data-ttu-id="16c51-115">아티팩트 JSON 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="16c51-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="16c51-116">Example 2</span></span>
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

<span data-ttu-id="16c51-117">인라인 매개 변수를 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="16c51-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="16c51-118">Example 3</span></span>
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

<span data-ttu-id="16c51-119">ARM 서식 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="16c51-120">변수</span><span class="sxs-lookup"><span data-stu-id="16c51-120">PARAMETERS</span></span>

### <span data-ttu-id="16c51-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="16c51-121">-ArtifactFile</span></span>
<span data-ttu-id="16c51-122">디스크의 JSON 형식에서 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-122">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-123">-청사진</span><span class="sxs-lookup"><span data-stu-id="16c51-123">-Blueprint</span></span>
<span data-ttu-id="16c51-124">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="16c51-124">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16c51-125">-DefaultProfile</span></span>
<span data-ttu-id="16c51-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="16c51-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="16c51-127">-DependsOn</span></span>
<span data-ttu-id="16c51-128">현재 아티팩트를 만들기 전에 만들어야 할 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-129">-설명</span><span class="sxs-lookup"><span data-stu-id="16c51-129">-Description</span></span>
<span data-ttu-id="16c51-130">아티팩트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-130">Description of the artifact.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-131">-이름</span><span class="sxs-lookup"><span data-stu-id="16c51-131">-Name</span></span>
<span data-ttu-id="16c51-132">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="16c51-132">Name of the artifact</span></span>

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

### <span data-ttu-id="16c51-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16c51-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="16c51-134">정책 정의의 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-134">Definition Id of the policy definition.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="16c51-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="16c51-136">정책 정의 아티팩트에 전달할 매개 변수의 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdatePolicyAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16c51-137">-ResourceGroupName</span></span>
<span data-ttu-id="16c51-138">아티팩트가 들어가는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-138">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="16c51-139">-RoleDefinitionId</span></span>
<span data-ttu-id="16c51-140">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="16c51-140">List of role definition</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="16c51-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="16c51-142">역할 정의 principal id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-142">List of role definition principal ids.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-143">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="16c51-143">-TemplateFile</span></span>
<span data-ttu-id="16c51-144">디스크에 있는 ARM 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-144">Location of the ARM template file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-145">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="16c51-145">-TemplateParameterFile</span></span>
<span data-ttu-id="16c51-146">디스크에 있는 ARM template 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-146">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-147">-Type</span><span class="sxs-lookup"><span data-stu-id="16c51-147">-Type</span></span>
<span data-ttu-id="16c51-148">아티팩트의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-148">Type of the artifact.</span></span>
<span data-ttu-id="16c51-149">지원 되는 형식에는 RoleAssignmentArtifact, PolicyAssignmentArtifact, 서식 가공물 등 3 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, UpdateRoleAssignmentArtifact, UpdatePolicyAssignmentArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16c51-150">-확인</span><span class="sxs-lookup"><span data-stu-id="16c51-150">-Confirm</span></span>
<span data-ttu-id="16c51-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16c51-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16c51-152">-WhatIf</span></span>
<span data-ttu-id="16c51-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="16c51-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16c51-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16c51-155">CommonParameters</span></span>
<span data-ttu-id="16c51-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="16c51-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16c51-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="16c51-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16c51-158">입력</span><span class="sxs-lookup"><span data-stu-id="16c51-158">INPUTS</span></span>

### <span data-ttu-id="16c51-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="16c51-159">System.String</span></span>

### <span data-ttu-id="16c51-160">Microsoft. i a m. 모델. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="16c51-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="16c51-161">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="16c51-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="16c51-162">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="16c51-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="16c51-163">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="16c51-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="16c51-164">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="16c51-164">System.String[]</span></span>

## <span data-ttu-id="16c51-165">출력</span><span class="sxs-lookup"><span data-stu-id="16c51-165">OUTPUTS</span></span>

### <span data-ttu-id="16c51-166">Microsoft. Azure.. i a n. 아티팩트</span><span class="sxs-lookup"><span data-stu-id="16c51-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="16c51-167">상속자</span><span class="sxs-lookup"><span data-stu-id="16c51-167">NOTES</span></span>

## <span data-ttu-id="16c51-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="16c51-168">RELATED LINKS</span></span>
