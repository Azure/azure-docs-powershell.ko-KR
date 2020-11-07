---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzManagementGroup.md
ms.openlocfilehash: 7998772b1a8e6a510e1eaec5daefaf4203259ab2
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878886"
---
# <span data-ttu-id="a5ec3-101">New-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5ec3-101">New-AzManagementGroup</span></span>

## <span data-ttu-id="a5ec3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ec3-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ec3-103">관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5ec3-103">Creates a Management Group</span></span>

## <span data-ttu-id="a5ec3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a5ec3-104">SYNTAX</span></span>

### <span data-ttu-id="a5ec3-105">GroupOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="a5ec3-105">GroupOperations (Default)</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="a5ec3-106">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="a5ec3-106">ParentGroupObject</span></span>
```
New-AzManagementGroup [-GroupName] <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ec3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="a5ec3-107">DESCRIPTION</span></span>
<span data-ttu-id="a5ec3-108">**새 AzManagementGroup** cmdlet은 관리 그룹을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-108">The **New-AzManagementGroup** cmdlet creates a management group.</span></span>

## <span data-ttu-id="a5ec3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="a5ec3-109">EXAMPLES</span></span>

### <span data-ttu-id="a5ec3-110">예제 1: 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5ec3-110">Example 1: Create a Management Group</span></span>
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

<span data-ttu-id="a5ec3-111">및가로 설정 된 새 그룹 만들기 `DisplayName` `ParentId` `null`</span><span class="sxs-lookup"><span data-stu-id="a5ec3-111">Creation of a new group with `DisplayName` and `ParentId` set to `null`.</span></span> <span data-ttu-id="a5ec3-112">은와 (과) `DisplayName` 같으며 `GroupName` , 그룹의 부모는 테 넌 트가 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-112">The `DisplayName` will be same as the `GroupName` and the parent of the group will be the tenant.</span></span>  

### <span data-ttu-id="a5ec3-113">예제 2: 표시 이름을 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5ec3-113">Example 2: Create a Management Group with a display name</span></span>
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

<span data-ttu-id="a5ec3-114">이 경우 그룹의 부모는 테 넌 트가 되며 `DisplayName` 지정 된 값으로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-114">In this case, the parent of the group will be the tenant and the `DisplayName` will be set to the value given.</span></span>

### <span data-ttu-id="a5ec3-115">예제 3: 부모 및 표시 이름을 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5ec3-115">Example 3: Create a Management Group with a parent and a display name</span></span>
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

### <span data-ttu-id="a5ec3-116">예제 4: 부모 개체를 사용 하 여 관리 그룹 만들기</span><span class="sxs-lookup"><span data-stu-id="a5ec3-116">Example 4: Create a Management Group with a parent (using a parent object)</span></span>
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

## <span data-ttu-id="a5ec3-117">변수</span><span class="sxs-lookup"><span data-stu-id="a5ec3-117">PARAMETERS</span></span>

### <span data-ttu-id="a5ec3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ec3-118">-DefaultProfile</span></span>
<span data-ttu-id="a5ec3-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-119">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a5ec3-120">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="a5ec3-120">-DisplayName</span></span>
<span data-ttu-id="a5ec3-121">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="a5ec3-121">Display Name of the management group</span></span>

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

### <span data-ttu-id="a5ec3-122">-GroupName</span><span class="sxs-lookup"><span data-stu-id="a5ec3-122">-GroupName</span></span>
<span data-ttu-id="a5ec3-123">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="a5ec3-123">Management Group Id</span></span>

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

### <span data-ttu-id="a5ec3-124">-ParentId</span><span class="sxs-lookup"><span data-stu-id="a5ec3-124">-ParentId</span></span>
<span data-ttu-id="a5ec3-125">관리 그룹의 상위 Id</span><span class="sxs-lookup"><span data-stu-id="a5ec3-125">Parent Id of the management group</span></span>

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

### <span data-ttu-id="a5ec3-126">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="a5ec3-126">-ParentObject</span></span>
<span data-ttu-id="a5ec3-127">부모 개체</span><span class="sxs-lookup"><span data-stu-id="a5ec3-127">Parent Object</span></span>

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

### <span data-ttu-id="a5ec3-128">-확인</span><span class="sxs-lookup"><span data-stu-id="a5ec3-128">-Confirm</span></span>
<span data-ttu-id="a5ec3-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ec3-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ec3-130">-WhatIf</span></span>
<span data-ttu-id="a5ec3-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ec3-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ec3-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ec3-133">CommonParameters</span></span>
<span data-ttu-id="a5ec3-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ec3-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ec3-136">입력</span><span class="sxs-lookup"><span data-stu-id="a5ec3-136">INPUTS</span></span>

### <span data-ttu-id="a5ec3-137">않아야</span><span class="sxs-lookup"><span data-stu-id="a5ec3-137">None</span></span>

## <span data-ttu-id="a5ec3-138">출력</span><span class="sxs-lookup"><span data-stu-id="a5ec3-138">OUTPUTS</span></span>

### <span data-ttu-id="a5ec3-139">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="a5ec3-139">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="a5ec3-140">상속자</span><span class="sxs-lookup"><span data-stu-id="a5ec3-140">NOTES</span></span>

## <span data-ttu-id="a5ec3-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a5ec3-141">RELATED LINKS</span></span>

[<span data-ttu-id="a5ec3-142">제거-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5ec3-142">Remove-AzManagementGroup</span></span>](./Remove-AzManagementGroup.md)

[<span data-ttu-id="a5ec3-143">업데이트-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5ec3-143">Update-AzManagementGroup</span></span>](./Update-AzManagementGroup.md)

[<span data-ttu-id="a5ec3-144">Get-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="a5ec3-144">Get-AzManagementGroup</span></span>](./Get-AzManagementGroup.md)