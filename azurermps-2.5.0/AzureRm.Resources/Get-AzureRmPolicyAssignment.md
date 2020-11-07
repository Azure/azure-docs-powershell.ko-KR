---
external help file: Microsoft.Azure.Commands.ResourceManager.Cmdlets.dll-Help.xml
Module Name: AzureRM.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/get-azurermpolicyassignment
schema: 2.0.0
ms.openlocfilehash: cabd2c86ed687b90b45e60b8078d89ad0a413c87
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93881754"
---
# <span data-ttu-id="e932b-101">Get-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e932b-101">Get-AzureRmPolicyAssignment</span></span>

## <span data-ttu-id="e932b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e932b-102">SYNOPSIS</span></span>
<span data-ttu-id="e932b-103">정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-103">Gets policy assignments.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="e932b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="e932b-104">SYNTAX</span></span>

### <span data-ttu-id="e932b-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="e932b-105">DefaultParameterSet (Default)</span></span>
```
Get-AzureRmPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e932b-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="e932b-106">NameParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>]
 [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e932b-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="e932b-107">IncludeDescendentParameterSet</span></span>
```
Get-AzureRmPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="e932b-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="e932b-108">IdParameterSet</span></span>
```
Get-AzureRmPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="e932b-109">설명은</span><span class="sxs-lookup"><span data-stu-id="e932b-109">DESCRIPTION</span></span>
<span data-ttu-id="e932b-110">**AzureRmPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-110">The **Get-AzureRmPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="e932b-111">정책 할당을 식별 하 여 이름, 범위 또는 ID로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="e932b-112">예제의</span><span class="sxs-lookup"><span data-stu-id="e932b-112">EXAMPLES</span></span>

### <span data-ttu-id="e932b-113">예제 1: 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="e932b-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzureRmPolicyAssignment
```

<span data-ttu-id="e932b-114">이 명령은 모든 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="e932b-115">예제 2: 특정 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="e932b-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzureRmResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzureRmPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="e932b-116">첫 번째 명령은 Get-AzureRMResourceGroup cmdletand 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzureRMResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="e932b-117">두 번째 명령은 $ResourceGroup **ResourceId** 속성이 식별 하는 범위에 대 한 PolicyAssignment07 라는 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="e932b-118">예제 3: 관리 그룹에 할당 된 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="e932b-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzureRmPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="e932b-119">첫 번째 명령은 쿼리할 관리 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="e932b-120">두 번째 명령은 ID가 ' myManagementGroup ' 인 관리 그룹에 할당 된 모든 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="e932b-121">변수</span><span class="sxs-lookup"><span data-stu-id="e932b-121">PARAMETERS</span></span>

### <span data-ttu-id="e932b-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="e932b-122">-ApiVersion</span></span>
<span data-ttu-id="e932b-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="e932b-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="e932b-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e932b-125">-DefaultProfile</span></span>
<span data-ttu-id="e932b-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="e932b-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="e932b-127">-Id</span><span class="sxs-lookup"><span data-stu-id="e932b-127">-Id</span></span>
<span data-ttu-id="e932b-128">이 cmdlet이 가져오는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: IdParameterSet
Aliases: ResourceId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932b-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="e932b-129">-IncludeDescendent</span></span>
<span data-ttu-id="e932b-130">상위 범위의 범위 및 하위 범위를 포함 하 여 지정 된 범위와 관련 된 모든 할당을 포함 하도록 반환 된 정책 할당 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: IncludeDescendentParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932b-131">-InformationAction</span><span class="sxs-lookup"><span data-stu-id="e932b-131">-InformationAction</span></span>
<span data-ttu-id="e932b-132">이 cmdlet이 정보 이벤트에 응답 하는 방법을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-132">Specifies how this cmdlet responds to an information event.</span></span>
<span data-ttu-id="e932b-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-133">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="e932b-134">하기로</span><span class="sxs-lookup"><span data-stu-id="e932b-134">Continue</span></span>
- <span data-ttu-id="e932b-135">숨기기</span><span class="sxs-lookup"><span data-stu-id="e932b-135">Ignore</span></span>
- <span data-ttu-id="e932b-136">Inquire</span><span class="sxs-lookup"><span data-stu-id="e932b-136">Inquire</span></span>
- <span data-ttu-id="e932b-137">SilentlyContinue</span><span class="sxs-lookup"><span data-stu-id="e932b-137">SilentlyContinue</span></span>
- <span data-ttu-id="e932b-138">중지가</span><span class="sxs-lookup"><span data-stu-id="e932b-138">Stop</span></span>
- <span data-ttu-id="e932b-139">대기</span><span class="sxs-lookup"><span data-stu-id="e932b-139">Suspend</span></span>

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

### <span data-ttu-id="e932b-140">-InformationVariable</span><span class="sxs-lookup"><span data-stu-id="e932b-140">-InformationVariable</span></span>
<span data-ttu-id="e932b-141">정보 변수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-141">Specifies an information variable.</span></span>

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

### <span data-ttu-id="e932b-142">-이름</span><span class="sxs-lookup"><span data-stu-id="e932b-142">-Name</span></span>
<span data-ttu-id="e932b-143">이 cmdlet이 가져오는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-143">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932b-144">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="e932b-144">-PolicyDefinitionId</span></span>
<span data-ttu-id="e932b-145">이 cmdlet이 가져오는 정책 할당의 정책 정의에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-145">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IdParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932b-146">-Pre</span><span class="sxs-lookup"><span data-stu-id="e932b-146">-Pre</span></span>
<span data-ttu-id="e932b-147">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-147">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="e932b-148">-범위</span><span class="sxs-lookup"><span data-stu-id="e932b-148">-Scope</span></span>
<span data-ttu-id="e932b-149">이 cmdlet이 가져오는 할당에 대해 정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-149">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: NameParameterSet, IncludeDescendentParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="e932b-150">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e932b-150">CommonParameters</span></span>
<span data-ttu-id="e932b-151">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="e932b-151">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e932b-152">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e932b-152">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e932b-153">입력</span><span class="sxs-lookup"><span data-stu-id="e932b-153">INPUTS</span></span>

## <span data-ttu-id="e932b-154">출력</span><span class="sxs-lookup"><span data-stu-id="e932b-154">OUTPUTS</span></span>

## <span data-ttu-id="e932b-155">상속자</span><span class="sxs-lookup"><span data-stu-id="e932b-155">NOTES</span></span>

## <span data-ttu-id="e932b-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e932b-156">RELATED LINKS</span></span>

[<span data-ttu-id="e932b-157">새로운 AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e932b-157">New-AzureRmPolicyAssignment</span></span>](./New-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e932b-158">제거-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e932b-158">Remove-AzureRmPolicyAssignment</span></span>](./Remove-AzureRmPolicyAssignment.md)

[<span data-ttu-id="e932b-159">Set-AzureRmPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="e932b-159">Set-AzureRmPolicyAssignment</span></span>](./Set-AzureRmPolicyAssignment.md)


