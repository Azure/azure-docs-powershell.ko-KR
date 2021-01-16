---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/get-azblueprint
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Get-AzBlueprint.md
ms.openlocfilehash: ab383b1fb46759c2369d94d4bb57284ba59cf671
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98494014"
---
# <span data-ttu-id="a657d-101">Get-AzBlueprint</span><span class="sxs-lookup"><span data-stu-id="a657d-101">Get-AzBlueprint</span></span>

## <span data-ttu-id="a657d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a657d-102">SYNOPSIS</span></span>
<span data-ttu-id="a657d-103">하나 이상의 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-103">Get one or more blueprint definitions.</span></span>

## <span data-ttu-id="a657d-104">구문</span><span class="sxs-lookup"><span data-stu-id="a657d-104">SYNTAX</span></span>

### <span data-ttu-id="a657d-105">SubscriptionScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="a657d-105">SubscriptionScope (Default)</span></span>
```
Get-AzBlueprint [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a657d-106">ByManagementGroupNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a657d-106">ByManagementGroupNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a657d-107">BySubscriptionAndName</span><span class="sxs-lookup"><span data-stu-id="a657d-107">BySubscriptionAndName</span></span>
```
Get-AzBlueprint [-Name <String>] [-SubscriptionId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a657d-108">ByManagementGroupAndName</span><span class="sxs-lookup"><span data-stu-id="a657d-108">ByManagementGroupAndName</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a657d-109">ByManagementGroupNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="a657d-109">ByManagementGroupNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> -ManagementGroupId <String> [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a657d-110">BySubscriptionNameAndLatestPublished</span><span class="sxs-lookup"><span data-stu-id="a657d-110">BySubscriptionNameAndLatestPublished</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-LatestPublished]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a657d-111">BySubscriptionNameAndVersion</span><span class="sxs-lookup"><span data-stu-id="a657d-111">BySubscriptionNameAndVersion</span></span>
```
Get-AzBlueprint -Name <String> [-SubscriptionId <String>] [-Version] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a657d-112">ManagementGroupScope</span><span class="sxs-lookup"><span data-stu-id="a657d-112">ManagementGroupScope</span></span>
```
Get-AzBlueprint -ManagementGroupId <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a657d-113">설명</span><span class="sxs-lookup"><span data-stu-id="a657d-113">DESCRIPTION</span></span>
<span data-ttu-id="a657d-114">하나 이상의 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-114">Get one or more blueprint definitions.</span></span> <span data-ttu-id="a657d-115">청사진 정의는 관리 그룹 또는 구독 범위에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-115">Blueprint definitions exist at the management group or subscription scope.</span></span>

## <span data-ttu-id="a657d-116">예제</span><span class="sxs-lookup"><span data-stu-id="a657d-116">EXAMPLES</span></span>

### <span data-ttu-id="a657d-117">예제 1</span><span class="sxs-lookup"><span data-stu-id="a657d-117">Example 1</span></span>
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

<span data-ttu-id="a657d-118">현재 구독 및 구독의 관리 그룹 계층 구조 내에서 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-118">Get the blueprint definitions within the current subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="a657d-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="a657d-119">Example 2</span></span>
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

<span data-ttu-id="a657d-120">지정된 관리 그룹 내에서 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-120">Get the blueprint definitions within the specified management group.</span></span>

### <span data-ttu-id="a657d-121">예제 3</span><span class="sxs-lookup"><span data-stu-id="a657d-121">Example 3</span></span>
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

<span data-ttu-id="a657d-122">지정된 구독 및 구독의 관리 그룹 계층 구조 내에서 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-122">Get the blueprint definitions within the specified subscription and the management group hierarchy of the subscription.</span></span>

### <span data-ttu-id="a657d-123">예제 4</span><span class="sxs-lookup"><span data-stu-id="a657d-123">Example 4</span></span>
```powershell
PS> Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
```

<span data-ttu-id="a657d-124">지정된 구독 내에서 지정된 이름으로 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-124">Get the blueprint definition with the given name within the specified subscription.</span></span>

### <span data-ttu-id="a657d-125">예제 5</span><span class="sxs-lookup"><span data-stu-id="a657d-125">Example 5</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -Version "myBlueprintVersion"
```

<span data-ttu-id="a657d-126">지정된 관리 그룹 내에서 지정된 이름 및 버전으로 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-126">Get the blueprint definition with the given name and version within the specified management group.</span></span>

### <span data-ttu-id="a657d-127">예제 6</span><span class="sxs-lookup"><span data-stu-id="a657d-127">Example 6</span></span>
```powershell
PS> Get-AzBlueprint -ManagementGroupId "myManagementGroupId" -Name "myBlueprintName" -LatestPublished
```

<span data-ttu-id="a657d-128">지정된 관리 그룹 내에서 지정된 이름으로 게시된 최신 청사진 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-128">Get the latest published blueprint definition with the given name within the specified management group.</span></span>

## <span data-ttu-id="a657d-129">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a657d-129">PARAMETERS</span></span>

### <span data-ttu-id="a657d-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a657d-130">-DefaultProfile</span></span>
<span data-ttu-id="a657d-131">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a657d-132">-LatestPublished</span><span class="sxs-lookup"><span data-stu-id="a657d-132">-LatestPublished</span></span>
<span data-ttu-id="a657d-133">게시된 최신 청사진 정의 플래그입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-133">The latest published blueprint definition flag.</span></span>
<span data-ttu-id="a657d-134">설정하면 실행은 청사진 정의의 최신 게시 버전을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-134">When set, execution returns the latest published version of the blueprint definition.</span></span>
<span data-ttu-id="a657d-135">기본값은 false입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-135">Defaults to false.</span></span>

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

### <span data-ttu-id="a657d-136">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="a657d-136">-ManagementGroupId</span></span>
<span data-ttu-id="a657d-137">청사진 정의가 저장되는 관리 그룹 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-137">Management Group Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="a657d-138">-Name</span><span class="sxs-lookup"><span data-stu-id="a657d-138">-Name</span></span>
<span data-ttu-id="a657d-139">청사진 정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-139">Blueprint definition name.</span></span>

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

### <span data-ttu-id="a657d-140">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a657d-140">-SubscriptionId</span></span>
<span data-ttu-id="a657d-141">청사진 정의가 저장되는 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-141">Subscription Id where the blueprint definition is saved.</span></span>

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

### <span data-ttu-id="a657d-142">-Version</span><span class="sxs-lookup"><span data-stu-id="a657d-142">-Version</span></span>
<span data-ttu-id="a657d-143">게시된 청사진 정의 버전입니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-143">Published blueprint definition version.</span></span>

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

### <span data-ttu-id="a657d-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a657d-144">CommonParameters</span></span>
<span data-ttu-id="a657d-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a657d-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a657d-146">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="a657d-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a657d-147">입력</span><span class="sxs-lookup"><span data-stu-id="a657d-147">INPUTS</span></span>

### <span data-ttu-id="a657d-148">System.String</span><span class="sxs-lookup"><span data-stu-id="a657d-148">System.String</span></span>

## <span data-ttu-id="a657d-149">출력</span><span class="sxs-lookup"><span data-stu-id="a657d-149">OUTPUTS</span></span>

### <span data-ttu-id="a657d-150">System.Object</span><span class="sxs-lookup"><span data-stu-id="a657d-150">System.Object</span></span>
## <span data-ttu-id="a657d-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a657d-151">NOTES</span></span>

## <span data-ttu-id="a657d-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a657d-152">RELATED LINKS</span></span>
