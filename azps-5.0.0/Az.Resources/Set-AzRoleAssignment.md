---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azroleassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzRoleAssignment.md
ms.openlocfilehash: 9342ea2486c28a44ba7ff4a22f21619846ac7010
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94226526"
---
# <span data-ttu-id="f9103-101">Set-AzRoleAssignment</span><span class="sxs-lookup"><span data-stu-id="f9103-101">Set-AzRoleAssignment</span></span>

## <span data-ttu-id="f9103-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9103-102">SYNOPSIS</span></span>
<span data-ttu-id="f9103-103">기존 역할 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-103">Update an existing Role Assignment.</span></span>

## <span data-ttu-id="f9103-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9103-104">SYNTAX</span></span>

### <span data-ttu-id="f9103-105">RoleAssignmentParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="f9103-105">RoleAssignmentParameterSet (Default)</span></span>
```
Set-AzRoleAssignment -InputObject <PSRoleAssignment> [-PassThru] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f9103-106">InputFileParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9103-106">InputFileParameterSet</span></span>
```
Set-AzRoleAssignment -InputFile <String> [-PassThru] [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9103-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f9103-107">DESCRIPTION</span></span>
<span data-ttu-id="f9103-108">New-AzRoleAssignment 명령을 사용 하 여 기존 과제를 수정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-108">Use the New-AzRoleAssignment command to modify an existing assignment.</span></span>  
<span data-ttu-id="f9103-109">설명은 유효한 문자열일 수 있으며,이를 사용 하 여 서로를 diferentiate.</span><span class="sxs-lookup"><span data-stu-id="f9103-109">Descriptions can be any valid string, use that to diferentiate from one another.</span></span>  
<span data-ttu-id="f9103-110">조건이 설정 된 경우에도 조건 버전을 설정 해야 하지만 필요 하지 않은 조건을 업데이트 하는 경우</span><span class="sxs-lookup"><span data-stu-id="f9103-110">if Condition is set Condition Version has to be set as well but if you're updating a Condition that is not necesary.</span></span>
<span data-ttu-id="f9103-111">조건 버전을 1.0에서 2.0로 업그레이드할 수 있지만 다시 다운 그레이드할 수는 없습니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-111">Condition Version can be upgraded from 1.0 to 2.0 but it can't not be downgraded back.</span></span> <span data-ttu-id="f9103-112">2.0는 1.0와 retrocompatible 되지 않기 때문에 주의를 기울여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-112">Be cautious as 2.0 is not retrocompatible with 1.0.</span></span>

## <span data-ttu-id="f9103-113">예제의</span><span class="sxs-lookup"><span data-stu-id="f9103-113">EXAMPLES</span></span>

### <span data-ttu-id="f9103-114">예제 1</span><span class="sxs-lookup"><span data-stu-id="f9103-114">Example 1</span></span>
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

<span data-ttu-id="f9103-115">개체를 수정 하 여 기존 역할 할당 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9103-115">Update an existing role assignment by modifying an object</span></span>

### <span data-ttu-id="f9103-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="f9103-116">Example 2</span></span>
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

<span data-ttu-id="f9103-117">파일을 사용 하 여 기존 역할 할당 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9103-117">Update an existing role assignment by using a file</span></span>

## <span data-ttu-id="f9103-118">변수</span><span class="sxs-lookup"><span data-stu-id="f9103-118">PARAMETERS</span></span>

### <span data-ttu-id="f9103-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9103-119">-DefaultProfile</span></span>
<span data-ttu-id="f9103-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-120">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9103-121">-InputFile</span><span class="sxs-lookup"><span data-stu-id="f9103-121">-InputFile</span></span>
<span data-ttu-id="f9103-122">단일 역할 정의를 포함 하는 파일 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-122">File name containing a single role definition.</span></span>

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

### <span data-ttu-id="f9103-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f9103-123">-InputObject</span></span>
<span data-ttu-id="f9103-124">역할 할당.</span><span class="sxs-lookup"><span data-stu-id="f9103-124">Role Assignment.</span></span>

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

### <span data-ttu-id="f9103-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="f9103-125">-PassThru</span></span>
<span data-ttu-id="f9103-126">지정 된 경우 업데이트 된 역할 할당을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-126">If specified, displays the updated role assignment</span></span>

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

### <span data-ttu-id="f9103-127">-확인</span><span class="sxs-lookup"><span data-stu-id="f9103-127">-Confirm</span></span>
<span data-ttu-id="f9103-128">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-128">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9103-129">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9103-129">-WhatIf</span></span>
<span data-ttu-id="f9103-130">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-130">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9103-131">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-131">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9103-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9103-132">CommonParameters</span></span>
<span data-ttu-id="f9103-133">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9103-134">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f9103-134">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9103-135">입력</span><span class="sxs-lookup"><span data-stu-id="f9103-135">INPUTS</span></span>

### <span data-ttu-id="f9103-136">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-136">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f9103-137">출력</span><span class="sxs-lookup"><span data-stu-id="f9103-137">OUTPUTS</span></span>

### <span data-ttu-id="f9103-138">.Resources. PSRoleAssignment를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9103-138">Microsoft.Azure.Commands.Resources.Models.Authorization.PSRoleAssignment</span></span>

## <span data-ttu-id="f9103-139">상속자</span><span class="sxs-lookup"><span data-stu-id="f9103-139">NOTES</span></span>

## <span data-ttu-id="f9103-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9103-140">RELATED LINKS</span></span>
