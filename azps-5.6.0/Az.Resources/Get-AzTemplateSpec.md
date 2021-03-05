---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: 0b2018eecc081f2fcee5da63ed17cc2e01486777
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101960112"
---
# <span data-ttu-id="56fa2-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="56fa2-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="56fa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="56fa2-102">SYNOPSIS</span></span>
<span data-ttu-id="56fa2-103">템플릿 사양을 얻거나 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="56fa2-104">구문</span><span class="sxs-lookup"><span data-stu-id="56fa2-104">SYNTAX</span></span>

### <span data-ttu-id="56fa2-105">ListTemplateSpecsParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="56fa2-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="56fa2-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="56fa2-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="56fa2-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="56fa2-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="56fa2-108">설명</span><span class="sxs-lookup"><span data-stu-id="56fa2-108">DESCRIPTION</span></span>
<span data-ttu-id="56fa2-109">이 cmdlet은 구독/리소스 그룹에 템플릿 사양을 나열하거나 이름 또는 ID로 특정 템플릿 사양을 얻을 때 사용할 수 있습니다. 특정 템플릿 사양을 이름/id로 가져올 때 **선택적으로 -Version** 매개 변수를 통해 버전 이름을 지정하여 특정 버전을 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="56fa2-110">**-Version을** 사용하는 경우 특정 버전 세부 정보만 \* 에 *존재합니다. 반환된* 템플릿 사양 개체의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-110">When **-Version** is used, only the specific version details will be present within \**.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="56fa2-111">템플릿 사양을 이름/id로 검색할 때 특정 버전이 지정되지 않으면 모든 버전이 \* 에 *표시됩니다. 반환된* 개체의 버전 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \**.Versions* property of the returned object.</span></span>

<span data-ttu-id="56fa2-112">**참고**: 구독 또는 리소스 그룹 내에서 모든 템플릿 사양을 나열할 때 반환된 템플릿 사양 *"입니다. 버전"* 속성은 *null입니다.*</span><span class="sxs-lookup"><span data-stu-id="56fa2-112">**Note**: When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="56fa2-113">버전 정보는 -Name 또는 -ResourceId 매개 변수가 제공될 때만 포함됩니다(예: 특정 템플릿 사양/버전을 요청하는 경우).</span><span class="sxs-lookup"><span data-stu-id="56fa2-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="56fa2-114">예제</span><span class="sxs-lookup"><span data-stu-id="56fa2-114">EXAMPLES</span></span>

### <span data-ttu-id="56fa2-115">예제 1: 현재 구독의 템플릿 사양 나열</span><span class="sxs-lookup"><span data-stu-id="56fa2-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="56fa2-116">현재 구독의 모든 템플릿 사양을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="56fa2-117">예제 2: 리소스 그룹에 템플릿 사양 나열</span><span class="sxs-lookup"><span data-stu-id="56fa2-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="56fa2-118">현재 구독의 리소스 그룹 'myRG'에 모든 템플릿 사양이 나열됩니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="56fa2-119">예제 3: 이름에 의해 템플릿 사양(모든 버전)을 얻음</span><span class="sxs-lookup"><span data-stu-id="56fa2-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="56fa2-120">리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="56fa2-121">**참고**: 템플릿 사양의 모든 버전이 "에 *있습니다. 반환* 개체의 버전 " 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-121">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="56fa2-122">예제 4: 이름별 템플릿 사양(특정 버전) 다운로드</span><span class="sxs-lookup"><span data-stu-id="56fa2-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="56fa2-123">리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'에 대한 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="56fa2-124">**참고**: *". 반환된 개체의 버전"* 속성에는 요청된 특정 버전만 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-124">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="56fa2-125">예제 5: 리소스 ID로 템플릿 사양(모든 버전 사용)을 얻음</span><span class="sxs-lookup"><span data-stu-id="56fa2-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="56fa2-126">구독 subId의 리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양에 대한 \{ 정보를 \} 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="56fa2-127">**참고**: 템플릿 사양의 모든 버전이 "에 *있습니다. 반환* 개체의 버전 " 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-127">**Note**: All of the Template Spec's versions will be present within the "*.Versions*" property of the return object.</span></span>

### <span data-ttu-id="56fa2-128">예제 6: 리소스 ID별 템플릿 사양(특정 버전) 다운로드</span><span class="sxs-lookup"><span data-stu-id="56fa2-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="56fa2-129">구독 subId의 리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'에 대한 정보를 \{ \} 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="56fa2-130">**참고**: *". 반환된 개체의 버전"* 속성에는 요청된 특정 버전만 포함되어 있습니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-130">**Note**: The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="56fa2-131">매개 변수</span><span class="sxs-lookup"><span data-stu-id="56fa2-131">PARAMETERS</span></span>

### <span data-ttu-id="56fa2-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="56fa2-132">-DefaultProfile</span></span>
<span data-ttu-id="56fa2-133">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="56fa2-134">-Name</span><span class="sxs-lookup"><span data-stu-id="56fa2-134">-Name</span></span>
<span data-ttu-id="56fa2-135">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-135">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56fa2-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="56fa2-136">-ResourceGroupName</span></span>
<span data-ttu-id="56fa2-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-137">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: ListTemplateSpecsParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56fa2-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="56fa2-138">-ResourceId</span></span>
<span data-ttu-id="56fa2-139">템플릿 사양의 완전히 자격을 갖춘 리소스 ID입니다. 예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="56fa2-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56fa2-140">-Version</span><span class="sxs-lookup"><span data-stu-id="56fa2-140">-Version</span></span>
<span data-ttu-id="56fa2-141">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-141">The version of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: GetTemplateSpecByNameParameterSet, GetTemplateSpecByIdParameterSet
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="56fa2-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="56fa2-142">CommonParameters</span></span>
<span data-ttu-id="56fa2-143">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="56fa2-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="56fa2-144">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="56fa2-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="56fa2-145">입력</span><span class="sxs-lookup"><span data-stu-id="56fa2-145">INPUTS</span></span>

### <span data-ttu-id="56fa2-146">System.String</span><span class="sxs-lookup"><span data-stu-id="56fa2-146">System.String</span></span>

## <span data-ttu-id="56fa2-147">출력</span><span class="sxs-lookup"><span data-stu-id="56fa2-147">OUTPUTS</span></span>

### <span data-ttu-id="56fa2-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="56fa2-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="56fa2-149">참고 사항</span><span class="sxs-lookup"><span data-stu-id="56fa2-149">NOTES</span></span>

## <span data-ttu-id="56fa2-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="56fa2-150">RELATED LINKS</span></span>
