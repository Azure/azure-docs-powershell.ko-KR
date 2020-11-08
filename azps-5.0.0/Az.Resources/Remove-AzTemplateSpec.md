---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-aztemplatespec
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzTemplateSpec.md
ms.openlocfilehash: 718de3ac2da38b8ed7950e8f8a59b0d8fc2f4db7
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226542"
---
# <span data-ttu-id="11c6c-101">Remove-AzTemplateSpec</span><span class="sxs-lookup"><span data-stu-id="11c6c-101">Remove-AzTemplateSpec</span></span>

## <span data-ttu-id="11c6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="11c6c-102">SYNOPSIS</span></span>
<span data-ttu-id="11c6c-103">서식 파일 사양을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-103">Removes a Template Spec</span></span>

## <span data-ttu-id="11c6c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="11c6c-104">SYNTAX</span></span>

### <span data-ttu-id="11c6c-105">RemoveByNameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="11c6c-105">RemoveByNameParameterSet (Default)</span></span>
```
Remove-AzTemplateSpec [-Force] [-ResourceGroupName] <String> [-Name] <String> [[-Version] <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="11c6c-106">RemoveByIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="11c6c-106">RemoveByIdParameterSet</span></span>
```
Remove-AzTemplateSpec [-Force] [[-Version] <String>] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="11c6c-107">설명은</span><span class="sxs-lookup"><span data-stu-id="11c6c-107">DESCRIPTION</span></span>
<span data-ttu-id="11c6c-108">지정 된 서식 파일 사양을 제거 합니다. 버전 **버전** 매개 변수를 제공 하면 지정 된 버전만 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-108">Removes a specified Template Spec. If the version **-Version** parameter is provided, only the specified version will be removed.</span></span> <span data-ttu-id="11c6c-109">특정 버전을 제공 하지 않으면 서식 파일 사양 및 해당 버전이 모두 제거 됩니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-109">If no specific version is provided, the Template Spec and all of its versions will be removed.</span></span> <span data-ttu-id="11c6c-110">**-Force** 플래그가 표시 되는 경우 제거에 대 한 확인 메시지가 표시 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-110">If the **-Force** flag is present there will be no confirmation prompt for removal.</span></span>

## <span data-ttu-id="11c6c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="11c6c-111">EXAMPLES</span></span>

### <span data-ttu-id="11c6c-112">예제 1: 이름으로 특정 버전 제거</span><span class="sxs-lookup"><span data-stu-id="11c6c-112">Example 1: Removing a specific version by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="11c6c-113">리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-113">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG'.</span></span>

### <span data-ttu-id="11c6c-114">예제 2: 리소스 id를 기준으로 특정 버전 제거</span><span class="sxs-lookup"><span data-stu-id="11c6c-114">Example 2: Removing a specific version by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -Version 'v1.0'
```

<span data-ttu-id="11c6c-115">구독 하위 id의 리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec ' 인 템플릿 사양의 ' v 1.0 ' 버전을 제거 \{ \} 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-115">Removes version 'v1.0' of the Template Spec named 'MyTemplateSpec' within the resource group 'myRG' of subscription \{subId\}.</span></span>

### <span data-ttu-id="11c6c-116">예제 3: 이름으로 템플릿 사양 및 모든 버전 제거</span><span class="sxs-lookup"><span data-stu-id="11c6c-116">Example 3: Removing a Template Spec and all versions by name</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceGroupName 'myRG' -Name 'MyTemplateSpec'
```

<span data-ttu-id="11c6c-117">리소스 그룹 ' myRG ' 내에서 이름이 ' MyTemplateSpec '이 고 해당 하는 모든 버전이 있는 템플릿 사양을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-117">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG'.</span></span>

### <span data-ttu-id="11c6c-118">예제 3: 리소스 id를 기준으로 템플릿 사양 및 모든 버전 제거</span><span class="sxs-lookup"><span data-stu-id="11c6c-118">Example 3: Removing a Template Spec and all versions by resource id</span></span>
```powershell
PS C:\> Remove-AzTemplateSpec -ResourceId '/subscriptions/{subId}/resourceGroups/myRG/providers/Microsoft.Resources/templateSpecs/MyTemplateSpec' -ResourceGroupName 'myRG'
```

<span data-ttu-id="11c6c-119">구독 하위 id의 리소스 그룹 ' myRG ' 내에 있는 ' MyTemplateSpec ' 및 해당 버전의 모든 버전이 포함 된 템플릿 사양을 제거 합니다 \{ \} .</span><span class="sxs-lookup"><span data-stu-id="11c6c-119">Removes the Template Spec named 'MyTemplateSpec' and all of its versions within the resource group 'myRG' of subscription \{subId\}.</span></span>

## <span data-ttu-id="11c6c-120">변수</span><span class="sxs-lookup"><span data-stu-id="11c6c-120">PARAMETERS</span></span>

### <span data-ttu-id="11c6c-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="11c6c-121">-DefaultProfile</span></span>
<span data-ttu-id="11c6c-122">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="11c6c-123">-Force</span><span class="sxs-lookup"><span data-stu-id="11c6c-123">-Force</span></span>
<span data-ttu-id="11c6c-124">확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-124">Do not ask for confirmation.</span></span>

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

### <span data-ttu-id="11c6c-125">-이름</span><span class="sxs-lookup"><span data-stu-id="11c6c-125">-Name</span></span>
<span data-ttu-id="11c6c-126">템플릿 사양의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-126">The name of the template spec.</span></span>

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

### <span data-ttu-id="11c6c-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="11c6c-127">-ResourceGroupName</span></span>
<span data-ttu-id="11c6c-128">템플릿 사양의 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-128">The name of the template spec's resource group.</span></span>

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

### <span data-ttu-id="11c6c-129">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="11c6c-129">-ResourceId</span></span>
<span data-ttu-id="11c6c-130">템플릿 사양의 정규화 된 리소스 Id입니다. 예:/subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span><span class="sxs-lookup"><span data-stu-id="11c6c-130">The fully qualified resource Id of the template spec. Example: /subscriptions/{subId}/resourceGroups/{rgName}/providers/Microsoft.Resources/templateSpecs/{templateSpecName}</span></span>

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

### <span data-ttu-id="11c6c-131">-버전</span><span class="sxs-lookup"><span data-stu-id="11c6c-131">-Version</span></span>
<span data-ttu-id="11c6c-132">삭제할 템플릿 사양의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-132">The version of the template spec to delete.</span></span>

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

### <span data-ttu-id="11c6c-133">-확인</span><span class="sxs-lookup"><span data-stu-id="11c6c-133">-Confirm</span></span>
<span data-ttu-id="11c6c-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="11c6c-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="11c6c-135">-WhatIf</span></span>
<span data-ttu-id="11c6c-136">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-136">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="11c6c-137">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-137">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="11c6c-138">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="11c6c-138">CommonParameters</span></span>
<span data-ttu-id="11c6c-139">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="11c6c-139">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="11c6c-140">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="11c6c-140">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="11c6c-141">입력</span><span class="sxs-lookup"><span data-stu-id="11c6c-141">INPUTS</span></span>

### <span data-ttu-id="11c6c-142">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="11c6c-142">System.String</span></span>

## <span data-ttu-id="11c6c-143">출력</span><span class="sxs-lookup"><span data-stu-id="11c6c-143">OUTPUTS</span></span>

### <span data-ttu-id="11c6c-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="11c6c-144">System.Boolean</span></span>

## <span data-ttu-id="11c6c-145">상속자</span><span class="sxs-lookup"><span data-stu-id="11c6c-145">NOTES</span></span>

## <span data-ttu-id="11c6c-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="11c6c-146">RELATED LINKS</span></span>
