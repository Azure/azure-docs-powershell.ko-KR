---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 63efc580cf47274363f04750dc6a3f8da93b6665
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208461"
---
# <span data-ttu-id="b478e-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b478e-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="b478e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b478e-102">SYNOPSIS</span></span>
<span data-ttu-id="b478e-103">정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="b478e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b478e-104">SYNTAX</span></span>

### <span data-ttu-id="b478e-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="b478e-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>]
 [-PolicySetDefinition <PsPolicySetDefinition>] [-Metadata <String>]
 [-EnforcementMode <PolicyAssignmentEnforcementMode>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b478e-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b478e-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b478e-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b478e-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PsPolicyDefinition> [-PolicySetDefinition <PsPolicySetDefinition>]
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b478e-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="b478e-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="b478e-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="b478e-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> [-Scope <String>] [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PsPolicyDefinition>] -PolicySetDefinition <PsPolicySetDefinition>
 -PolicyParameter <String> [-Metadata <String>] [-EnforcementMode <PolicyAssignmentEnforcementMode>]
 [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b478e-110">설명</span><span class="sxs-lookup"><span data-stu-id="b478e-110">DESCRIPTION</span></span>
<span data-ttu-id="b478e-111">**New-AzPolicyAssignment** cmdlet은 정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="b478e-112">정책 및 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="b478e-113">예제</span><span class="sxs-lookup"><span data-stu-id="b478e-113">EXAMPLES</span></span>

### <span data-ttu-id="b478e-114">예제 1: 구독 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-114">Example 1: Policy assignment at subscription level</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)"
```

<span data-ttu-id="b478e-115">첫 번째 명령은 Get-AzSubscription cmdlet을 사용하여 Subscription01이라는 구독을 $Subscription 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-115">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="b478e-116">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b478e-117">마지막 명령은 구독 범위 $Policy 식별된 구독 수준에서 정책에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-117">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span>

### <span data-ttu-id="b478e-118">예제 2: 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-118">Example 2: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b478e-119">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b478e-120">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-120">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b478e-121">마지막 명령은 $Policy **ResourceId** 속성으로 식별되는 리소스 그룹 수준에서 정책의 $ResourceGroup.</span><span class="sxs-lookup"><span data-stu-id="b478e-121">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="b478e-122">예제 3: 정책 매개 변수 개체를 사용하여 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-122">Example 3: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="b478e-123">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-123">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="b478e-124">이 명령은 해당 개체를 $ResourceGroup 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-124">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b478e-125">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 허용되는 위치에 대한 기본 제공 정책 정의를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-125">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b478e-126">이 명령은 해당 개체를 $Policy 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-126">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="b478e-127">세 번째 및 네 번째 명령은 이름에 "east"이 있는 모든 Azure 지역을 포함하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-127">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="b478e-128">명령은 해당 개체를 $AllowedLocations 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-128">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="b478e-129">마지막 명령은 $Policy 정책 매개 변수 개체를 사용하여 리소스 그룹 수준에서 $AllowedLocations.</span><span class="sxs-lookup"><span data-stu-id="b478e-129">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="b478e-130">리소스 **그룹의 ResourceId** 속성은 $ResourceGroup 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-130">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="b478e-131">예제 4: 정책 매개 변수 파일을 사용하여 리소스 그룹 수준에서 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-131">Example 4: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="b478e-132">로컬 작업 디렉터리에AllowedLocations.js _다음_ 내용으로 "on"이라는 파일을 만들 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-132">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="b478e-133">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b478e-134">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 허용되는 위치에 대한 기본 제공 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b478e-135">마지막 명령은 로컬 $Policy 디렉터리의 정책 매개 변수 파일을 사용하여 $ResourceGroup **ResourceId** 속성으로 식별된 리소스 AllowedLocations.js정책에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-135">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="b478e-136">예제 5: 관리 ID를 통해 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-136">Example 5: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity
```

<span data-ttu-id="b478e-137">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-137">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="b478e-138">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-138">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b478e-139">마지막 명령은 리소스 그룹에 $Policy 정책을 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-139">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="b478e-140">관리 ID가 자동으로 만들어지며 정책 할당에 할당됩니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-140">A managed identity is automatically created and assigned to the policy assignment.</span></span>

### <span data-ttu-id="b478e-141">예제 6: 적용 모드 속성이 있는 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b478e-141">Example 6: Policy assignment with an enforcement mode property</span></span>
```
PS C:\> $Subscription = Get-AzSubscription -SubscriptionName 'Subscription01'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope "/subscriptions/$($Subscription.Id)" -EnforcementMode DoNotEnforce
```

<span data-ttu-id="b478e-142">첫 번째 명령은 Get-AzSubscription cmdlet을 사용하여 Subscription01이라는 구독을 $Subscription 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-142">The first command gets a subscription named Subscription01 by using the Get-AzSubscription cmdlet and stores it in the $Subscription variable.</span></span>
<span data-ttu-id="b478e-143">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용하여 VirtualMachinePolicy라는 정책 정의를 $Policy 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-143">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="b478e-144">마지막 명령은 구독 범위 $Policy 식별된 구독 수준에서 정책에 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-144">The final command assigns the policy in $Policy at the level of the subscription identified by the subscription scope string.</span></span> <span data-ttu-id="b478e-145">할당은 _DoNotEnforce의_ EnforcementMode 값으로 설정됩니다. 리소스 생성 또는 업데이트 중에 정책 효과가 적용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-145">The assignment is set with an EnforcementMode value of _DoNotEnforce_ i.e. the policy effect is not enforced during resource creation or update.</span></span>

## <span data-ttu-id="b478e-146">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b478e-146">PARAMETERS</span></span>

### <span data-ttu-id="b478e-147">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b478e-147">-ApiVersion</span></span>
<span data-ttu-id="b478e-148">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-148">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b478e-149">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-149">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b478e-150">-AssignIdentity</span><span class="sxs-lookup"><span data-stu-id="b478e-150">-AssignIdentity</span></span>
<span data-ttu-id="b478e-151">이 정책 할당에 대한 Azure Active Directory ID를 생성하고 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-151">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="b478e-152">ID는 'deployIfNotExists' 정책에 대한 배포를 실행할 때 사용됩니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-152">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="b478e-153">ID를 할당할 때 위치가 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-153">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="b478e-154">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b478e-154">-DefaultProfile</span></span>
<span data-ttu-id="b478e-155">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="b478e-155">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="b478e-156">-Description</span><span class="sxs-lookup"><span data-stu-id="b478e-156">-Description</span></span>
<span data-ttu-id="b478e-157">정책 할당에 대한 설명</span><span class="sxs-lookup"><span data-stu-id="b478e-157">The description for policy assignment</span></span>

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

### <span data-ttu-id="b478e-158">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b478e-158">-DisplayName</span></span>
<span data-ttu-id="b478e-159">정책 할당에 대한 표시 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-159">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b478e-160">-EnforcementMode</span><span class="sxs-lookup"><span data-stu-id="b478e-160">-EnforcementMode</span></span>
<span data-ttu-id="b478e-161">정책 할당에 대한 적용 모드입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-161">The enforcement mode for policy assignment.</span></span> <span data-ttu-id="b478e-162">현재 유효한 값은 Default, DoNotEnforce입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-162">Currently, valid values are Default, DoNotEnforce.</span></span>

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

### <span data-ttu-id="b478e-163">-Location</span><span class="sxs-lookup"><span data-stu-id="b478e-163">-Location</span></span>
<span data-ttu-id="b478e-164">정책 할당의 리소스 ID의 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-164">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="b478e-165">-AssignIdentity 스위치를 사용할 때 필요합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-165">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="b478e-166">-Metadata</span><span class="sxs-lookup"><span data-stu-id="b478e-166">-Metadata</span></span>
<span data-ttu-id="b478e-167">새 정책 할당에 대한 메타데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-167">The metadata for the new policy assignment.</span></span> <span data-ttu-id="b478e-168">메타데이터를 포함하는 파일 이름의 경로 또는 메타데이터를 문자열로 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-168">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="b478e-169">-Name</span><span class="sxs-lookup"><span data-stu-id="b478e-169">-Name</span></span>
<span data-ttu-id="b478e-170">정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-170">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="b478e-171">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b478e-171">-NotScope</span></span>
<span data-ttu-id="b478e-172">정책 할당에 대한 범위가 아 없습니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-172">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="b478e-173">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b478e-173">-PolicyDefinition</span></span>
<span data-ttu-id="b478e-174">정책 규칙을 포함하는 **PsPolicyDefinition** 개체로 정책을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-174">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

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

### <span data-ttu-id="b478e-175">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b478e-175">-PolicyParameter</span></span>
<span data-ttu-id="b478e-176">정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-176">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="b478e-177">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b478e-177">-PolicyParameterObject</span></span>
<span data-ttu-id="b478e-178">정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-178">The policy parameter object.</span></span>

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

### <span data-ttu-id="b478e-179">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b478e-179">-PolicySetDefinition</span></span>
<span data-ttu-id="b478e-180">정책 집합 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-180">The policy set definition object.</span></span>

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

### <span data-ttu-id="b478e-181">-Pre</span><span class="sxs-lookup"><span data-stu-id="b478e-181">-Pre</span></span>
<span data-ttu-id="b478e-182">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-182">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b478e-183">-Scope</span><span class="sxs-lookup"><span data-stu-id="b478e-183">-Scope</span></span>
<span data-ttu-id="b478e-184">정책을 할당할 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-184">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="b478e-185">예를 들어 리소스 그룹에 정책을 할당하려면 구독 ID 리소스 그룹 이름을 `/subscriptions/` `/resourcegroups/` 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-185">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="b478e-186">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b478e-186">CommonParameters</span></span>
<span data-ttu-id="b478e-187">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b478e-187">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b478e-188">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b478e-188">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b478e-189">입력</span><span class="sxs-lookup"><span data-stu-id="b478e-189">INPUTS</span></span>

### <span data-ttu-id="b478e-190">System.String</span><span class="sxs-lookup"><span data-stu-id="b478e-190">System.String</span></span>

### <span data-ttu-id="b478e-191">System.String[]</span><span class="sxs-lookup"><span data-stu-id="b478e-191">System.String[]</span></span>

### <span data-ttu-id="b478e-192">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b478e-192">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b478e-193">출력</span><span class="sxs-lookup"><span data-stu-id="b478e-193">OUTPUTS</span></span>

### <span data-ttu-id="b478e-194">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="b478e-194">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b478e-195">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b478e-195">NOTES</span></span>

## <span data-ttu-id="b478e-196">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b478e-196">RELATED LINKS</span></span>

[<span data-ttu-id="b478e-197">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b478e-197">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="b478e-198">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b478e-198">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="b478e-199">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b478e-199">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="b478e-200">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b478e-200">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


