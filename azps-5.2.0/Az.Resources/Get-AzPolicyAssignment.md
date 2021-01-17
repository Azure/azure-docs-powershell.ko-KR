---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ResourceManager.dll-Help.xml
Module Name: Az.Resources
ms.assetid: 2DBAF415-A039-479E-B3CA-E00FD5E476C9
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/get-azpolicyassignment
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Get-AzPolicyAssignment.md
ms.openlocfilehash: 4d5b230b741deec10daa44dab7e4faa44ac96b61
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98340197"
---
# <span data-ttu-id="43fb0-101">Get-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43fb0-101">Get-AzPolicyAssignment</span></span>

## <span data-ttu-id="43fb0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="43fb0-102">SYNOPSIS</span></span>
<span data-ttu-id="43fb0-103">정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-103">Gets policy assignments.</span></span>

## <span data-ttu-id="43fb0-104">구문</span><span class="sxs-lookup"><span data-stu-id="43fb0-104">SYNTAX</span></span>

### <span data-ttu-id="43fb0-105">DefaultParameterSet(기본값)</span><span class="sxs-lookup"><span data-stu-id="43fb0-105">DefaultParameterSet (Default)</span></span>
```
Get-AzPolicyAssignment [-ApiVersion <String>] [-Pre] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="43fb0-106">NameParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fb0-106">NameParameterSet</span></span>
```
Get-AzPolicyAssignment [-Name <String>] [-Scope <String>] [-PolicyDefinitionId <String>] [-ApiVersion <String>]
 [-Pre] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43fb0-107">IncludeDescendentParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fb0-107">IncludeDescendentParameterSet</span></span>
```
Get-AzPolicyAssignment [-Scope <String>] [-IncludeDescendent] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="43fb0-108">IdParameterSet</span><span class="sxs-lookup"><span data-stu-id="43fb0-108">IdParameterSet</span></span>
```
Get-AzPolicyAssignment -Id <String> [-PolicyDefinitionId <String>] [-ApiVersion <String>] [-Pre]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="43fb0-109">설명</span><span class="sxs-lookup"><span data-stu-id="43fb0-109">DESCRIPTION</span></span>
<span data-ttu-id="43fb0-110">**Get-AzPolicyAssignment** cmdlet은 모든 정책 할당 또는 특정 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-110">The **Get-AzPolicyAssignment** cmdlet gets all policy assignments or particular assignments.</span></span>
<span data-ttu-id="43fb0-111">이름 및 범위 또는 ID로 얻을 정책 할당을 식별합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-111">Identify a policy assignment to get by name and scope or by ID.</span></span>

## <span data-ttu-id="43fb0-112">예제</span><span class="sxs-lookup"><span data-stu-id="43fb0-112">EXAMPLES</span></span>

### <span data-ttu-id="43fb0-113">예제 1: 모든 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-113">Example 1: Get all policy assignments</span></span>
```
PS C:\> Get-AzPolicyAssignment
```

<span data-ttu-id="43fb0-114">이 명령은 모든 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-114">This command gets all the policy assignments.</span></span>

### <span data-ttu-id="43fb0-115">예제 2: 특정 정책 할당을 얻게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-115">Example 2: Get a specific policy assignment</span></span>
```
PS C:\> $ResourceGroup = Get-AzResourceGroup -Name 'ResourceGroup11'
PS C:\> Get-AzPolicyAssignment -Name 'PolicyAssignment07' -Scope $ResourceGroup.ResourceId
```

<span data-ttu-id="43fb0-116">첫 번째 명령은 Get-AzResourceGroup cmdlet을 사용하여 ResourceGroup11이라는 리소스 그룹을 $ResourceGroup 변수에 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-116">The first command gets a resource group named ResourceGroup11 by using the Get-AzResourceGroup cmdlet and stores it in the $ResourceGroup variable.</span></span>
<span data-ttu-id="43fb0-117">두 번째 명령은 해당 리소스의 **ResourceId** 속성이 식별하는 범위에 대한 PolicyAssignment07이라는 $ResourceGroup 할당합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-117">The second command gets the policy assignment named PolicyAssignment07 for the scope that the **ResourceId** property of $ResourceGroup identifies.</span></span>

### <span data-ttu-id="43fb0-118">예제 3: 관리 그룹에 할당된 모든 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-118">Example 3: Get all policy assignments assigned to a management group</span></span>
```
PS C:\> $mgId = 'myManagementGroup'
PS C:\> Get-AzPolicyAssignment -Scope '/providers/Microsoft.Management/managementgroups/$mgId'
```

<span data-ttu-id="43fb0-119">첫 번째 명령은 쿼리할 관리 그룹의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-119">The first command specifies the ID of the management group to query.</span></span>
<span data-ttu-id="43fb0-120">두 번째 명령은 ID가 'myManagementGroup'인 관리 그룹에 할당된 모든 정책 할당을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-120">The second command gets all of the policy assignments that are assigned to the management group with ID 'myManagementGroup'.</span></span>

## <span data-ttu-id="43fb0-121">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="43fb0-121">PARAMETERS</span></span>

### <span data-ttu-id="43fb0-122">-ApiVersion</span><span class="sxs-lookup"><span data-stu-id="43fb0-122">-ApiVersion</span></span>
<span data-ttu-id="43fb0-123">사용할 리소스 공급자 API의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-123">Specifies the version of the resource provider API to use.</span></span>
<span data-ttu-id="43fb0-124">버전을 지정하지 않으면 이 cmdlet은 사용 가능한 최신 버전을 사용하게 됩니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-124">If you do not specify a version, this cmdlet uses the latest available version.</span></span>

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

### <span data-ttu-id="43fb0-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="43fb0-125">-DefaultProfile</span></span>
<span data-ttu-id="43fb0-126">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="43fb0-126">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="43fb0-127">-Id</span><span class="sxs-lookup"><span data-stu-id="43fb0-127">-Id</span></span>
<span data-ttu-id="43fb0-128">이 cmdlet에서 얻을 정책 할당에 대한 정식 리소스 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-128">Specifies the fully qualified resource ID for the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43fb0-129">-IncludeDescendent</span><span class="sxs-lookup"><span data-stu-id="43fb0-129">-IncludeDescendent</span></span>
<span data-ttu-id="43fb0-130">반환된 정책 할당 목록에 조상 범위의 할당과 내하원 범위의 할당을 포함하여 주어진 범위와 관련된 모든 할당을 포함하게 합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-130">Causes the list of returned policy assignments to include all assignments related to the given scope, including those from ancestor scopes and those from descendent scopes.</span></span>

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

### <span data-ttu-id="43fb0-131">-Name</span><span class="sxs-lookup"><span data-stu-id="43fb0-131">-Name</span></span>
<span data-ttu-id="43fb0-132">이 cmdlet이 얻을 정책 할당의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-132">Specifies the name of the policy assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43fb0-133">-PolicyDefinitionId</span><span class="sxs-lookup"><span data-stu-id="43fb0-133">-PolicyDefinitionId</span></span>
<span data-ttu-id="43fb0-134">이 cmdlet에서 얻을 정책 할당의 정책 정의 ID를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-134">Specifies the ID of the policy definition of the policy assignments that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43fb0-135">-Pre</span><span class="sxs-lookup"><span data-stu-id="43fb0-135">-Pre</span></span>
<span data-ttu-id="43fb0-136">이 cmdlet은 사용할 버전을 자동으로 결정할 때 릴리스 전 API 버전을 고려합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-136">Indicates that this cmdlet considers pre-release API versions when it automatically determines which version to use.</span></span>

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

### <span data-ttu-id="43fb0-137">-Scope</span><span class="sxs-lookup"><span data-stu-id="43fb0-137">-Scope</span></span>
<span data-ttu-id="43fb0-138">이 cmdlet이 얻을 할당에 대해 정책이 적용되는 범위를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-138">Specifies the scope at which the policy is applied for the assignment that this cmdlet gets.</span></span>

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

### <span data-ttu-id="43fb0-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="43fb0-139">CommonParameters</span></span>
<span data-ttu-id="43fb0-140">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="43fb0-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="43fb0-141">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="43fb0-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="43fb0-142">입력</span><span class="sxs-lookup"><span data-stu-id="43fb0-142">INPUTS</span></span>

### <span data-ttu-id="43fb0-143">System.String</span><span class="sxs-lookup"><span data-stu-id="43fb0-143">System.String</span></span>

### <span data-ttu-id="43fb0-144">System.Management.Automation.SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="43fb0-144">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="43fb0-145">출력</span><span class="sxs-lookup"><span data-stu-id="43fb0-145">OUTPUTS</span></span>

### <span data-ttu-id="43fb0-146">System.Management.Automation.PSObject</span><span class="sxs-lookup"><span data-stu-id="43fb0-146">System.Management.Automation.PSObject</span></span>

## <span data-ttu-id="43fb0-147">참고 사항</span><span class="sxs-lookup"><span data-stu-id="43fb0-147">NOTES</span></span>

## <span data-ttu-id="43fb0-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="43fb0-148">RELATED LINKS</span></span>

[<span data-ttu-id="43fb0-149">New-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43fb0-149">New-AzPolicyAssignment</span></span>](./New-AzPolicyAssignment.md)

[<span data-ttu-id="43fb0-150">Remove-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43fb0-150">Remove-AzPolicyAssignment</span></span>](./Remove-AzPolicyAssignment.md)

[<span data-ttu-id="43fb0-151">Set-AzPolicyAssignment</span><span class="sxs-lookup"><span data-stu-id="43fb0-151">Set-AzPolicyAssignment</span></span>](./Set-AzPolicyAssignment.md)


