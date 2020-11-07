---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: BA40BD11-8167-48D7-AC71-72B2FD9924F2
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/New-AzureRmPolicyAssignment.md
ms.openlocfilehash: fa43b462cf06b9e2cd58df5d6796c098e942fafc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703631"
---
# <span data-ttu-id="b1947-101">New-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1947-101">New-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="b1947-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b1947-102">SYNOPSIS</span></span>
<span data-ttu-id="b1947-103">정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-103">Creates a policy assignment.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b1947-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b1947-104">SYNTAX</span></span>

### <span data-ttu-id="b1947-105">매개 변수 없이 정책 할당 (기본값)</span><span class="sxs-lookup"><span data-stu-id="b1947-105">Policy assignment without parameters (Default)</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] [-PolicySetDefinition <PSObject>] [-Sku <Hashtable>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1947-106">정책 매개 변수 개체를 통해 매개 변수를 사용한 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b1947-106">Policy assignment with parameters via policy parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1947-107">정책 매개 변수 문자열을 통해 매개 변수를 사용한 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b1947-107">Policy assignment with parameters via policy parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] -PolicyDefinition <PSObject> [-PolicySetDefinition <PSObject>]
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1947-108">정책 집합 매개 변수 개체를 통해 매개 변수를 사용한 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b1947-108">Policy assignment with parameters via policy set parameter object</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameterObject <Hashtable> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b1947-109">정책 집합 매개 변수 문자열을 통한 매개 변수를 사용한 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b1947-109">Policy assignment with parameters via policy set parameter string</span></span>
```
New-AzureRmPolicyAssignment -Name <String> -Scope <String> [-NotScope <String[]>] [-DisplayName <String>]
 [-Description <String>] [-PolicyDefinition <PSObject>] -PolicySetDefinition <PSObject>
 -PolicyParameter <String> [-Sku <Hashtable>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b1947-110">설명은</span><span class="sxs-lookup"><span data-stu-id="b1947-110">DESCRIPTION</span></span>
<span data-ttu-id="b1947-111">**새 AzureRmPolicyAssignment** cmdlet은 정책 할당을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-111">The **New-AzureRmPolicyAssignment** cmdlet creates a policy assignment.</span></span>
<span data-ttu-id="b1947-112">정책 및 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-112">Specify a policy and scope.</span></span>

## <span data-ttu-id="b1947-113">예제의</span><span class="sxs-lookup"><span data-stu-id="b1947-113">EXAMPLES</span></span>

### <span data-ttu-id="b1947-114">예제 1: 리소스 그룹 수준의 정책 할당</span><span class="sxs-lookup"><span data-stu-id="b1947-114">Example 1: Policy assignment at resource group level</span></span>
```
PS C:\>$ResourceGroup = Get-AzureRmResourceGroup -Name "ResourceGroup11"
PS C:\> $Policy = Get-AzureRmPolicyDefinition -Name "VirtualMachinePolicy"
PS C:\> New-AzureRmPolicyAssignment -Name "VirtualMachinePolicyAssignment" -PolicyDefinition $Policy -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="b1947-115">첫 번째 명령은 Get-AzureRMResourceGroup cmdlet을 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-115">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdlet.</span></span>
<span data-ttu-id="b1947-116">명령이 $ResourceGroup 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-116">The command stores that object in the $ResourceGroup variable.</span></span>

<span data-ttu-id="b1947-117">두 번째 명령은 Get-AzureRmPolicyDefinition cmdlet을 사용 하 여 VirtualMachinePolicy 라는 정책 정의를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-117">The second command gets the policy definition named VirtualMachinePolicy by using the Get-AzureRmPolicyDefinition cmdlet.</span></span>
<span data-ttu-id="b1947-118">명령이 $Policy 변수에 해당 개체를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-118">The command stores that object in the $Policy variable.</span></span>

<span data-ttu-id="b1947-119">마지막 명령은 리소스 그룹의 수준에서 $Policy에 정책을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-119">The final command assigns the policy in $Policy at the level of a resource group.</span></span>
<span data-ttu-id="b1947-120">리소스 그룹을 식별 하는 $ResourceGroup의 **ResourceId** 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-120">The **ResourceId** property of $ResourceGroup identifies the resource group.</span></span>

## <span data-ttu-id="b1947-121">변수</span><span class="sxs-lookup"><span data-stu-id="b1947-121">PARAMETERS</span></span>

### <span data-ttu-id="b1947-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="b1947-122">-ApiVersion</span></span>
<span data-ttu-id="b1947-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="b1947-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="b1947-125">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="b1947-125">-DisplayName</span></span>
<span data-ttu-id="b1947-126">정책 할당의 표시 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-126">Specifies a display name for the policy assignment.</span></span>

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

### <span data-ttu-id="b1947-127">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="b1947-127">-InformationAction</span></span>
<span data-ttu-id="b1947-128">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-128">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b1947-129">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-129">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b1947-130">하기로</span><span class="sxs-lookup"><span data-stu-id="b1947-130">Continue</span></span>
- <span data-ttu-id="b1947-131">숨기기</span><span class="sxs-lookup"><span data-stu-id="b1947-131">Ignore</span></span>
- <span data-ttu-id="b1947-132">Inquire</span><span class="sxs-lookup"><span data-stu-id="b1947-132">Inquire</span></span>
- <span data-ttu-id="b1947-133">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="b1947-133">SilentlyContinue</span></span>
- <span data-ttu-id="b1947-134">중지가</span><span class="sxs-lookup"><span data-stu-id="b1947-134">Stop</span></span>
- <span data-ttu-id="b1947-135">대기</span><span class="sxs-lookup"><span data-stu-id="b1947-135">Suspend</span></span>

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

### <span data-ttu-id="b1947-136">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="b1947-136">-InformationVariable</span></span>
<span data-ttu-id="b1947-137">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-137">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b1947-138">-이름</span><span class="sxs-lookup"><span data-stu-id="b1947-138">-Name</span></span>
<span data-ttu-id="b1947-139">정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-139">Specifies a name for the policy assignment.</span></span>

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

### <span data-ttu-id="b1947-140">-NotScope</span><span class="sxs-lookup"><span data-stu-id="b1947-140">-NotScope</span></span>
<span data-ttu-id="b1947-141">정책 할당의 범위를 지정 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-141">The not scopes for policy assignment.</span></span>

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

### <span data-ttu-id="b1947-142">-PolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b1947-142">-PolicyDefinition</span></span>
<span data-ttu-id="b1947-143">정책을 정책 규칙을 포함 하는 **PSObject** 개체로 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-143">Specifies a policy, as a **PSObject** object that contains the policy rule.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1947-144">-PolicyParameter</span><span class="sxs-lookup"><span data-stu-id="b1947-144">-PolicyParameter</span></span>
<span data-ttu-id="b1947-145">정책 매개 변수 파일 경로 또는 정책 매개 변수 문자열입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-145">The policy parameter file path or policy parameter string.</span></span>

```yaml
Type: System.String
Parameter Sets: Policy assignment with parameters via policy parameter string, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1947-146">-PolicyParameterObject</span><span class="sxs-lookup"><span data-stu-id="b1947-146">-PolicyParameterObject</span></span>
<span data-ttu-id="b1947-147">정책 매개 변수 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-147">The policy parameter object.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy set parameter object
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1947-148">-PolicySetDefinition</span><span class="sxs-lookup"><span data-stu-id="b1947-148">-PolicySetDefinition</span></span>
<span data-ttu-id="b1947-149">정책 집합 정의 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-149">The policy set definition object.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment without parameters, Policy assignment with parameters via policy parameter object, Policy assignment with parameters via policy parameter string
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: Policy assignment with parameters via policy set parameter object, Policy assignment with parameters via policy set parameter string
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b1947-150">-Pre</span><span class="sxs-lookup"><span data-stu-id="b1947-150">-Pre</span></span>
<span data-ttu-id="b1947-151">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-151">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="b1947-152">-범위</span><span class="sxs-lookup"><span data-stu-id="b1947-152">-Scope</span></span>
<span data-ttu-id="b1947-153">정책을 할당할 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-153">Specifies the scope at which to assign the policy.</span></span>
<span data-ttu-id="b1947-154">예를 들어 리소스 그룹에 정책을 할당 하려면 다음을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-154">For instance, to assign a policy to a resource group, specify the following:</span></span>

<span data-ttu-id="b1947-155">`/subscriptions/`구독 ID `/resourcegroups/` 리소스 그룹 이름</span><span class="sxs-lookup"><span data-stu-id="b1947-155">`/subscriptions/`subscription ID`/resourcegroups/`resource group name</span></span>

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

### <span data-ttu-id="b1947-156">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b1947-156">-DefaultProfile</span></span>
<span data-ttu-id="b1947-157">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-157">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b1947-158">-설명</span><span class="sxs-lookup"><span data-stu-id="b1947-158">-Description</span></span>
<span data-ttu-id="b1947-159">정책 할당에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-159">The description for policy assignment.</span></span>

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

### <span data-ttu-id="b1947-160">-Sku</span><span class="sxs-lookup"><span data-stu-id="b1947-160">-Sku</span></span>
<span data-ttu-id="b1947-161">Sku 속성을 나타내는 해시 테이블입니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-161">A hash table which represents sku properties.</span></span> <span data-ttu-id="b1947-162">무료 Sku: Name = A0, 티어 = Free로 설정 됩니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-162">Defaults to Free Sku: Name = A0, Tier = Free</span></span>

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

### <span data-ttu-id="b1947-163">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b1947-163">CommonParameters</span></span>
<span data-ttu-id="b1947-164">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b1947-164">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b1947-165">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b1947-165">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b1947-166">입력</span><span class="sxs-lookup"><span data-stu-id="b1947-166">INPUTS</span></span>

## <span data-ttu-id="b1947-167">출력</span><span class="sxs-lookup"><span data-stu-id="b1947-167">OUTPUTS</span></span>

### <span data-ttu-id="b1947-168">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="b1947-168">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="b1947-169">상속자</span><span class="sxs-lookup"><span data-stu-id="b1947-169">NOTES</span></span>

## <span data-ttu-id="b1947-170">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b1947-170">RELATED LINKS</span></span>

[<span data-ttu-id="b1947-171">Get-AzureRmPolicyDefinition</span><span class="sxs-lookup"><span data-stu-id="b1947-171">Get-AzureRmPolicyDefinition</span></span>](./Get-AzureRmPolicyDefinition.md)

[<span data-ttu-id="b1947-172">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1947-172">Get-AzureRmPolicyAssignment</span></span>](./Get-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b1947-173">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1947-173">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="b1947-174">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="b1947-174">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


