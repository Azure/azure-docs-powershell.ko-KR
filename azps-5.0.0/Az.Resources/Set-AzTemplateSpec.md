---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzTemplateSpec.md
ms.openlocfilehash: ff2911c1fd8e49e5057c13c086f68a2b3489ad2f
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217038"
---
# <span data-ttu-id="0b5da-101">Set-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="0b5da-101">Set-AzTemplateSpec</span></span>

## <span data-ttu-id="0b5da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0b5da-102">SYNOPSIS</span></span>
<span data-ttu-id="0b5da-103">템플릿 사양을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-103">Modifies a Template Spec.</span></span>

## <span data-ttu-id="0b5da-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0b5da-104">SYNTAX</span></span>

### <span data-ttu-id="0b5da-105">FromJsonStringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="0b5da-105">FromJsonStringParameterSet (Default)</span></span>
```
Set-AzTemplateSpec [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="0b5da-106">UpdateByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-106">UpdateByIdParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> [-Description <String>] [-DisplayName <String>] [-Location <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5da-107">UpdateVersionByIdFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-107">UpdateVersionByIdFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5da-108">UpdateVersionByIdFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-108">UpdateVersionByIdFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceId <String> -Version <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5da-109">UpdateByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-109">UpdateByNameParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> [-Description <String>] [-DisplayName <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5da-110">UpdateVersionByNameFromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-110">UpdateVersionByNameFromJsonFileParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0b5da-111">UpdateVersionByNameFromJsonParameterSet</span><span class="sxs-lookup"><span data-stu-id="0b5da-111">UpdateVersionByNameFromJsonParameterSet</span></span>
```
Set-AzTemplateSpec -ResourceGroupName <String> -Name <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0b5da-112">설명은</span><span class="sxs-lookup"><span data-stu-id="0b5da-112">DESCRIPTION</span></span>
<span data-ttu-id="0b5da-113">Templace 사양을 수정 합니다. 지정 된 이름 및/또는 특정 버전의 템플릿 사양이 아직 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-113">Modifies a Templace Spec. If the Template Spec with the specified name and/or specific version does not already exist, it will be created.</span></span>

<span data-ttu-id="0b5da-114">템플릿 사양 버전의 ARM Template 콘텐츠를 수정 하는 경우, **UpdateVersionByNameFromJsonParameterSet** 매개 변수 집합을 사용 하는 원시 json 문자열 또는 **UpdateVersionByNameFromJsonFileParameterSet** 매개 변수 집합을 사용 하 여 지정 된 JSON 파일에서 콘텐츠를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-114">When modifying a Template Spec version's ARM Template content, the content can either come from a raw JSON string (using **UpdateVersionByNameFromJsonParameterSet** parameter set) or from a specified JSON file (using **UpdateVersionByNameFromJsonFileParameterSet** parameter set).</span></span>

## <span data-ttu-id="0b5da-115">예제의</span><span class="sxs-lookup"><span data-stu-id="0b5da-115">EXAMPLES</span></span>

### <span data-ttu-id="0b5da-116">예제 1:</span><span class="sxs-lookup"><span data-stu-id="0b5da-116">Example 1:</span></span>
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

<span data-ttu-id="0b5da-117">"MyTemplateSpec" 라는 서식 파일 사양의 버전 "v 1.0"을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-117">Modifies version "v1.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="0b5da-118">지정 된 버전에는 버전의 ARM 서식 파일과의 $templateJson이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-118">The specified version will have $templateJson as the version's ARM Template content.</span></span> <span data-ttu-id="0b5da-119">루트 템플릿 사양 및/또는 버전이 아직 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-119">If the root Template Spec and/or version do not already exist they will be created.</span></span>


<span data-ttu-id="0b5da-120">**상속자**</span><span class="sxs-lookup"><span data-stu-id="0b5da-120">**Notes:**</span></span> 

* <span data-ttu-id="0b5da-121">이 예제의 ARM 템플릿은 실제 리소스를 포함 하지 않으므로 op입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-121">The ARM Template in the example is a no-op as it contains no actual resources.</span></span>
* <span data-ttu-id="0b5da-122">위치는 템플릿 사양이 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-122">Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="0b5da-123">예제 2:</span><span class="sxs-lookup"><span data-stu-id="0b5da-123">Example 2:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="0b5da-124">"MyTemplateSpec" 라는 서식 파일 사양의 버전 "v 2.0"을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-124">Modifies version "v2.0" of a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="0b5da-125">지정 된 버전에는 로컬 파일 "myTemplateContent.json"의 콘텐츠가 버전의 암 서식 파일 내용으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-125">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span> <span data-ttu-id="0b5da-126">루트 템플릿 사양 및/또는 버전이 아직 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-126">If the root Template Spec and/or version do not already exist they will be created.</span></span>

<span data-ttu-id="0b5da-127">**참고:** 위치는 템플릿 사양이 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-127">**Note:** Location is only required when the Template Spec does not already exist</span></span>

### <span data-ttu-id="0b5da-128">예제 3:</span><span class="sxs-lookup"><span data-stu-id="0b5da-128">Example 3:</span></span>
```powershell
PS C:\> Set-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec'  -Location 'West US' -Description 'My updated Template Spec'
```

<span data-ttu-id="0b5da-129">"MyRG" 리소스 그룹에서 "myTemplateSpec" 라는 템플릿 사양의 설명을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-129">Modifies the description of the Template Spec named "myTemplateSpec" in resource group "myRG".</span></span> <span data-ttu-id="0b5da-130">템플릿 사양이 아직 없는 경우 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-130">If the Template Spec does not already exist it will be created.</span></span>

<span data-ttu-id="0b5da-131">**참고:** 위치는 템플릿 사양이 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-131">**Note:** Location is only required when the Template Spec does not already exist</span></span>

## <span data-ttu-id="0b5da-132">변수</span><span class="sxs-lookup"><span data-stu-id="0b5da-132">PARAMETERS</span></span>

### <span data-ttu-id="0b5da-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0b5da-133">-DefaultProfile</span></span>
<span data-ttu-id="0b5da-134">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-134">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0b5da-135">-설명</span><span class="sxs-lookup"><span data-stu-id="0b5da-135">-Description</span></span>
<span data-ttu-id="0b5da-136">서식 파일 사양에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-136">The description of the template spec.</span></span>

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

### <span data-ttu-id="0b5da-137">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0b5da-137">-DisplayName</span></span>
<span data-ttu-id="0b5da-138">템플릿 사양의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-138">The display name of the template spec.</span></span>

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

### <span data-ttu-id="0b5da-139">-위치</span><span class="sxs-lookup"><span data-stu-id="0b5da-139">-Location</span></span>
<span data-ttu-id="0b5da-140">템플릿 사양의 위치입니다. 템플릿 사양이 아직 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-140">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="0b5da-141">-이름</span><span class="sxs-lookup"><span data-stu-id="0b5da-141">-Name</span></span>
<span data-ttu-id="0b5da-142">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-142">The name of the template spec.</span></span>

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

### <span data-ttu-id="0b5da-143">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0b5da-143">-ResourceGroupName</span></span>
<span data-ttu-id="0b5da-144">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-144">The name of the resource group.</span></span>

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

### <span data-ttu-id="0b5da-145">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="0b5da-145">-ResourceId</span></span>
<span data-ttu-id="0b5da-146">템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="0b5da-146">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="0b5da-147">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="0b5da-147">-TemplateFile</span></span>
<span data-ttu-id="0b5da-148">로컬 Azure 리소스 관리자 템플릿 JSON 파일에 대 한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-148">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="0b5da-149">-서식 기능 Json</span><span class="sxs-lookup"><span data-stu-id="0b5da-149">-TemplateJson</span></span>
<span data-ttu-id="0b5da-150">Azure Resource Manager 템플릿 JSON.</span><span class="sxs-lookup"><span data-stu-id="0b5da-150">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="0b5da-151">-버전</span><span class="sxs-lookup"><span data-stu-id="0b5da-151">-Version</span></span>
<span data-ttu-id="0b5da-152">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-152">The version of the template spec.</span></span>

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

### <span data-ttu-id="0b5da-153">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="0b5da-153">-VersionDescription</span></span>
<span data-ttu-id="0b5da-154">버전에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-154">The description of the version.</span></span>

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

### <span data-ttu-id="0b5da-155">-확인</span><span class="sxs-lookup"><span data-stu-id="0b5da-155">-Confirm</span></span>
<span data-ttu-id="0b5da-156">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-156">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0b5da-157">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0b5da-157">-WhatIf</span></span>
<span data-ttu-id="0b5da-158">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-158">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="0b5da-159">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-159">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0b5da-160">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0b5da-160">CommonParameters</span></span>
<span data-ttu-id="0b5da-161">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0b5da-161">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0b5da-162">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="0b5da-162">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0b5da-163">입력</span><span class="sxs-lookup"><span data-stu-id="0b5da-163">INPUTS</span></span>

### <span data-ttu-id="0b5da-164">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="0b5da-164">System.String</span></span>

## <span data-ttu-id="0b5da-165">출력</span><span class="sxs-lookup"><span data-stu-id="0b5da-165">OUTPUTS</span></span>

### <span data-ttu-id="0b5da-166">SdkModels. PSTemplateSpec에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="0b5da-166">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="0b5da-167">상속자</span><span class="sxs-lookup"><span data-stu-id="0b5da-167">NOTES</span></span>

## <span data-ttu-id="0b5da-168">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0b5da-168">RELATED LINKS</span></span>
