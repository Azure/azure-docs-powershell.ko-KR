---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/export-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Export-AzTemplateSpec.md
ms.openlocfilehash: eb6311dacd05f539cf508657e52637524ea98ea7
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101974480"
---
# <span data-ttu-id="40290-101">Export-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="40290-101">Export-AzTemplateSpec</span></span>

## <span data-ttu-id="40290-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40290-102">SYNOPSIS</span></span>
<span data-ttu-id="40290-103">템플릿 사양을 로컬 파일로 내보내기</span><span class="sxs-lookup"><span data-stu-id="40290-103">Exports a Template Spec to the local filesystem</span></span>

## <span data-ttu-id="40290-104">구문</span><span class="sxs-lookup"><span data-stu-id="40290-104">SYNTAX</span></span>

### <span data-ttu-id="40290-105">ExportByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="40290-105">ExportByNameParameterSet (Default)</span></span>
```
Export-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="40290-106">ExportByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="40290-106">ExportByIdParameterSet</span></span>
```
Export-AzTemplateSpec [-ResourceId] <String> -Version <String> -OutputFolder <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="40290-107">설명</span><span class="sxs-lookup"><span data-stu-id="40290-107">DESCRIPTION</span></span>
<span data-ttu-id="40290-108">특정 템플릿 사양 버전을 로컬 파일로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40290-108">Exports a specific Template Spec version to the local filesystem.</span></span>

## <span data-ttu-id="40290-109">예제</span><span class="sxs-lookup"><span data-stu-id="40290-109">EXAMPLES</span></span>

### <span data-ttu-id="40290-110">예제 1: 이름으로 내보내기</span><span class="sxs-lookup"><span data-stu-id="40290-110">Example 1: Export by name</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="40290-111">리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'을 로컬 출력 폴더 "v1"로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40290-111">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' to the local output folder "v1".</span></span>

### <span data-ttu-id="40290-112">예제 2: 리소스 ID로 내보내기</span><span class="sxs-lookup"><span data-stu-id="40290-112">Example 2: Export by resource id</span></span>
```powershell
PS C:\> Export-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0' -OutputFolder 'v1'
```

<span data-ttu-id="40290-113">구독 하위 하위의 리소스 그룹 내에서 'MyTemplateSpec'라는 템플릿 사양의 버전 'v1.0'을 로컬 출력 폴더 \{ \} "v1"으로 내보낼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="40290-113">Exports version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\} to the local output folder "v1".</span></span>

## <span data-ttu-id="40290-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40290-114">PARAMETERS</span></span>

### <span data-ttu-id="40290-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40290-115">-DefaultProfile</span></span>
<span data-ttu-id="40290-116">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40290-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40290-117">-Name</span><span class="sxs-lookup"><span data-stu-id="40290-117">-Name</span></span>
<span data-ttu-id="40290-118">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40290-118">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40290-119">-OutputFolder</span><span class="sxs-lookup"><span data-stu-id="40290-119">-OutputFolder</span></span>
<span data-ttu-id="40290-120">템플릿 사양 버전이 출력될 폴더의 경로입니다.</span><span class="sxs-lookup"><span data-stu-id="40290-120">The path to the folder where the template spec version will be output to.</span></span>

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

### <span data-ttu-id="40290-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40290-121">-ResourceGroupName</span></span>
<span data-ttu-id="40290-122">템플릿 사양의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40290-122">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40290-123">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="40290-123">-ResourceId</span></span>
<span data-ttu-id="40290-124">템플릿 사양의 완전히 자격을 갖춘 리소스 ID입니다. 예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="40290-124">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: ExportByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="40290-125">-Version</span><span class="sxs-lookup"><span data-stu-id="40290-125">-Version</span></span>
<span data-ttu-id="40290-126">내보낼 템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="40290-126">The version of the template spec to export.</span></span>

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

### <span data-ttu-id="40290-127">-확인</span><span class="sxs-lookup"><span data-stu-id="40290-127">-Confirm</span></span>
<span data-ttu-id="40290-128">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="40290-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="40290-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="40290-129">-WhatIf</span></span>
<span data-ttu-id="40290-130">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="40290-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="40290-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40290-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="40290-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40290-132">CommonParameters</span></span>
<span data-ttu-id="40290-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40290-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40290-134">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="40290-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40290-135">입력</span><span class="sxs-lookup"><span data-stu-id="40290-135">INPUTS</span></span>

### <span data-ttu-id="40290-136">System.String</span><span class="sxs-lookup"><span data-stu-id="40290-136">System.String</span></span>

## <span data-ttu-id="40290-137">출력</span><span class="sxs-lookup"><span data-stu-id="40290-137">OUTPUTS</span></span>

### <span data-ttu-id="40290-138">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="40290-138">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="40290-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40290-139">NOTES</span></span>

## <span data-ttu-id="40290-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40290-140">RELATED LINKS</span></span>
