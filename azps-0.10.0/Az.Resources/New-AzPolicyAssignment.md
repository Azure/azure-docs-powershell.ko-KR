---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/new-Azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/New-AzPolicyAssignment.md
ms.openlocfilehash: 1b8a7bd3d0c9f73b551cf6eefcb2564918fde1fa
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876435"
---
# <span data-ttu-id="df73b-101">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="df73b-101">New-AzPolicyAssignment</span></span>

## <span data-ttu-id="df73b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="df73b-102">SYNOPSIS</span></span>
<span data-ttu-id="df73b-103">정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-103">Creates a policy assignment.</span></span>

## <span data-ttu-id="df73b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="df73b-104">SYNTAX</span></span>

### <span data-ttu-id="df73b-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="df73b-105">DefaultParameterSet (Default)</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Metadata <String>]
 [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="df73b-106">PolicyParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df73b-106">PolicyParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="df73b-107">PolicyParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="df73b-107">PolicyParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="df73b-108">PolicySetParameterObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="df73b-108">PolicySetParameterObjectParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity]
 [-Location <String>] [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="df73b-109">PolicySetParameterStringParameterSet</span><span class="sxs-lookup"><span data-stu-id="df73b-109">PolicySetParameterStringParameterSet</span></span>
```
New-AzPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Metadata <String>] [-Sku <Hashtable>] [-AssignIdentity] [-Location <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="df73b-110">설명은</span><span class="sxs-lookup"><span data-stu-id="df73b-110">DESCRIPTION</span></span>
<span data-ttu-id="df73b-111">**새 AzPolicyAssignment** cmdlet은 정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-111">The **New-AzPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="df73b-112">정책 및 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="df73b-113">예제의</span><span class="sxs-lookup"><span data-stu-id="df73b-113">EXAMPLES</span></span>

### <span data-ttu-id="df73b-114">예제 1: 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="df73b-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="df73b-115">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="df73b-116">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져와 $Policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-116">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="df73b-117">마지막 명령은 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-117">The final command assigns the policy in $Policy at the level of the resource group identified by the **ResourceId** property of $ResourceGroup.</span></span>

### <span data-ttu-id="df73b-118">예제 2: 정책 매개 변수 개체를 사용 하 여 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="df73b-118">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -BuiltIn | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations'}
PS C:\> $Locations = Get-AzLocation | where displayname -like '*east*'
PS C:\> $AllowedLocations = @{'listOfAllowedLocations'=($Locations.location)}
PS C:\> New-AzPolicyAssignment -Name 'RestrictLocationPolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="df73b-119">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-119">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet.</span></span>
<span data-ttu-id="df73b-120">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-120">The command stores that object in the $ResourceGroup variable.</span></span>
<span data-ttu-id="df73b-121">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-121">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="df73b-122">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-122">The command stores that object in the $Policy variable.</span></span>
<span data-ttu-id="df73b-123">세 번째와 네 번째 명령은 이름에 "동쪽"이 포함 된 모든 Azure 지역을 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-123">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="df73b-124">명령은 $AllowedLocations 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-124">The commands store that object in the $AllowedLocations variable.</span></span>
<span data-ttu-id="df73b-125">마지막 명령은 $AllowedLocations의 정책 매개 변수 개체를 사용 하 여 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-125">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="df73b-126">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-126">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="df73b-127">예제 3: 정책 매개 변수 파일이 있는 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="df73b-127">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="df73b-128">로컬 작업 디렉터리에 다음 콘텐츠를 포함 하는 _AllowedLocations.js_ 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-128">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>

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

<span data-ttu-id="df73b-129">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-129">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="df73b-130">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져와 $Policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-130">The second command gets the built-in policy definition for allowed locations by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="df73b-131">마지막 명령은 로컬 작업 디렉터리에서 정책 매개 변수 파일 AllowedLocations.js를 사용 하 여 $ResourceGroup의 **ResourceId** 속성으로 식별 되는 리소스 그룹의 $Policy 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-131">The final command assigns the policy in $Policy at the resource group identified by the **ResourceId** property of $ResourceGroup using the policy parameter file AllowedLocations.json from the local working directory.</span></span>

### <span data-ttu-id="df73b-132">예제 4: 관리 id를 사용 하 여 정책 할당</span><span class="sxs-lookup"><span data-stu-id="df73b-132">Example 4: Policy assignment with a managed identity</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> $Policy = Get-AzPolicyDefinition -Name 'VirtualMachinePolicy'
PS C:\> New-AzPolicyAssignment -Name 'VirtualMachinePolicyAssignment' -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -Location 'eastus' -AssignIdentity 
```

<span data-ttu-id="df73b-133">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-133">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="df73b-134">두 번째 명령은 Get-AzPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져와 $Policy 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-134">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzPolicyDefinition cmdlet and stores it in the $Policy variable.</span></span>
<span data-ttu-id="df73b-135">마지막 명령은 $Policy의 정책을 리소스 그룹에 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-135">The final command assigns the policy in $Policy to the resource group.</span></span> <span data-ttu-id="df73b-136">관리 id가 자동으로 만들어지고 정책 할당에 할당 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-136">A managed identity is automatically created and assigned to the policy assignment.</span></span>

## <span data-ttu-id="df73b-137">변수</span><span class="sxs-lookup"><span data-stu-id="df73b-137">PARAMETERS</span></span>

### <span data-ttu-id="df73b-138">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="df73b-138">-ApiVersion</span></span>
<span data-ttu-id="df73b-139">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-139">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="df73b-140">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-140">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="df73b-141">-Id 할당</span><span class="sxs-lookup"><span data-stu-id="df73b-141">-AssignIdentity</span></span>
<span data-ttu-id="df73b-142">이 정책 할당에 대 한 Azure Active Directory Id를 생성 하 고 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-142">Generate and assign an Azure Active Directory Identity for this policy assignment.</span></span> <span data-ttu-id="df73b-143">Id는 ' deployIfNotExists ' 정책에 대 한 배포를 실행 하는 경우에 사용 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-143">The identity will be used when executing deployments for 'deployIfNotExists' policies.</span></span> <span data-ttu-id="df73b-144">Id를 할당할 때 위치가 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-144">Location is required when assigning an identity.</span></span>

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

### <span data-ttu-id="df73b-145">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="df73b-145">-DefaultProfile</span></span>
<span data-ttu-id="df73b-146">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="df73b-146">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-147">-설명</span><span class="sxs-lookup"><span data-stu-id="df73b-147">-Description</span></span>
<span data-ttu-id="df73b-148">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="df73b-148">The description for policy assignment</span></span>

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

### <span data-ttu-id="df73b-149">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="df73b-149">-DisplayName</span></span>
<span data-ttu-id="df73b-150">정책 할당의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-150">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="df73b-151">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="df73b-151">-InformationAction</span></span>
<span data-ttu-id="df73b-152">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-152">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="df73b-153">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-153">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="df73b-154">하기로</span><span class="sxs-lookup"><span data-stu-id="df73b-154">Continue</span></span>
- <span data-ttu-id="df73b-155">숨기기</span><span class="sxs-lookup"><span data-stu-id="df73b-155">Ignore</span></span>
- <span data-ttu-id="df73b-156">Inquire</span><span class="sxs-lookup"><span data-stu-id="df73b-156">Inquire</span></span>
- <span data-ttu-id="df73b-157">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="df73b-157">SilentlyContinue</span></span>
- <span data-ttu-id="df73b-158">중지가</span><span class="sxs-lookup"><span data-stu-id="df73b-158">Stop</span></span>
- <span data-ttu-id="df73b-159">대기</span><span class="sxs-lookup"><span data-stu-id="df73b-159">Suspend</span></span>

```yaml
Type: System.Management.Automation.ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-160">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="df73b-160">-InformationVariable</span></span>
<span data-ttu-id="df73b-161">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-161">Specifies an information variable.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-162">-위치</span><span class="sxs-lookup"><span data-stu-id="df73b-162">-Location</span></span>
<span data-ttu-id="df73b-163">정책 할당의 리소스 id 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-163">The location of the policy assignment's resource identity.</span></span> <span data-ttu-id="df73b-164">이는-할당 Id 스위치를 사용 하는 경우에 필요 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-164">This is required when the -AssignIdentity switch is used.</span></span>

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

### <span data-ttu-id="df73b-165">-Metadata</span><span class="sxs-lookup"><span data-stu-id="df73b-165">-Metadata</span></span>
<span data-ttu-id="df73b-166">새 정책 할당에 대 한 메타 데이터입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-166">The metadata for the new policy assignment.</span></span> <span data-ttu-id="df73b-167">메타 데이터를 포함 하는 파일 이름의 경로 이거나 메타 데이터를 문자열로 지정할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-167">This can either be a path to a file name containing the metadata, or the metadata as a string.</span></span>

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

### <span data-ttu-id="df73b-168">-이름</span><span class="sxs-lookup"><span data-stu-id="df73b-168">-Name</span></span>
<span data-ttu-id="df73b-169">정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-169">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="df73b-170">-NotScope</span><span class="sxs-lookup"><span data-stu-id="df73b-170">-NotScope</span></span>
<span data-ttu-id="df73b-171">정책 할당의 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-171">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="df73b-172">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="df73b-172">-PolicyDefinition</span></span>
<span data-ttu-id="df73b-173">정책을 정책 규칙을 포함 하는 **PsPolicyDefinition** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-173">Specifies a policy, as a **PsPolicyDefinition** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-174">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="df73b-174">-PolicyParameter</span></span>
<span data-ttu-id="df73b-175">정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-175">The policy parameter file path or policy parameter string.</span></span>

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

### <span data-ttu-id="df73b-176">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="df73b-176">-PolicyParameterObject</span></span>
<span data-ttu-id="df73b-177">정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-177">The policy parameter object.</span></span>

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

### <span data-ttu-id="df73b-178">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="df73b-178">-PolicySetDefinition</span></span>
<span data-ttu-id="df73b-179">정책 집합 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-179">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: DefaultParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicyParameterObjectParameterSet, PolicyParameterStringParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: PolicySetParameterObjectParameterSet, PolicySetParameterStringParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-180">-Pre</span><span class="sxs-lookup"><span data-stu-id="df73b-180">-Pre</span></span>
<span data-ttu-id="df73b-181">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-181">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="df73b-182">-범위</span><span class="sxs-lookup"><span data-stu-id="df73b-182">-Scope</span></span>
<span data-ttu-id="df73b-183">정책을 할당할 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-183">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="df73b-184">예를 들어 리소스 그룹에 정책을 할당 하려면 다음을 지정 합니다. `/subscriptions/` 구독 ID `/resourcegroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="df73b-184">For instance, to assign a policy to a resource group, specify the following: `/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="df73b-185">-Sku</span><span class="sxs-lookup"><span data-stu-id="df73b-185">-Sku</span></span>
<span data-ttu-id="df73b-186">SKU 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-186">A hash table which represents SKU properties.</span></span> <span data-ttu-id="df73b-187">기본적으로 다음 값이 포함 된 무료 SKU로 설정 `@{Name = 'A0'; Tier = 'Free'}` 됩니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-187">Defaults to the Free SKU with the values: `@{Name = 'A0'; Tier = 'Free'}`.</span></span> <span data-ttu-id="df73b-188">표준 SKU를 사용 하려면 다음 값을 사용 합니다 `@{Name = 'A1'; Tier = 'Standard'}` .</span><span class="sxs-lookup"><span data-stu-id="df73b-188">To use the Standard SKU, use the values: `@{Name = 'A1'; Tier = 'Standard'}`.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="df73b-189">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="df73b-189">CommonParameters</span></span>
<span data-ttu-id="df73b-190">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="df73b-190">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="df73b-191">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="df73b-191">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="df73b-192">입력</span><span class="sxs-lookup"><span data-stu-id="df73b-192">INPUTS</span></span>

## <span data-ttu-id="df73b-193">출력</span><span class="sxs-lookup"><span data-stu-id="df73b-193">OUTPUTS</span></span>

## <span data-ttu-id="df73b-194">상속자</span><span class="sxs-lookup"><span data-stu-id="df73b-194">NOTES</span></span>

## <span data-ttu-id="df73b-195">관련 링크</span><span class="sxs-lookup"><span data-stu-id="df73b-195">RELATED LINKS</span></span>

[<span data-ttu-id="df73b-196">Get-AzPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="df73b-196">Get-AzPolicyDefinition</span></span>](./Get-AzPolicyDefinition.md)

[<span data-ttu-id="df73b-197">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="df73b-197">Get-AzPolicyAssignment</span></span>](./Get-AzPolicyAssignment.md)

[<span data-ttu-id="df73b-198">제거-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="df73b-198">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="df73b-199">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="df73b-199">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


