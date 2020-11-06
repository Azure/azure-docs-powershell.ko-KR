---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/new-azurermpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: 364411d6b69c04d8b29c1c32e2809ec3c4789b09
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532644"
---
# <span data-ttu-id="79fa5-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="79fa5-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="79fa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79fa5-102">SYNOPSIS</span></span>
<span data-ttu-id="79fa5-103">정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="79fa5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79fa5-104">SYNTAX</span></span>

### <span data-ttu-id="79fa5-105">CreateWithoutParameters (기본값)</span><span class="sxs-lookup"><span data-stu-id="79fa5-105">CreateWithoutParameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79fa5-106">CreateWithPolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="79fa5-106">CreateWithPolicyParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79fa5-107">CreateWithPolicyParameterString</span><span class="sxs-lookup"><span data-stu-id="79fa5-107">CreateWithPolicyParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79fa5-108">CreateWithPolicySetParameterObject</span><span class="sxs-lookup"><span data-stu-id="79fa5-108">CreateWithPolicySetParameterObject</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="79fa5-109">CreateWithPolicySetParameterString</span><span class="sxs-lookup"><span data-stu-id="79fa5-109">CreateWithPolicySetParameterString</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="79fa5-110">설명은</span><span class="sxs-lookup"><span data-stu-id="79fa5-110">DESCRIPTION</span></span>
<span data-ttu-id="79fa5-111">**새 AzureRmPolicyAssignment** cmdlet은 정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="79fa5-112">정책 및 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="79fa5-113">예제의</span><span class="sxs-lookup"><span data-stu-id="79fa5-113">EXAMPLES</span></span>

### <span data-ttu-id="79fa5-114">예제 1: 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="79fa5-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="79fa5-115">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="79fa5-116">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="79fa5-117">두 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="79fa5-118">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="79fa5-119">마지막 명령은 리소스 그룹의 수준에서 $Policy에 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="79fa5-120">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="79fa5-121">예제 2: 정책 매개 변수 개체를 사용 하 여 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="79fa5-121">Example 2: Policy assignment at resource group level with policy parameter object</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> $Locations = Get-AzureRmLocation | where displayname -like "*east*"
PS C:\> $AllowedLocations = @{"listOfAllowedLocations"=($Locations.location)}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameterObject $AllowedLocations
```

<span data-ttu-id="79fa5-122">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-122">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="79fa5-123">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-123">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="79fa5-124">두 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-124">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="79fa5-125">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-125">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="79fa5-126">세 번째와 네 번째 명령은 이름에 "동쪽"이 포함 된 모든 Azure 지역을 포함 하는 개체를 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-126">The third and fourth commands create an object containing all Azure regions with "east" in the name.</span></span>
<span data-ttu-id="79fa5-127">명령은 $AllowedLocations 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-127">The commands store that object in the $AllowedLocations variable.</span></span>

<span data-ttu-id="79fa5-128">마지막 명령은 $AllowedLocations의 정책 매개 변수 개체를 사용 하 여 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-128">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter object in $AllowedLocations.</span></span>
<span data-ttu-id="79fa5-129">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-129">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

### <span data-ttu-id="79fa5-130">예제 3: 정책 매개 변수 파일이 있는 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="79fa5-130">Example 3: Policy assignment at resource group level with policy parameter file</span></span>
<span data-ttu-id="79fa5-131">로컬 작업 디렉터리에 다음 콘텐츠를 포함 하는 _AllowedLocations.js_ 파일을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-131">Create a file called _AllowedLocations.json_ in the local working directory with the following content.</span></span>
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
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition | Where-Object {$_.Properties.DisplayName -eq 'Allowed locations' -and $_.Properties.PolicyType -eq 'BuiltIn'}
PS C:\> New-AzureRmPolicyAssignment -Name "RestrictLocationPolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId -PolicyParameter .\AllowedLocations.json
```

<span data-ttu-id="79fa5-132">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-132">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="79fa5-133">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-133">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="79fa5-134">두 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 허용 된 위치에 대 한 기본 제공 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-134">The second command gets the built-in policy definition for allowed locations by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="79fa5-135">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-135">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="79fa5-136">마지막 명령은 로컬 작업 디렉터리에서 AllowedLocations.js정책 매개 변수 파일을 사용 하 여 리소스 그룹의 수준에서 $Policy 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-136">The final command assigns the policy in $Policy at the level of a resource group using the policy parameter file AllowedLocations.json from the local working directory.</span></span>
<span data-ttu-id="79fa5-137">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-137">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>


## <span data-ttu-id="79fa5-138">변수</span><span class="sxs-lookup"><span data-stu-id="79fa5-138">PARAMETERS</span></span>

### <span data-ttu-id="79fa5-139">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="79fa5-139">-ApiVersion</span></span>
<span data-ttu-id="79fa5-140">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-140">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="79fa5-141">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-141">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-142">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79fa5-142">-DefaultProfile</span></span>
<span data-ttu-id="79fa5-143">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="79fa5-143">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-144">-설명</span><span class="sxs-lookup"><span data-stu-id="79fa5-144">-Description</span></span>
<span data-ttu-id="79fa5-145">정책 할당에 대 한 설명</span><span class="sxs-lookup"><span data-stu-id="79fa5-145">The description for policy assignment</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-146">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="79fa5-146">-DisplayName</span></span>
<span data-ttu-id="79fa5-147">정책 할당의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-147">Specifies a display name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-148">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="79fa5-148">-InformationAction</span></span>
<span data-ttu-id="79fa5-149">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-149">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="79fa5-150">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-150">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="79fa5-151">하기로</span><span class="sxs-lookup"><span data-stu-id="79fa5-151">Continue</span></span>
- <span data-ttu-id="79fa5-152">숨기기</span><span class="sxs-lookup"><span data-stu-id="79fa5-152">Ignore</span></span>
- <span data-ttu-id="79fa5-153">Inquire</span><span class="sxs-lookup"><span data-stu-id="79fa5-153">Inquire</span></span>
- <span data-ttu-id="79fa5-154">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="79fa5-154">SilentlyContinue</span></span>
- <span data-ttu-id="79fa5-155">중지가</span><span class="sxs-lookup"><span data-stu-id="79fa5-155">Stop</span></span>
- <span data-ttu-id="79fa5-156">대기</span><span class="sxs-lookup"><span data-stu-id="79fa5-156">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-157">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="79fa5-157">-InformationVariable</span></span>
<span data-ttu-id="79fa5-158">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-158">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-159">-이름</span><span class="sxs-lookup"><span data-stu-id="79fa5-159">-Name</span></span>
<span data-ttu-id="79fa5-160">정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-160">Specifies a name for the policy assignment.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-161">-NotScope</span><span class="sxs-lookup"><span data-stu-id="79fa5-161">-NotScope</span></span>
<span data-ttu-id="79fa5-162">정책 할당의 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-162">The not scopes for policy assignment.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-163">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="79fa5-163">-PolicyDefinition</span></span>
<span data-ttu-id="79fa5-164">정책을 정책 규칙을 포함 하는 **PSObject** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-164">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-165">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="79fa5-165">-PolicyParameter</span></span>
<span data-ttu-id="79fa5-166">정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-166">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: String
Parameter Sets: CreateWithPolicyParameterString, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-167">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="79fa5-167">-PolicyParameterObject</span></span>
<span data-ttu-id="79fa5-168">정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-168">The policy parameter object.</span></span>

```yaml
Type: Hashtable
Parameter Sets: CreateWithPolicyParameterObject, CreateWithPolicySetParameterObject
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-169">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="79fa5-169">-PolicySetDefinition</span></span>
<span data-ttu-id="79fa5-170">정책 집합 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-170">The policy set definition object.</span></span>

```yaml
Type: PSObject
Parameter Sets: CreateWithoutParameters, CreateWithPolicyParameterObject, CreateWithPolicyParameterString
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: PSObject
Parameter Sets: CreateWithPolicySetParameterObject, CreateWithPolicySetParameterString
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-171">-Pre</span><span class="sxs-lookup"><span data-stu-id="79fa5-171">-Pre</span></span>
<span data-ttu-id="79fa5-172">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-172">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-173">-범위</span><span class="sxs-lookup"><span data-stu-id="79fa5-173">-Scope</span></span>
<span data-ttu-id="79fa5-174">정책을 할당할 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-174">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="79fa5-175">예를 들어 리소스 그룹에 정책을 할당 하려면 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-175">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="79fa5-176">`/subscriptions/`구독 ID `/resourcegroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="79fa5-176">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-177">-Sku</span><span class="sxs-lookup"><span data-stu-id="79fa5-177">-Sku</span></span>
<span data-ttu-id="79fa5-178">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-178">A hash table which represents sku properties.</span></span> <span data-ttu-id="79fa5-179">기본적으로 무료 Sku: Name = A0, 티어 = Fre</span><span class="sxs-lookup"><span data-stu-id="79fa5-179">Defaults to Free Sku: Name = A0, Tier = Fre</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: SkuObject

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="79fa5-180">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79fa5-180">CommonParameters</span></span>
<span data-ttu-id="79fa5-181">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-181">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79fa5-182">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="79fa5-182">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79fa5-183">입력</span><span class="sxs-lookup"><span data-stu-id="79fa5-183">INPUTS</span></span>

### <span data-ttu-id="79fa5-184">않아야</span><span class="sxs-lookup"><span data-stu-id="79fa5-184">None</span></span>
<span data-ttu-id="79fa5-185">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="79fa5-185">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="79fa5-186">출력</span><span class="sxs-lookup"><span data-stu-id="79fa5-186">OUTPUTS</span></span>

### <span data-ttu-id="79fa5-187">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="79fa5-187">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="79fa5-188">상속자</span><span class="sxs-lookup"><span data-stu-id="79fa5-188">NOTES</span></span>

## <span data-ttu-id="79fa5-189">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79fa5-189">RELATED LINKS</span></span>

[<span data-ttu-id="79fa5-190">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="79fa5-190">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="79fa5-191">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="79fa5-191">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="79fa5-192">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="79fa5-192">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="79fa5-193">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="79fa5-193">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


