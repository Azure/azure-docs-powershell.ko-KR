---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: f1510cbe9b3223173372a42696b0de28ed542df6
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699432"
---
# <span data-ttu-id="6058e-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6058e-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="6058e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6058e-102">SYNOPSIS</span></span>
<span data-ttu-id="6058e-103">정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-103">Gets policy assignments.</span></span>

## <span data-ttu-id="6058e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6058e-104">SYNTAX</span></span>

### <span data-ttu-id="6058e-105">DefaultParameterSet (기본값)</span><span class="sxs-lookup"><span data-stu-id="6058e-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="6058e-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="6058e-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6058e-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="6058e-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6058e-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="6058e-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6058e-109">설명은</span><span class="sxs-lookup"><span data-stu-id="6058e-109">DESCRIPTION</span></span>
<span data-ttu-id="6058e-110">**AzPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="6058e-111">정책 할당을 식별 하 여 이름, 범위 또는 ID로 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="6058e-112">예제의</span><span class="sxs-lookup"><span data-stu-id="6058e-112">EXAMPLES</span></span>

### <span data-ttu-id="6058e-113">예제 1: 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="6058e-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="6058e-114">이 명령은 모든 정책 과제를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="6058e-115">예제 2: 특정 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="6058e-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="6058e-116">첫 번째 명령은 Get-AzResourceGroup cmdletand 사용 하 여 ResourceGroup11 이라는 리소스 그룹을 가져와 $ResourceGroup 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdletand stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="6058e-117">두 번째 명령은 $ResourceGroup **ResourceId** 속성이 식별 하는 범위에 대 한 PolicyAssignment07 라는 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="6058e-118">예제 3: 관리 그룹에 할당 된 모든 정책 할당 가져오기</span><span class="sxs-lookup"><span data-stu-id="6058e-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="6058e-119">첫 번째 명령은 쿼리할 관리 그룹의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="6058e-120">두 번째 명령은 ID가 ' myManagementGroup ' 인 관리 그룹에 할당 된 모든 정책 할당을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="6058e-121">변수</span><span class="sxs-lookup"><span data-stu-id="6058e-121">PARAMETERS</span></span>

### <span data-ttu-id="6058e-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="6058e-122">-ApiVersion</span></span>
<span data-ttu-id="6058e-123">사용할 리소스 공급자 API의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="6058e-124">버전을 지정 하지 않으면이 cmdlet은 사용 가능한 최신 버전을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="6058e-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6058e-125">-DefaultProfile</span></span>
<span data-ttu-id="6058e-126">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="6058e-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="6058e-127">-Id</span><span class="sxs-lookup"><span data-stu-id="6058e-127">-Id</span></span>
<span data-ttu-id="6058e-128">이 cmdlet이 가져오는 정책 할당에 대 한 정규화 된 리소스 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6058e-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="6058e-129">-IncludeDescendent</span></span>
<span data-ttu-id="6058e-130">상위 범위의 범위 및 하위 범위를 포함 하 여 지정 된 범위와 관련 된 모든 할당을 포함 하도록 반환 된 정책 할당 목록에 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="6058e-131">-이름</span><span class="sxs-lookup"><span data-stu-id="6058e-131">-Name</span></span>
<span data-ttu-id="6058e-132">이 cmdlet이 가져오는 정책 할당의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6058e-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="6058e-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="6058e-134">이 cmdlet이 가져오는 정책 할당의 정책 정의에 대 한 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6058e-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="6058e-135">-Pre</span></span>
<span data-ttu-id="6058e-136">이 cmdlet이 사용할 버전을 자동으로 결정 하는 경우 시험판 API 버전을 고려 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="6058e-137">-범위</span><span class="sxs-lookup"><span data-stu-id="6058e-137">-Scope</span></span>
<span data-ttu-id="6058e-138">이 cmdlet이 가져오는 할당에 대해 정책이 적용 되는 범위를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="6058e-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6058e-139">CommonParameters</span></span>
<span data-ttu-id="6058e-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6058e-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6058e-141">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6058e-141">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6058e-142">입력</span><span class="sxs-lookup"><span data-stu-id="6058e-142">INPUTS</span></span>

### <span data-ttu-id="6058e-143">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6058e-143">System.String</span></span>

### <span data-ttu-id="6058e-144">System.webserver 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6058e-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="6058e-145">출력</span><span class="sxs-lookup"><span data-stu-id="6058e-145">OUTPUTS</span></span>

### <span data-ttu-id="6058e-146">System.webserver. 자동. PSObject</span><span class="sxs-lookup"><span data-stu-id="6058e-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="6058e-147">상속자</span><span class="sxs-lookup"><span data-stu-id="6058e-147">NOTES</span></span>

## <span data-ttu-id="6058e-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6058e-148">RELATED LINKS</span></span>

[<span data-ttu-id="6058e-149">새로운 AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6058e-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="6058e-150">제거-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6058e-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="6058e-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="6058e-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


