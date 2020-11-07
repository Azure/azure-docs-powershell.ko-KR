---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermmanagementgroup/
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Get-AzureRmManagementGroup.md
ms.openlocfilehash: 275b13efa25bbffd2c104a1e9cfa3baf04fffe89
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703133"
---
# <span data-ttu-id="d2840-101">Get-AzureRmManagementGroup</span><span class="sxs-lookup"><span data-stu-id="d2840-101">Get-AzureRmManagementGroup</span></span>

## <span data-ttu-id="d2840-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d2840-102">SYNOPSIS</span></span>
<span data-ttu-id="d2840-103">관리 그룹 (들)을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-103">Gets Management Group(s)</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d2840-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d2840-104">SYNTAX</span></span>

### <span data-ttu-id="d2840-105">ListOperation (기본값)</span><span class="sxs-lookup"><span data-stu-id="d2840-105">ListOperation (Default)</span></span>
```
Get-AzureRmManagementGroup [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d2840-106">GetOperation</span><span class="sxs-lookup"><span data-stu-id="d2840-106">GetOperation</span></span>
```
Get-AzureRmManagementGroup [-GroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-Expand]
 [-Recurse] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d2840-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d2840-107">DESCRIPTION</span></span>
<span data-ttu-id="d2840-108">Get-AzureRMManagementGroup cmdlet은 모든 또는 특정 관리 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-108">The Get-AzureRMManagementGroup cmdlet Gets all or a specific Management Group.</span></span>

## <span data-ttu-id="d2840-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d2840-109">EXAMPLES</span></span>

### <span data-ttu-id="d2840-110">예제 1: 모든 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2840-110">Example 1: Get all Management Groups</span></span>
```
PS C:\> Get-AzureRmManagementGroup

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

### <span data-ttu-id="d2840-111">예제 2: 특정 관리 그룹 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2840-111">Example 2: Get specific Management Group</span></span>
```
PS C:\> Get-AzureRmManagementGroup -GroupName TestGroup

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

### <span data-ttu-id="d2840-112">예제 3: 특정 관리 그룹 및 계층의 첫 번째 수준 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2840-112">Example 3: Get specific Management Group and first level of hierarchy</span></span>
```
PS C:\> $reponse = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand
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

<span data-ttu-id="d2840-113">플래그를 사용 하 여 `Expand` `Children` 배열을 탐색 하 고 각 자식에 대 한 세부 정보를 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-113">With the `Expand` flag, one can navigate through the `Children` array and get details for each child.</span></span> <span data-ttu-id="d2840-114">예를 들어 `Children[0]` 표시 이름을 사용 하 여 그룹에 대 한 세부 정보를 제공 `TestGroup1DisplayName` 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-114">For example, `Children[0]` will give details for the group with display name `TestGroup1DisplayName`.</span></span>

### <span data-ttu-id="d2840-115">예제 4: 특정 관리 그룹 및 모든 수준의 hiearchy 가져오기</span><span class="sxs-lookup"><span data-stu-id="d2840-115">Example 4: Get specific Management Group and all levels of hiearchy</span></span>
```
PS C:\> $response = Get-AzureRmManagementGroup -GroupName TestGroupParent -Expand -Recurse
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

## <span data-ttu-id="d2840-116">변수</span><span class="sxs-lookup"><span data-stu-id="d2840-116">PARAMETERS</span></span>

### <span data-ttu-id="d2840-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d2840-117">-DefaultProfile</span></span>
<span data-ttu-id="d2840-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2840-119">-확장</span><span class="sxs-lookup"><span data-stu-id="d2840-119">-Expand</span></span>
<span data-ttu-id="d2840-120">출력을 확장 하 여 관리 그룹의 하위 항목 나열</span><span class="sxs-lookup"><span data-stu-id="d2840-120">Expand the output to list the children of the management group</span></span>

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

### <span data-ttu-id="d2840-121">-GroupName</span><span class="sxs-lookup"><span data-stu-id="d2840-121">-GroupName</span></span>
<span data-ttu-id="d2840-122">관리 그룹 Id</span><span class="sxs-lookup"><span data-stu-id="d2840-122">Management Group Id</span></span>

```yaml
Type: System.String
Parameter Sets: GetOperation
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d2840-123">-재귀적으로</span><span class="sxs-lookup"><span data-stu-id="d2840-123">-Recurse</span></span>
<span data-ttu-id="d2840-124">관리 그룹의 자식을 재귀적으로 나열</span><span class="sxs-lookup"><span data-stu-id="d2840-124">Recursively list the children of the management group</span></span>

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

### <span data-ttu-id="d2840-125">-확인</span><span class="sxs-lookup"><span data-stu-id="d2840-125">-Confirm</span></span>
<span data-ttu-id="d2840-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d2840-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d2840-127">-WhatIf</span></span>
<span data-ttu-id="d2840-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d2840-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d2840-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d2840-130">CommonParameters</span></span>
<span data-ttu-id="d2840-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d2840-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d2840-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d2840-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d2840-133">입력</span><span class="sxs-lookup"><span data-stu-id="d2840-133">INPUTS</span></span>

### <span data-ttu-id="d2840-134">않아야</span><span class="sxs-lookup"><span data-stu-id="d2840-134">None</span></span>

## <span data-ttu-id="d2840-135">출력</span><span class="sxs-lookup"><span data-stu-id="d2840-135">OUTPUTS</span></span>

### <span data-ttu-id="d2840-136">PSManagementGroupInfo-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="d2840-136">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroupInfo</span></span>

### <span data-ttu-id="d2840-137">PSManagementGroup-.Resources. 모델. 관리 그룹.</span><span class="sxs-lookup"><span data-stu-id="d2840-137">Microsoft.Azure.Commands.Resources.Models.ManagementGroups.PSManagementGroup</span></span>

## <span data-ttu-id="d2840-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d2840-138">NOTES</span></span>

## <span data-ttu-id="d2840-139">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d2840-139">RELATED LINKS</span></span>
