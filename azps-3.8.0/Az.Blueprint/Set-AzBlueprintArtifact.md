---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintartifact
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintArtifact.md
ms.openlocfilehash: c71a587dc755ae1834198f14142d5a511fe17ea2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034449"
---
# <span data-ttu-id="a529c-101">Set-AzBlueprintArtifact</span><span class="sxs-lookup"><span data-stu-id="a529c-101">Set-AzBlueprintArtifact</span></span>

## <span data-ttu-id="a529c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a529c-102">SYNOPSIS</span></span>
<span data-ttu-id="a529c-103">청사진 정의의 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-103">Update an artifact in a blueprint definition.</span></span>

## <span data-ttu-id="a529c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a529c-104">SYNTAX</span></span>


### <span data-ttu-id="a529c-105">UpdateTemplateArtifact (기본값)</span><span class="sxs-lookup"><span data-stu-id="a529c-105">UpdateTemplateArtifact (Default)</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -TemplateParameterFile <String> -TemplateFile <String> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a529c-106">UpdateArtifactByInputFile</span><span class="sxs-lookup"><span data-stu-id="a529c-106">UpdateArtifactByInputFile</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Blueprint <PSBlueprintBase> -ArtifactFile <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a529c-107">UpdateRoleAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a529c-107">UpdateRoleAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -RoleDefinitionId <String> -RoleDefinitionPrincipalId <String[]> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a529c-108">UpdatePolicyAssignmentArtifact</span><span class="sxs-lookup"><span data-stu-id="a529c-108">UpdatePolicyAssignmentArtifact</span></span>
```
Set-AzBlueprintArtifact -Name <String> -Type <PSArtifactKind> -Blueprint <PSBlueprintBase>
 [-Description <String>] [-DependsOn <System.Collections.Generic.List`1[System.String]>]
 -PolicyDefinitionId <String> -PolicyDefinitionParameter <Hashtable> [-ResourceGroupName <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a529c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="a529c-109">DESCRIPTION</span></span>
<span data-ttu-id="a529c-110">아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-110">Update an artifact.</span></span> <span data-ttu-id="a529c-111">아티팩트를 입력 파일로 업데이트 하거나 아티팩트에 대 한 인라인 매개 변수를 제공 하는 등 두 가지 방법 중 하나를 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-111">There are two ways to update an artifact: either through an artifact JSON as an input file or through providing inline parameters for the artifact.</span></span> <span data-ttu-id="a529c-112">JSON 메서드에는 인라인 매개 변수 메서드를 제공할 아티팩트의 형식이 필요 하지 않지만 사용자는 아티팩트를 통해 형식의 매개 변수를 제공 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-112">While the JSON method doesn't require type of the artifact to be provided inline parameter method requires user to provide the type of the artifact through -Type parameter.</span></span>

## <span data-ttu-id="a529c-113">예제의</span><span class="sxs-lookup"><span data-stu-id="a529c-113">EXAMPLES</span></span>

### <span data-ttu-id="a529c-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="a529c-114">Example 1</span></span>
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

<span data-ttu-id="a529c-115">아티팩트 JSON 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-115">Update an artifact through an artifact JSON file.</span></span>

### <span data-ttu-id="a529c-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="a529c-116">Example 2</span></span>
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

<span data-ttu-id="a529c-117">인라인 매개 변수를 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-117">Update an artifact through inline parameters.</span></span>


### <span data-ttu-id="a529c-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="a529c-118">Example 3</span></span>
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

<span data-ttu-id="a529c-119">ARM 서식 파일을 통해 아티팩트를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-119">Update an artifact through an ARM template file.</span></span>

## <span data-ttu-id="a529c-120">변수</span><span class="sxs-lookup"><span data-stu-id="a529c-120">PARAMETERS</span></span>

### <span data-ttu-id="a529c-121">-ArtifactFile</span><span class="sxs-lookup"><span data-stu-id="a529c-121">-ArtifactFile</span></span>
<span data-ttu-id="a529c-122">디스크의 JSON 형식에서 아티팩트 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-122">Location of the artifact file in JSON format on disk.</span></span>

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

### <span data-ttu-id="a529c-123">-청사진</span><span class="sxs-lookup"><span data-stu-id="a529c-123">-Blueprint</span></span>
<span data-ttu-id="a529c-124">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="a529c-124">Blueprint object.</span></span>

```yaml
Type: PSBlueprintBase
Parameter Sets: UpdateTemplateArtifact, ArtifactsByBlueprint, CreateRoleAssignmentArtifact, CreatePolicyArtifact
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

### <span data-ttu-id="a529c-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a529c-125">-DefaultProfile</span></span>
<span data-ttu-id="a529c-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-126">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a529c-127">-DependsOn</span><span class="sxs-lookup"><span data-stu-id="a529c-127">-DependsOn</span></span>
<span data-ttu-id="a529c-128">현재 아티팩트를 만들기 전에 만들어야 할 아티팩트의 이름 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-128">List of the names of artifacts that needs to be created before current artifact is created.</span></span>

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

### <span data-ttu-id="a529c-129">-설명</span><span class="sxs-lookup"><span data-stu-id="a529c-129">-Description</span></span>
<span data-ttu-id="a529c-130">아티팩트에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-130">Description of the artifact.</span></span>

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

### <span data-ttu-id="a529c-131">-이름</span><span class="sxs-lookup"><span data-stu-id="a529c-131">-Name</span></span>
<span data-ttu-id="a529c-132">아티팩트의 이름</span><span class="sxs-lookup"><span data-stu-id="a529c-132">Name of the artifact</span></span>

```yaml
Type: String
Parameter Sets: UpdateTemplateArtifact, CreateArtifactByInputFile, CreateRoleAssignmentArtifact, CreatePolicyArtifact
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

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

### <span data-ttu-id="a529c-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a529c-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="a529c-134">정책 정의의 정의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-134">Definition Id of the policy definition.</span></span>

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

### <span data-ttu-id="a529c-135">-PolicyDefinitionParameter</span><span class="sxs-lookup"><span data-stu-id="a529c-135">-PolicyDefinitionParameter</span></span>
<span data-ttu-id="a529c-136">정책 정의 아티팩트에 전달할 매개 변수의 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-136">Hashtable of parameters to pass to the policy definition artifact.</span></span>

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

### <span data-ttu-id="a529c-137">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a529c-137">-ResourceGroupName</span></span>
<span data-ttu-id="a529c-138">아티팩트가 들어가는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-138">Name of the resource group the artifact is going to be under.</span></span>

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

### <span data-ttu-id="a529c-139">-RoleDefinitionId</span><span class="sxs-lookup"><span data-stu-id="a529c-139">-RoleDefinitionId</span></span>
<span data-ttu-id="a529c-140">역할 정의 목록</span><span class="sxs-lookup"><span data-stu-id="a529c-140">List of role definition</span></span>

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

### <span data-ttu-id="a529c-141">-RoleDefinitionPrincipalId</span><span class="sxs-lookup"><span data-stu-id="a529c-141">-RoleDefinitionPrincipalId</span></span>
<span data-ttu-id="a529c-142">역할 정의 principal id의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-142">List of role definition principal ids.</span></span>

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

### <span data-ttu-id="a529c-143">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="a529c-143">-TemplateFile</span></span>
<span data-ttu-id="a529c-144">디스크에 있는 ARM 서식 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-144">Location of the ARM template file on disk.</span></span>

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

### <span data-ttu-id="a529c-145">-서식 파일 Parameterfile</span><span class="sxs-lookup"><span data-stu-id="a529c-145">-TemplateParameterFile</span></span>
<span data-ttu-id="a529c-146">디스크에 있는 ARM template 매개 변수 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-146">Location of the ARM template parameter file on disk.</span></span>

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

### <span data-ttu-id="a529c-147">-Type</span><span class="sxs-lookup"><span data-stu-id="a529c-147">-Type</span></span>
<span data-ttu-id="a529c-148">아티팩트의 유형입니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-148">Type of the artifact.</span></span>
<span data-ttu-id="a529c-149">지원 되는 형식에는 RoleAssignmentArtifact, PolicyAssignmentArtifact, 서식 가공물 등 3 가지가 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-149">There are 3 types supported: RoleAssignmentArtifact, PolicyAssignmentArtifact, TemplateArtifact.</span></span>

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

### <span data-ttu-id="a529c-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a529c-150">CommonParameters</span></span>
<span data-ttu-id="a529c-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a529c-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span>
<span data-ttu-id="a529c-152">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a529c-152">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a529c-153">입력</span><span class="sxs-lookup"><span data-stu-id="a529c-153">INPUTS</span></span>

### <span data-ttu-id="a529c-154">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="a529c-154">System.String</span></span>

### <span data-ttu-id="a529c-155">Microsoft. i a m. 모델. PSArtifactKind</span><span class="sxs-lookup"><span data-stu-id="a529c-155">Microsoft.Azure.Commands.Blueprint.Models.PSArtifactKind</span></span>

### <span data-ttu-id="a529c-156">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="a529c-156">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="a529c-157">System.webserver. List ' 1 [[System. String, mscorlib, Version = 4.0.0.0, Culture = 중립, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="a529c-157">System.Collections.Generic.List\`1[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

### <span data-ttu-id="a529c-158">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="a529c-158">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a529c-159">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="a529c-159">System.String[]</span></span>

## <span data-ttu-id="a529c-160">출력</span><span class="sxs-lookup"><span data-stu-id="a529c-160">OUTPUTS</span></span>

### <span data-ttu-id="a529c-161">Microsoft. Azure.. i a n. 아티팩트</span><span class="sxs-lookup"><span data-stu-id="a529c-161">Microsoft.Azure.Management.Blueprint.Models.Artifact</span></span>

## <span data-ttu-id="a529c-162">상속자</span><span class="sxs-lookup"><span data-stu-id="a529c-162">NOTES</span></span>

## <span data-ttu-id="a529c-163">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a529c-163">RELATED LINKS</span></span>
