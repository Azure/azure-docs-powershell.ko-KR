---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: 2d0eb49a46e0d6fbbe02d145e42195d059c5176f
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100201881"
---
# <span data-ttu-id="dc2de-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="dc2de-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="dc2de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc2de-102">SYNOPSIS</span></span>
<span data-ttu-id="dc2de-103">새 템플릿 사양을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="dc2de-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc2de-104">SYNTAX</span></span>

### <span data-ttu-id="dc2de-105">FromJsonStringParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc2de-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateJson <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="dc2de-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc2de-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] [-Tag <Hashtable>] -TemplateFile <String>
 [-VersionDescription <String>] [-Force] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="dc2de-107">설명</span><span class="sxs-lookup"><span data-stu-id="dc2de-107">DESCRIPTION</span></span>
<span data-ttu-id="dc2de-108">지정된 템플릿 콘텐츠로 새 템플릿 사양 ARM 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="dc2de-109">콘텐츠는 원시 JSON **문자열(FromJsonStringParameterSet** 매개 변수 집합 사용) 또는 지정된 JSON **파일(FromJsonFileParameterSet** 매개 변수 집합 사용)에서 올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="dc2de-110">루트 템플릿 사양이 아직 없는 경우 템플릿 사양 버전과 함께 만들어집니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="dc2de-111">지정된 이름의 템플릿 사양이 이미 있는 경우 지정한 버전이 업데이트됩니다(다른 기존 버전은 보존됩니다).</span><span class="sxs-lookup"><span data-stu-id="dc2de-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="dc2de-112">예제</span><span class="sxs-lookup"><span data-stu-id="dc2de-112">EXAMPLES</span></span>

### <span data-ttu-id="dc2de-113">예제 1:</span><span class="sxs-lookup"><span data-stu-id="dc2de-113">Example 1:</span></span>
```powershell
PS C:\> $templateJson = @"
{
    "$schema": "http://schema.management.azure.com/schemas/2015-01-01/deploymentTemplate.json#",
    "contentVersion": "1.0.0.0",
    "parameters": {},
    "resources": []
}
"@
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v1.0' -Location 'West US' -TemplateJson $templateJson
```

<span data-ttu-id="dc2de-114">"myTemplateSpec"라는 템플릿 사양에 새 템플릿 사양 버전 "v1.0"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="dc2de-115">지정된 버전은 $templateJson 템플릿 콘텐츠로 ARM 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="dc2de-116">**참고:** 예제의 ARM 템플릿은 실제 리소스를 포함하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="dc2de-117">예제 2:</span><span class="sxs-lookup"><span data-stu-id="dc2de-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="dc2de-118">"myTemplateSpec"라는 템플릿 사양에 새 템플릿 사양 버전 "v2.0"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="dc2de-119">지정된 버전은 로컬 파일 "myTemplateContent.json"의 콘텐츠를 해당 ARM 템플릿 콘텐츠로 하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="dc2de-120">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="dc2de-120">PARAMETERS</span></span>

### <span data-ttu-id="dc2de-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc2de-121">-DefaultProfile</span></span>
<span data-ttu-id="dc2de-122">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="dc2de-123">-Description</span><span class="sxs-lookup"><span data-stu-id="dc2de-123">-Description</span></span>
<span data-ttu-id="dc2de-124">템플릿 사양에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="dc2de-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc2de-125">-DisplayName</span></span>
<span data-ttu-id="dc2de-126">템플릿 사양의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="dc2de-127">-Force</span><span class="sxs-lookup"><span data-stu-id="dc2de-127">-Force</span></span>
<span data-ttu-id="dc2de-128">기존 버전을 덮어 사용할 때 확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="dc2de-129">-Location</span><span class="sxs-lookup"><span data-stu-id="dc2de-129">-Location</span></span>
<span data-ttu-id="dc2de-130">템플릿 사양의 위치입니다. 템플릿 사양이 아직 없는 경우 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="dc2de-131">-Name</span><span class="sxs-lookup"><span data-stu-id="dc2de-131">-Name</span></span>
<span data-ttu-id="dc2de-132">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-132">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2de-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dc2de-133">-ResourceGroupName</span></span>
<span data-ttu-id="dc2de-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-134">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2de-135">-Tag</span><span class="sxs-lookup"><span data-stu-id="dc2de-135">-Tag</span></span>
<span data-ttu-id="dc2de-136">새 템플릿 사양 리소스에 대한 태그의 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-136">Hashtable of tags for the new template spec resource(s).</span></span>

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

### <span data-ttu-id="dc2de-137">-TemplateFile</span><span class="sxs-lookup"><span data-stu-id="dc2de-137">-TemplateFile</span></span>
<span data-ttu-id="dc2de-138">로컬 Azure Resource Manager 템플릿 JSON 파일에 대한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-138">The file path to the local Azure Resource Manager template JSON file.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonFileParameterSet
Aliases: InputFile

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2de-139">-TemplateJson</span><span class="sxs-lookup"><span data-stu-id="dc2de-139">-TemplateJson</span></span>
<span data-ttu-id="dc2de-140">Azure Resource Manager 템플릿 JSON입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-140">The Azure Resource Manager template JSON.</span></span>

```yaml
Type: System.String
Parameter Sets: FromJsonStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc2de-141">-Version</span><span class="sxs-lookup"><span data-stu-id="dc2de-141">-Version</span></span>
<span data-ttu-id="dc2de-142">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-142">The version of the template spec.</span></span>

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

### <span data-ttu-id="dc2de-143">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="dc2de-143">-VersionDescription</span></span>
<span data-ttu-id="dc2de-144">버전에 대한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-144">The description of the version.</span></span>

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

### <span data-ttu-id="dc2de-145">-Confirm</span><span class="sxs-lookup"><span data-stu-id="dc2de-145">-Confirm</span></span>
<span data-ttu-id="dc2de-146">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-146">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="dc2de-147">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="dc2de-147">-WhatIf</span></span>
<span data-ttu-id="dc2de-148">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="dc2de-148">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="dc2de-149">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-149">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="dc2de-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc2de-150">CommonParameters</span></span>
<span data-ttu-id="dc2de-151">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc2de-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc2de-152">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="dc2de-152">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc2de-153">입력</span><span class="sxs-lookup"><span data-stu-id="dc2de-153">INPUTS</span></span>

### <span data-ttu-id="dc2de-154">System.String</span><span class="sxs-lookup"><span data-stu-id="dc2de-154">System.String</span></span>

## <span data-ttu-id="dc2de-155">출력</span><span class="sxs-lookup"><span data-stu-id="dc2de-155">OUTPUTS</span></span>

### <span data-ttu-id="dc2de-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="dc2de-156">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="dc2de-157">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc2de-157">NOTES</span></span>

## <span data-ttu-id="dc2de-158">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc2de-158">RELATED LINKS</span></span>
