---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 3edb92ae8c46ab67e0e22ee808e38dad7101bfdf
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101990206"
---
# <span data-ttu-id="40b57-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="40b57-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="40b57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="40b57-102">SYNOPSIS</span></span>
<span data-ttu-id="40b57-103">VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책 상태(세부 정보)를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="40b57-104">이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="40b57-105">구문</span><span class="sxs-lookup"><span data-stu-id="40b57-105">SYNTAX</span></span>

### <span data-ttu-id="40b57-106">VmScope(기본값)</span><span class="sxs-lookup"><span data-stu-id="40b57-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b57-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="40b57-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b57-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="40b57-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="40b57-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="40b57-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="40b57-110">설명</span><span class="sxs-lookup"><span data-stu-id="40b57-110">DESCRIPTION</span></span>
<span data-ttu-id="40b57-111">Get-AzVMGuestPolicyStatus cmdlet은 VM에 할당된 "게스트 구성"의 이니셔티브에 대한 게스트 구성 정책 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="40b57-112">이니셔티브는 정의 형식 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="40b57-113">이 cmdlet은 VM의 규정 준수 상태와 이니셔티브의 개별 정책에 대해 규정을 준수하지 않는 이유를 제공합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="40b57-114">예제</span><span class="sxs-lookup"><span data-stu-id="40b57-114">EXAMPLES</span></span>

### <span data-ttu-id="40b57-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="40b57-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="40b57-116">VM에 대한 모든 최신 게스트 구성 정책 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="40b57-117">상태는 "게스트 구성"형식의 모든 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="40b57-118">결과에 최신 상태가 포함되고 이전 기록 상태가 포함되어 있지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="40b57-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="40b57-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="40b57-120">이니셔티브 ID를 통해 최신 게스트 구성 정책 상태를 얻습니다. 상태는 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="40b57-121">결과에 생성된 이전 상태가 포함되어 있지 않습니다. 이니셔티브의 각 정책에 대한 최신 상태만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="40b57-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="40b57-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="40b57-123">이니셔티브 이름으로 최신 게스트 구성 정책 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="40b57-124">상태는 이니셔티브의 각 정책에 대한 VM의 준수 상태, 규정 준수 이유, 규정 준수 검사 시간, 규정 준수 확인을 위해 확인된 리소스 정보를 포함합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="40b57-125">결과에 생성된 이전 상태가 포함되어 있지 않습니다. 이니셔티브의 각 정책에 대한 최신 상태만 포함됩니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="40b57-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="40b57-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="40b57-127">ReportId를 통해 게스트 구성 정책 상태를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="40b57-128">ReportId는 initiativeId 또는 Initiative 이름으로 Get-AzVMGuestPolicyStatus 결과에서 찾을 수 있는 ReportId 속성입니다(다른 예제 참조).</span><span class="sxs-lookup"><span data-stu-id="40b57-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="40b57-129">매개 변수</span><span class="sxs-lookup"><span data-stu-id="40b57-129">PARAMETERS</span></span>

### <span data-ttu-id="40b57-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="40b57-130">-DefaultProfile</span></span>
<span data-ttu-id="40b57-131">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="40b57-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="40b57-132">-InitiativeId</span></span>
<span data-ttu-id="40b57-133">정의 형식이 이니셔티브 및 범주인 정책의 정의 ID는 게스트 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

```yaml
Type: System.String
Parameter Sets: InitiativeIdScope
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="40b57-134">-InitiativeName</span></span>
<span data-ttu-id="40b57-135">정의 형식이 이니셔티브 및 범주인 정책의 이름은 게스트 구성입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="40b57-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="40b57-136">-ReportId</span></span>
<span data-ttu-id="40b57-137">게스트 구성 정책 상태의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="40b57-138">정의 형식이 이니셔티브이고 범주가 게스트 구성인 정책은 상태를 얻기 위해 범위에 할당되어야 합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

```yaml
Type: System.String
Parameter Sets: ReportIdScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="40b57-139">-ResourceGroupName</span></span>
<span data-ttu-id="40b57-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-140">Resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="40b57-141">-VMName</span></span>
<span data-ttu-id="40b57-142">VM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-142">VM name.</span></span>

```yaml
Type: System.String
Parameter Sets: VmScope, InitiativeIdScope, InitiativeNameScope
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="40b57-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="40b57-143">CommonParameters</span></span>
<span data-ttu-id="40b57-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="40b57-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="40b57-145">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="40b57-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="40b57-146">입력</span><span class="sxs-lookup"><span data-stu-id="40b57-146">INPUTS</span></span>

### <span data-ttu-id="40b57-147">없음</span><span class="sxs-lookup"><span data-stu-id="40b57-147">None</span></span>
## <span data-ttu-id="40b57-148">출력</span><span class="sxs-lookup"><span data-stu-id="40b57-148">OUTPUTS</span></span>

### <span data-ttu-id="40b57-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span><span class="sxs-lookup"><span data-stu-id="40b57-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="40b57-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="40b57-150">NOTES</span></span>

## <span data-ttu-id="40b57-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="40b57-151">RELATED LINKS</span></span>
