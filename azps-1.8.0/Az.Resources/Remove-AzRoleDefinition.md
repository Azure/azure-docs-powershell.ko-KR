---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2D882B33-2B62-4785-AF8F-5F4644E9504D
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/remove-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Remove-AzRoleDefinition.md
ms.openlocfilehash: f7ed4b70b3b0575b41f081e088e55944b46656aa
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699323"
---
# <span data-ttu-id="6bae1-101">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bae1-101">Remove-AzRoleDefinition</span></span>

## <span data-ttu-id="6bae1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6bae1-102">SYNOPSIS</span></span>
<span data-ttu-id="6bae1-103">Azure RBAC에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-103">Deletes a custom role in Azure RBAC.</span></span>
<span data-ttu-id="6bae1-104">삭제할 역할은 역할의 Id 속성을 사용 하 여 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-104">The role to be deleted is specified using the Id property of the role.</span></span>
<span data-ttu-id="6bae1-105">사용자 지정 역할에 대 한 기존 역할 할당이 있으면 Delete가 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-105">Delete will fail if there are existing role assignments made to the custom role.</span></span>

## <span data-ttu-id="6bae1-106">구문과</span><span class="sxs-lookup"><span data-stu-id="6bae1-106">SYNTAX</span></span>

### <span data-ttu-id="6bae1-107">RoleDefinitionIdParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6bae1-107">RoleDefinitionIdParameterSet (Default)</span></span>
```
Remove-AzRoleDefinition -Id <Guid> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bae1-108">RoleDefinitionNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bae1-108">RoleDefinitionNameParameterSet</span></span>
```
Remove-AzRoleDefinition [-Name] <String> [-Scope <String>] [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6bae1-109">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="6bae1-109">InputObjectParameterSet</span></span>
```
Remove-AzRoleDefinition -InputObject <PSRoleDefinition> [-Force] [-PassThru]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6bae1-110">설명은</span><span class="sxs-lookup"><span data-stu-id="6bae1-110">DESCRIPTION</span></span>
<span data-ttu-id="6bae1-111">Remove-AzRoleDefinition cmdlet은 Azure Role-Based 액세스 제어에서 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-111">The Remove-AzRoleDefinition cmdlet deletes a custom role in Azure Role-Based Access Control.</span></span>
<span data-ttu-id="6bae1-112">기존 사용자 지정 역할의 Id 매개 변수를 제공 하 여 해당 사용자 지정 역할을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-112">Provide the Id parameter of an existing custom role to delete that custom role.</span></span>
<span data-ttu-id="6bae1-113">기본적으로 Remove-AzRoleDefinition 확인 메시지가 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-113">By default, Remove-AzRoleDefinition prompts you for confirmation.</span></span>
<span data-ttu-id="6bae1-114">프롬프트를 표시 하지 않으려면 Force 매개 변수를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-114">To suppress the prompt, use the Force parameter.</span></span>
<span data-ttu-id="6bae1-115">사용자 지정 역할에 대해 삭제 될 기존 역할 할당이 있는 경우 삭제는 실패 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-115">If there are existing role assignments made to the custom role to be deleted, the delete will fail.</span></span>

## <span data-ttu-id="6bae1-116">예제의</span><span class="sxs-lookup"><span data-stu-id="6bae1-116">EXAMPLES</span></span>

### <span data-ttu-id="6bae1-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="6bae1-117">Example 1</span></span>
```
Get-AzRoleDefinition -Name "Virtual Machine Operator" | Remove-AzRoleDefinition
```

### <span data-ttu-id="6bae1-118">예제 2</span><span class="sxs-lookup"><span data-stu-id="6bae1-118">Example 2</span></span>
```
Remove-AzRoleDefinition -Id "52a6cc13-ff92-47a8-a39b-2a8205c3087e"
```

## <span data-ttu-id="6bae1-119">변수</span><span class="sxs-lookup"><span data-stu-id="6bae1-119">PARAMETERS</span></span>

### <span data-ttu-id="6bae1-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6bae1-120">-DefaultProfile</span></span>
<span data-ttu-id="6bae1-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6bae1-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6bae1-122">-Force</span><span class="sxs-lookup"><span data-stu-id="6bae1-122">-Force</span></span>
<span data-ttu-id="6bae1-123">설정 하는 경우 사용자 지정 역할을 삭제 하기 전에 확인 메시지를 표시 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-123">If set, does not prompt for a confirmation before deleting the custom role</span></span>

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

### <span data-ttu-id="6bae1-124">-Id</span><span class="sxs-lookup"><span data-stu-id="6bae1-124">-Id</span></span>
<span data-ttu-id="6bae1-125">삭제할 역할 정의의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-125">Id of the Role definition to be deleted</span></span>

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

### <span data-ttu-id="6bae1-126">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6bae1-126">-InputObject</span></span>
<span data-ttu-id="6bae1-127">제거할 역할 정의를 나타내는 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-127">The object representing the role definition to be removed.</span></span>

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

### <span data-ttu-id="6bae1-128">-이름</span><span class="sxs-lookup"><span data-stu-id="6bae1-128">-Name</span></span>
<span data-ttu-id="6bae1-129">삭제할 역할 정의의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-129">Name of the Role definition to be deleted.</span></span>

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

### <span data-ttu-id="6bae1-130">-PassThru</span><span class="sxs-lookup"><span data-stu-id="6bae1-130">-PassThru</span></span>
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

### <span data-ttu-id="6bae1-131">-범위</span><span class="sxs-lookup"><span data-stu-id="6bae1-131">-Scope</span></span>
<span data-ttu-id="6bae1-132">역할 정의 범위</span><span class="sxs-lookup"><span data-stu-id="6bae1-132">Role definition scope.</span></span>

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

### <span data-ttu-id="6bae1-133">-확인</span><span class="sxs-lookup"><span data-stu-id="6bae1-133">-Confirm</span></span>
<span data-ttu-id="6bae1-134">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-134">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6bae1-135">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6bae1-135">-WhatIf</span></span>
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

### <span data-ttu-id="6bae1-136">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6bae1-136">CommonParameters</span></span>
<span data-ttu-id="6bae1-137">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6bae1-137">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6bae1-138">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6bae1-138">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6bae1-139">입력</span><span class="sxs-lookup"><span data-stu-id="6bae1-139">INPUTS</span></span>

### <span data-ttu-id="6bae1-140">시스템 Guid</span><span class="sxs-lookup"><span data-stu-id="6bae1-140">System.Guid</span></span>

### <span data-ttu-id="6bae1-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6bae1-141">System.String</span></span>

### <span data-ttu-id="6bae1-142">Microsoft. a. PSRoleDefinition (.Resources.</span><span class="sxs-lookup"><span data-stu-id="6bae1-142">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="6bae1-143">출력</span><span class="sxs-lookup"><span data-stu-id="6bae1-143">OUTPUTS</span></span>

### <span data-ttu-id="6bae1-144">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="6bae1-144">System.Boolean</span></span>

## <span data-ttu-id="6bae1-145">상속자</span><span class="sxs-lookup"><span data-stu-id="6bae1-145">NOTES</span></span>
<span data-ttu-id="6bae1-146">키워드: azure, azurerm, arm, resource, 관리, 관리자, 리소스, 그룹, 서식 파일, 배포</span><span class="sxs-lookup"><span data-stu-id="6bae1-146">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="6bae1-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6bae1-147">RELATED LINKS</span></span>

[<span data-ttu-id="6bae1-148">새로운 AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bae1-148">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="6bae1-149">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bae1-149">Get-AzRoleDefinition</span></span>](./Get-AzRoleDefinition.md)

[<span data-ttu-id="6bae1-150">Set-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="6bae1-150">Set-AzRoleDefinition</span></span>](./Set-AzRoleDefinition.md)
