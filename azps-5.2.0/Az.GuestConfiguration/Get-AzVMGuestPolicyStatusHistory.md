---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-azvmguestpolicystatushistory
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatusHistory.md
ms.openlocfilehash: 929bc417cf4b84800635b85e7f503972509aa7fc
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98336002"
---
# <span data-ttu-id="c9402-101">Get-AzVMGuestPolicyStatusHistory</span><span class="sxs-lookup"><span data-stu-id="c9402-101">Get-AzVMGuestPolicyStatusHistory</span></span>

## <span data-ttu-id="c9402-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c9402-102">SYNOPSIS</span></span>
<span data-ttu-id="c9402-103">VM에 할당된 "게스트 구성" 유형의 이니셔티브에 대한 게스트 구성 정책 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-103">Gets guest configuration policy compliance status history for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="c9402-104">이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="c9402-105">구문</span><span class="sxs-lookup"><span data-stu-id="c9402-105">SYNTAX</span></span>

### <span data-ttu-id="c9402-106">InitiativeNameScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="c9402-106">InitiativeNameScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c9402-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="c9402-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatusHistory [-ResourceGroupName] <String> [-VMName] <String> [[-InitiativeId] <String>]
 [-ShowOnlyChange] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c9402-108">설명</span><span class="sxs-lookup"><span data-stu-id="c9402-108">DESCRIPTION</span></span>
<span data-ttu-id="c9402-109">Get-AzVMGuestPolicyStatusHistory cmdlet은 VM에 할당된 "게스트 구성" 유형의 이니셔티브에 대한 게스트 구성 정책의 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-109">The Get-AzVMGuestPolicyStatusHistory cmdlet gets compliance status history of guest configuration policies for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="c9402-110">이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-110">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="c9402-111">Get-AzVMGuestPolicyStatus cmdlet의 출력에서 찾을 수 있는 ReportId를 사용하여 단일 준수 상태에 대한 세부 정보를 Get-AzVMGuestPolicyStatusHistory cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-111">Use Get-AzVMGuestPolicyStatus cmdlet to get details of a single compliance status using ReportId that can be found in output of Get-AzVMGuestPolicyStatusHistory cmdlet.</span></span>

## <span data-ttu-id="c9402-112">예제</span><span class="sxs-lookup"><span data-stu-id="c9402-112">EXAMPLES</span></span>

### <span data-ttu-id="c9402-113">예제 1</span><span class="sxs-lookup"><span data-stu-id="c9402-113">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af" -ShowOnlyChange
```

<span data-ttu-id="c9402-114">이니셔티브 ID를 통해 준수 상태 기록을 얻습니다. ShowOnlyChange 스위치에는 기록 상태 변경 내용만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-114">Gets compliance status history by initiative Id. ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="c9402-115">두 규정 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-115">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="c9402-116">예제 2</span><span class="sxs-lookup"><span data-stu-id="c9402-116">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17" -ShowOnlyChange
```

<span data-ttu-id="c9402-117">이니셔티브 이름으로 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-117">Gets compliance status history by initiative name.</span></span>
<span data-ttu-id="c9402-118">ShowOnlyChange 스위치에는 기록 상태 변경 내용만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-118">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="c9402-119">두 규정 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-119">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="c9402-120">예제 3</span><span class="sxs-lookup"><span data-stu-id="c9402-120">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -ShowOnlyChange
```

<span data-ttu-id="c9402-121">VM에 할당된 모든 게스트 구성 정책에 대한 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-121">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>
<span data-ttu-id="c9402-122">ShowOnlyChange 스위치에는 기록 상태 변경 내용만 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-122">ShowOnlyChange switch shows only historical status changes.</span></span>
<span data-ttu-id="c9402-123">두 규정 준수 검사 간에 변경되지 않은 상태를 건너뜁합니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-123">Skips statuses that have not changed between two compliance checks.</span></span>

### <span data-ttu-id="c9402-124">예제 4</span><span class="sxs-lookup"><span data-stu-id="c9402-124">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="c9402-125">이니셔티브 ID를 통해 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-125">Gets compliance status history by initiative Id.</span></span>

### <span data-ttu-id="c9402-126">예제 5</span><span class="sxs-lookup"><span data-stu-id="c9402-126">Example 5</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="c9402-127">이니셔티브 이름으로 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-127">Gets compliance status history by initiative name.</span></span>

### <span data-ttu-id="c9402-128">예제 6</span><span class="sxs-lookup"><span data-stu-id="c9402-128">Example 6</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```
<span data-ttu-id="c9402-129">VM에 할당된 모든 게스트 구성 정책에 대한 규정 준수 상태 기록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-129">Gets compliance status history for all guest configuration policies assigned to the VM.</span></span>

### <span data-ttu-id="c9402-130">예제 7</span><span class="sxs-lookup"><span data-stu-id="c9402-130">Example 7</span></span>
```powershell
PS C:\>$x = Get-AzVMGuestPolicyStatusHistory -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
PS C:\>$x[10].ReportId
/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac
PS C:\> Get-AzVMGuestPolicyStatus -ReportId $x[10].ReportId
```

<span data-ttu-id="c9402-131">ReportId를 통해 게스트 구성 정책 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-131">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="c9402-132">ReportId는 Get-AzVMGuestPolicyStatusHistory의 결과에서 찾을 수 있는 ReportId 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-132">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatusHistory.</span></span> <span data-ttu-id="c9402-133">(다른 예제 참조)</span><span class="sxs-lookup"><span data-stu-id="c9402-133">(please refer other examples)</span></span>

## <span data-ttu-id="c9402-134">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="c9402-134">PARAMETERS</span></span>

### <span data-ttu-id="c9402-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c9402-135">-DefaultProfile</span></span>
<span data-ttu-id="c9402-136">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-136">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c9402-137">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="c9402-137">-InitiativeId</span></span>
<span data-ttu-id="c9402-138">정의 형식이 이니셔티브 및 범주인 정책의 정의 ID는 게스트 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-138">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9402-139">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="c9402-139">-InitiativeName</span></span>
<span data-ttu-id="c9402-140">정의 형식이 이니셔티브 및 범주가 게스트 구성인 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-140">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeNameScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9402-141">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c9402-141">-ResourceGroupName</span></span>
<span data-ttu-id="c9402-142">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-142">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9402-143">-ShowOnlyChange</span><span class="sxs-lookup"><span data-stu-id="c9402-143">-ShowOnlyChange</span></span>
<span data-ttu-id="c9402-144">게스트 구성 정책에 대한 기록 상태 변경 내용만 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-144">Shows historical status changes only for guest configuration policies.</span></span>
<span data-ttu-id="c9402-145">두 준수 상태 감사 실행 간에 변경되지 않은 상태를 건너뜁.</span><span class="sxs-lookup"><span data-stu-id="c9402-145">Skips statuses that have not changed between two compliance status audit runs.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9402-146">-VMName</span><span class="sxs-lookup"><span data-stu-id="c9402-146">-VMName</span></span>
<span data-ttu-id="c9402-147">VM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-147">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c9402-148">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c9402-148">CommonParameters</span></span>
<span data-ttu-id="c9402-149">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c9402-149">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c9402-150">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="c9402-150">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c9402-151">입력</span><span class="sxs-lookup"><span data-stu-id="c9402-151">INPUTS</span></span>

### <span data-ttu-id="c9402-152">없음</span><span class="sxs-lookup"><span data-stu-id="c9402-152">None</span></span>
## <span data-ttu-id="c9402-153">출력</span><span class="sxs-lookup"><span data-stu-id="c9402-153">OUTPUTS</span></span>

### <span data-ttu-id="c9402-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span><span class="sxs-lookup"><span data-stu-id="c9402-154">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatus</span></span>
## <span data-ttu-id="c9402-155">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c9402-155">NOTES</span></span>

## <span data-ttu-id="c9402-156">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c9402-156">RELATED LINKS</span></span>
