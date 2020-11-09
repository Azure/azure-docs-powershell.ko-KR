---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzTemplateSpec.md
ms.openlocfilehash: be3a16707303016e22be8052721efcb35c608b3e
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308825"
---
# <span data-ttu-id="82193-101">Get-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="82193-101">Get-AzTemplateSpec</span></span>

## <span data-ttu-id="82193-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82193-102">SYNOPSIS</span></span>
<span data-ttu-id="82193-103">템플릿 사양 가져오기 또는 나열</span><span class="sxs-lookup"><span data-stu-id="82193-103">Gets or lists Template Specs</span></span>

## <span data-ttu-id="82193-104">구문과</span><span class="sxs-lookup"><span data-stu-id="82193-104">SYNTAX</span></span>

### <span data-ttu-id="82193-105">ListTemplateSpecsParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="82193-105">ListTemplateSpecsParameterSet (Default)</span></span>
```
Get-AzTemplateSpec [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="82193-106">GetTemplateSpecByNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="82193-106">GetTemplateSpecByNameParameterSet</span></span>
```
Get-AzTemplateSpec [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="82193-107">GetTemplateSpecByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="82193-107">GetTemplateSpecByIdParameterSet</span></span>
```
Get-AzTemplateSpec [[-Version] <String>] [-ResourceId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="82193-108">설명은</span><span class="sxs-lookup"><span data-stu-id="82193-108">DESCRIPTION</span></span>
<span data-ttu-id="82193-109">이 cmdlet을 사용 하 여 구독/리소스 그룹에 서식 파일 사양을 나열 하거나 이름 또는 id를 기준으로 특정 템플릿 사양을 가져올 수 있습니다. 이름/id로 특정 서식 파일 사양을 가져올 때 **-version** 매개 변수를 통해 버전 이름을 지정 하 여 특정 버전을 선택적으로 검색할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="82193-109">This cmdlet can be used to list Template Specs in a subscription/resource group or get a specific Template Spec by name or id. When getting a specific Template Spec by name/id a specific version can optionally be retrieved by specifying a version name through the **-Version** parameter.</span></span> <span data-ttu-id="82193-110">**-버전** 을 사용 하는 경우에는 특정 버전 세부 정보만 \* 내에 표시 됩니다 *.* 반환 된 템플릿 사양 개체의 버전.</span><span class="sxs-lookup"><span data-stu-id="82193-110">When **-Version** is used, only the specific version details will be present within \* *.Versions* on the returned Template Spec object.</span></span> <span data-ttu-id="82193-111">템플릿 사양을 이름/i d에 따라 검색할 때 지정 된 특정 버전이 없으면 \* 내에 모든 버전이 표시 됩니다 *.* 반환 된 개체의 Versions 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-111">If no specific version is specified when retrieving a Template Spec by name/id, all versions will be present within the  \* *.Versions* property of the returned object.</span></span>

<span data-ttu-id="82193-112">**참고** : 구독 또는 리소스 그룹 내에 모든 템플릿 사양을 나열할 때 각 반환 된 템플릿 사양의 *". 버전 "* 속성은 *null* 입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-112">**Note** : When listing all Template Specs within a subscription or resource group, each returned Template Spec's *".Versions"* property will be *null*.</span></span> <span data-ttu-id="82193-113">버전 정보는-Name 또는-ResourceId 매개 변수가 제공 되는 경우에만 포함 됩니다 (예: 특정 서식 파일 사양/버전 요청).</span><span class="sxs-lookup"><span data-stu-id="82193-113">Version information is only included when -Name or -ResourceId parameters are provided (eg: you are requesting a specific template spec/version).</span></span>

## <span data-ttu-id="82193-114">예제의</span><span class="sxs-lookup"><span data-stu-id="82193-114">EXAMPLES</span></span>

### <span data-ttu-id="82193-115">예제 1: 현재 구독의 목록 서식 사양</span><span class="sxs-lookup"><span data-stu-id="82193-115">Example 1: List Template Specs in current subscription</span></span>
```powershell
PS C:\> Get-AzTemplateSpec
```

<span data-ttu-id="82193-116">현재 구독에 모든 서식 파일 사양을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="82193-116">Lists all Template Specs in the current subscription.</span></span>

### <span data-ttu-id="82193-117">예제 2: 리소스 그룹의 목록 서식 파일 사양</span><span class="sxs-lookup"><span data-stu-id="82193-117">Example 2: List Template Specs in a resource group</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG'
```

<span data-ttu-id="82193-118">현재 구독의 리소스 그룹 ' myRG '에 모든 템플릿 사양을 나열 합니다.</span><span class="sxs-lookup"><span data-stu-id="82193-118">Lists all Template Specs in the resource group 'myRG' of the current subscription.</span></span>

### <span data-ttu-id="82193-119">예제 3: 이름으로 템플릿 사양 가져오기 (모든 버전 포함)</span><span class="sxs-lookup"><span data-stu-id="82193-119">Example 3: Get Template Spec (with all versions) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="82193-120">리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82193-120">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="82193-121">**참고** : 모든 템플릿 사양 버전은 "에 표시 됩니다 *. Versions* 의 반환 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-121">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="82193-122">예제 4: 이름으로 템플릿 사양 (특정 버전) 가져오기</span><span class="sxs-lookup"><span data-stu-id="82193-122">Example 4: Get Template Spec (specific version) by name</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="82193-123">리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전에 대 한 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="82193-123">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

<span data-ttu-id="82193-124">**참고** : *". Versions "* 속성에는 요청 된 특정 버전만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82193-124">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

### <span data-ttu-id="82193-125">예제 5: 리소스 id에 따라 템플릿 사양 가져오기 (모든 버전 포함)</span><span class="sxs-lookup"><span data-stu-id="82193-125">Example 5: Get Template Spec (with all versions) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec'
```

<span data-ttu-id="82193-126">구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양에 대 한 정보를 가져옵니다 \{ \} .</span><span class="sxs-lookup"><span data-stu-id="82193-126">Gets information about the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="82193-127">**참고** : 모든 템플릿 사양 버전은 "에 표시 됩니다 *. Versions* 의 반환 개체 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-127">**Note** : All of the Template Spec's versions will be present within the " *.Versions* " property of the return object.</span></span>

### <span data-ttu-id="82193-128">예제 6: 리소스 id 별 템플릿 사양 (특정 버전) 가져오기</span><span class="sxs-lookup"><span data-stu-id="82193-128">Example 6: Get Template Spec (specific version) by resource id</span></span>
```powershell
PS C:\> Get-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="82193-129">구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전에 대 한 정보를 가져옵니다 \{ \} .</span><span class="sxs-lookup"><span data-stu-id="82193-129">Gets information about version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

<span data-ttu-id="82193-130">**참고** : *". Versions "* 속성에는 요청 된 특정 버전만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="82193-130">**Note** : The *".Versions"* property of the returned object will contain only the specific version requested.</span></span>

## <span data-ttu-id="82193-131">변수</span><span class="sxs-lookup"><span data-stu-id="82193-131">PARAMETERS</span></span>

### <span data-ttu-id="82193-132">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82193-132">-DefaultProfile</span></span>
<span data-ttu-id="82193-133">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-133">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="82193-134">-이름</span><span class="sxs-lookup"><span data-stu-id="82193-134">-Name</span></span>
<span data-ttu-id="82193-135">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-135">The name of the template spec.</span></span>

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

### <span data-ttu-id="82193-136">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82193-136">-ResourceGroupName</span></span>
<span data-ttu-id="82193-137">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-137">The name of the resource group.</span></span>

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

### <span data-ttu-id="82193-138">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="82193-138">-ResourceId</span></span>
<span data-ttu-id="82193-139">템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="82193-139">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="82193-140">-버전</span><span class="sxs-lookup"><span data-stu-id="82193-140">-Version</span></span>
<span data-ttu-id="82193-141">템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="82193-141">The version of the template spec.</span></span>

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

### <span data-ttu-id="82193-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82193-142">CommonParameters</span></span>
<span data-ttu-id="82193-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="82193-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82193-144">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="82193-144">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82193-145">입력</span><span class="sxs-lookup"><span data-stu-id="82193-145">INPUTS</span></span>

### <span data-ttu-id="82193-146">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="82193-146">System.String</span></span>

## <span data-ttu-id="82193-147">출력</span><span class="sxs-lookup"><span data-stu-id="82193-147">OUTPUTS</span></span>

### <span data-ttu-id="82193-148">SdkModels. PSTemplateSpec에 대 한 명령</span><span class="sxs-lookup"><span data-stu-id="82193-148">Microsoft.Azure.Commands.ResourceManager.Cmdlets.SdkModels.PSTemplateSpec</span></span>

## <span data-ttu-id="82193-149">상속자</span><span class="sxs-lookup"><span data-stu-id="82193-149">NOTES</span></span>

## <span data-ttu-id="82193-150">관련 링크</span><span class="sxs-lookup"><span data-stu-id="82193-150">RELATED LINKS</span></span>
