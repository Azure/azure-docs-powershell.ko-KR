---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: C3B2C33F-8BD4-4E31-9450-EF6A3A6A5325
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/set-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Set-AzPolicyAssignment.md
ms.openlocfilehash: 8efda1a15546a09f0946506f3bc7fd27462b3c03
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98372044"
---
# <span data-ttu-id="e95b3-101">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e95b3-101">Set-AzPolicyAssignment</span></span>

## <span data-ttu-id="e95b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e95b3-102">SYNOPSIS</span></span>
<span data-ttu-id="e95b3-103">정책 할당을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-103">Modifies a policy assignment.</span></span>

## <span data-ttu-id="e95b3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e95b3-104">SYNTAX</span></span>

### <span data-ttu-id="e95b3-105">NameParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="e95b3-105">NameParameterSet (Default)</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-106">PolicyParameterNameObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-106">PolicyParameterNameObjectParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity]
 [-Location <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-107">PolicyParameterNameStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-107">PolicyParameterNameStringParameterSet</span></span>
```
Set-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-108">IdParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-109">PolicyParameterIdObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-109">PolicyParameterIdObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameterObject <Hashtable> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-110">PolicyParameterIdStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-110">PolicyParameterIdStringParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] -Id <String> [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] -PolicyParameter <String> [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e95b3-111">InputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e95b3-111">InputObjectParameterSet</span></span>
```
Set-AzPolicyAssignment [-NotScope <String[]>] [-DisplayName <String>] [-Description <String>]
 [-Metadata <String>] [-AssignIdentity] [-Location <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] -InputObject <PsPolicyAssignment> [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e95b3-112">설명</span><span class="sxs-lookup"><span data-stu-id="e95b3-112">DESCRIPTION</span></span>
<span data-ttu-id="e95b3-113">**Set-AzPolicyAssignment** cmdlet은 정책 할당을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-113">The **Set-AzPolicyAssignment** cmdlet modifies a policy assignment.</span></span>
<span data-ttu-id="e95b3-114">ID 또는 이름 및 범위로 할당을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-114">Specify an assignment by ID or by name and scope.</span></span>

## <span data-ttu-id="e95b3-115">예제</span><span class="sxs-lookup"><span data-stu-id="e95b3-115">EXAMPLES</span></span>

### <span data-ttu-id="e95b3-116">예제 1: 표시 이름 업데이트</span><span class="sxs-lookup"><span data-stu-id="e95b3-116">Example 1: Update the display name</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -DisplayName 'Do not allow VM creation'
```

<span data-ttu-id="e95b3-117">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-117">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e95b3-118">이 명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-118">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e95b3-119">두 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용하여 PolicyAssignment라는 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-119">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e95b3-120">이 명령은 해당 개체를 $PolicyAssignment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-120">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e95b3-121">마지막 명령은 리소스 그룹의 **ResourceId** 속성으로 식별된 리소스 그룹의 정책 할당에 대한 표시 이름을 $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e95b3-121">The final command updates the display name on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="e95b3-122">예제 2: 정책 할당에 관리 ID 추가</span><span class="sxs-lookup"><span data-stu-id="e95b3-122">Example 2: Add a managed identity to the policy assignment</span></span>
```
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -AssignIdentity -Location 'westus'
```

<span data-ttu-id="e95b3-123">첫 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용하여 현재 구독에서 PolicyAssignment라는 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-123">The first command gets the policy assignment named PolicyAssignment from the current subscription by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e95b3-124">이 명령은 해당 개체를 $PolicyAssignment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-124">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e95b3-125">마지막 명령은 관리 ID를 정책 할당에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-125">The final command assigns a managed identity to the policy assignment.</span></span>

### <span data-ttu-id="e95b3-126">예제 3: 새 정책 매개 변수 개체를 사용하여 정책 할당 매개 변수 업데이트</span><span class="sxs-lookup"><span data-stu-id="e95b3-126">Example 3: Update policy assignment parameters with new policy parameter object</span></span>
```
PS C:\> $Locations = Get-AzLocation | where {($_.displayname -like 'france*') -or ($_.displayname -like 'uk*')}
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment'
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="e95b3-127">첫 번째 및 두 번째 명령은 이름이 "france" 또는 "uk"로 시작하는 모든 Azure 지역을 포함하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-127">The first and second commands create an object containing all Azure regions whose names start with "france" or "uk".</span></span>
<span data-ttu-id="e95b3-128">두 번째 명령은 해당 개체를 $AllowedLocations 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-128">The second command stores that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="e95b3-129">세 번째 명령은 'PolicyAssignment'라는 정책 할당을 $PolicyAssignment 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-129">The third command gets the policy assignment named 'PolicyAssignment' The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e95b3-130">마지막 명령은 PolicyAssignment라는 정책 할당의 매개 변수 값을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-130">The final command updates the parameter values on the policy assignment named PolicyAssignment.</span></span>

### <span data-ttu-id="e95b3-131">예제 4: 정책 매개 변수 파일을 사용하여 정책 할당 매개 변수 업데이트</span><span class="sxs-lookup"><span data-stu-id="e95b3-131">Example 4: Update policy assignment parameters with policy parameter file</span></span>
<span data-ttu-id="e95b3-132">로컬 작업 디렉터리에AllowedLocations.js _다음_ 내용으로AllowedLocations.js파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="e95b3-133">이 명령은 로컬 작업 디렉터리의 정책 매개 AllowedLocations.js파일을 사용하여 'PolicyAssignment'라는 정책 할당을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-133">The command updates the policy assignment named 'PolicyAssignment' using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="e95b3-134">예제 5: enforcementMode 업데이트</span><span class="sxs-lookup"><span data-stu-id="e95b3-134">Example 5: Update an enforcementMode</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $PolicyAssignment = Get-AzPolicyAssignment -Name 'PolicyAssignment' -Scope $ResourceGroup.ResourceId
PS C:\> Set-AzPolicyAssignment -Id $PolicyAssignment.ResourceId -EnforcementMode Default
```

<span data-ttu-id="e95b3-135">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-135">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="e95b3-136">이 명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-136">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e95b3-137">두 번째 명령은 Get-AzPolicyAssignment cmdlet을 사용하여 PolicyAssignment라는 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-137">The second command gets the policy assignment named PolicyAssignment by using the Get-AzPolicyAssignment cmdlet.</span></span>
<span data-ttu-id="e95b3-138">이 명령은 해당 개체를 $PolicyAssignment 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-138">The command stores that object in the $PolicyAssignment variable.</span></span>
<span data-ttu-id="e95b3-139">마지막 명령은 리소스 그룹의 **ResourceId** 속성으로 식별된 리소스 그룹에 대한 policy 할당에 대한 enforcementMode 속성을 $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="e95b3-139">The final command updates the enforcementMode property on the policy assignment on the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

## <span data-ttu-id="e95b3-140">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e95b3-140">PARAMETERS</span></span>

### <span data-ttu-id="e95b3-141">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e95b3-141">-ApiVersion</span></span>
<span data-ttu-id="e95b3-142">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-142">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e95b3-143">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-143">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e95b3-144">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="e95b3-144">-AssignIdentity</span></span>
<span data-ttu-id="e95b3-145">이 정책 할당에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-145">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="e95b3-146">ID는 'deployIfNotExists' 정책에 대한 배포를 실행할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-146">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="e95b3-147">ID를 할당할 때 위치가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-147">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="e95b3-148">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e95b3-148">-DefaultProfile</span></span>
<span data-ttu-id="e95b3-149">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e95b3-149">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e95b3-150">-Description</span><span class="sxs-lookup"><span data-stu-id="e95b3-150">-Description</span></span>
<span data-ttu-id="e95b3-151">정책 할당에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="e95b3-151">The description for policy assignment</span></span>

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

### <span data-ttu-id="e95b3-152">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="e95b3-152">-DisplayName</span></span>
<span data-ttu-id="e95b3-153">정책 할당에 대한 새 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-153">Specifies a new display name for the policy assignment.</span></span>

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

### <span data-ttu-id="e95b3-154">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="e95b3-154">-EnforcementMode</span></span>
<span data-ttu-id="e95b3-155">정책 할당에 대한 적용 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-155">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="e95b3-156">현재 유효한 값은 Default, DoNotEnforce입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-156">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="e95b3-157">-Id</span><span class="sxs-lookup"><span data-stu-id="e95b3-157">-Id</span></span>
<span data-ttu-id="e95b3-158">이 cmdlet이 수정하는 정책 할당에 대한 정식 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-158">Specifies the fully qualified resource ID for the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e95b3-159">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e95b3-159">-InputObject</span></span>
<span data-ttu-id="e95b3-160">다른 cmdlet의 출력인 업데이트할 정책 할당 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-160">The policy assignment object to update that was output from another cmdlet.</span></span>

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

### <span data-ttu-id="e95b3-161">-Location</span><span class="sxs-lookup"><span data-stu-id="e95b3-161">-Location</span></span>
<span data-ttu-id="e95b3-162">정책 할당의 리소스 ID의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-162">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="e95b3-163">-AssignIdentity 스위치를 사용할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-163">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="e95b3-164">-Metadata</span><span class="sxs-lookup"><span data-stu-id="e95b3-164">-Metadata</span></span>
<span data-ttu-id="e95b3-165">정책 할당에 대한 업데이트된 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-165">The updated metadata for the policy assignment.</span></span> <span data-ttu-id="e95b3-166">메타데이터를 포함하는 파일 이름의 경로 또는 메타데이터를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-166">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="e95b3-167">-Name</span><span class="sxs-lookup"><span data-stu-id="e95b3-167">-Name</span></span>
<span data-ttu-id="e95b3-168">이 cmdlet이 수정하는 정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-168">Specifies the name of the policy assignment that this cmdlet modifies.</span></span>

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

### <span data-ttu-id="e95b3-169">-NotScope</span><span class="sxs-lookup"><span data-stu-id="e95b3-169">-NotScope</span></span>
<span data-ttu-id="e95b3-170">범위가 아닌 정책 할당입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-170">The policy assignment not scopes.</span></span>

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

### <span data-ttu-id="e95b3-171">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="e95b3-171">-PolicyParameter</span></span>
<span data-ttu-id="e95b3-172">새 정책 매개 변수 파일 경로 또는 정책 할당에 대한 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-172">The new policy parameters file path or string for the policy assignment.</span></span>

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

### <span data-ttu-id="e95b3-173">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="e95b3-173">-PolicyParameterObject</span></span>
<span data-ttu-id="e95b3-174">정책 할당에 대한 새 정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-174">The new policy parameters object for the policy assignment.</span></span>

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

### <span data-ttu-id="e95b3-175">-Pre</span><span class="sxs-lookup"><span data-stu-id="e95b3-175">-Pre</span></span>
<span data-ttu-id="e95b3-176">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-176">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e95b3-177">-Scope</span><span class="sxs-lookup"><span data-stu-id="e95b3-177">-Scope</span></span>
<span data-ttu-id="e95b3-178">정책이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-178">Specifies the scope at which the policy is applied.</span></span>

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

### <span data-ttu-id="e95b3-179">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e95b3-179">CommonParameters</span></span>
<span data-ttu-id="e95b3-180">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e95b3-180">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e95b3-181">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e95b3-181">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e95b3-182">입력</span><span class="sxs-lookup"><span data-stu-id="e95b3-182">INPUTS</span></span>

### <span data-ttu-id="e95b3-183">System.String</span><span class="sxs-lookup"><span data-stu-id="e95b3-183">System.String</span></span>

### <span data-ttu-id="e95b3-184">System.String[]</span><span class="sxs-lookup"><span data-stu-id="e95b3-184">System.String[]</span></span>

## <span data-ttu-id="e95b3-185">출력</span><span class="sxs-lookup"><span data-stu-id="e95b3-185">OUTPUTS</span></span>

### <span data-ttu-id="e95b3-186">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="e95b3-186">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="e95b3-187">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e95b3-187">NOTES</span></span>

## <span data-ttu-id="e95b3-188">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e95b3-188">RELATED LINKS</span></span>

[<span data-ttu-id="e95b3-189">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e95b3-189">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="e95b3-190">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e95b3-190">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="e95b3-191">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e95b3-191">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)


