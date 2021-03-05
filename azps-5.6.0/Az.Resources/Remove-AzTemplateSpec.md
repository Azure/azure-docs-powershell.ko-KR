---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 6383a1fb0a6dbaa20bee50a268d8f78abf59de65
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101979408"
---
# <span data-ttu-id="a7d2b-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="a7d2b-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="a7d2b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a7d2b-102">SYNOPSIS</span></span>
<span data-ttu-id="a7d2b-103">템플릿 사양 제거</span><span class="sxs-lookup"><span data-stu-id="a7d2b-103">Removes a Template Spec</span></span>

## <span data-ttu-id="a7d2b-104">구문</span><span class="sxs-lookup"><span data-stu-id="a7d2b-104">SYNTAX</span></span>

### <span data-ttu-id="a7d2b-105">RemoveByNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="a7d2b-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a7d2b-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="a7d2b-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a7d2b-107">설명</span><span class="sxs-lookup"><span data-stu-id="a7d2b-107">DESCRIPTION</span></span>
<span data-ttu-id="a7d2b-108">지정된 템플릿 사양을 제거합니다. 버전 **-Version 매개 변수가** 제공되면 지정된 버전만 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="a7d2b-109">특정 버전이 제공되지 않고 템플릿 사양과 해당 버전이 모두 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="a7d2b-110">**-Force 플래그가** 있는 경우 제거에 대한 확인 프롬프트가 없습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="a7d2b-111">예제</span><span class="sxs-lookup"><span data-stu-id="a7d2b-111">EXAMPLES</span></span>

### <span data-ttu-id="a7d2b-112">예제 1: 이름별 특정 버전 제거</span><span class="sxs-lookup"><span data-stu-id="a7d2b-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="a7d2b-113">리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="a7d2b-114">예제 2: 리소스 ID별 특정 버전 제거</span><span class="sxs-lookup"><span data-stu-id="a7d2b-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="a7d2b-115">구독 subId의 리소스 그룹 'myRG'에서 'MyTemplateSpec'이라는 템플릿 사양의 버전 'v1.0'을 \{ \} 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="a7d2b-116">예제 3: 템플릿 사양 및 이름에 의해 모든 버전 제거</span><span class="sxs-lookup"><span data-stu-id="a7d2b-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="a7d2b-117">'MyTemplateSpec'이라는 템플릿 사양과 리소스 그룹 'myRG' 내의 모든 버전이 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="a7d2b-118">예제 3: 템플릿 사양 및 리소스 ID로 모든 버전 제거</span><span class="sxs-lookup"><span data-stu-id="a7d2b-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="a7d2b-119">'MyTemplateSpec'이라는 템플릿 사양과 구독 subId의 리소스 그룹 'myRG' 내의 모든 \{ 버전이 \} 제거됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="a7d2b-120">매개 변수</span><span class="sxs-lookup"><span data-stu-id="a7d2b-120">PARAMETERS</span></span>

### <span data-ttu-id="a7d2b-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a7d2b-121">-DefaultProfile</span></span>
<span data-ttu-id="a7d2b-122">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a7d2b-123">-Force</span><span class="sxs-lookup"><span data-stu-id="a7d2b-123">-Force</span></span>
<span data-ttu-id="a7d2b-124">확인을 요청하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="a7d2b-125">-Name</span><span class="sxs-lookup"><span data-stu-id="a7d2b-125">-Name</span></span>
<span data-ttu-id="a7d2b-126">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-126">The name of the template spec.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d2b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a7d2b-127">-ResourceGroupName</span></span>
<span data-ttu-id="a7d2b-128">템플릿 사양의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-128">The name of the template spec's resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d2b-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="a7d2b-129">-ResourceId</span></span>
<span data-ttu-id="a7d2b-130">템플릿 사양의 완전히 자격을 갖춘 리소스 ID입니다. 예: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resource/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="a7d2b-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveByIdParameterSet
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d2b-131">-Version</span><span class="sxs-lookup"><span data-stu-id="a7d2b-131">-Version</span></span>
<span data-ttu-id="a7d2b-132">삭제할 템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-132">The version of the template spec to delete.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a7d2b-133">-확인</span><span class="sxs-lookup"><span data-stu-id="a7d2b-133">-Confirm</span></span>
<span data-ttu-id="a7d2b-134">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a7d2b-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a7d2b-135">-WhatIf</span></span>
<span data-ttu-id="a7d2b-136">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="a7d2b-137">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a7d2b-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a7d2b-138">CommonParameters</span></span>
<span data-ttu-id="a7d2b-139">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a7d2b-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a7d2b-140">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="a7d2b-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a7d2b-141">입력</span><span class="sxs-lookup"><span data-stu-id="a7d2b-141">INPUTS</span></span>

### <span data-ttu-id="a7d2b-142">System.String</span><span class="sxs-lookup"><span data-stu-id="a7d2b-142">System.String</span></span>

## <span data-ttu-id="a7d2b-143">출력</span><span class="sxs-lookup"><span data-stu-id="a7d2b-143">OUTPUTS</span></span>

### <span data-ttu-id="a7d2b-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="a7d2b-144">System.Boolean</span></span>

## <span data-ttu-id="a7d2b-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a7d2b-145">NOTES</span></span>

## <span data-ttu-id="a7d2b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a7d2b-146">RELATED LINKS</span></span>
