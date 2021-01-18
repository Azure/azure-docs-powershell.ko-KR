---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98495414"
---
# <span data-ttu-id="51d22-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51d22-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="51d22-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="51d22-102">SYNOPSIS</span></span>
<span data-ttu-id="51d22-103">기존 역할 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="51d22-104">구문</span><span class="sxs-lookup"><span data-stu-id="51d22-104">SYNTAX</span></span>

### <span data-ttu-id="51d22-105">RoleAssignmentParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="51d22-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="51d22-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="51d22-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="51d22-107">설명</span><span class="sxs-lookup"><span data-stu-id="51d22-107">DESCRIPTION</span></span>
<span data-ttu-id="51d22-108">New-AzRoleAssignment 명령을 사용하여 기존 할당을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="51d22-109">설명은 유효한 문자열일 수 있습니다. 이 문자열을 사용하여 다른 문자열을 추론할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="51d22-110">조건이 설정된 경우 조건 버전을 설정해야 하지만 필요하지 않은 조건을 업데이트하는 경우</span><span class="sxs-lookup"><span data-stu-id="51d22-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="51d22-111">조건 버전은 1.0에서 2.0으로 업그레이드할 수 있지만 다시 다운그레시할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="51d22-112">2.0은 1.0과 소급할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="51d22-113">예제</span><span class="sxs-lookup"><span data-stu-id="51d22-113">EXAMPLES</span></span>

### <span data-ttu-id="51d22-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="51d22-114">Example 1</span></span>
```powershell
$ConditionVersion = "2.0"
  $Description = "This is a new role assignment for John"
  $Condition = "@Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'"

  $roleAssignment = Get-AzRoleAssignment -Scope "/subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg" -PrincipalId "0c0f6cdc-90dd-4664-83c0-a0d986c4c604"
  $roleAssignment.Description = $Description
  $roleAssignment.Condition = $Condition
  $roleAssignment.ConditionVersion = $ConditionVersion

  Set-AzRoleAssignment -InputObject $roleAssignment -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="51d22-115">개체를 수정하여 기존 역할 할당 업데이트</span><span class="sxs-lookup"><span data-stu-id="51d22-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="51d22-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="51d22-116">Example 2</span></span>
```powershell
Set-AzRoleAssignment -InputFile "C:\RoleAssignments\example.json" -PassThru

  RoleAssignmentId   : /providers/Microsoft.Management/managementGroups/1273adef-00a3
                     -4086-a51a-dbcce1857d36/providers/Microsoft.Authorization/role
                     Assignments/926c2a76-be19-4281-94de-38777629b9dc
  Scope              : /subscriptions/4e5329a6-39ce-4e13-b12e-11b30f015986/resourceGroups/contoso_rg
  DisplayName        : John Doe
  SignInName         : John.Doe@Contoso.com
  RoleDefinitionName : Owner
  RoleDefinitionId   : 8e3af657-a8ff-443c-a75c-2fe8c4bcb635
  ObjectId           : 0c0f6cdc-90dd-4664-83c0-a0d986c4c604
  ObjectType         : User
  CanDelegate        : False
  Description        : This is a new role assignment for John
  ConditionVersion   : 2.0
  Condition          : @Resource[Microsoft.Storage/storageAccounts/blobServices/containers/blobs:Path] StringEqualsIgnoreCase 'foo_storage_container'
```

<span data-ttu-id="51d22-117">파일을 사용하여 기존 역할 할당 업데이트</span><span class="sxs-lookup"><span data-stu-id="51d22-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="51d22-118">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="51d22-118">PARAMETERS</span></span>

### <span data-ttu-id="51d22-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="51d22-119">-DefaultProfile</span></span>
<span data-ttu-id="51d22-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="51d22-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="51d22-121">-InputFile</span></span>
<span data-ttu-id="51d22-122">단일 역할 정의를 포함하는 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-122">File name containing a single role definition.</span></span>

```yaml
Type: System.String
Parameter Sets: InputFileParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="51d22-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="51d22-123">-InputObject</span></span>
<span data-ttu-id="51d22-124">역할 할당.</span><span class="sxs-lookup"><span data-stu-id="51d22-124">Role Assignment.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment
Parameter Sets: RoleAssignmentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="51d22-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="51d22-125">-PassThru</span></span>
<span data-ttu-id="51d22-126">지정된 경우 업데이트된 역할 할당을 표시</span><span class="sxs-lookup"><span data-stu-id="51d22-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="51d22-127">-Confirm</span><span class="sxs-lookup"><span data-stu-id="51d22-127">-Confirm</span></span>
<span data-ttu-id="51d22-128">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="51d22-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="51d22-129">-WhatIf</span></span>
<span data-ttu-id="51d22-130">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="51d22-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="51d22-131">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="51d22-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="51d22-132">CommonParameters</span></span>
<span data-ttu-id="51d22-133">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="51d22-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="51d22-134">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="51d22-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="51d22-135">입력</span><span class="sxs-lookup"><span data-stu-id="51d22-135">INPUTS</span></span>

### <span data-ttu-id="51d22-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51d22-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="51d22-137">출력</span><span class="sxs-lookup"><span data-stu-id="51d22-137">OUTPUTS</span></span>

### <span data-ttu-id="51d22-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="51d22-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="51d22-139">참고 사항</span><span class="sxs-lookup"><span data-stu-id="51d22-139">NOTES</span></span>

## <span data-ttu-id="51d22-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="51d22-140">RELATED LINKS</span></span>
