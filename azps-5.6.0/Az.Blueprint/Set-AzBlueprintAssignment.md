---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: 0e5c562d5b536e95d40bdbc1c08b2d778574fd41
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "102001867"
---
# <span data-ttu-id="3a16b-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="3a16b-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="3a16b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3a16b-102">SYNOPSIS</span></span>
<span data-ttu-id="3a16b-103">기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="3a16b-104">구문</span><span class="sxs-lookup"><span data-stu-id="3a16b-104">SYNTAX</span></span>

### <span data-ttu-id="3a16b-105">UpdateBlueprintAssignment(기본값)</span><span class="sxs-lookup"><span data-stu-id="3a16b-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3a16b-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="3a16b-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> [-Blueprint <PSBlueprintBase>] [-AssignmentFile <String>]
 [-ManagementGroupId <String>] [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3a16b-107">설명</span><span class="sxs-lookup"><span data-stu-id="3a16b-107">DESCRIPTION</span></span>
<span data-ttu-id="3a16b-108">기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="3a16b-109">예제</span><span class="sxs-lookup"><span data-stu-id="3a16b-109">EXAMPLES</span></span>

### <span data-ttu-id="3a16b-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="3a16b-110">Example 1</span></span>
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

<span data-ttu-id="3a16b-111">지정된 구독 내에서 청사진 정의의 기존 청사진 할당을 `$blueprintObject` 업데이트하고 매개 변수를 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="3a16b-112">시스템 할당 ID를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-112">Uses system-assigned identity.</span></span> <span data-ttu-id="3a16b-113">위치는 관리 ID를 만들기 위한 지역을 정의합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="3a16b-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="3a16b-114">Example 2</span></span>
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

<span data-ttu-id="3a16b-115">할당 파일을 통해 기존 청사진 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="3a16b-116">과제 파일의 형식은 다음의 요청/응답 샘플에서 찾을 수 있습니다. https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="3a16b-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

### <span data-ttu-id="3a16b-117">예제 3</span><span class="sxs-lookup"><span data-stu-id="3a16b-117">Example 3</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -ManagementGroup "myManagementGroup" -Name "myBlueprintName"
PS C:\> Set-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -ManagementGroupId "myManagementGroup" -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"}
```

<span data-ttu-id="3a16b-118">정의된 매개 변수를 사용하여 지정된 관리 그룹 내에서 지정된 구독을 대상으로 하는 청사진 정의의 기존 청사진 `$blueprintObject` 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-118">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` targeting the specified subscription within the specified management group using the defined parameter.</span></span>

## <span data-ttu-id="3a16b-119">매개 변수</span><span class="sxs-lookup"><span data-stu-id="3a16b-119">PARAMETERS</span></span>

### <span data-ttu-id="3a16b-120">-AssignmentFile</span><span class="sxs-lookup"><span data-stu-id="3a16b-120">-AssignmentFile</span></span>
<span data-ttu-id="3a16b-121">디스크의 JSON 형식으로 할당 파일의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-121">Location of the assignment file in JSON format on disk.</span></span>

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

### <span data-ttu-id="3a16b-122">-Blueprint</span><span class="sxs-lookup"><span data-stu-id="3a16b-122">-Blueprint</span></span>
<span data-ttu-id="3a16b-123">청사진 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-123">Blueprint object.</span></span>

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

### <span data-ttu-id="3a16b-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3a16b-124">-DefaultProfile</span></span>
<span data-ttu-id="3a16b-125">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3a16b-126">-Location</span><span class="sxs-lookup"><span data-stu-id="3a16b-126">-Location</span></span>
<span data-ttu-id="3a16b-127">에서 만들 관리 ID에 대한 지역입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-127">Region for managed identity to be created in.</span></span>
<span data-ttu-id="3a16b-128">자세한 내용은 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="3a16b-128">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="3a16b-129">-Lock</span><span class="sxs-lookup"><span data-stu-id="3a16b-129">-Lock</span></span>
<span data-ttu-id="3a16b-130">리소스를 잠글 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-130">Lock resources.</span></span>
<span data-ttu-id="3a16b-131">자세한 내용은 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="3a16b-131">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="3a16b-132">-ManagementGroupId</span><span class="sxs-lookup"><span data-stu-id="3a16b-132">-ManagementGroupId</span></span>
<span data-ttu-id="3a16b-133">Blueprint 할당이 저장되는 관리 그룹의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-133">The ID of the management group where the Blueprint assignment(s) will be saved.</span></span>

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

### <span data-ttu-id="3a16b-134">-Name</span><span class="sxs-lookup"><span data-stu-id="3a16b-134">-Name</span></span>
<span data-ttu-id="3a16b-135">청사진 할당 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="3a16b-136">-매개 변수</span><span class="sxs-lookup"><span data-stu-id="3a16b-136">-Parameter</span></span>
<span data-ttu-id="3a16b-137">아티팩트 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-137">Artifact parameter.</span></span>

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

### <span data-ttu-id="3a16b-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="3a16b-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="3a16b-139">리소스 그룹 아티팩트에 전달할 매개 변수의 해시테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-139">Hashtable of parameters to pass to the resource group artifact.</span></span>

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

### <span data-ttu-id="3a16b-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="3a16b-140">-SecureStringParameter</span></span>
<span data-ttu-id="3a16b-141">KeyVault 리소스 ID, 이름 및 버전에 대한 문자열 매개 변수를 보호합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="3a16b-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="3a16b-142">-SubscriptionId</span></span>
<span data-ttu-id="3a16b-143">SubscriptionId에서 청사진을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-143">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="3a16b-144">subscriptionId 문자열의 콤마로 지정된 목록일 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="3a16b-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3a16b-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="3a16b-146">시스템 할당 ID(MSI)를 통해 아티팩트를 배포합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="3a16b-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="3a16b-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="3a16b-148">아티팩트를 배포하기 위해 MSI(사용자 할당 ID)입니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="3a16b-149">-확인</span><span class="sxs-lookup"><span data-stu-id="3a16b-149">-Confirm</span></span>
<span data-ttu-id="3a16b-150">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3a16b-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3a16b-151">-WhatIf</span></span>
<span data-ttu-id="3a16b-152">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3a16b-153">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3a16b-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3a16b-154">CommonParameters</span></span>
<span data-ttu-id="3a16b-155">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="3a16b-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3a16b-156">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="3a16b-156">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3a16b-157">입력</span><span class="sxs-lookup"><span data-stu-id="3a16b-157">INPUTS</span></span>

### <span data-ttu-id="3a16b-158">System.String</span><span class="sxs-lookup"><span data-stu-id="3a16b-158">System.String</span></span>

### <span data-ttu-id="3a16b-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span><span class="sxs-lookup"><span data-stu-id="3a16b-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="3a16b-160">System.String[]</span><span class="sxs-lookup"><span data-stu-id="3a16b-160">System.String[]</span></span>

### <span data-ttu-id="3a16b-161">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="3a16b-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="3a16b-162">출력</span><span class="sxs-lookup"><span data-stu-id="3a16b-162">OUTPUTS</span></span>

### <span data-ttu-id="3a16b-163">System.Object</span><span class="sxs-lookup"><span data-stu-id="3a16b-163">System.Object</span></span>
## <span data-ttu-id="3a16b-164">참고 사항</span><span class="sxs-lookup"><span data-stu-id="3a16b-164">NOTES</span></span>

## <span data-ttu-id="3a16b-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3a16b-165">RELATED LINKS</span></span>
