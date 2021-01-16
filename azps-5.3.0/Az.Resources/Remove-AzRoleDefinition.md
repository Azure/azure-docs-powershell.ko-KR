---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: a2bd64daf4b9895de3ef8ca12ff0fec7295cd094
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98375740"
---
# <span data-ttu-id="61e24-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61e24-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="61e24-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61e24-102">SYNOPSIS</span></span>
<span data-ttu-id="61e24-103">Azure RBAC에서 사용자 지정 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="61e24-104">삭제할 역할은 역할의 ID 속성을 사용하여 지정됩니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="61e24-105">사용자 지정 역할에 대한 기존 역할 할당이 있는 경우 삭제가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="61e24-106">구문</span><span class="sxs-lookup"><span data-stu-id="61e24-106">SYNTAX</span></span>

### <span data-ttu-id="61e24-107">RoleDefinitionIdParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="61e24-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e24-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e24-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="61e24-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="61e24-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="61e24-110">설명</span><span class="sxs-lookup"><span data-stu-id="61e24-110">DESCRIPTION</span></span>
<span data-ttu-id="61e24-111">Remove-AzRoleDefinition cmdlet은 Azure Role-Based Access Control에서 사용자 지정 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="61e24-112">기존 사용자 지정 역할의 ID 매개 변수를 제공하여 해당 사용자 지정 역할을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="61e24-113">기본적으로 Remove-AzRoleDefinition 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="61e24-114">프롬프트를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="61e24-115">삭제할 사용자 지정 역할에 대한 기존 역할 할당이 있는 경우 삭제가 실패합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="61e24-116">예제</span><span class="sxs-lookup"><span data-stu-id="61e24-116">EXAMPLES</span></span>

### <span data-ttu-id="61e24-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="61e24-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="61e24-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="61e24-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="61e24-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61e24-119">PARAMETERS</span></span>

### <span data-ttu-id="61e24-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61e24-120">-DefaultProfile</span></span>
<span data-ttu-id="61e24-121">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="61e24-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="61e24-122">-Force</span><span class="sxs-lookup"><span data-stu-id="61e24-122">-Force</span></span>
<span data-ttu-id="61e24-123">설정한 경우 사용자 지정 역할을 삭제하기 전에 확인 메시지를 표시하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="61e24-124">-Id</span><span class="sxs-lookup"><span data-stu-id="61e24-124">-Id</span></span>
<span data-ttu-id="61e24-125">삭제할 역할 정의의 ID</span><span class="sxs-lookup"><span data-stu-id="61e24-125">Id of the Role definition to be deleted</span></span>

```yaml
Type: System.Guid
Parameter Sets: RoleDefinitionIdParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e24-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="61e24-126">-InputObject</span></span>
<span data-ttu-id="61e24-127">제거할 역할 정의를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-127">The object representing the role definition to be removed.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="61e24-128">-Name</span><span class="sxs-lookup"><span data-stu-id="61e24-128">-Name</span></span>
<span data-ttu-id="61e24-129">삭제할 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-129">Name of the Role definition to be deleted.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e24-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="61e24-130">-PassThru</span></span>
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

### <span data-ttu-id="61e24-131">-Scope</span><span class="sxs-lookup"><span data-stu-id="61e24-131">-Scope</span></span>
<span data-ttu-id="61e24-132">역할 정의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-132">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionIdParameterSet, RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="61e24-133">-Confirm</span><span class="sxs-lookup"><span data-stu-id="61e24-133">-Confirm</span></span>
<span data-ttu-id="61e24-134">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="61e24-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="61e24-135">-WhatIf</span></span>
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

### <span data-ttu-id="61e24-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61e24-136">CommonParameters</span></span>
<span data-ttu-id="61e24-137">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61e24-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61e24-138">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61e24-138">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61e24-139">입력</span><span class="sxs-lookup"><span data-stu-id="61e24-139">INPUTS</span></span>

### <span data-ttu-id="61e24-140">System.Guid</span><span class="sxs-lookup"><span data-stu-id="61e24-140">System.Guid</span></span>

### <span data-ttu-id="61e24-141">System.String</span><span class="sxs-lookup"><span data-stu-id="61e24-141">System.String</span></span>

### <span data-ttu-id="61e24-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61e24-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="61e24-143">출력</span><span class="sxs-lookup"><span data-stu-id="61e24-143">OUTPUTS</span></span>

### <span data-ttu-id="61e24-144">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="61e24-144">System.Boolean</span></span>

## <span data-ttu-id="61e24-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61e24-145">NOTES</span></span>
<span data-ttu-id="61e24-146">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="61e24-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="61e24-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61e24-147">RELATED LINKS</span></span>

[<span data-ttu-id="61e24-148">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61e24-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="61e24-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61e24-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="61e24-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="61e24-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)

