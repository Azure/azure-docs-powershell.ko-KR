---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 7740AC3B-F643-4F8D-8DC5-ACBF59323BD8
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azroledefinition
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzRoleDefinition.md
ms.openlocfilehash: 5cd9a76f71f63b1d16003cce467d2d91eddc5b04
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208501"
---
# <span data-ttu-id="7a9a3-101">Get-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7a9a3-101">Get-AzRoleDefinition</span></span>

## <span data-ttu-id="7a9a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7a9a3-102">SYNOPSIS</span></span>
<span data-ttu-id="7a9a3-103">할당에 사용할 수 있는 모든 Azure RBAC 역할을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-103">Lists all Azure RBAC roles that are available for assignment.</span></span>

## <span data-ttu-id="7a9a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="7a9a3-104">SYNTAX</span></span>

### <span data-ttu-id="7a9a3-105">RoleDefinitionNameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="7a9a3-105">RoleDefinitionNameParameterSet (Default)</span></span>
```
Get-AzRoleDefinition [[-Name] <String>] [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a9a3-106">RoleDefinitionIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a9a3-106">RoleDefinitionIdParameterSet</span></span>
```
Get-AzRoleDefinition -Id <Guid> [-Scope <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="7a9a3-107">RoleDefinitionCustomParameterSet</span><span class="sxs-lookup"><span data-stu-id="7a9a3-107">RoleDefinitionCustomParameterSet</span></span>
```
Get-AzRoleDefinition [-Scope <String>] [-Custom] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7a9a3-108">설명</span><span class="sxs-lookup"><span data-stu-id="7a9a3-108">DESCRIPTION</span></span>
<span data-ttu-id="7a9a3-109">특정 Get-AzRoleDefinition 이름과 함께 Get-AzRoleDefinition 명령을 사용하여 세부 정보를 볼 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-109">Use the Get-AzRoleDefinition command with a particular role name to view its details.</span></span>
<span data-ttu-id="7a9a3-110">역할이 액세스 권한을 부여하는 개별 작업을 검사하기 위해 역할의 작업 및 NotActions 속성을 검토합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-110">To inspect individual operations that a role grants access to, review the Actions and NotActions properties of the role.</span></span>

## <span data-ttu-id="7a9a3-111">예제</span><span class="sxs-lookup"><span data-stu-id="7a9a3-111">EXAMPLES</span></span>

### <span data-ttu-id="7a9a3-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="7a9a3-112">Example 1</span></span>
```
PS C:\> Get-AzRoleDefinition -Name Reader
```

<span data-ttu-id="7a9a3-113">판독기 역할 정의를 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-113">Get the Reader role definition</span></span>

### <span data-ttu-id="7a9a3-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="7a9a3-114">Example 2</span></span>
```
PS C:\> Get-AzRoleDefinition
```

<span data-ttu-id="7a9a3-115">모든 RBAC 역할 정의를 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-115">Lists all RBAC role definitions</span></span>

## <span data-ttu-id="7a9a3-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7a9a3-116">PARAMETERS</span></span>

### <span data-ttu-id="7a9a3-117">-Custom</span><span class="sxs-lookup"><span data-stu-id="7a9a3-117">-Custom</span></span>
<span data-ttu-id="7a9a3-118">지정된 경우 디렉터리에 사용자 지정 만든 역할만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-118">If specified, only displays the custom created roles in the directory.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: RoleDefinitionCustomParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a9a3-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7a9a3-119">-DefaultProfile</span></span>
<span data-ttu-id="7a9a3-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="7a9a3-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="7a9a3-121">-Id</span><span class="sxs-lookup"><span data-stu-id="7a9a3-121">-Id</span></span>
<span data-ttu-id="7a9a3-122">역할 정의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-122">Role definition Id.</span></span>

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

### <span data-ttu-id="7a9a3-123">-Name</span><span class="sxs-lookup"><span data-stu-id="7a9a3-123">-Name</span></span>
<span data-ttu-id="7a9a3-124">역할 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-124">Role definition name.</span></span>
<span data-ttu-id="7a9a3-125">예: 판독기, 참가자, Virtual Machine 기여자.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-125">For e.g. Reader, Contributor, Virtual Machine Contributor.</span></span>

```yaml
Type: System.String
Parameter Sets: RoleDefinitionNameParameterSet
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7a9a3-126">-Scope</span><span class="sxs-lookup"><span data-stu-id="7a9a3-126">-Scope</span></span>
<span data-ttu-id="7a9a3-127">역할 정의 범위입니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-127">Role definition scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7a9a3-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7a9a3-128">CommonParameters</span></span>
<span data-ttu-id="7a9a3-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7a9a3-130">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7a9a3-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7a9a3-131">입력</span><span class="sxs-lookup"><span data-stu-id="7a9a3-131">INPUTS</span></span>

### <span data-ttu-id="7a9a3-132">System.String</span><span class="sxs-lookup"><span data-stu-id="7a9a3-132">System.String</span></span>

### <span data-ttu-id="7a9a3-133">System.Guid</span><span class="sxs-lookup"><span data-stu-id="7a9a3-133">System.Guid</span></span>

### <span data-ttu-id="7a9a3-134">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="7a9a3-134">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="7a9a3-135">출력</span><span class="sxs-lookup"><span data-stu-id="7a9a3-135">OUTPUTS</span></span>

### <span data-ttu-id="7a9a3-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7a9a3-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleDefinition</span></span>

## <span data-ttu-id="7a9a3-137">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7a9a3-137">NOTES</span></span>
<span data-ttu-id="7a9a3-138">키워드: azure, azurerm, arm, 리소스, 관리, 관리자, 리소스, 그룹, 템플릿, 배포</span><span class="sxs-lookup"><span data-stu-id="7a9a3-138">Keywords: azure, azurerm, arm, resource, management, manager, resource, group, template, deployment</span></span>

## <span data-ttu-id="7a9a3-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7a9a3-139">RELATED LINKS</span></span>

[<span data-ttu-id="7a9a3-140">New-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7a9a3-140">New-AzRoleAssignment</span></span>](./New-AzRoleAssignment.md)

[<span data-ttu-id="7a9a3-141">Get-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="7a9a3-141">Get-AzRoleAssignment</span></span>](./Get-AzRoleAssignment.md)

[<span data-ttu-id="7a9a3-142">New-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7a9a3-142">New-AzRoleDefinition</span></span>](./New-AzRoleDefinition.md)

[<span data-ttu-id="7a9a3-143">Remove-AzRoleDefinition</span><span class="sxs-lookup"><span data-stu-id="7a9a3-143">Remove-AzRoleDefinition</span></span>](./Remove-AzRoleDefinition.md)

