---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/set-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/Set-AzBlueprintAssignment.md
ms.openlocfilehash: df1d25f2d5362a81bd33b74bad223bbfb952daa7
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697628"
---
# <span data-ttu-id="e2208-101">Set-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="e2208-101">Set-AzBlueprintAssignment</span></span>

## <span data-ttu-id="e2208-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e2208-102">SYNOPSIS</span></span>
<span data-ttu-id="e2208-103">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-103">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e2208-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e2208-104">SYNTAX</span></span>

### <span data-ttu-id="e2208-105">UpdateBlueprintAssignment (기본값)</span><span class="sxs-lookup"><span data-stu-id="e2208-105">UpdateBlueprintAssignment (Default)</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e2208-106">UpdateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="e2208-106">UpdateBlueprintAssignmentByFile</span></span>
```
Set-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="e2208-107">설명은</span><span class="sxs-lookup"><span data-stu-id="e2208-107">DESCRIPTION</span></span>
<span data-ttu-id="e2208-108">기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-108">Update an existing blueprint assignment.</span></span>

## <span data-ttu-id="e2208-109">예제의</span><span class="sxs-lookup"><span data-stu-id="e2208-109">EXAMPLES</span></span>

### <span data-ttu-id="e2208-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="e2208-110">Example 1</span></span>
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

<span data-ttu-id="e2208-111">지정 된 구독 내에서 청사진 정의에 대 한 기존 청사진 과제 `$blueprintObject` 를 업데이트 하 고 매개 변수를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-111">Update an existing blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription, updating the parameters.</span></span> <span data-ttu-id="e2208-112">시스템 할당 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-112">Uses system-assigned identity.</span></span> <span data-ttu-id="e2208-113">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="e2208-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="e2208-114">Example 2</span></span>
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

<span data-ttu-id="e2208-115">과제 파일을 통해 기존 청사진 과제를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-115">Update an existing blueprint assignment through an assignment file.</span></span> <span data-ttu-id="e2208-116">과제물 파일의 형식은 다음의 요청/응답 샘플에서 찾을 수 있습니다. https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="e2208-116">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="e2208-117">변수</span><span class="sxs-lookup"><span data-stu-id="e2208-117">PARAMETERS</span></span>

### <span data-ttu-id="e2208-118">-청사진</span><span class="sxs-lookup"><span data-stu-id="e2208-118">-Blueprint</span></span>
<span data-ttu-id="e2208-119">청사진 개체</span><span class="sxs-lookup"><span data-stu-id="e2208-119">Blueprint object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e2208-120">-DefaultProfile</span></span>
<span data-ttu-id="e2208-121">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="e2208-122">-위치</span><span class="sxs-lookup"><span data-stu-id="e2208-122">-Location</span></span>
<span data-ttu-id="e2208-123">에서 만들 관리 되는 id의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-123">Region for managed identity to be created in.</span></span>
<span data-ttu-id="e2208-124">자세한 정보 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="e2208-124">Learn more at aka.ms/blueprintmsi</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-125">-잠금</span><span class="sxs-lookup"><span data-stu-id="e2208-125">-Lock</span></span>
<span data-ttu-id="e2208-126">리소스 잠그기.</span><span class="sxs-lookup"><span data-stu-id="e2208-126">Lock resources.</span></span>
<span data-ttu-id="e2208-127">자세한 정보 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="e2208-127">Learn more at aka.ms/blueprintlocks</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.Blueprint.Models.PSLockMode]
Parameter Sets: (All)
Aliases:
Accepted values: None, AllResourcesReadOnly, AllResourcesDoNotDelete

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-128">-이름</span><span class="sxs-lookup"><span data-stu-id="e2208-128">-Name</span></span>
<span data-ttu-id="e2208-129">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="e2208-129">Blueprint assignment name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-130">-Parameter</span><span class="sxs-lookup"><span data-stu-id="e2208-130">-Parameter</span></span>
<span data-ttu-id="e2208-131">아티팩트 매개 변수</span><span class="sxs-lookup"><span data-stu-id="e2208-131">Artifact parameter.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-132">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="e2208-132">-ResourceGroupParameter</span></span>
<span data-ttu-id="e2208-133">{{ResourceGroupParameter 매개 변수 설명}}</span><span class="sxs-lookup"><span data-stu-id="e2208-133">{{Fill ResourceGroupParameter Description}}</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-134">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="e2208-134">-SecureStringParameter</span></span>
<span data-ttu-id="e2208-135">KeyVault 리소스 id, 이름 및 버전에 대 한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-135">Secure string parameter for KeyVault resource id, name and version.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-136">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="e2208-136">-SubscriptionId</span></span>
<span data-ttu-id="e2208-137">SubscriptionId는 청사진을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-137">SubscriptionId to assign the Blueprint.</span></span>
<span data-ttu-id="e2208-138">SubscriptionId 문자열의 쉼표로 구분 된 목록이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-138">Can be a comma delimited list of subscriptionId strings.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-139">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2208-139">-SystemAssignedIdentity</span></span>
<span data-ttu-id="e2208-140">시스템 할당 id (MSI)를 통해 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-140">System assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-141">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="e2208-141">-UserAssignedIdentity</span></span>
<span data-ttu-id="e2208-142">사용자가 할당 한 id (MSI)를 사용 하 여 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-142">User assigned identity(MSI) to deploy the artifacts.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e2208-143">-확인</span><span class="sxs-lookup"><span data-stu-id="e2208-143">-Confirm</span></span>
<span data-ttu-id="e2208-144">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-144">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e2208-145">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e2208-145">-WhatIf</span></span>
<span data-ttu-id="e2208-146">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-146">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e2208-147">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-147">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e2208-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e2208-148">CommonParameters</span></span>
<span data-ttu-id="e2208-149">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e2208-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e2208-150">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e2208-150">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e2208-151">입력</span><span class="sxs-lookup"><span data-stu-id="e2208-151">INPUTS</span></span>

### <span data-ttu-id="e2208-152">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="e2208-152">System.String</span></span>

### <span data-ttu-id="e2208-153">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="e2208-153">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="e2208-154">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="e2208-154">System.String[]</span></span>

### <span data-ttu-id="e2208-155">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="e2208-155">System.Collections.Hashtable</span></span>

## <span data-ttu-id="e2208-156">출력</span><span class="sxs-lookup"><span data-stu-id="e2208-156">OUTPUTS</span></span>

### <span data-ttu-id="e2208-157">System. 개체</span><span class="sxs-lookup"><span data-stu-id="e2208-157">System.Object</span></span>
## <span data-ttu-id="e2208-158">상속자</span><span class="sxs-lookup"><span data-stu-id="e2208-158">NOTES</span></span>

## <span data-ttu-id="e2208-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e2208-159">RELATED LINKS</span></span>
