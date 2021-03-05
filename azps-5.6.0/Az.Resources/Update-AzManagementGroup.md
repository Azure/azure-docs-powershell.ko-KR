---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: 23d60b0251c50f5bf4d5174e1ea1b5ef6f60b0ae
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972576"
---
# <span data-ttu-id="c844f-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c844f-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="c844f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c844f-102">SYNOPSIS</span></span>
<span data-ttu-id="c844f-103">관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="c844f-103">Updates a Management Group</span></span>

## <span data-ttu-id="c844f-104">구문</span><span class="sxs-lookup"><span data-stu-id="c844f-104">SYNTAX</span></span>

### <span data-ttu-id="c844f-105">GroupOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="c844f-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c844f-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="c844f-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c844f-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="c844f-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c844f-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="c844f-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c844f-109">설명</span><span class="sxs-lookup"><span data-stu-id="c844f-109">DESCRIPTION</span></span>
<span data-ttu-id="c844f-110">**Update-AzManagementGroup** cmdlet은 관리 그룹에 대한 **ParentId** 또는 **DisplayName을** 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="c844f-111">예제</span><span class="sxs-lookup"><span data-stu-id="c844f-111">EXAMPLES</span></span>

### <span data-ttu-id="c844f-112">예제 1: 관리 그룹의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="c844f-112">Example 1: Update a Management Group's Display Name</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -DisplayName "New Display Name"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : New Display Name
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentName        : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
ParentDisplayName : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
```

### <span data-ttu-id="c844f-113">예제 2: 관리 그룹의 부모 업데이트</span><span class="sxs-lookup"><span data-stu-id="c844f-113">Example 2: Update a Management Group's Parent</span></span>
```
PS C:\> Update-AzManagementGroup -Group "TestGroup" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestGroup
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="c844f-114">예제 3: PSManagementGroup 개체를 피핑하여 관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="c844f-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
```
PS C:\> Get-AzManagementGroup -GroupName "TestGroup" | Update-AzManagementGroup -DisplayName "TestDisplayName" -ParentId "/providers/Microsoft.Management/managementGroups/TestGroupParent"

Id                : /providers/Microsoft.Management/managementGroups/TestGroup
Type              : /providers/Microsoft.Management/managementGroups
Name              : TestGroup
TenantId          : 6b2064b9-34bd-46e6-9092-52f2dd5f7fc0
DisplayName       : TestDisplayName
UpdatedTime       : 2/1/2018 12:03:37 PM
UpdatedBy         : 64360beb-ffb4-43a8-9314-01aa34db95a9
ParentId          : /providers/Microsoft.Management/managementGroups/TestGroupParent
ParentName        : TestGroupParent
ParentDisplayName : TestGroupParent
```

### <span data-ttu-id="c844f-115">예제 4: ParentObject를 사용하여 관리 그룹의 부모 업데이트</span><span class="sxs-lookup"><span data-stu-id="c844f-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
```
PS C:\> $parentObject = Get-AzManagementGroup -GroupName "TestGroupParent"
PS C:\> Update-AzManagementGroup -GroupName "TestGroup" -ParentObject $parentObject

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

## <span data-ttu-id="c844f-116">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c844f-116">PARAMETERS</span></span>

### <span data-ttu-id="c844f-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c844f-117">-DefaultProfile</span></span>
<span data-ttu-id="c844f-118">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c844f-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="c844f-119">-DisplayName</span></span>
<span data-ttu-id="c844f-120">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="c844f-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="c844f-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="c844f-121">-GroupName</span></span>
<span data-ttu-id="c844f-122">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="c844f-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases: GroupId

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c844f-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="c844f-123">-InputObject</span></span>
<span data-ttu-id="c844f-124">호출 시작에서 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c844f-124">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ManagementGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c844f-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="c844f-125">-ParentId</span></span>
<span data-ttu-id="c844f-126">관리 그룹의 부모 ID</span><span class="sxs-lookup"><span data-stu-id="c844f-126">Parent Id of the management group</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ManagementGroupObject
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c844f-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="c844f-127">-ParentObject</span></span>
<span data-ttu-id="c844f-128">호출 시작에서 입력 개체</span><span class="sxs-lookup"><span data-stu-id="c844f-128">Input Object from the Get call</span></span>

```yaml
Type: Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup
Parameter Sets: ParentAndManagementGroupObject, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c844f-129">-확인</span><span class="sxs-lookup"><span data-stu-id="c844f-129">-Confirm</span></span>
<span data-ttu-id="c844f-130">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c844f-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c844f-131">-WhatIf</span></span>
<span data-ttu-id="c844f-132">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c844f-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c844f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c844f-134">CommonParameters</span></span>
<span data-ttu-id="c844f-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c844f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c844f-136">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c844f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c844f-137">입력</span><span class="sxs-lookup"><span data-stu-id="c844f-137">INPUTS</span></span>

### <span data-ttu-id="c844f-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c844f-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="c844f-139">출력</span><span class="sxs-lookup"><span data-stu-id="c844f-139">OUTPUTS</span></span>

### <span data-ttu-id="c844f-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="c844f-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="c844f-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c844f-141">NOTES</span></span>

## <span data-ttu-id="c844f-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c844f-142">RELATED LINKS</span></span>
