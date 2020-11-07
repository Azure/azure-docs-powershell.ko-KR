---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Blueprint.dll-Help.xml
Module Name: Az.Blueprint
online version: https://docs.microsoft.com/en-us/powershell/module/az.blueprint/new-azblueprintassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Blueprint/Blueprint/help/New-AzBlueprintAssignment.md
ms.openlocfilehash: 6adc5674674de903b30993b09d5bb680f8569398
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93697637"
---
# <span data-ttu-id="5194f-101">New-AzBlueprintAssignment</span><span class="sxs-lookup"><span data-stu-id="5194f-101">New-AzBlueprintAssignment</span></span>

## <span data-ttu-id="5194f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5194f-102">SYNOPSIS</span></span>
<span data-ttu-id="5194f-103">구독에 청사진 정의를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-103">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="5194f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5194f-104">SYNTAX</span></span>

### <span data-ttu-id="5194f-105">CreateBlueprintAssignment (기본값)</span><span class="sxs-lookup"><span data-stu-id="5194f-105">CreateBlueprintAssignment (Default)</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> -Location <String>
 [-SystemAssignedIdentity] [-UserAssignedIdentity <String>] [-Lock <PSLockMode>]
 [-SecureStringParameter <Hashtable>] [-ResourceGroupParameter <Hashtable>] [-Parameter <Hashtable>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5194f-106">CreateBlueprintAssignmentByFile</span><span class="sxs-lookup"><span data-stu-id="5194f-106">CreateBlueprintAssignmentByFile</span></span>
```
New-AzBlueprintAssignment -Name <String> -Blueprint <PSBlueprintBase> [-AssignmentFile <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5194f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="5194f-107">DESCRIPTION</span></span>
<span data-ttu-id="5194f-108">구독에 청사진 정의를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-108">Assign a blueprint definition to a subscription.</span></span>

## <span data-ttu-id="5194f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="5194f-109">EXAMPLES</span></span>

### <span data-ttu-id="5194f-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="5194f-110">Example 1</span></span>
```powershell
PS C:\> $rg = @{ResourceGroup=@{name='storage_rg';location='eastus'}}
PS C:\> $params = @{applytaganditsdefaultvalue_tagName="Department_Cost_Center"; applytaganditsdefaultvalue_tagValue="Contoso/RnD/Dev/986754"}
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> $secureString = @{mySecureStringParam=@{keyVaultId='/subscriptions/00000000-1111-0000-1111-000000000000/rsourcegroups/myResourceGroup/providers/Microsoft.Keyvault/Vaults/myKeyVault';secretName='mySecret';secretVersion='1.0'}}
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -Location "West US" -ResourceGroupParameter $rg -Parameter $params -SecureStringParameter $secureString

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="5194f-111">`$blueprintObject`정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정 된 구독 내에서 청사진 정의에 대 한 새 청사진 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-111">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary.</span></span> <span data-ttu-id="5194f-112">시스템 할당 id를 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-112">Uses system-assigned identity.</span></span> <span data-ttu-id="5194f-113">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-113">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="5194f-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="5194f-114">Example 2</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -Lock AllResourcesReadOnly
```

<span data-ttu-id="5194f-115">정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정 된 구독 내에 청사진 정의에 대 한 새 청사진 과제를 만들고 리소스 `$blueprintObject` 잠금을 **allresources** 로 구성 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-115">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary and configuring resource locking to **AllResources**.</span></span> <span data-ttu-id="5194f-116">시스템 할당 id를 사용 하는 기본값입니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-116">Defaults to using system-assigned identity.</span></span>  <span data-ttu-id="5194f-117">위치는 관리 되는 id를 만들 영역을 정의 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-117">The location defines the region for creating the managed identity.</span></span>

### <span data-ttu-id="5194f-118">예제 3</span><span class="sxs-lookup"><span data-stu-id="5194f-118">Example 3</span></span>
```powershell
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId 00000000-1111-0000-1111-000000000000 -Location "West US" -Parameter @{P1="v1"; P2="v2"} -UserAssignedIdentity "/subscriptions/00000000-1111-0000-1111-000000000000/resourceGroups/my-resource-group/providers/Microsoft.ManagedIdentity/userAssignedIdentities/my-user-defined-identity"
```

<span data-ttu-id="5194f-119">`$blueprintObject`지정 된 사용자 할당 id id를 사용 하 여 정의 된 매개 변수 및 리소스 그룹 사전을 사용 하 여 지정한 구독에서 청사진 정의에 대 한 새 청사진 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-119">Create a new blueprint assignment of the blueprint definition `$blueprintObject` within the specified subscription using the defined parameter and resource group dictionary using the specified user-assigned identity id.</span></span>

### <span data-ttu-id="5194f-120">예제 4</span><span class="sxs-lookup"><span data-stu-id="5194f-120">Example 4</span></span>
```powershell
PS C:\> $blueprintObject =  Get-AzBlueprint -SubscriptionId "00000000-1111-0000-1111-000000000000" -Name "myBlueprintName"
PS C:\> New-AzBlueprintAssignment -Name "myAssignment" -Blueprint $blueprintObject -SubscriptionId "00000000-1111-0000-1111-000000000000" -AssignmentFile C:\myAssignmentfile.json

Name              : myAssignment
Id                : /subscriptions/00000000-1111-0000-1111-000000000000/providers/Microsoft.Blueprint/blueprintAssignments/myAssignment
Scope             : /subscriptions/00000000-1111-0000-1111-000000000000
LastModified      : 2019-01-08
LockMode          : None
ProvisioningState : Creating
Parameters        : {applytaganditsdefaultvalue_tagName, applytaganditsdefaultvalue_tagValue}
ResourceGroups    : ResourceGroup
```

<span data-ttu-id="5194f-121">과제 파일을 통해 청사진 과제를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-121">Create a blueprint assignment through an assignment file.</span></span> <span data-ttu-id="5194f-122">과제물 파일의 형식은 다음의 요청/응답 샘플에서 찾을 수 있습니다. https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span><span class="sxs-lookup"><span data-stu-id="5194f-122">The format of the assignment file can be found in the request/response samples at: https://github.com/Azure/azure-rest-api-specs/tree/master/specification/blueprint/resource-manager/Microsoft.Blueprint/preview/2018-11-01-preview/examples</span></span>

## <span data-ttu-id="5194f-123">변수</span><span class="sxs-lookup"><span data-stu-id="5194f-123">PARAMETERS</span></span>

### <span data-ttu-id="5194f-124">-청사진</span><span class="sxs-lookup"><span data-stu-id="5194f-124">-Blueprint</span></span>
<span data-ttu-id="5194f-125">청사진 정의 개체</span><span class="sxs-lookup"><span data-stu-id="5194f-125">Blueprint definition object.</span></span>

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

### <span data-ttu-id="5194f-126">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5194f-126">-DefaultProfile</span></span>
<span data-ttu-id="5194f-127">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-127">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="5194f-128">-위치</span><span class="sxs-lookup"><span data-stu-id="5194f-128">-Location</span></span>
<span data-ttu-id="5194f-129">에서 만들 관리 되는 id의 영역입니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-129">Region for managed identity to be created in.</span></span>
<span data-ttu-id="5194f-130">자세한 정보 aka.ms/blueprintmsi</span><span class="sxs-lookup"><span data-stu-id="5194f-130">Learn more at aka.ms/blueprintmsi</span></span>

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

### <span data-ttu-id="5194f-131">-잠금</span><span class="sxs-lookup"><span data-stu-id="5194f-131">-Lock</span></span>
<span data-ttu-id="5194f-132">리소스 잠그기.</span><span class="sxs-lookup"><span data-stu-id="5194f-132">Lock resources.</span></span>
<span data-ttu-id="5194f-133">자세한 정보 aka.ms/blueprintlocks</span><span class="sxs-lookup"><span data-stu-id="5194f-133">Learn more at aka.ms/blueprintlocks</span></span>

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

### <span data-ttu-id="5194f-134">-이름</span><span class="sxs-lookup"><span data-stu-id="5194f-134">-Name</span></span>
<span data-ttu-id="5194f-135">청사진 과제 이름.</span><span class="sxs-lookup"><span data-stu-id="5194f-135">Blueprint assignment name.</span></span>

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

### <span data-ttu-id="5194f-136">-Parameter</span><span class="sxs-lookup"><span data-stu-id="5194f-136">-Parameter</span></span>
<span data-ttu-id="5194f-137">아티팩트 매개 변수</span><span class="sxs-lookup"><span data-stu-id="5194f-137">Artifact parameters.</span></span>

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

### <span data-ttu-id="5194f-138">-ResourceGroupParameter</span><span class="sxs-lookup"><span data-stu-id="5194f-138">-ResourceGroupParameter</span></span>
<span data-ttu-id="5194f-139">{{ResourceGroupParameter 매개 변수 설명}}</span><span class="sxs-lookup"><span data-stu-id="5194f-139">{{Fill ResourceGroupParameter Description}}</span></span>

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

### <span data-ttu-id="5194f-140">-SecureStringParameter</span><span class="sxs-lookup"><span data-stu-id="5194f-140">-SecureStringParameter</span></span>
<span data-ttu-id="5194f-141">KeyVault 리소스 id, 이름 및 버전에 대 한 보안 문자열 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-141">Secure string parameter for KeyVault resource id, name and version.</span></span>

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

### <span data-ttu-id="5194f-142">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="5194f-142">-SubscriptionId</span></span>
<span data-ttu-id="5194f-143">청사진 정의를 할당 하는 구독 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-143">Subscription Id to assign the blueprint definition.</span></span>
<span data-ttu-id="5194f-144">SubscriptionId 문자열의 쉼표로 구분 된 목록이 될 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-144">Can be a comma delimited list of subscriptionId strings.</span></span>

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

### <span data-ttu-id="5194f-145">-SystemAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5194f-145">-SystemAssignedIdentity</span></span>
<span data-ttu-id="5194f-146">시스템 할당 id (MSI)를 통해 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-146">System assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="5194f-147">-UserAssignedIdentity</span><span class="sxs-lookup"><span data-stu-id="5194f-147">-UserAssignedIdentity</span></span>
<span data-ttu-id="5194f-148">사용자가 할당 한 id (MSI)를 사용 하 여 아티팩트를 배포 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-148">User assigned identity(MSI) to deploy the artifacts.</span></span>

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

### <span data-ttu-id="5194f-149">-확인</span><span class="sxs-lookup"><span data-stu-id="5194f-149">-Confirm</span></span>
<span data-ttu-id="5194f-150">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-150">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="5194f-151">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5194f-151">-WhatIf</span></span>
<span data-ttu-id="5194f-152">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-152">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5194f-153">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-153">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="5194f-154">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5194f-154">CommonParameters</span></span>
<span data-ttu-id="5194f-155">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5194f-155">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5194f-156">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5194f-156">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5194f-157">입력</span><span class="sxs-lookup"><span data-stu-id="5194f-157">INPUTS</span></span>

### <span data-ttu-id="5194f-158">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="5194f-158">System.String</span></span>

### <span data-ttu-id="5194f-159">PSBlueprintBase (.).</span><span class="sxs-lookup"><span data-stu-id="5194f-159">Microsoft.Azure.Commands.Blueprint.Models.PSBlueprintBase</span></span>

### <span data-ttu-id="5194f-160">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="5194f-160">System.String[]</span></span>

### <span data-ttu-id="5194f-161">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="5194f-161">System.Collections.Hashtable</span></span>

## <span data-ttu-id="5194f-162">출력</span><span class="sxs-lookup"><span data-stu-id="5194f-162">OUTPUTS</span></span>

### <span data-ttu-id="5194f-163">System. 개체</span><span class="sxs-lookup"><span data-stu-id="5194f-163">System.Object</span></span>
## <span data-ttu-id="5194f-164">상속자</span><span class="sxs-lookup"><span data-stu-id="5194f-164">NOTES</span></span>

## <span data-ttu-id="5194f-165">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5194f-165">RELATED LINKS</span></span>
