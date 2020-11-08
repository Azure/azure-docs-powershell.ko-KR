---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: 7187994ca1e6e6ba9da3980be2e75b7b4ad1a877
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94056765"
---
# <span data-ttu-id="d2833-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="d2833-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="d2833-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2833-102">SYNOPSIS</span></span>
<span data-ttu-id="d2833-103">청사진 정의의 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="d2833-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2833-104">SYNTAX</span></span>

### <span data-ttu-id="d2833-105">UpdateTemplateArtifact (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2833-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2833-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="d2833-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2833-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="d2833-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2833-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="d2833-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2833-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d2833-109">DESCRIPTION</span></span>
<span data-ttu-id="d2833-110">아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-110">Update an artifact.</span></span> <span data-ttu-id="d2833-111">아티팩트를 입력 파일로 업데이트 하거나 아티팩트에 대 한 인라인 매개 변수를 제공 하는 등 두 가지 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="d2833-112">JSON 메서드에는 인라인 매개 변수 메서드를 제공할 아티팩트의 형식이 필요 하지 않지만 사용자는 아티팩트를 통해 형식의 매개 변수를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="d2833-113">예제의</span><span class="sxs-lookup"><span data-stu-id="d2833-113">EXAMPLES</span></span>

### <span data-ttu-id="d2833-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="d2833-114">Example 1</span></span>
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

<span data-ttu-id="d2833-115">아티팩트 JSON 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="d2833-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="d2833-116">Example 2</span></span>
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

<span data-ttu-id="d2833-117">인라인 매개 변수를 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-117">Update an artifact through inline parameters.</span></span>

### <span data-ttu-id="d2833-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="d2833-118">Example 3</span></span>
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

<span data-ttu-id="d2833-119">ARM 서식 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="d2833-120">변수</span><span class="sxs-lookup"><span data-stu-id="d2833-120">PARAMETERS</span></span>

### <span data-ttu-id="d2833-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="d2833-121">-ArtifactFile</span></span>
<span data-ttu-id="d2833-122">디스크의 JSON 형식에서 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="d2833-123">-청사진</span><span class="sxs-lookup"><span data-stu-id="d2833-123">-Blueprint</span></span>
<span data-ttu-id="d2833-124">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="d2833-124">Blueprint object.</span></span>

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

### <span data-ttu-id="d2833-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2833-125">-DefaultProfile</span></span>
<span data-ttu-id="d2833-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d2833-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="d2833-127">-DependsOn</span></span>
<span data-ttu-id="d2833-128">현재 아티팩트를 만들기 전에 만들어야 할 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="d2833-129">-설명</span><span class="sxs-lookup"><span data-stu-id="d2833-129">-Description</span></span>
<span data-ttu-id="d2833-130">아티팩트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="d2833-131">-이름</span><span class="sxs-lookup"><span data-stu-id="d2833-131">-Name</span></span>
<span data-ttu-id="d2833-132">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="d2833-132">Name of the artifact</span></span>

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

### <span data-ttu-id="d2833-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d2833-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="d2833-134">정책 정의의 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="d2833-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="d2833-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="d2833-136">정책 정의 아티팩트에 전달할 매개 변수의 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="d2833-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d2833-137">-ResourceGroupName</span></span>
<span data-ttu-id="d2833-138">아티팩트가 들어가는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="d2833-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="d2833-139">-RoleDefinitionId</span></span>
<span data-ttu-id="d2833-140">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="d2833-140">List of role definition</span></span>

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

### <span data-ttu-id="d2833-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="d2833-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="d2833-142">역할 정의 principal id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="d2833-143">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="d2833-143">-TemplateFile</span></span>
<span data-ttu-id="d2833-144">디스크에 있는 ARM 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="d2833-145">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="d2833-145">-TemplateParameterFile</span></span>
<span data-ttu-id="d2833-146">디스크에 있는 ARM template 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="d2833-147">-Type</span><span class="sxs-lookup"><span data-stu-id="d2833-147">-Type</span></span>
<span data-ttu-id="d2833-148">아티팩트의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-148">Type of the artifact.</span></span>
<span data-ttu-id="d2833-149">지원 되는 형식에는 RoleAssignmentArtifact, PolicyAssignmentArtifact, 서식 가공물 등 3 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="d2833-150">-확인</span><span class="sxs-lookup"><span data-stu-id="d2833-150">-Confirm</span></span>
<span data-ttu-id="d2833-151">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-151">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2833-152">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2833-152">-WhatIf</span></span>
<span data-ttu-id="d2833-153">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-153">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d2833-154">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-154">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2833-155">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2833-155">CommonParameters</span></span>
<span data-ttu-id="d2833-156">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2833-156">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2833-157">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d2833-157">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2833-158">입력</span><span class="sxs-lookup"><span data-stu-id="d2833-158">INPUTS</span></span>

### <span data-ttu-id="d2833-159">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d2833-159">System.String</span></span>

### <span data-ttu-id="d2833-160">Microsoft. i a m. 모델. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="d2833-160">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="d2833-161">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="d2833-161">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="d2833-162">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="d2833-162">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="d2833-163">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="d2833-163">System.Collections.Hashtable</span></span>

### <span data-ttu-id="d2833-164">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="d2833-164">System.String[]</span></span>

## <span data-ttu-id="d2833-165">출력</span><span class="sxs-lookup"><span data-stu-id="d2833-165">OUTPUTS</span></span>

### <span data-ttu-id="d2833-166">Microsoft. Azure.. i a n. 아티팩트</span><span class="sxs-lookup"><span data-stu-id="d2833-166">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="d2833-167">상속자</span><span class="sxs-lookup"><span data-stu-id="d2833-167">NOTES</span></span>

## <span data-ttu-id="d2833-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2833-168">RELATED LINKS</span></span>
