---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 07272df9b1892373d23b89447f1c21a5a4fb53c0
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98344078"
---
# <span data-ttu-id="34d94-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="34d94-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="34d94-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="34d94-102">SYNOPSIS</span></span>
<span data-ttu-id="34d94-103">관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-103">Creates a Management Group</span></span>

## <span data-ttu-id="34d94-104">구문</span><span class="sxs-lookup"><span data-stu-id="34d94-104">SYNTAX</span></span>

### <span data-ttu-id="34d94-105">GroupOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="34d94-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="34d94-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="34d94-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="34d94-107">설명</span><span class="sxs-lookup"><span data-stu-id="34d94-107">DESCRIPTION</span></span>
<span data-ttu-id="34d94-108">**New-AzManagementGroup** cmdlet은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="34d94-109">예제</span><span class="sxs-lookup"><span data-stu-id="34d94-109">EXAMPLES</span></span>

### <span data-ttu-id="34d94-110">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="34d94-110">Example 1: Create a Management Group</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="34d94-111">.로 설정된 새 `DisplayName` `ParentId` 그룹 만들기 `null`</span><span class="sxs-lookup"><span data-stu-id="34d94-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="34d94-112">그룹의 부모와 동일하며 `DisplayName` `GroupName` 테넌트가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="34d94-113">예제 2: 표시 이름을 사용하여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="34d94-113">Example 2: Create a Management Group with a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 11:06:27 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/14307de0-5e6f-46cf-b2ba-64a062964d30
ParentName        : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentDisplayName : 14307de0-5e6f-46cf-b2ba-64a062964d30
```

<span data-ttu-id="34d94-114">이 경우 그룹의 부모는 테넌트가 며, 이 값은 주어진 `DisplayName` 값으로 설정됩니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="34d94-115">예제 3: 부모 및 표시 이름을 사용하여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="34d94-115">Example 3: Create a Management Group with a parent and a display name</span></span>
```
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -DisplayName "TestGroupDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="34d94-116">예제 4: 부모가 있는 관리 그룹 만들기(부모 개체 사용)</span><span class="sxs-lookup"><span data-stu-id="34d94-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> New-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 14307de0-5e6f-46cf-b2ba-64a062964d30
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 14307de0-5e6f-46cf-b2ba-64a062964d30
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

## <span data-ttu-id="34d94-117">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="34d94-117">PARAMETERS</span></span>

### <span data-ttu-id="34d94-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="34d94-118">-DefaultProfile</span></span>
<span data-ttu-id="34d94-119">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="34d94-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="34d94-120">-DisplayName</span></span>
<span data-ttu-id="34d94-121">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="34d94-121">Display Name of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d94-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="34d94-122">-GroupName</span></span>
<span data-ttu-id="34d94-123">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="34d94-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d94-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="34d94-124">-ParentId</span></span>
<span data-ttu-id="34d94-125">관리 그룹의 부모 ID</span><span class="sxs-lookup"><span data-stu-id="34d94-125">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d94-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="34d94-126">-ParentObject</span></span>
<span data-ttu-id="34d94-127">부모 개체</span><span class="sxs-lookup"><span data-stu-id="34d94-127">Parent Object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="34d94-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="34d94-128">-Confirm</span></span>
<span data-ttu-id="34d94-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="34d94-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="34d94-130">-WhatIf</span></span>
<span data-ttu-id="34d94-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="34d94-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="34d94-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="34d94-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="34d94-133">CommonParameters</span></span>
<span data-ttu-id="34d94-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="34d94-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="34d94-135">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="34d94-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="34d94-136">입력</span><span class="sxs-lookup"><span data-stu-id="34d94-136">INPUTS</span></span>

### <span data-ttu-id="34d94-137">없음</span><span class="sxs-lookup"><span data-stu-id="34d94-137">None</span></span>

## <span data-ttu-id="34d94-138">출력</span><span class="sxs-lookup"><span data-stu-id="34d94-138">OUTPUTS</span></span>

### <span data-ttu-id="34d94-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="34d94-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="34d94-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="34d94-140">NOTES</span></span>

## <span data-ttu-id="34d94-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="34d94-141">RELATED LINKS</span></span>

[<span data-ttu-id="34d94-142">Remove-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="34d94-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="34d94-143">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="34d94-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="34d94-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="34d94-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)