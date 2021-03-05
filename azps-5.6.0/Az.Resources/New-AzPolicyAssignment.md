---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: d1e6b5b2b2e76c4ec807c27922f9ce577d94a7d8
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101972640"
---
# <span data-ttu-id="dc564-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dc564-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="dc564-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dc564-102">SYNOPSIS</span></span>
<span data-ttu-id="dc564-103">정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="dc564-104">구문</span><span class="sxs-lookup"><span data-stu-id="dc564-104">SYNTAX</span></span>

### <span data-ttu-id="dc564-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="dc564-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc564-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc564-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc564-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc564-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc564-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc564-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="dc564-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="dc564-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dc564-110">설명</span><span class="sxs-lookup"><span data-stu-id="dc564-110">DESCRIPTION</span></span>
<span data-ttu-id="dc564-111">**New-AzPolicyAssignment** cmdlet은 정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="dc564-112">정책 및 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="dc564-113">예제</span><span class="sxs-lookup"><span data-stu-id="dc564-113">EXAMPLES</span></span>

### <span data-ttu-id="dc564-114">예제 1: 구독 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="dc564-115">첫 번째 명령은 Get-AzSubscription cmdlet을 사용하여 Subscription01이라는 구독을 $Subscription 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="dc564-116">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dc564-117">마지막 명령은 구독 범위 $Policy 식별된 구독 수준에서 정책에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="dc564-118">예제 2: 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="dc564-119">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dc564-120">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dc564-121">마지막 명령은 $Policy **ResourceId** 속성에 의해 식별된 리소스 그룹의 수준에서 $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="dc564-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="dc564-122">예제 3: 정책 매개 변수 개체가 있는 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="dc564-123">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="dc564-124">명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dc564-125">두 번째 명령은 허용되는 위치에 대한 기본 제공 정책 정의를 Get-AzPolicyDefinition cmdlet을 사용합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="dc564-126">명령은 해당 개체를 $Policy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="dc564-127">세 번째 및 네 번째 명령은 이름에 "east"가 있는 모든 Azure 지역을 포함하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="dc564-128">명령은 해당 개체를 $AllowedLocations 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="dc564-129">마지막 명령은 $Policy 매개 변수 개체를 사용하여 리소스 그룹의 수준에서 $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="dc564-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="dc564-130">$ResourceGroup **ResourceId** 속성은 리소스 그룹을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="dc564-131">예제 4: 정책 매개 변수 파일을 사용하여 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="dc564-132">다음 콘텐츠가AllowedLocations.js로컬 작업 _디렉터리에서_ AllowedLocations.js파일을 만드십시오.</span><span class="sxs-lookup"><span data-stu-id="dc564-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

```
{
    "listOfAllowedLocations":  {
      "value": [
        "westus",
        "westeurope",
        "japanwest"
      ]
    }
}
```

```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="dc564-133">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dc564-134">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 허용되는 위치에 대한 기본 제공 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dc564-135">최종 명령은 로컬 작업 디렉터리에서 $Policy 있는 정책 매개 변수 파일을 사용하여 $ResourceGroup **리소스** 그룹에서 AllowedLocations.js할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="dc564-136">예제 5: 관리 ID가 있는 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="dc564-137">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="dc564-138">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dc564-139">마지막 명령은 리소스 그룹에 $Policy 정책을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="dc564-140">관리 ID가 자동으로 만들어지며 정책 할당에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="dc564-141">예제 6: 적용 모드 속성이 있는 정책 할당</span><span class="sxs-lookup"><span data-stu-id="dc564-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="dc564-142">첫 번째 명령은 Get-AzSubscription cmdlet을 사용하여 Subscription01이라는 구독을 $Subscription 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="dc564-143">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="dc564-144">마지막 명령은 구독 범위 $Policy 식별된 구독 수준에서 정책에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="dc564-145">할당은 _DoNotEnforce의_ EnforcementMode 값으로 설정됩니다. 예: 리소스 만들기 또는 업데이트 중에 정책 효과가 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="dc564-146">매개 변수</span><span class="sxs-lookup"><span data-stu-id="dc564-146">PARAMETERS</span></span>

### <span data-ttu-id="dc564-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="dc564-147">-ApiVersion</span></span>
<span data-ttu-id="dc564-148">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="dc564-149">버전을 지정하지 않으면 이 cmdlet에서는 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="dc564-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="dc564-150">-AssignIdentity</span></span>
<span data-ttu-id="dc564-151">이 정책 할당에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="dc564-152">ID는 'deployIfNotExists' 정책에 대한 배포를 실행할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="dc564-153">ID를 할당할 때 위치가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="dc564-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dc564-154">-DefaultProfile</span></span>
<span data-ttu-id="dc564-155">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="dc564-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="dc564-156">-Description</span><span class="sxs-lookup"><span data-stu-id="dc564-156">-Description</span></span>
<span data-ttu-id="dc564-157">정책 할당에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="dc564-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="dc564-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="dc564-158">-DisplayName</span></span>
<span data-ttu-id="dc564-159">정책 할당에 대한 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="dc564-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="dc564-160">-EnforcementMode</span></span>
<span data-ttu-id="dc564-161">정책 할당에 대한 적용 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="dc564-162">현재 유효한 값은 기본값인 DoNotEnforce입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="dc564-163">-Location</span><span class="sxs-lookup"><span data-stu-id="dc564-163">-Location</span></span>
<span data-ttu-id="dc564-164">정책 할당의 리소스 ID의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="dc564-165">-AssignIdentity 스위치를 사용할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="dc564-166">-메타데이터</span><span class="sxs-lookup"><span data-stu-id="dc564-166">-Metadata</span></span>
<span data-ttu-id="dc564-167">새 정책 할당의 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="dc564-168">메타데이터를 포함하는 파일 이름에 대한 경로 또는 메타데이터를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="dc564-169">-Name</span><span class="sxs-lookup"><span data-stu-id="dc564-169">-Name</span></span>
<span data-ttu-id="dc564-170">정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="dc564-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="dc564-171">-NotScope</span></span>
<span data-ttu-id="dc564-172">정책 할당에 대한 범위가 아닌 경우</span><span class="sxs-lookup"><span data-stu-id="dc564-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="dc564-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc564-173">-PolicyDefinition</span></span>
<span data-ttu-id="dc564-174">정책 규칙을 포함하는 **PsPolicyDefinition 개체로** 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicyDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc564-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="dc564-175">-PolicyParameter</span></span>
<span data-ttu-id="dc564-176">정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-176">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: PolicyParameterStringParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc564-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="dc564-177">-PolicyParameterObject</span></span>
<span data-ttu-id="dc564-178">정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-178">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: PolicyParameterObjectParameterSet, PolicySetParameterObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dc564-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="dc564-179">-PolicySetDefinition</span></span>
<span data-ttu-id="dc564-180">정책 집합 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-180">The policy set definition object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: Microsoft.Azure.Commands.ResourceManager.Cmdlets.Implementation.Policy.PsPolicySetDefinition
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dc564-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="dc564-181">-Pre</span></span>
<span data-ttu-id="dc564-182">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려하고 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="dc564-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="dc564-183">-Scope</span></span>
<span data-ttu-id="dc564-184">정책을 할당할 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="dc564-185">예를 들어 리소스 그룹에 정책을 할당하려면 구독 ID 리소스 그룹 이름을 `/subscriptions/` `/resourcegroups/` 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="dc564-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dc564-186">CommonParameters</span></span>
<span data-ttu-id="dc564-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="dc564-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dc564-188">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="dc564-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dc564-189">입력</span><span class="sxs-lookup"><span data-stu-id="dc564-189">INPUTS</span></span>

### <span data-ttu-id="dc564-190">System.String</span><span class="sxs-lookup"><span data-stu-id="dc564-190">System.String</span></span>

### <span data-ttu-id="dc564-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="dc564-191">System.String[]</span></span>

### <span data-ttu-id="dc564-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="dc564-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dc564-193">출력</span><span class="sxs-lookup"><span data-stu-id="dc564-193">OUTPUTS</span></span>

### <span data-ttu-id="dc564-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="dc564-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="dc564-195">참고 사항</span><span class="sxs-lookup"><span data-stu-id="dc564-195">NOTES</span></span>

## <span data-ttu-id="dc564-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dc564-196">RELATED LINKS</span></span>

[<span data-ttu-id="dc564-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="dc564-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="dc564-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dc564-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="dc564-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dc564-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="dc564-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="dc564-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


