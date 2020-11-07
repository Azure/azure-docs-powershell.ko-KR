---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprintArtifact.md
ms.openlocfilehash: 94a0ff1d4e16748b769f51303fb397da7e029026
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697648"
---
# <span data-ttu-id="f0831-101">Get-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="f0831-101">Get-AzBlueprintArtifact</span></span>

## <span data-ttu-id="f0831-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f0831-102">SYNOPSIS</span></span>
<span data-ttu-id="f0831-103">청사진 정의에서 아티팩트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-103">Retrieve artifacts from a blueprint definition.</span></span>

## <span data-ttu-id="f0831-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f0831-104">SYNTAX</span></span>

```
Get-AzBlueprintArtifact [-Name <String>] -Blueprint <PSBlueprintBase> [-BlueprintVersion <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f0831-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f0831-105">DESCRIPTION</span></span>
<span data-ttu-id="f0831-106">청사진 정의에서 아티팩트를 검색 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-106">Retrieve artifacts from a blueprint definition.</span></span> <span data-ttu-id="f0831-107">청사진 정의 버전을 지정 하지 않으면 초안 버전이 검색 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-107">If a blueprint definition version is not specified, the draft version is retrieved.</span></span> <span data-ttu-id="f0831-108">초안 버전이 없는 경우에는 게시 된 최신 청사진 정의가 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-108">In the case where there is no draft version, the latest published blueprint definition is returned.</span></span>

## <span data-ttu-id="f0831-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f0831-109">EXAMPLES</span></span>

### <span data-ttu-id="f0831-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f0831-110">Example 1</span></span>
```powershell
PS C:\> $bp = Get-AzBlueprint -Name SimpleBlueprint
PS C:\> Get-AzBlueprintArtifact -Blueprint $bp 

DisplayName        : Audit use of classic virtual machines
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1d84d5fb-01f6-4d12-ba4f-4a26081d403d
Parameters         : {[effect, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      : SimpleBlueprintRG
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/3ab44511-0228-4275-9641-7e93e6f34178
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 3ab44511-0228-4275-9641-7e93e6f34178

DisplayName        : Enforce tag and its value
Description        :
DependsOn          :
PolicyDefinitionId : /providers/Microsoft.Authorization/policyDefinitions/1e30110a-5ceb-460c-a204-c1c3969c6d62
Parameters         : {[tagName, Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue], [tagValue,
                     Microsoft.Azure.Commands.Blueprint.Models.PSParameterValue]}
ResourceGroup      :
Id                 : /providers/Microsoft.Management/managementGroups/{mgId}/providers/Microsoft.Blueprint/blueprints/SimpleBlueprint/artifacts/0e1593da-47d5-4b75-800c-9a797dd23192
Type               : Microsoft.Blueprint/blueprints/artifacts
Name               : 0e1593da-47d5-4b75-800c-9a797dd23192

```

<span data-ttu-id="f0831-111">청사진 정의에서 아티팩트 검색.</span><span class="sxs-lookup"><span data-stu-id="f0831-111">Retrieve artifacts from a blueprint definition..</span></span> 

## <span data-ttu-id="f0831-112">변수</span><span class="sxs-lookup"><span data-stu-id="f0831-112">PARAMETERS</span></span>

### <span data-ttu-id="f0831-113">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="f0831-113">-ArtifactFile</span></span>
<span data-ttu-id="f0831-114">디스크의 JSON 형식에서 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-114">Location of the artifact file in JSON format on disk.</span></span>

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-115">-청사진</span><span class="sxs-lookup"><span data-stu-id="f0831-115">-Blueprint</span></span>
<span data-ttu-id="f0831-116">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="f0831-116">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: ArtifactsByBlueprint, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: PSBlueprintBase
Parameter Sets: CreateArtifactByInputFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-117">-BlueprintVersion</span><span class="sxs-lookup"><span data-stu-id="f0831-117">-BlueprintVersion</span></span>
<span data-ttu-id="f0831-118">아티팩트를 가져올 청사진 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-118">Version of the blueprint to get the artifacts from.</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f0831-119">-DefaultProfile</span></span>
<span data-ttu-id="f0831-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-121">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="f0831-121">-DependsOn</span></span>
<span data-ttu-id="f0831-122">현재 아티팩트를 만들기 전에 만들어야 할 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-122">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

```yaml
Type: System.Collections.Generic.List`1[System.String]
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-123">-설명</span><span class="sxs-lookup"><span data-stu-id="f0831-123">-Description</span></span>
<span data-ttu-id="f0831-124">아티팩트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-124">Description of the artifact.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-125">-이름</span><span class="sxs-lookup"><span data-stu-id="f0831-125">-Name</span></span>
<span data-ttu-id="f0831-126">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="f0831-126">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: ArtifactsByBlueprint
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: CreateArtifactByInputFile, UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-127">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f0831-127">-PolicyDefinitionId</span></span>
<span data-ttu-id="f0831-128">정책 정의의 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-128">Definition Id of the policy definition.</span></span>

```yaml
Type: String
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-129">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="f0831-129">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="f0831-130">정책 정의 아티팩트에 전달할 매개 변수의 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-130">Hashtable of parameters to pass to the policy definition artifact.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f0831-131">-ResourceGroupName</span></span>
<span data-ttu-id="f0831-132">아티팩트가 들어가는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-132">Name of the resource group the artifact is going to be under.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-133">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="f0831-133">-RoleDefinitionId</span></span>
<span data-ttu-id="f0831-134">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="f0831-134">List of role definition</span></span>

```yaml
Type: String
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-135">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="f0831-135">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="f0831-136">역할 정의 principal id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-136">List of role definition principal ids.</span></span>

```yaml
Type: String[]
Parameter Sets: CreateRoleAssignmentArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-137">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="f0831-137">-TemplateFile</span></span>
<span data-ttu-id="f0831-138">디스크에 있는 ARM 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-138">Location of the ARM template file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-139">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="f0831-139">-TemplateParameterFile</span></span>
<span data-ttu-id="f0831-140">디스크에 있는 ARM template 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-140">Location of the ARM template parameter file on disk.</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-141">-Type</span><span class="sxs-lookup"><span data-stu-id="f0831-141">-Type</span></span>
<span data-ttu-id="f0831-142">아티팩트의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-142">Type of the artifact.</span></span>
<span data-ttu-id="f0831-143">지원 되는 형식에는 RoleAssignmentArtifact, PolicyAssignmentArtifact, 서식 가공물 등 3 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-143">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

```yaml
Type: PSArtifactKind
Parameter Sets: UpdateTemplateArtifact, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:
Accepted values: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-144">-확인</span><span class="sxs-lookup"><span data-stu-id="f0831-144">-Confirm</span></span>
<span data-ttu-id="f0831-145">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-145">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-146">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f0831-146">-WhatIf</span></span>
<span data-ttu-id="f0831-147">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-147">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f0831-148">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-148">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f0831-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f0831-149">CommonParameters</span></span>
<span data-ttu-id="f0831-150">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f0831-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="f0831-151">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f0831-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f0831-152">입력</span><span class="sxs-lookup"><span data-stu-id="f0831-152">INPUTS</span></span>

### <span data-ttu-id="f0831-153">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f0831-153">System.String</span></span>

### <span data-ttu-id="f0831-154">Microsoft. i a m. 모델. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="f0831-154">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="f0831-155">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="f0831-155">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="f0831-156">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f0831-156">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="f0831-157">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="f0831-157">System.Collections.Hashtable</span></span>

### <span data-ttu-id="f0831-158">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="f0831-158">System.String[]</span></span>

## <span data-ttu-id="f0831-159">출력</span><span class="sxs-lookup"><span data-stu-id="f0831-159">OUTPUTS</span></span>

### <span data-ttu-id="f0831-160">PSBlueprintAssignment (.).</span><span class="sxs-lookup"><span data-stu-id="f0831-160">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintAssignment</span></span>

## <span data-ttu-id="f0831-161">상속자</span><span class="sxs-lookup"><span data-stu-id="f0831-161">NOTES</span></span>

## <span data-ttu-id="f0831-162">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f0831-162">RELATED LINKS</span></span>
