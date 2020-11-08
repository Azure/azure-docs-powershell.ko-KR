---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204066"
---
# <span data-ttu-id="57f09-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="57f09-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="57f09-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="57f09-102">SYNOPSIS</span></span>
<span data-ttu-id="57f09-103">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="57f09-104">구문과</span><span class="sxs-lookup"><span data-stu-id="57f09-104">SYNTAX</span></span>

### <span data-ttu-id="57f09-105">UpdateBlueprintAssignment (기본값)</span><span class="sxs-lookup"><span data-stu-id="57f09-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="57f09-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="57f09-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="57f09-107">설명은</span><span class="sxs-lookup"><span data-stu-id="57f09-107">DESCRIPTION</span></span>
<span data-ttu-id="57f09-108">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="57f09-109">예제의</span><span class="sxs-lookup"><span data-stu-id="57f09-109">EXAMPLES</span></span>

### <span data-ttu-id="57f09-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="57f09-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/HR/Dev/0001"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -Parameter $params -ResourceGroupParameter $rg -SystemAssignedIdentity

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="57f09-111">지정 된 구독 내에서 청사진 정의에 대 한 기존 청사진 과제 `$blueprintObject` 를 업데이트 하 고 매개 변수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="57f09-112">시스템 할당 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-112">Uses system-assigned identity.</span></span> <span data-ttu-id="57f09-113">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="57f09-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="57f09-114">Example 2</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="57f09-115">과제 파일을 통해 기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="57f09-116">과제물 파일의 형식은 다음의 요청/응답 샘플에서 찾을 수 있습니다. https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="57f09-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="57f09-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="57f09-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="57f09-118">`$blueprintObject`정의 된 매개 변수를 사용 하 여 지정 된 관리 그룹 내에서 지정 된 구독을 대상으로 하는 청사진 정의의 기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="57f09-119">변수</span><span class="sxs-lookup"><span data-stu-id="57f09-119">PARAMETERS</span></span>

### <span data-ttu-id="57f09-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="57f09-120">-AssignmentFile</span></span>
<span data-ttu-id="57f09-121">디스크의 JSON 형식에서 할당 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-121">Location of the assignment file in JSON format on disk.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-122">-청사진</span><span class="sxs-lookup"><span data-stu-id="57f09-122">-Blueprint</span></span>
<span data-ttu-id="57f09-123">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="57f09-123">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="57f09-124">-DefaultProfile</span></span>
<span data-ttu-id="57f09-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="57f09-126">-위치</span><span class="sxs-lookup"><span data-stu-id="57f09-126">-Location</span></span>
<span data-ttu-id="57f09-127">에서 만들 관리 되는 id의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="57f09-128">자세한 정보 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="57f09-128">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-129">-잠금</span><span class="sxs-lookup"><span data-stu-id="57f09-129">-Lock</span></span>
<span data-ttu-id="57f09-130">리소스 잠그기.</span><span class="sxs-lookup"><span data-stu-id="57f09-130">Lock resources.</span></span>
<span data-ttu-id="57f09-131">자세한 정보 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="57f09-131">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: UpdateBlueprintAssignment
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="57f09-132">-ManagementGroupId</span></span>
<span data-ttu-id="57f09-133">청사진 할당이 저장 될 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-134">-이름</span><span class="sxs-lookup"><span data-stu-id="57f09-134">-Name</span></span>
<span data-ttu-id="57f09-135">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="57f09-135">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="57f09-136">-Parameter</span></span>
<span data-ttu-id="57f09-137">아티팩트 매개 변수</span><span class="sxs-lookup"><span data-stu-id="57f09-137">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="57f09-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="57f09-139">리소스 그룹 아티팩트에 전달할 매개 변수의 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="57f09-140">-SecureStringParameter</span></span>
<span data-ttu-id="57f09-141">KeyVault 리소스 id, 이름 및 버전에 대 한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="57f09-142">-SubscriptionId</span></span>
<span data-ttu-id="57f09-143">SubscriptionId는 청사진을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="57f09-144">SubscriptionId 문자열의 쉼표로 구분 된 목록이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-144">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String[]
Parameter Sets: UpdateBlueprintAssignmentByFile
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57f09-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="57f09-146">시스템 할당 id (MSI)를 통해 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="57f09-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="57f09-148">사용자가 할당 한 id (MSI)를 사용 하 여 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: UpdateBlueprintAssignment
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="57f09-149">-확인</span><span class="sxs-lookup"><span data-stu-id="57f09-149">-Confirm</span></span>
<span data-ttu-id="57f09-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="57f09-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="57f09-151">-WhatIf</span></span>
<span data-ttu-id="57f09-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="57f09-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="57f09-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="57f09-154">CommonParameters</span></span>
<span data-ttu-id="57f09-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="57f09-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="57f09-156">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="57f09-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="57f09-157">입력</span><span class="sxs-lookup"><span data-stu-id="57f09-157">INPUTS</span></span>

### <span data-ttu-id="57f09-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="57f09-158">System.String</span></span>

### <span data-ttu-id="57f09-159">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="57f09-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="57f09-160">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="57f09-160">System.String[]</span></span>

### <span data-ttu-id="57f09-161">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="57f09-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="57f09-162">출력</span><span class="sxs-lookup"><span data-stu-id="57f09-162">OUTPUTS</span></span>

### <span data-ttu-id="57f09-163">System. 개체</span><span class="sxs-lookup"><span data-stu-id="57f09-163">System.Object</span></span>
## <span data-ttu-id="57f09-164">상속자</span><span class="sxs-lookup"><span data-stu-id="57f09-164">NOTES</span></span>

## <span data-ttu-id="57f09-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="57f09-165">RELATED LINKS</span></span>
