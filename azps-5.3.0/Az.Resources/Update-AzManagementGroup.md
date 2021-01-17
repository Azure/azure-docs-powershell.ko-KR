---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: bdef58db8dcda735a7a8c08350b806c9fd00cf21
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98491653"
---
# <span data-ttu-id="2c959-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c959-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="2c959-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2c959-102">SYNOPSIS</span></span>
<span data-ttu-id="2c959-103">관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c959-103">Updates a Management Group</span></span>

## <span data-ttu-id="2c959-104">구문</span><span class="sxs-lookup"><span data-stu-id="2c959-104">SYNTAX</span></span>

### <span data-ttu-id="2c959-105">GroupOperations(기본값)</span><span class="sxs-lookup"><span data-stu-id="2c959-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c959-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c959-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="2c959-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c959-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="2c959-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="2c959-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="2c959-109">설명</span><span class="sxs-lookup"><span data-stu-id="2c959-109">DESCRIPTION</span></span>
<span data-ttu-id="2c959-110">**Update-AzManagementGroup** cmdlet은 관리 그룹에 대한 **ParentId** 또는 **DisplayName을** 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="2c959-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="2c959-111">예제</span><span class="sxs-lookup"><span data-stu-id="2c959-111">EXAMPLES</span></span>

### <span data-ttu-id="2c959-112">예제 1: 관리 그룹의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c959-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="2c959-113">예제 2: 관리 그룹의 부모 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c959-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="2c959-114">예제 3: PSManagementGroup 개체를 파이핑하여 관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c959-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="2c959-115">예제 4: ParentObject를 사용하여 관리 그룹의 부모 업데이트</span><span class="sxs-lookup"><span data-stu-id="2c959-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="2c959-116">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="2c959-116">PARAMETERS</span></span>

### <span data-ttu-id="2c959-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2c959-117">-DefaultProfile</span></span>
<span data-ttu-id="2c959-118">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2c959-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2c959-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="2c959-119">-DisplayName</span></span>
<span data-ttu-id="2c959-120">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="2c959-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="2c959-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="2c959-121">-GroupName</span></span>
<span data-ttu-id="2c959-122">관리 그룹 ID</span><span class="sxs-lookup"><span data-stu-id="2c959-122">Management Group Id</span></span>

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

### <span data-ttu-id="2c959-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2c959-123">-InputObject</span></span>
<span data-ttu-id="2c959-124">Get 호출의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="2c959-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="2c959-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="2c959-125">-ParentId</span></span>
<span data-ttu-id="2c959-126">관리 그룹의 부모 ID</span><span class="sxs-lookup"><span data-stu-id="2c959-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="2c959-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="2c959-127">-ParentObject</span></span>
<span data-ttu-id="2c959-128">Get 호출의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="2c959-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="2c959-129">-Confirm</span><span class="sxs-lookup"><span data-stu-id="2c959-129">-Confirm</span></span>
<span data-ttu-id="2c959-130">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="2c959-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="2c959-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="2c959-131">-WhatIf</span></span>
<span data-ttu-id="2c959-132">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="2c959-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="2c959-133">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2c959-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="2c959-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2c959-134">CommonParameters</span></span>
<span data-ttu-id="2c959-135">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="2c959-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2c959-136">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="2c959-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2c959-137">입력</span><span class="sxs-lookup"><span data-stu-id="2c959-137">INPUTS</span></span>

### <span data-ttu-id="2c959-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c959-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="2c959-139">출력</span><span class="sxs-lookup"><span data-stu-id="2c959-139">OUTPUTS</span></span>

### <span data-ttu-id="2c959-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span><span class="sxs-lookup"><span data-stu-id="2c959-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="2c959-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="2c959-141">NOTES</span></span>

## <span data-ttu-id="2c959-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2c959-142">RELATED LINKS</span></span>
