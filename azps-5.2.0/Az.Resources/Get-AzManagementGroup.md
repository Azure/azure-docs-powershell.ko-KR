---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzManagementGroup.md
ms.openlocfilehash: f21a6d641e06916ce70c71338b539ef0909db6de
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98325254"
---
# <span data-ttu-id="e55bf-101">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e55bf-101">Get-AzManagementGroup</span></span>

## <span data-ttu-id="e55bf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e55bf-102">SYNOPSIS</span></span>
<span data-ttu-id="e55bf-103">관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-103">Gets Management Group(s)</span></span>

## <span data-ttu-id="e55bf-104">구문</span><span class="sxs-lookup"><span data-stu-id="e55bf-104">SYNTAX</span></span>

### <span data-ttu-id="e55bf-105">ListOperation(기본값)</span><span class="sxs-lookup"><span data-stu-id="e55bf-105">ListOperation (Default)</span></span>
```
Get-AzManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e55bf-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="e55bf-106">GetOperation</span></span>
```
Get-AzManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand] [-Recurse]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e55bf-107">설명</span><span class="sxs-lookup"><span data-stu-id="e55bf-107">DESCRIPTION</span></span>
<span data-ttu-id="e55bf-108">Get-AzManagementGroup cmdlet은 전체 또는 특정 관리 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-108">The Get-AzManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="e55bf-109">예제</span><span class="sxs-lookup"><span data-stu-id="e55bf-109">EXAMPLES</span></span>

### <span data-ttu-id="e55bf-110">예제 1: 모든 관리 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="e55bf-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzManagementGroup

Id          : /providers/Microsoft.Management/managementGroups/TestGroup
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroup
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupDisplayName

Id          : /providers/Microsoft.Management/managementGroups/TestGroupChild
Type        : /providers/Microsoft.Management/managementGroups
Name        : TestGroupChild
TenantId    : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName : TestGroupChildDisplayName
```

### <span data-ttu-id="e55bf-111">예제 2: 특정 관리 그룹 얻기</span><span class="sxs-lookup"><span data-stu-id="e55bf-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName TestGroup

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupDisplayName
UpdatedTime       : 2/1/2018 11:16:12 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="e55bf-112">예제 3: 특정 관리 그룹 및 첫 번째 계층 구조 수준 얻기</span><span class="sxs-lookup"><span data-stu-id="e55bf-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzManagementGroup -GroupName TestGroupParent -Expand
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    :
```

<span data-ttu-id="e55bf-113">플래그를 사용하여 배열을 탐색하고 각 자식에 대한 `Expand` 세부 정보를 얻을 수 `Children` 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="e55bf-114">예를 들어 표시 이름이 있는 그룹에 `Children[0]` 대한 세부 정보를 `TestGroup1DisplayName` 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="e55bf-115">예제 4: 특정 관리 그룹 및 모든 계층 구조 수준 얻기</span><span class="sxs-lookup"><span data-stu-id="e55bf-115">Example 4: Get specific Management Group and all levels of hierarchy</span></span>
```
PS C:\> $response = Get-AzManagementGroup -GroupName TestGroupParent -Expand -Recurse
PS C:\> $response

Id                : /providers/Microsoft.Management/managementGroups/TestGroupParent
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroupParent
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroupParent
UpdatedTime       : 2/1/2018 11:15:46 AM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
Children          : {TestGroup1DisplayName, TestGroup2DisplayName}

PS C:\> $response.Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestGroup1
Name        : TestGroup1
DisplayName : TestGroup1DisplayName
Children    : {TestRecurseChild}

PS C:\> $response.Children[0].Children[0]

Type        : /managementGroup
Id          : /providers/Microsoft.Management/managementGroups/TestRecurseChild
Name        : TestRecurseChild
DisplayName : TestRecurseChild
Children    :
```

## <span data-ttu-id="e55bf-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e55bf-116">PARAMETERS</span></span>

### <span data-ttu-id="e55bf-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e55bf-117">-DefaultProfile</span></span>
<span data-ttu-id="e55bf-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e55bf-119">-Expand</span><span class="sxs-lookup"><span data-stu-id="e55bf-119">-Expand</span></span>
<span data-ttu-id="e55bf-120">출력을 확장하여 관리 그룹의 자식 목록을 나열합니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-120">Expand the output to list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55bf-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="e55bf-121">-GroupName</span></span>
<span data-ttu-id="e55bf-122">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="e55bf-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases: GroupId

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55bf-123">-Recurse</span><span class="sxs-lookup"><span data-stu-id="e55bf-123">-Recurse</span></span>
<span data-ttu-id="e55bf-124">관리 그룹의 자식 항목 다시 나열</span><span class="sxs-lookup"><span data-stu-id="e55bf-124">Recursively list the children of the management group</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: GetOperation
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e55bf-125">-Confirm</span><span class="sxs-lookup"><span data-stu-id="e55bf-125">-Confirm</span></span>
<span data-ttu-id="e55bf-126">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e55bf-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e55bf-127">-WhatIf</span></span>
<span data-ttu-id="e55bf-128">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="e55bf-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e55bf-129">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e55bf-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e55bf-130">CommonParameters</span></span>
<span data-ttu-id="e55bf-131">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e55bf-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e55bf-132">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e55bf-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e55bf-133">입력</span><span class="sxs-lookup"><span data-stu-id="e55bf-133">INPUTS</span></span>

### <span data-ttu-id="e55bf-134">없음</span><span class="sxs-lookup"><span data-stu-id="e55bf-134">None</span></span>

## <span data-ttu-id="e55bf-135">출력</span><span class="sxs-lookup"><span data-stu-id="e55bf-135">OUTPUTS</span></span>

### <span data-ttu-id="e55bf-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span><span class="sxs-lookup"><span data-stu-id="e55bf-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="e55bf-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="e55bf-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="e55bf-138">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e55bf-138">NOTES</span></span>

## <span data-ttu-id="e55bf-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e55bf-139">RELATED LINKS</span></span>
