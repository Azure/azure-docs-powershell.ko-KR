---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94308735"
---
# <span data-ttu-id="3732e-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3732e-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="3732e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3732e-102">SYNOPSIS</span></span>
<span data-ttu-id="3732e-103">정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="3732e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="3732e-104">SYNTAX</span></span>

### <span data-ttu-id="3732e-105">NameParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="3732e-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="3732e-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="3732e-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3732e-112">설명은</span><span class="sxs-lookup"><span data-stu-id="3732e-112">DESCRIPTION</span></span>
<span data-ttu-id="3732e-113">**Set-AzPolicyAssignment** cmdlet은 정책 할당을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="3732e-114">ID 또는 이름 및 범위를 기준으로 과제를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="3732e-115">예제의</span><span class="sxs-lookup"><span data-stu-id="3732e-115">EXAMPLES</span></span>

### <span data-ttu-id="3732e-116">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="3732e-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="3732e-117">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3732e-118">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3732e-119">두 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="3732e-120">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3732e-121">마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 정책 할당에 대 한 표시 이름을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="3732e-122">예제 2: 정책 할당에 관리 되는 id 추가</span><span class="sxs-lookup"><span data-stu-id="3732e-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="3732e-123">첫 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용 하 여 현재 구독에서 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="3732e-124">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3732e-125">마지막 명령은 정책 할당에 관리 되는 id를 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="3732e-126">예제 3: 새 정책 매개 변수 개체를 사용 하 여 정책 할당 매개 변수 업데이트</span><span class="sxs-lookup"><span data-stu-id="3732e-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="3732e-127">첫 번째 및 두 번째 명령은 이름이 "프랑스" 또는 "영국"으로 시작 하는 모든 Azure 지역을 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="3732e-128">두 번째 명령은 $AllowedLocations 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="3732e-129">세 번째 명령은 명령이 ' PolicyAssignment ' 이라는 정책 과제를 가져와 해당 개체를 $PolicyAssignment 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3732e-130">마지막 명령은 PolicyAssignment 이라는 정책 할당에 대 한 매개 변수 값을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="3732e-131">예제 4: 정책 매개 변수 파일을 사용 하 여 정책 할당 매개 변수 업데이트</span><span class="sxs-lookup"><span data-stu-id="3732e-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="3732e-132">로컬 작업 디렉터리에 다음 콘텐츠를 포함 하는 _AllowedLocations.js_ 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "uksouth",
        "ukwest",
        "francecentral",
        "francesouth"
      ]
    }
}
```

```
PS C:\> Set-AzPolicyAssignment -Name 'PolicyAssignment' -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="3732e-133">이 명령은 정책 매개 변수 파일을 사용 하 여 ' PolicyAssignment ' 이라는 정책 할당을 로컬 작업 디렉터리에서 AllowedLocations.js업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="3732e-134">예제 5: enforcementMode 업데이트</span><span class="sxs-lookup"><span data-stu-id="3732e-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="3732e-135">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="3732e-136">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="3732e-137">두 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용 하 여 PolicyAssignment 이라는 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="3732e-138">명령이 $PolicyAssignment 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="3732e-139">마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 정책 할당에 대 한 enforcementMode 속성을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="3732e-140">변수</span><span class="sxs-lookup"><span data-stu-id="3732e-140">PARAMETERS</span></span>

### <span data-ttu-id="3732e-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="3732e-141">-ApiVersion</span></span>
<span data-ttu-id="3732e-142">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="3732e-143">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="3732e-144">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="3732e-144">-AssignIdentity</span></span>
<span data-ttu-id="3732e-145">이 정책 할당에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="3732e-146">Id는 ' deployIfNotExists ' 정책에 대 한 배포를 실행 하는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="3732e-147">Id를 할당할 때 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="3732e-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3732e-148">-DefaultProfile</span></span>
<span data-ttu-id="3732e-149">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="3732e-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="3732e-150">-설명</span><span class="sxs-lookup"><span data-stu-id="3732e-150">-Description</span></span>
<span data-ttu-id="3732e-151">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="3732e-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="3732e-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3732e-152">-DisplayName</span></span>
<span data-ttu-id="3732e-153">정책 할당에 대 한 새 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="3732e-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="3732e-154">-EnforcementMode</span></span>
<span data-ttu-id="3732e-155">정책 할당에 대 한 적용 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="3732e-156">현재 유효한 값은 Default, DoNotEnforce입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-156">Currently, valid values are Default, DoNotEnforce.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Commands.ResourceManager.Cmdlets.Entities.Policy.PolicyAssignmentEnforcementMode]
Parameter Sets: (All)
Aliases:
Accepted values: Default, DoNotEnforce

Required: False
Position: Named
Default value: Default
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-157">-Id</span><span class="sxs-lookup"><span data-stu-id="3732e-157">-Id</span></span>
<span data-ttu-id="3732e-158">이 cmdlet이 수정 하는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet, PolicyParameterIdObjectParameterSet, PolicyParameterIdStringParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3732e-159">-InputObject</span></span>
<span data-ttu-id="3732e-160">다른 cmdlet에서 출력 된 업데이트할 정책 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-160">The policy assignment object to update that was output from another cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyAssignment
Parameter Sets: InputObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-161">-위치</span><span class="sxs-lookup"><span data-stu-id="3732e-161">-Location</span></span>
<span data-ttu-id="3732e-162">정책 할당의 리소스 id 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="3732e-163">이는-할당 Id 스위치를 사용 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="3732e-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="3732e-164">-Metadata</span></span>
<span data-ttu-id="3732e-165">정책 할당에 대 한 업데이트 된 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="3732e-166">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="3732e-167">-이름</span><span class="sxs-lookup"><span data-stu-id="3732e-167">-Name</span></span>
<span data-ttu-id="3732e-168">이 cmdlet이 수정 하는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="3732e-169">-NotScope</span></span>
<span data-ttu-id="3732e-170">정책 할당이 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="3732e-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="3732e-171">-PolicyParameter</span></span>
<span data-ttu-id="3732e-172">정책 할당에 대 한 새 정책 매개 변수 파일 경로 또는 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-172">The new policy parameters file path or string for the policy assignment.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterNameStringParameterSet, PolicyParameterIdStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="3732e-173">-PolicyParameterObject</span></span>
<span data-ttu-id="3732e-174">정책 할당에 대 한 새 정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-174">The new policy parameters object for the policy assignment.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterNameObjectParameterSet, PolicyParameterIdObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="3732e-175">-Pre</span></span>
<span data-ttu-id="3732e-176">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="3732e-177">-범위</span><span class="sxs-lookup"><span data-stu-id="3732e-177">-Scope</span></span>
<span data-ttu-id="3732e-178">정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-178">Specifies the scope at which the policy is applied.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, PolicyParameterNameObjectParameterSet, PolicyParameterNameStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3732e-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3732e-179">CommonParameters</span></span>
<span data-ttu-id="3732e-180">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="3732e-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3732e-181">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="3732e-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3732e-182">입력</span><span class="sxs-lookup"><span data-stu-id="3732e-182">INPUTS</span></span>

### <span data-ttu-id="3732e-183">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="3732e-183">System.String</span></span>

### <span data-ttu-id="3732e-184">System.webserver []</span><span class="sxs-lookup"><span data-stu-id="3732e-184">System.String[]</span></span>

## <span data-ttu-id="3732e-185">출력</span><span class="sxs-lookup"><span data-stu-id="3732e-185">OUTPUTS</span></span>

### <span data-ttu-id="3732e-186">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="3732e-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="3732e-187">상속자</span><span class="sxs-lookup"><span data-stu-id="3732e-187">NOTES</span></span>

## <span data-ttu-id="3732e-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="3732e-188">RELATED LINKS</span></span>

[<span data-ttu-id="3732e-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3732e-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="3732e-190">새로운 AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3732e-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="3732e-191">제거-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="3732e-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


