---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzTemplateSpec.md
ms.openlocfilehash: b19653570c7bfbf62cb94107bb2fa354a9fda3f1
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94217041"
---
# <span data-ttu-id="4e5b2-101">New-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="4e5b2-101">New-AzTemplateSpec</span></span>

## <span data-ttu-id="4e5b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e5b2-102">SYNOPSIS</span></span>
<span data-ttu-id="4e5b2-103">새 템플릿 사양을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-103">Creates a new Template Spec.</span></span>

## <span data-ttu-id="4e5b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e5b2-104">SYNTAX</span></span>

### <span data-ttu-id="4e5b2-105">FromJsonStringParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="4e5b2-105">FromJsonStringParameterSet (Default)</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateJson <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="4e5b2-106">FromJsonFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="4e5b2-106">FromJsonFileParameterSet</span></span>
```
New-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> [-Description <String>]
 [-DisplayName <String>] [-Location <String>] -TemplateFile <String> [-VersionDescription <String>] [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="4e5b2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4e5b2-107">DESCRIPTION</span></span>
<span data-ttu-id="4e5b2-108">지정 된 팔 템플릿 콘텐츠를 사용 하 여 새 템플릿 사양 버전을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-108">Creates a new Template Spec version with the specified ARM Template content.</span></span> <span data-ttu-id="4e5b2-109">**FromJsonStringParameterSet** 매개 변수 집합을 사용 하는 원시 json 문자열 또는 **FromJsonFileParameterSet** 매개 변수 집합을 사용 하 여 지정 된 JSON 파일에서 콘텐츠를 얻을 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-109">The content can either come from a raw JSON string (using **FromJsonStringParameterSet** parameter set) or from a specified JSON file (using **FromJsonFileParameterSet** parameter set).</span></span>  

<span data-ttu-id="4e5b2-110">루트 템플릿 사양이 아직 없는 경우 템플릿 사양 버전과 함께 생성 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-110">If the root Template Spec does not already exist it will be created along with the Template Spec version.</span></span> <span data-ttu-id="4e5b2-111">지정 된 이름을 사용 하 여 템플릿 사양이 이미 존재 하는 경우, 지정 된 버전이 업데이트 됩니다 (다른 모든 기존 버전이 보존 됨).</span><span class="sxs-lookup"><span data-stu-id="4e5b2-111">If a Template Spec already exists with the given name, it and the specified version will be updated (any other existing versions will be preserved).</span></span>

## <span data-ttu-id="4e5b2-112">예제의</span><span class="sxs-lookup"><span data-stu-id="4e5b2-112">EXAMPLES</span></span>

### <span data-ttu-id="4e5b2-113">예제 1:</span><span class="sxs-lookup"><span data-stu-id="4e5b2-113">Example 1:</span></span>
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

<span data-ttu-id="4e5b2-114">"MyTemplateSpec" 라는 템플릿 사양에 새 템플릿 사양 버전 "v 1.0"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-114">Creates a new Template Spec version "v1.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="4e5b2-115">지정 된 버전에는 버전의 ARM 서식 파일과의 $templateJson이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-115">The specified version will have $templateJson as the version's ARM Template content.</span></span>

 <span data-ttu-id="4e5b2-116">**참고:** 이 예제의 ARM 템플릿은 실제 리소스를 포함 하지 않으므로 op입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-116">**Note:** The ARM Template in the example is a no-op as it contains no actual resources.</span></span>

### <span data-ttu-id="4e5b2-117">예제 2:</span><span class="sxs-lookup"><span data-stu-id="4e5b2-117">Example 2:</span></span>
```powershell
PS C:\> New-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'myTemplateSpec' -Version 'v2.0' -Location 'West US' -TemplateFile 'myTemplateContent.json'
```

<span data-ttu-id="4e5b2-118">"MyTemplateSpec" 라는 템플릿 사양에 새 템플릿 사양 버전 "v 2.0"을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-118">Creates a new Template Spec version "v2.0" in a Template Spec named "myTemplateSpec".</span></span> <span data-ttu-id="4e5b2-119">지정 된 버전에는 로컬 파일 "myTemplateContent.json"의 콘텐츠가 버전의 암 서식 파일 내용으로 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-119">The specified version will have the content from the local file "myTemplateContent.json" as the version's ARM Template content.</span></span>

## <span data-ttu-id="4e5b2-120">변수</span><span class="sxs-lookup"><span data-stu-id="4e5b2-120">PARAMETERS</span></span>

### <span data-ttu-id="4e5b2-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e5b2-121">-DefaultProfile</span></span>
<span data-ttu-id="4e5b2-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4e5b2-123">-설명</span><span class="sxs-lookup"><span data-stu-id="4e5b2-123">-Description</span></span>
<span data-ttu-id="4e5b2-124">서식 파일 사양에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-124">The description of the template spec.</span></span>

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

### <span data-ttu-id="4e5b2-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="4e5b2-125">-DisplayName</span></span>
<span data-ttu-id="4e5b2-126">템플릿 사양의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-126">The display name of the template spec.</span></span>

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

### <span data-ttu-id="4e5b2-127">-Force</span><span class="sxs-lookup"><span data-stu-id="4e5b2-127">-Force</span></span>
<span data-ttu-id="4e5b2-128">기존 버전을 덮어쓸 때 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-128">Do not ask for confirmation when overwriting an existing version.</span></span>

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

### <span data-ttu-id="4e5b2-129">-위치</span><span class="sxs-lookup"><span data-stu-id="4e5b2-129">-Location</span></span>
<span data-ttu-id="4e5b2-130">템플릿 사양의 위치입니다. 템플릿 사양이 아직 없는 경우에만 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-130">The location of the template spec. Only required if the template spec does not already exist.</span></span>

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

### <span data-ttu-id="4e5b2-131">-이름</span><span class="sxs-lookup"><span data-stu-id="4e5b2-131">-Name</span></span>
<span data-ttu-id="4e5b2-132">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-132">The name of the template spec.</span></span>

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

### <span data-ttu-id="4e5b2-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4e5b2-133">-ResourceGroupName</span></span>
<span data-ttu-id="4e5b2-134">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-134">The name of the resource group.</span></span>

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

### <span data-ttu-id="4e5b2-135">-서식 파일</span><span class="sxs-lookup"><span data-stu-id="4e5b2-135">-TemplateFile</span></span>
<span data-ttu-id="4e5b2-136">로컬 Azure 리소스 관리자 템플릿 JSON 파일에 대 한 파일 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-136">The file path to the local Azure Resource Manager template JSON file.</span></span>

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

### <span data-ttu-id="4e5b2-137">-서식 기능 Json</span><span class="sxs-lookup"><span data-stu-id="4e5b2-137">-TemplateJson</span></span>
<span data-ttu-id="4e5b2-138">Azure Resource Manager 템플릿 JSON.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-138">The Azure Resource Manager template JSON.</span></span>

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

### <span data-ttu-id="4e5b2-139">-버전</span><span class="sxs-lookup"><span data-stu-id="4e5b2-139">-Version</span></span>
<span data-ttu-id="4e5b2-140">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-140">The version of the template spec.</span></span>

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

### <span data-ttu-id="4e5b2-141">-VersionDescription</span><span class="sxs-lookup"><span data-stu-id="4e5b2-141">-VersionDescription</span></span>
<span data-ttu-id="4e5b2-142">버전에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-142">The description of the version.</span></span>

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

### <span data-ttu-id="4e5b2-143">-확인</span><span class="sxs-lookup"><span data-stu-id="4e5b2-143">-Confirm</span></span>
<span data-ttu-id="4e5b2-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="4e5b2-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="4e5b2-145">-WhatIf</span></span>
<span data-ttu-id="4e5b2-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-146">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="4e5b2-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="4e5b2-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e5b2-148">CommonParameters</span></span>
<span data-ttu-id="4e5b2-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e5b2-150">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="4e5b2-150">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e5b2-151">입력</span><span class="sxs-lookup"><span data-stu-id="4e5b2-151">INPUTS</span></span>

### <span data-ttu-id="4e5b2-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="4e5b2-152">System.String</span></span>

## <span data-ttu-id="4e5b2-153">출력</span><span class="sxs-lookup"><span data-stu-id="4e5b2-153">OUTPUTS</span></span>

### <span data-ttu-id="4e5b2-154">SdkModels. PSTemplateSpec에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="4e5b2-154">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="4e5b2-155">상속자</span><span class="sxs-lookup"><span data-stu-id="4e5b2-155">NOTES</span></span>

## <span data-ttu-id="4e5b2-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e5b2-156">RELATED LINKS</span></span>
