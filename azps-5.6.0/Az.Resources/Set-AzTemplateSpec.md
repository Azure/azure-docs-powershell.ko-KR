---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: 48a700f29a80b03df0fd4fc2d858dcb1c1c57f76
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101982176"
---
# <span data-ttu-id="e2504-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e2504-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="e2504-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2504-102">SYNOPSIS</span></span>
<span data-ttu-id="e2504-103">템플릿 사양을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="e2504-104">구문</span><span class="sxs-lookup"><span data-stu-id="e2504-104">SYNTAX</span></span>

### <span data-ttu-id="e2504-105">FromJsonStringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e2504-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2504-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2504-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2504-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2504-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-Tag <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2504-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e2504-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="e2504-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e2504-112">설명</span><span class="sxs-lookup"><span data-stu-id="e2504-112">DESCRIPTION</span></span>
<span data-ttu-id="e2504-113">Templace 사양을 수정합니다. 지정된 이름 및/또는 특정 버전이 있는 템플릿 사양이 아직 없는 경우 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="e2504-114">템플릿 사양 버전의 템플릿 ARM 수정할 때 콘텐츠는 원시 JSON **문자열(UpdateVersionByNameFromJsonParameterSet** 매개 변수 집합 사용) 또는 지정된 JSON **파일(UpdateVersionByNameFromJsonFileParameterSet** 매개 변수 집합 사용)에서 올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="e2504-115">예제</span><span class="sxs-lookup"><span data-stu-id="e2504-115">EXAMPLES</span></span>

### <span data-ttu-id="e2504-116">예제 1:</span><span class="sxs-lookup"><span data-stu-id="e2504-116">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="e2504-117">"myTemplateSpec"라는 템플릿 사양의 버전 "v1.0"을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e2504-118">지정된 버전은 $templateJson 템플릿 콘텐츠로 ARM 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="e2504-119">루트 템플릿 사양 및/또는 버전이 아직 없는 경우 해당 템플릿이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="e2504-120">**참고 사항:**</span><span class="sxs-lookup"><span data-stu-id="e2504-120">**Notes:**</span></span> 

* <span data-ttu-id="e2504-121">예제의 ARM 템플릿은 실제 리소스를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="e2504-122">위치는 템플릿 사양이 아직 없는 경우만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e2504-123">예제 2:</span><span class="sxs-lookup"><span data-stu-id="e2504-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="e2504-124">"myTemplateSpec"라는 템플릿 사양의 버전 "v2.0"을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="e2504-125">지정된 버전에는 로컬 파일 "myTemplateContent.js"의 콘텐츠가 버전의 템플릿 ARM 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="e2504-126">루트 템플릿 사양 및/또는 버전이 아직 없는 경우 해당 템플릿이 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="e2504-127">**참고:** 위치는 템플릿 사양이 아직 없는 경우만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="e2504-128">예제 3:</span><span class="sxs-lookup"><span data-stu-id="e2504-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="e2504-129">리소스 그룹 "myRG"에서 "myTemplateSpec"이라는 템플릿 사양에 대한 설명을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="e2504-130">템플릿 사양이 아직 없는 경우 생성됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="e2504-131">**참고:** 위치는 템플릿 사양이 아직 없는 경우만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="e2504-132">매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2504-132">PARAMETERS</span></span>

### <span data-ttu-id="e2504-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2504-133">-DefaultProfile</span></span>
<span data-ttu-id="e2504-134">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2504-135">-Description</span><span class="sxs-lookup"><span data-stu-id="e2504-135">-Description</span></span>
<span data-ttu-id="e2504-136">템플릿 사양에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-136">The description of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e2504-137">-DisplayName</span></span>
<span data-ttu-id="e2504-138">템플릿 사양의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-138">The display name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-139">-Location</span><span class="sxs-lookup"><span data-stu-id="e2504-139">-Location</span></span>
<span data-ttu-id="e2504-140">템플릿 사양의 위치입니다. 템플릿 사양이 아직 없는 경우만 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-141">-Name</span><span class="sxs-lookup"><span data-stu-id="e2504-141">-Name</span></span>
<span data-ttu-id="e2504-142">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-142">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e2504-143">-ResourceGroupName</span></span>
<span data-ttu-id="e2504-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-144">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByNameParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="e2504-145">-ResourceId</span></span>
<span data-ttu-id="e2504-146">템플릿 사양의 완전히 자격을 갖춘 리소스 ID입니다. 예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="e2504-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateByIdParameterSet, UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-147">-Tag</span><span class="sxs-lookup"><span data-stu-id="e2504-147">-Tag</span></span>
<span data-ttu-id="e2504-148">템플릿 사양 및/또는 버전에 대한 태그 해시테이블</span><span class="sxs-lookup"><span data-stu-id="e2504-148">Hashtable of tags for the template spec and/or version</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-149">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="e2504-149">-TemplateFile</span></span>
<span data-ttu-id="e2504-150">로컬 Azure Resource Manager 템플릿 JSON 파일에 대한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-150">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByNameFromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-151">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="e2504-151">-TemplateJson</span></span>
<span data-ttu-id="e2504-152">Azure Resource Manager 템플릿 JSON입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-152">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-153">-Version</span><span class="sxs-lookup"><span data-stu-id="e2504-153">-Version</span></span>
<span data-ttu-id="e2504-154">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-154">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-155">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="e2504-155">-VersionDescription</span></span>
<span data-ttu-id="e2504-156">버전에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-156">The description of the version.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateVersionByIdFromJsonFileParameterSet, UpdateVersionByIdFromJsonParameterSet, UpdateVersionByNameFromJsonFileParameterSet, UpdateVersionByNameFromJsonParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2504-157">-확인</span><span class="sxs-lookup"><span data-stu-id="e2504-157">-Confirm</span></span>
<span data-ttu-id="e2504-158">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-158">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2504-159">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2504-159">-WhatIf</span></span>
<span data-ttu-id="e2504-160">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-160">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e2504-161">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-161">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2504-162">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2504-162">CommonParameters</span></span>
<span data-ttu-id="e2504-163">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e2504-163">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2504-164">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="e2504-164">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2504-165">입력</span><span class="sxs-lookup"><span data-stu-id="e2504-165">INPUTS</span></span>

### <span data-ttu-id="e2504-166">System.String</span><span class="sxs-lookup"><span data-stu-id="e2504-166">System.String</span></span>

## <span data-ttu-id="e2504-167">출력</span><span class="sxs-lookup"><span data-stu-id="e2504-167">OUTPUTS</span></span>

### <span data-ttu-id="e2504-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="e2504-168">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="e2504-169">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e2504-169">NOTES</span></span>

## <span data-ttu-id="e2504-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2504-170">RELATED LINKS</span></span>
