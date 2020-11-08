---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94216114"
---
# <span data-ttu-id="46e2a-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="46e2a-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="46e2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46e2a-102">SYNOPSIS</span></span>
<span data-ttu-id="46e2a-103">하나 이상의 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="46e2a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46e2a-104">SYNTAX</span></span>

### <span data-ttu-id="46e2a-105">구독 범위 (기본값)</span><span class="sxs-lookup"><span data-stu-id="46e2a-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2a-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="46e2a-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2a-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="46e2a-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46e2a-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="46e2a-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="46e2a-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="46e2a-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2a-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="46e2a-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2a-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="46e2a-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="46e2a-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="46e2a-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46e2a-113">설명은</span><span class="sxs-lookup"><span data-stu-id="46e2a-113">DESCRIPTION</span></span>
<span data-ttu-id="46e2a-114">하나 이상의 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="46e2a-115">청사진 정의는 관리 그룹 또는 구독 범위에 존재 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="46e2a-116">예제의</span><span class="sxs-lookup"><span data-stu-id="46e2a-116">EXAMPLES</span></span>

### <span data-ttu-id="46e2a-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="46e2a-117">Example 1</span></span>
```powershell
PS> Get-AzBlueprint

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="46e2a-118">현재 구독 및 구독의 관리 그룹 계층 구조 내에서 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="46e2a-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="46e2a-119">Example 2</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId"

Name                 : PS-MG-BlueprintDefinition
Id                   : /providers/Microsoft.Management/managementGroups/myManagementGroupId/providers/Microsoft.Blueprint/blueprints/PS-MG-BlueprintDefinition
ManagementGroupId    : myManagementGroupId
Versions             : {1.0, 2.0, 3.0, 4.0}
TimeCreated          : 2019-03-04
TargetScope          : Subscription
Parameters           : {enforcetaganditsvalue_tagName, enforcetaganditsvalue_tagValue, [Usergrouporapplicationname]:Contributor_RoleAssignmentName,
                       [Usergrouporapplicationname]:Owner_RoleAssignmentName}
ResourceGroups       : {ResourceGroup, ResourceGroup2}
```

<span data-ttu-id="46e2a-120">지정 된 관리 그룹 내에서 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="46e2a-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="46e2a-121">Example 3</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000"

Name                 : PS-BlueprintDefinition
Id                   : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprints/PS-BlueprintDefinition
SubscriptionId       : 00000000-1111-0000-1111-000000000000
Versions             : {1.0}
Description          : Powershell test blueprint
TimeCreated          : 2019-02-01
TargetScope          : Subscription
Parameters           : {storageData_storageAccountType, storageData_location, allowedlocations_listOfAllowedLocations}
ResourceGroups       : ResourceGroup
```

<span data-ttu-id="46e2a-122">지정 된 구독 및 구독의 관리 그룹 계층 구조 내에서 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="46e2a-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="46e2a-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="46e2a-124">지정 된 구독 내에서 주어진 이름으로 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="46e2a-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="46e2a-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="46e2a-126">지정 된 관리 그룹 내에서 주어진 이름 및 버전을 사용 하 여 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="46e2a-127">예제 6</span><span class="sxs-lookup"><span data-stu-id="46e2a-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="46e2a-128">지정 된 관리 그룹 내에서 주어진 이름으로 게시 된 최신 청사진 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="46e2a-129">변수</span><span class="sxs-lookup"><span data-stu-id="46e2a-129">PARAMETERS</span></span>

### <span data-ttu-id="46e2a-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46e2a-130">-DefaultProfile</span></span>
<span data-ttu-id="46e2a-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="46e2a-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="46e2a-132">-LatestPublished</span></span>
<span data-ttu-id="46e2a-133">게시 된 최신 청사진 정의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="46e2a-134">Set을 실행 하면 청사진 정의의 최신 게시 버전이 반환 됩니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="46e2a-135">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-135">Defaults to false.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="46e2a-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="46e2a-136">-ManagementGroupId</span></span>
<span data-ttu-id="46e2a-137">청사진 정의가 저장 된 관리 그룹 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-137">Management Group Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, ManagementGroupScope
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2a-138">-이름</span><span class="sxs-lookup"><span data-stu-id="46e2a-138">-Name</span></span>
<span data-ttu-id="46e2a-139">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-139">Blueprint definition name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, ByManagementGroupAndName, ByManagementGroupNameAndLatestPublished, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: BySubscriptionAndName
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2a-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="46e2a-140">-SubscriptionId</span></span>
<span data-ttu-id="46e2a-141">청사진 정의가 저장 되는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-141">Subscription Id where the blueprint definition is saved.</span></span>

```yaml
Type: System.String
Parameter Sets: SubscriptionScope, BySubscriptionAndName, BySubscriptionNameAndLatestPublished, BySubscriptionNameAndVersion
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2a-142">-버전</span><span class="sxs-lookup"><span data-stu-id="46e2a-142">-Version</span></span>
<span data-ttu-id="46e2a-143">게시 된 청사진 정의 버전.</span><span class="sxs-lookup"><span data-stu-id="46e2a-143">Published blueprint definition version.</span></span>

```yaml
Type: System.String
Parameter Sets: ByManagementGroupNameAndVersion, BySubscriptionNameAndVersion
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="46e2a-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46e2a-144">CommonParameters</span></span>
<span data-ttu-id="46e2a-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46e2a-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46e2a-146">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="46e2a-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46e2a-147">입력</span><span class="sxs-lookup"><span data-stu-id="46e2a-147">INPUTS</span></span>

### <span data-ttu-id="46e2a-148">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="46e2a-148">System.String</span></span>

## <span data-ttu-id="46e2a-149">출력</span><span class="sxs-lookup"><span data-stu-id="46e2a-149">OUTPUTS</span></span>

### <span data-ttu-id="46e2a-150">System. 개체</span><span class="sxs-lookup"><span data-stu-id="46e2a-150">System.Object</span></span>
## <span data-ttu-id="46e2a-151">상속자</span><span class="sxs-lookup"><span data-stu-id="46e2a-151">NOTES</span></span>

## <span data-ttu-id="46e2a-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46e2a-152">RELATED LINKS</span></span>
