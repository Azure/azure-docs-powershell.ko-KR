---
external help file: Microsoft.Azure.PowerShell.Cmdlets.GuestConfiguration.dll-Help.xml
Module Name: Az.GuestConfiguration
online version: https://docs.microsoft.com/en-us/powershell/module/az.guestconfiguration/get-AzVMGuestPolicyStatus
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/GuestConfiguration/GuestConfiguration/help/Get-AzVMGuestPolicyStatus.md
ms.openlocfilehash: 49148f1c62b71436e48b2b92a4591a7cdb36cccf
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94215402"
---
# <span data-ttu-id="adfb2-101">Get-AzVMGuestPolicyStatus</span><span class="sxs-lookup"><span data-stu-id="adfb2-101">Get-AzVMGuestPolicyStatus</span></span>

## <span data-ttu-id="adfb2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="adfb2-102">SYNOPSIS</span></span>
<span data-ttu-id="adfb2-103">VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책 상태 (상세)를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-103">Gets guest configuration policy statuses (detailed) for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="adfb2-104">이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-104">An initiative is a policy of definition type "Initiative".</span></span>

## <span data-ttu-id="adfb2-105">구문과</span><span class="sxs-lookup"><span data-stu-id="adfb2-105">SYNTAX</span></span>

### <span data-ttu-id="adfb2-106">VmScope (기본값)</span><span class="sxs-lookup"><span data-stu-id="adfb2-106">VmScope (Default)</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfb2-107">InitiativeIdScope</span><span class="sxs-lookup"><span data-stu-id="adfb2-107">InitiativeIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfb2-108">InitiativeNameScope</span><span class="sxs-lookup"><span data-stu-id="adfb2-108">InitiativeNameScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ResourceGroupName] <String> [-VMName] <String> [-InitiativeName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="adfb2-109">ReportIdScope</span><span class="sxs-lookup"><span data-stu-id="adfb2-109">ReportIdScope</span></span>
```
Get-AzVMGuestPolicyStatus [-ReportId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="adfb2-110">설명은</span><span class="sxs-lookup"><span data-stu-id="adfb2-110">DESCRIPTION</span></span>
<span data-ttu-id="adfb2-111">Get-AzVMGuestPolicyStatus cmdlet는 VM에 할당 된 "게스트 구성" 유형의 이니셔티브에 대 한 게스트 구성 정책 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-111">The Get-AzVMGuestPolicyStatus cmdlet gets guest configuration policy statuses for an initiative of type "Guest Configuration" that is assigned to a VM.</span></span>
<span data-ttu-id="adfb2-112">이니셔티브는 정의 유형 "이니셔티브"의 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-112">An initiative is a policy of definition type "Initiative".</span></span>
<span data-ttu-id="adfb2-113">이 cmdlet은 VM의 준수 상태와 이니셔티브의 개별 정책에 대해 비규격 이유가 아닌 이유를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-113">This cmdlet gets compliance statuses of the VM and reasons why it is non-compliant for the individual policies in the initiative.</span></span>

## <span data-ttu-id="adfb2-114">예제의</span><span class="sxs-lookup"><span data-stu-id="adfb2-114">EXAMPLES</span></span>

### <span data-ttu-id="adfb2-115">예제 1</span><span class="sxs-lookup"><span data-stu-id="adfb2-115">Example 1</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName"
```

<span data-ttu-id="adfb2-116">VM에 대 한 최신 게스트 구성 정책 상태를 모두 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-116">Get all latest guest configuration policy statuses for a VM.</span></span>
<span data-ttu-id="adfb2-117">상태에는 "게스트 구성" 형식의 모든 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-117">The status includes compliance status of the VM for each policy in all initiatives of type "Guest Configuration", compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="adfb2-118">결과에는 최신 상태가 포함 되며 이전 기록 상태가 포함 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-118">The results include latest statuses, does not include previous historical statuses.</span></span>

### <span data-ttu-id="adfb2-119">예제 2</span><span class="sxs-lookup"><span data-stu-id="adfb2-119">Example 2</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeId "/providers/Microsoft.Authorization/policySetDefinitions/3fa7cbf5-c0a4-4a59-85a5-cca4d996d5af"
```

<span data-ttu-id="adfb2-120">이니셔티브 Id를 기준으로 최신 게스트 구성 정책 상태를 가져옵니다. 상태에는 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-120">Get the latest guest configuration policy statuses by initiative Id. The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="adfb2-121">결과에는 생성 된 이전 상태가 포함 되지 않으며, 여기에는 이니셔티브의 각 정책에 대 한 최신 상태만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-121">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="adfb2-122">예제 3</span><span class="sxs-lookup"><span data-stu-id="adfb2-122">Example 3</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ResourceGroupName "MyResourceGroupName" -VMName "MyVMName" -InitiativeName "b5a822e0-ba98-4e54-9278-5d9833aa9b17"
```

<span data-ttu-id="adfb2-123">이니셔티브 이름으로 최신 게스트 구성 정책 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-123">Get the latest guest configuration policy statuses by initiative name.</span></span>
<span data-ttu-id="adfb2-124">상태에는 이니셔티브의 각 정책에 대 한 VM의 준수 상태, 준수 이유, 준수 검사 시간, 준수 여부를 확인 한 리소스 정보 등이 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-124">The status includes compliance status of the VM for each policy in the initiative, compliance reasons, time of the compliance check, resource information which was checked for compliance.</span></span>
<span data-ttu-id="adfb2-125">결과에는 생성 된 이전 상태가 포함 되지 않으며, 여기에는 이니셔티브의 각 정책에 대 한 최신 상태만 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-125">The results does not include previous statuses generated, it just includes latest status for each policy in the initiative.</span></span>

### <span data-ttu-id="adfb2-126">예제 4</span><span class="sxs-lookup"><span data-stu-id="adfb2-126">Example 4</span></span>
```powershell
PS C:\> Get-AzVMGuestPolicyStatus -ReportId "/subscriptions/4e6c6ed2-0bf6-41d7-9d21-a452c2cc7920/resourceGroups/MyResourceGroupName/providers/Microsoft.Compute/virtualMachines/MyVMName/providers/Microsoft.GuestConfiguration/guestConfigurationAssignments/MaximumPasswordAge/reports/c271f845-2c0a-4456-a441-e48fc332d0ac"
```

<span data-ttu-id="adfb2-127">ReportId를 기준으로 게스트 구성 정책 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-127">Get guest configuration policy status by ReportId.</span></span>
<span data-ttu-id="adfb2-128">ReportId는 initiativeId 또는 이니셔티브 이름으로 Get-AzVMGuestPolicyStatus 결과에서 찾을 수 있는 ReportId 속성으로, 다른 예를 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="adfb2-128">The ReportId is the ReportId property that can be found in the results of Get-AzVMGuestPolicyStatus by initiativeId or Initiative name (please refer other examples)</span></span>

## <span data-ttu-id="adfb2-129">변수</span><span class="sxs-lookup"><span data-stu-id="adfb2-129">PARAMETERS</span></span>

### <span data-ttu-id="adfb2-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="adfb2-130">-DefaultProfile</span></span>
<span data-ttu-id="adfb2-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="adfb2-132">-InitiativeId</span><span class="sxs-lookup"><span data-stu-id="adfb2-132">-InitiativeId</span></span>
<span data-ttu-id="adfb2-133">정의 형식이 이니셔티브이 고 범주가 게스트 구성 인 정책의 정의 Id</span><span class="sxs-lookup"><span data-stu-id="adfb2-133">Definition Id of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="adfb2-134">-InitiativeName</span><span class="sxs-lookup"><span data-stu-id="adfb2-134">-InitiativeName</span></span>
<span data-ttu-id="adfb2-135">정의 형식이 이니셔티브이 고 범주가 게스트 구성 인 정책의 이름</span><span class="sxs-lookup"><span data-stu-id="adfb2-135">Name of a policy where definition type is Initiative and category is Guest Configuration</span></span>

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

### <span data-ttu-id="adfb2-136">-ReportId</span><span class="sxs-lookup"><span data-stu-id="adfb2-136">-ReportId</span></span>
<span data-ttu-id="adfb2-137">게스트 구성 정책 상태의 Id입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-137">Id of a Guest Configuration policy status.</span></span>
<span data-ttu-id="adfb2-138">정의 형식이 이니셔티브이 고 category는 상태를 가져오려면 범위에 게스트 구성을 할당 해야 하는 정책입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-138">A policy where definition type is Initiative and category is Guest Configuration must be assigned to a scope to get statuses.</span></span>

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

### <span data-ttu-id="adfb2-139">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="adfb2-139">-ResourceGroupName</span></span>
<span data-ttu-id="adfb2-140">리소스 그룹 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-140">Resource group name.</span></span>

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

### <span data-ttu-id="adfb2-141">-VMName</span><span class="sxs-lookup"><span data-stu-id="adfb2-141">-VMName</span></span>
<span data-ttu-id="adfb2-142">VM 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-142">VM name.</span></span>

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

### <span data-ttu-id="adfb2-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="adfb2-143">CommonParameters</span></span>
<span data-ttu-id="adfb2-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="adfb2-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="adfb2-145">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="adfb2-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="adfb2-146">입력</span><span class="sxs-lookup"><span data-stu-id="adfb2-146">INPUTS</span></span>

### <span data-ttu-id="adfb2-147">않아야</span><span class="sxs-lookup"><span data-stu-id="adfb2-147">None</span></span>
## <span data-ttu-id="adfb2-148">출력</span><span class="sxs-lookup"><span data-stu-id="adfb2-148">OUTPUTS</span></span>

### <span data-ttu-id="adfb2-149">GuestConfiguration. PolicyStatusDetailed.</span><span class="sxs-lookup"><span data-stu-id="adfb2-149">Microsoft.Azure.Commands.GuestConfiguration.Models.PolicyStatusDetailed</span></span>
## <span data-ttu-id="adfb2-150">상속자</span><span class="sxs-lookup"><span data-stu-id="adfb2-150">NOTES</span></span>

## <span data-ttu-id="adfb2-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="adfb2-151">RELATED LINKS</span></span>
