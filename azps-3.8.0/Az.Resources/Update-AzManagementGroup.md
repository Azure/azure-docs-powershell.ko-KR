---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzManagementGroup.md
ms.openlocfilehash: d65a94e104b7a5b3e5503b30aefe87fd7b1fa531
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93878058"
---
# <span data-ttu-id="409d8-101">Update-AzManagementGroup</span><span class="sxs-lookup"><span data-stu-id="409d8-101">Update-AzManagementGroup</span></span>

## <span data-ttu-id="409d8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="409d8-102">SYNOPSIS</span></span>
<span data-ttu-id="409d8-103">관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="409d8-103">Updates a Management Group</span></span>

## <span data-ttu-id="409d8-104">구문과</span><span class="sxs-lookup"><span data-stu-id="409d8-104">SYNTAX</span></span>

### <span data-ttu-id="409d8-105">GroupOperations (기본값)</span><span class="sxs-lookup"><span data-stu-id="409d8-105">GroupOperations (Default)</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409d8-106">ParentAndManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="409d8-106">ParentAndManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>]
 [-DefaultProfile <IAzureContextContainer>] -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="409d8-107">ManagementGroupObject</span><span class="sxs-lookup"><span data-stu-id="409d8-107">ManagementGroupObject</span></span>
```
Update-AzManagementGroup -InputObject <PSManagementGroup> [-DisplayName <String>] [-ParentId <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="409d8-108">ParentGroupObject</span><span class="sxs-lookup"><span data-stu-id="409d8-108">ParentGroupObject</span></span>
```
Update-AzManagementGroup -GroupName <String> [-DisplayName <String>] [-DefaultProfile <IAzureContextContainer>]
 -ParentObject <PSManagementGroup> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="409d8-109">설명은</span><span class="sxs-lookup"><span data-stu-id="409d8-109">DESCRIPTION</span></span>
<span data-ttu-id="409d8-110">**업데이트 AzManagementGroup** Cmdlet은 관리 그룹의 **ParentId** 또는 **DisplayName** 을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-110">The **Update-AzManagementGroup** cmdlet updates the **ParentId** or **DisplayName** for a Management Group.</span></span>

## <span data-ttu-id="409d8-111">예제의</span><span class="sxs-lookup"><span data-stu-id="409d8-111">EXAMPLES</span></span>

### <span data-ttu-id="409d8-112">예제 1: 관리 그룹의 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="409d8-112">Example 1: Update a Management Group's Display Name</span></span>
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

### <span data-ttu-id="409d8-113">예제 2: 관리 그룹의 상위 업데이트</span><span class="sxs-lookup"><span data-stu-id="409d8-113">Example 2: Update a Management Group's Parent</span></span>
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

### <span data-ttu-id="409d8-114">예제 3: 파이핑 PSManagementGroup 개체를 기준으로 관리 그룹 업데이트</span><span class="sxs-lookup"><span data-stu-id="409d8-114">Example 3: Update a Management Group by piping PSManagementGroup Object</span></span>
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

### <span data-ttu-id="409d8-115">예제 4: ParentObject를 사용 하 여 관리 그룹의 상위 업데이트</span><span class="sxs-lookup"><span data-stu-id="409d8-115">Example 4: Update a Management Group's parent using the ParentObject</span></span>
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

## <span data-ttu-id="409d8-116">변수</span><span class="sxs-lookup"><span data-stu-id="409d8-116">PARAMETERS</span></span>

### <span data-ttu-id="409d8-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="409d8-117">-DefaultProfile</span></span>
<span data-ttu-id="409d8-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="409d8-119">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="409d8-119">-DisplayName</span></span>
<span data-ttu-id="409d8-120">관리 그룹의 표시 이름</span><span class="sxs-lookup"><span data-stu-id="409d8-120">Display Name of the management group</span></span>

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

### <span data-ttu-id="409d8-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="409d8-121">-GroupName</span></span>
<span data-ttu-id="409d8-122">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="409d8-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GroupOperations, ParentGroupObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="409d8-123">-InputObject</span><span class="sxs-lookup"><span data-stu-id="409d8-123">-InputObject</span></span>
<span data-ttu-id="409d8-124">Get 전화의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="409d8-124">Input Object from the Get call</span></span>

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

### <span data-ttu-id="409d8-125">-ParentId</span><span class="sxs-lookup"><span data-stu-id="409d8-125">-ParentId</span></span>
<span data-ttu-id="409d8-126">관리 그룹의 상위 Id</span><span class="sxs-lookup"><span data-stu-id="409d8-126">Parent Id of the management group</span></span>

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

### <span data-ttu-id="409d8-127">-ParentObject</span><span class="sxs-lookup"><span data-stu-id="409d8-127">-ParentObject</span></span>
<span data-ttu-id="409d8-128">Get 전화의 입력 개체</span><span class="sxs-lookup"><span data-stu-id="409d8-128">Input Object from the Get call</span></span>

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

### <span data-ttu-id="409d8-129">-확인</span><span class="sxs-lookup"><span data-stu-id="409d8-129">-Confirm</span></span>
<span data-ttu-id="409d8-130">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-130">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="409d8-131">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="409d8-131">-WhatIf</span></span>
<span data-ttu-id="409d8-132">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-132">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="409d8-133">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-133">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="409d8-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="409d8-134">CommonParameters</span></span>
<span data-ttu-id="409d8-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="409d8-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="409d8-136">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="409d8-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="409d8-137">입력</span><span class="sxs-lookup"><span data-stu-id="409d8-137">INPUTS</span></span>

### <span data-ttu-id="409d8-138">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="409d8-138">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="409d8-139">출력</span><span class="sxs-lookup"><span data-stu-id="409d8-139">OUTPUTS</span></span>

### <span data-ttu-id="409d8-140">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="409d8-140">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="409d8-141">상속자</span><span class="sxs-lookup"><span data-stu-id="409d8-141">NOTES</span></span>

## <span data-ttu-id="409d8-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="409d8-142">RELATED LINKS</span></span>
