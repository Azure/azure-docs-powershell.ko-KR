---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: fc16d7ba4600e29c449469202046639a2f805fc2
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876442"
---
# <span data-ttu-id="0a2a2-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0a2a2-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="0a2a2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a2a2-102">SYNOPSIS</span></span>
<span data-ttu-id="0a2a2-103">관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0a2a2-103">Creates a Management Group</span></span>

## <span data-ttu-id="0a2a2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a2a2-104">SYNTAX</span></span>

### <span data-ttu-id="0a2a2-105">GroupOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="0a2a2-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="0a2a2-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="0a2a2-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="0a2a2-107">설명은</span><span class="sxs-lookup"><span data-stu-id="0a2a2-107">DESCRIPTION</span></span>
<span data-ttu-id="0a2a2-108">**새 AzManagementGroup** cmdlet은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="0a2a2-109">예제의</span><span class="sxs-lookup"><span data-stu-id="0a2a2-109">EXAMPLES</span></span>

### <span data-ttu-id="0a2a2-110">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0a2a2-110">Example 1: Create a Management Group</span></span>
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

<span data-ttu-id="0a2a2-111">및가로 설정 된 새 그룹 만들기 `DisplayName` `ParentId` `null`</span><span class="sxs-lookup"><span data-stu-id="0a2a2-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="0a2a2-112">은와 (과) `DisplayName` 같으며 `GroupName` , 그룹의 부모는 테 넌 트가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="0a2a2-113">예제 2: 표시 이름을 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0a2a2-113">Example 2: Create a Management Group with a display name</span></span>
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

<span data-ttu-id="0a2a2-114">이 경우 그룹의 부모는 테 넌 트가 되며 `DisplayName` 지정 된 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="0a2a2-115">예제 3: 부모 및 표시 이름을 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0a2a2-115">Example 3: Create a Management Group with a parent and a display name</span></span>
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

### <span data-ttu-id="0a2a2-116">예제 4: 부모 개체를 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="0a2a2-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
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

## <span data-ttu-id="0a2a2-117">변수</span><span class="sxs-lookup"><span data-stu-id="0a2a2-117">PARAMETERS</span></span>

### <span data-ttu-id="0a2a2-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a2a2-118">-DefaultProfile</span></span>
<span data-ttu-id="0a2a2-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2a2-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="0a2a2-120">-DisplayName</span></span>
<span data-ttu-id="0a2a2-121">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="0a2a2-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="0a2a2-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="0a2a2-122">-GroupName</span></span>
<span data-ttu-id="0a2a2-123">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="0a2a2-123">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0a2a2-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="0a2a2-124">-ParentId</span></span>
<span data-ttu-id="0a2a2-125">관리 그룹의 상위 Id</span><span class="sxs-lookup"><span data-stu-id="0a2a2-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="0a2a2-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="0a2a2-126">-ParentObject</span></span>
<span data-ttu-id="0a2a2-127">부모 개체</span><span class="sxs-lookup"><span data-stu-id="0a2a2-127">Parent Object</span></span>

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

### <span data-ttu-id="0a2a2-128">-확인</span><span class="sxs-lookup"><span data-stu-id="0a2a2-128">-Confirm</span></span>
<span data-ttu-id="0a2a2-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a2a2-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a2a2-130">-WhatIf</span></span>
<span data-ttu-id="0a2a2-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a2a2-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a2a2-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a2a2-133">CommonParameters</span></span>
<span data-ttu-id="0a2a2-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a2a2-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a2a2-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a2a2-136">입력</span><span class="sxs-lookup"><span data-stu-id="0a2a2-136">INPUTS</span></span>

### <span data-ttu-id="0a2a2-137">않아야</span><span class="sxs-lookup"><span data-stu-id="0a2a2-137">None</span></span>

## <span data-ttu-id="0a2a2-138">출력</span><span class="sxs-lookup"><span data-stu-id="0a2a2-138">OUTPUTS</span></span>

### <span data-ttu-id="0a2a2-139">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="0a2a2-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="0a2a2-140">상속자</span><span class="sxs-lookup"><span data-stu-id="0a2a2-140">NOTES</span></span>

## <span data-ttu-id="0a2a2-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a2a2-141">RELATED LINKS</span></span>

[<span data-ttu-id="0a2a2-142">제거-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0a2a2-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="0a2a2-143">업데이트-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0a2a2-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="0a2a2-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="0a2a2-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)