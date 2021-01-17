---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: b8913ead9844a55190a6117f57f01d243e004fde
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326542"
---
# <span data-ttu-id="f6801-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="f6801-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="f6801-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6801-102">SYNOPSIS</span></span>
<span data-ttu-id="f6801-103">기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="f6801-104">구문</span><span class="sxs-lookup"><span data-stu-id="f6801-104">SYNTAX</span></span>

### <span data-ttu-id="f6801-105">UpdateBlueprintAssignment(기본값)</span><span class="sxs-lookup"><span data-stu-id="f6801-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f6801-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="f6801-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f6801-107">설명</span><span class="sxs-lookup"><span data-stu-id="f6801-107">DESCRIPTION</span></span>
<span data-ttu-id="f6801-108">기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="f6801-109">예제</span><span class="sxs-lookup"><span data-stu-id="f6801-109">EXAMPLES</span></span>

### <span data-ttu-id="f6801-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f6801-110">Example 1</span></span>
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

<span data-ttu-id="f6801-111">지정된 구독 내에서 청사진 정의의 기존 청사진 할당을 `$blueprintObject` 업데이트하여 매개 변수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="f6801-112">시스템 할당 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-112">Uses system-assigned identity.</span></span> <span data-ttu-id="f6801-113">위치는 관리 ID를 만들기 위한 지역을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="f6801-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="f6801-114">Example 2</span></span>
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

<span data-ttu-id="f6801-115">할당 파일을 통해 기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="f6801-116">할당 파일의 형식은 다음의 요청/응답 샘플에서 찾을 수 있습니다. https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="f6801-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="f6801-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="f6801-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="f6801-118">정의된 매개 변수를 사용하여 지정된 관리 그룹 내에서 지정된 구독을 대상으로 하는 청사진 정의의 기존 청사진 `$blueprintObject` 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="f6801-119">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f6801-119">PARAMETERS</span></span>

### <span data-ttu-id="f6801-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="f6801-120">-AssignmentFile</span></span>
<span data-ttu-id="f6801-121">디스크의 JSON 형식인 할당 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="f6801-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="f6801-122">-Blueprint</span></span>
<span data-ttu-id="f6801-123">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-123">Blueprint object.</span></span>

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

### <span data-ttu-id="f6801-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6801-124">-DefaultProfile</span></span>
<span data-ttu-id="f6801-125">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f6801-126">-Location</span><span class="sxs-lookup"><span data-stu-id="f6801-126">-Location</span></span>
<span data-ttu-id="f6801-127">관리 ID를 만들 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="f6801-128">자세한 내용은 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="f6801-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="f6801-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="f6801-129">-Lock</span></span>
<span data-ttu-id="f6801-130">리소스를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-130">Lock resources.</span></span>
<span data-ttu-id="f6801-131">자세한 내용은 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="f6801-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="f6801-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="f6801-132">-ManagementGroupId</span></span>
<span data-ttu-id="f6801-133">청사진 할당을 저장할 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="f6801-134">-Name</span><span class="sxs-lookup"><span data-stu-id="f6801-134">-Name</span></span>
<span data-ttu-id="f6801-135">청사진 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="f6801-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="f6801-136">-Parameter</span></span>
<span data-ttu-id="f6801-137">아티팩트 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="f6801-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="f6801-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="f6801-139">리소스 그룹 아티팩트에 전달할 매개 변수의 해시가 가능합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="f6801-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="f6801-140">-SecureStringParameter</span></span>
<span data-ttu-id="f6801-141">KeyVault 리소스 ID, 이름 및 버전에 대한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="f6801-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="f6801-142">-SubscriptionId</span></span>
<span data-ttu-id="f6801-143">Blueprint를 할당할 SubscriptionId입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="f6801-144">subscriptionId 문자열의 콤마로분된 목록일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="f6801-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f6801-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="f6801-146">아티팩트를 배포할 시스템 할당 ID(MSI)입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="f6801-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="f6801-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="f6801-148">아티팩트를 배포할 사용자 할당 ID(MSI)입니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="f6801-149">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f6801-149">-Confirm</span></span>
<span data-ttu-id="f6801-150">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f6801-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f6801-151">-WhatIf</span></span>
<span data-ttu-id="f6801-152">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f6801-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f6801-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f6801-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6801-154">CommonParameters</span></span>
<span data-ttu-id="f6801-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f6801-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6801-156">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f6801-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6801-157">입력</span><span class="sxs-lookup"><span data-stu-id="f6801-157">INPUTS</span></span>

### <span data-ttu-id="f6801-158">System.String</span><span class="sxs-lookup"><span data-stu-id="f6801-158">System.String</span></span>

### <span data-ttu-id="f6801-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="f6801-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="f6801-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="f6801-160">System.String[]</span></span>

### <span data-ttu-id="f6801-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6801-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6801-162">출력</span><span class="sxs-lookup"><span data-stu-id="f6801-162">OUTPUTS</span></span>

### <span data-ttu-id="f6801-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="f6801-163">System.Object</span></span>
## <span data-ttu-id="f6801-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f6801-164">NOTES</span></span>

## <span data-ttu-id="f6801-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f6801-165">RELATED LINKS</span></span>
