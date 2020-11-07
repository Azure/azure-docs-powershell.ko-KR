---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/close-azsalert
schema: 2.0.0
ms.openlocfilehash: 885ffca453cd7a13e9ec137da89a402375eeec55
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876049"
---
# <span data-ttu-id="05ba7-101">Close-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="05ba7-101">Close-AzsAlert</span></span>

## <span data-ttu-id="05ba7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="05ba7-102">SYNOPSIS</span></span>
<span data-ttu-id="05ba7-103">지정 된 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-103">Closes the given alert.</span></span>

## <span data-ttu-id="05ba7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="05ba7-104">SYNTAX</span></span>

### <span data-ttu-id="05ba7-105">CloseExpanded 됨 (기본값)</span><span class="sxs-lookup"><span data-stu-id="05ba7-105">CloseExpanded (Default)</span></span>
```
Close-AzsAlert -Name <String> -User <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String>] [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>]
 [-ClosedTimestamp <String>] [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>]
 [-FaultTypeId <String>] [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>]
 [-ImpactedResourceId <String>] [-LastUpdatedTimestamp <String>] [-Location1 <String>]
 [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>] [-ResourceRegistrationId <String>]
 [-Severity <String>] [-State <String>] [-Tag <Hashtable>] [-Title <String>] [-DefaultProfile <PSObject>]
 [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05ba7-106">닫았다가</span><span class="sxs-lookup"><span data-stu-id="05ba7-106">Close</span></span>
```
Close-AzsAlert -Name <String> -User <String> -Alert <IAlert> [-Location <String>]
 [-ResourceGroupName <String>] [-SubscriptionId <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="05ba7-107">CloseViaIdentity</span><span class="sxs-lookup"><span data-stu-id="05ba7-107">CloseViaIdentity</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> -Alert <IAlert>
 [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="05ba7-108">CloseViaIdentityExpanded</span><span class="sxs-lookup"><span data-stu-id="05ba7-108">CloseViaIdentityExpanded</span></span>
```
Close-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> -User <String> [-Location <String>]
 [-AlertId <String>] [-AlertProperty <Hashtable>] [-ClosedByUserAlias <String>] [-ClosedTimestamp <String>]
 [-CreatedTimestamp <String>] [-Description <IDictionary[]>] [-FaultId <String>] [-FaultTypeId <String>]
 [-HasValidRemediationAction] [-ImpactedResourceDisplayName <String>] [-ImpactedResourceId <String>]
 [-LastUpdatedTimestamp <String>] [-Remediation <IDictionary[]>] [-ResourceProviderRegistrationId <String>]
 [-ResourceRegistrationId <String>] [-Severity <String>] [-State <String>] [-Tag <Hashtable>]
 [-Title <String>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="05ba7-109">설명은</span><span class="sxs-lookup"><span data-stu-id="05ba7-109">DESCRIPTION</span></span>
<span data-ttu-id="05ba7-110">지정 된 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-110">Closes the given alert.</span></span>

## <span data-ttu-id="05ba7-111">예제의</span><span class="sxs-lookup"><span data-stu-id="05ba7-111">EXAMPLES</span></span>

### <span data-ttu-id="05ba7-112">예제 1:</span><span class="sxs-lookup"><span data-stu-id="05ba7-112">Example 1:</span></span>
```powershell
PS C:\> Close-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="05ba7-113">이름으로 알림을 종료 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-113">Close an alert by Name.</span></span>

### <span data-ttu-id="05ba7-114">예제 2:</span><span class="sxs-lookup"><span data-stu-id="05ba7-114">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Close-AzsAlert
```

<span data-ttu-id="05ba7-115">파이핑을 통해 경고를 닫습니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-115">Close an alert through piping.</span></span>

## <span data-ttu-id="05ba7-116">변수</span><span class="sxs-lookup"><span data-stu-id="05ba7-116">PARAMETERS</span></span>

### <span data-ttu-id="05ba7-117">-경고</span><span class="sxs-lookup"><span data-stu-id="05ba7-117">-Alert</span></span>
<span data-ttu-id="05ba7-118">이 개체는 알림 리소스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-118">This object represents an alert resource.</span></span>
<span data-ttu-id="05ba7-119">생성 하려면 경고 속성 및 해시 테이블 만들기에 대 한 참고 섹션을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05ba7-119">To construct, see NOTES section for ALERT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert
Parameter Sets: Close, CloseViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-120">-AlertId</span><span class="sxs-lookup"><span data-stu-id="05ba7-120">-AlertId</span></span>
<span data-ttu-id="05ba7-121">경고의 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-121">Gets or sets the ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-122">-AlertProperty</span><span class="sxs-lookup"><span data-stu-id="05ba7-122">-AlertProperty</span></span>
<span data-ttu-id="05ba7-123">경고의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-123">Properties of the alert.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-124">-ClosedByUserAlias</span><span class="sxs-lookup"><span data-stu-id="05ba7-124">-ClosedByUserAlias</span></span>
<span data-ttu-id="05ba7-125">알림을 닫은 사용자 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-125">User alias who closed the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-126">-ClosedTimestamp</span><span class="sxs-lookup"><span data-stu-id="05ba7-126">-ClosedTimestamp</span></span>
<span data-ttu-id="05ba7-127">알림을 닫은 시간에 대 한 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-127">Timestamp when the alert was closed.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-128">-CreatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="05ba7-128">-CreatedTimestamp</span></span>
<span data-ttu-id="05ba7-129">경고가 생성 된 시점의 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-129">Timestamp when the alert was created.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-130">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="05ba7-130">-DefaultProfile</span></span>
<span data-ttu-id="05ba7-131">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-131">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-132">-설명</span><span class="sxs-lookup"><span data-stu-id="05ba7-132">-Description</span></span>
<span data-ttu-id="05ba7-133">경고에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-133">Description of the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-134">-FaultId</span><span class="sxs-lookup"><span data-stu-id="05ba7-134">-FaultId</span></span>
<span data-ttu-id="05ba7-135">알림의 오류 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-135">Gets or sets the fault ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-136">-FaultTypeId</span><span class="sxs-lookup"><span data-stu-id="05ba7-136">-FaultTypeId</span></span>
<span data-ttu-id="05ba7-137">알림의 오류 유형 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-137">Gets or sets the fault type ID of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-138">-HasValidRemediationAction</span><span class="sxs-lookup"><span data-stu-id="05ba7-138">-HasValidRemediationAction</span></span>
<span data-ttu-id="05ba7-139">알림을 재구성 가능 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-139">Indicates if the alert can be remediated.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-140">-ImpactedResourceDisplayName</span><span class="sxs-lookup"><span data-stu-id="05ba7-140">-ImpactedResourceDisplayName</span></span>
<span data-ttu-id="05ba7-141">영향을 받는 항목의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-141">Display name for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-142">-ImpactedResourceId</span><span class="sxs-lookup"><span data-stu-id="05ba7-142">-ImpactedResourceId</span></span>
<span data-ttu-id="05ba7-143">영향을 받는 항목의 리소스 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-143">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-144">-InputObject</span><span class="sxs-lookup"><span data-stu-id="05ba7-144">-InputObject</span></span>
<span data-ttu-id="05ba7-145">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-145">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: CloseViaIdentity, CloseViaIdentityExpanded
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-146">-LastUpdatedTimestamp</span><span class="sxs-lookup"><span data-stu-id="05ba7-146">-LastUpdatedTimestamp</span></span>
<span data-ttu-id="05ba7-147">경고가 마지막으로 업데이트 된 시간에 대 한 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-147">Timestamp when the alert was last updated.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-148">-위치</span><span class="sxs-lookup"><span data-stu-id="05ba7-148">-Location</span></span>
<span data-ttu-id="05ba7-149">지역 이름</span><span class="sxs-lookup"><span data-stu-id="05ba7-149">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-150">-Location1</span><span class="sxs-lookup"><span data-stu-id="05ba7-150">-Location1</span></span>
<span data-ttu-id="05ba7-151">자원이 거주 하는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="05ba7-151">The Azure Region where the resource lives</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-152">-이름</span><span class="sxs-lookup"><span data-stu-id="05ba7-152">-Name</span></span>
<span data-ttu-id="05ba7-153">경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-153">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-154">-업데이트 관리</span><span class="sxs-lookup"><span data-stu-id="05ba7-154">-Remediation</span></span>
<span data-ttu-id="05ba7-155">경고에 대 한 관리자의 쉬운 재구성 지침을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-155">Gets or sets the admin friendly remediation instructions for the alert.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IDictionary[]
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-156">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="05ba7-156">-ResourceGroupName</span></span>
<span data-ttu-id="05ba7-157">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-157">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-158">-ResourceProviderRegistrationId</span><span class="sxs-lookup"><span data-stu-id="05ba7-158">-ResourceProviderRegistrationId</span></span>
<span data-ttu-id="05ba7-159">알림이 속한 서비스의 등록 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-159">Gets or sets the registration ID of the service the alert belongs to.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-160">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="05ba7-160">-ResourceRegistrationId</span></span>
<span data-ttu-id="05ba7-161">알림과 연결 된 리소스의 등록 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-161">Gets or sets the registration ID of the resource associated with the alert.</span></span>
<span data-ttu-id="05ba7-162">경고가 리소스와 연결 되어 있지 않은 경우 리소스 등록 ID는 null입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-162">If the alert is not associated with a resource, the resource registration ID is null.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-163">-심각도</span><span class="sxs-lookup"><span data-stu-id="05ba7-163">-Severity</span></span>
<span data-ttu-id="05ba7-164">경고의 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-164">Severity of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-165">-상태</span><span class="sxs-lookup"><span data-stu-id="05ba7-165">-State</span></span>
<span data-ttu-id="05ba7-166">경고의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-166">State of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-167">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="05ba7-167">-SubscriptionId</span></span>
<span data-ttu-id="05ba7-168">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-168">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="05ba7-169">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-169">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Close, CloseExpanded
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-170">태그</span><span class="sxs-lookup"><span data-stu-id="05ba7-170">-Tag</span></span>
<span data-ttu-id="05ba7-171">리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="05ba7-171">Resource tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-172">-Title</span><span class="sxs-lookup"><span data-stu-id="05ba7-172">-Title</span></span>
<span data-ttu-id="05ba7-173">영향을 받는 항목의 리소스 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-173">Gets or sets the Resource ID for the impacted item.</span></span>

```yaml
Type: System.String
Parameter Sets: CloseExpanded, CloseViaIdentityExpanded
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-174">-사용자</span><span class="sxs-lookup"><span data-stu-id="05ba7-174">-User</span></span>
<span data-ttu-id="05ba7-175">작업을 수행 하는 데 사용 되는 사용자 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-175">The username used to perform the operation.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-176">-확인</span><span class="sxs-lookup"><span data-stu-id="05ba7-176">-Confirm</span></span>
<span data-ttu-id="05ba7-177">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-177">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-178">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="05ba7-178">-WhatIf</span></span>
<span data-ttu-id="05ba7-179">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-179">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="05ba7-180">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-180">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="05ba7-181">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="05ba7-181">CommonParameters</span></span>
<span data-ttu-id="05ba7-182">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-182">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="05ba7-183">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="05ba7-183">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="05ba7-184">입력</span><span class="sxs-lookup"><span data-stu-id="05ba7-184">INPUTS</span></span>

### <span data-ttu-id="05ba7-185">InfrastructureInsightsAdmin Api20160501. i i m/. i i m Alert</span><span class="sxs-lookup"><span data-stu-id="05ba7-185">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>

### <span data-ttu-id="05ba7-186">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="05ba7-186">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="05ba7-187">출력</span><span class="sxs-lookup"><span data-stu-id="05ba7-187">OUTPUTS</span></span>

### <span data-ttu-id="05ba7-188">InfrastructureInsightsAdmin Api20160501. i i m/. i i m Alert</span><span class="sxs-lookup"><span data-stu-id="05ba7-188">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="05ba7-189">상속자</span><span class="sxs-lookup"><span data-stu-id="05ba7-189">NOTES</span></span>

<span data-ttu-id="05ba7-190">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-190">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="05ba7-191">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="05ba7-191">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="05ba7-192">알림 <IAlert> :이 개체는 알림 리소스를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-192">ALERT <IAlert>: This object represents an alert resource.</span></span>
  - <span data-ttu-id="05ba7-193">`[Location <String>]`: 자원이 거주 하는 Azure 지역</span><span class="sxs-lookup"><span data-stu-id="05ba7-193">`[Location <String>]`: The Azure Region where the resource lives</span></span>
  - <span data-ttu-id="05ba7-194">`[Tag <ITrackedResourceTags>]`: 리소스 태그.</span><span class="sxs-lookup"><span data-stu-id="05ba7-194">`[Tag <ITrackedResourceTags>]`: Resource tags.</span></span>
    - <span data-ttu-id="05ba7-195">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-195">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="05ba7-196">`[AlertId <String>]`: 경고의 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-196">`[AlertId <String>]`: Gets or sets the ID of the alert.</span></span>
  - <span data-ttu-id="05ba7-197">`[AlertProperty <IAlertModelAlertProperties>]`: 경고의 속성입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-197">`[AlertProperty <IAlertModelAlertProperties>]`: Properties of the alert.</span></span>
    - <span data-ttu-id="05ba7-198">`[(Any) <String>]`:이 개체에 모든 속성이 추가 될 수 있음을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-198">`[(Any) <String>]`: This indicates any property can be added to this object.</span></span>
  - <span data-ttu-id="05ba7-199">`[ClosedByUserAlias <String>]`: 알림을 닫은 사용자 별칭입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-199">`[ClosedByUserAlias <String>]`: User alias who closed the alert.</span></span>
  - <span data-ttu-id="05ba7-200">`[ClosedTimestamp <String>]`: 경고가 닫힌 경우의 타임 스탬프입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-200">`[ClosedTimestamp <String>]`: Timestamp when the alert was closed.</span></span>
  - <span data-ttu-id="05ba7-201">`[CreatedTimestamp <String>]`: 경고가 생성 된 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-201">`[CreatedTimestamp <String>]`: Timestamp when the alert was created.</span></span>
  - <span data-ttu-id="05ba7-202">`[Description <IDictionary[]>]`: 경고에 대 한 설명입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-202">`[Description <IDictionary[]>]`: Description of the alert.</span></span>
  - <span data-ttu-id="05ba7-203">`[FaultId <String>]`: 알림의 오류 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-203">`[FaultId <String>]`: Gets or sets the fault ID of the alert.</span></span>
  - <span data-ttu-id="05ba7-204">`[FaultTypeId <String>]`: 알림의 오류 유형 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-204">`[FaultTypeId <String>]`: Gets or sets the fault type ID of the alert.</span></span>
  - <span data-ttu-id="05ba7-205">`[HasValidRemediationAction <Boolean?>]`: 알림을 재구성 가능 여부를 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-205">`[HasValidRemediationAction <Boolean?>]`: Indicates if the alert can be remediated.</span></span>
  - <span data-ttu-id="05ba7-206">`[ImpactedResourceDisplayName <String>]`: 영향을 받는 항목의 표시 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-206">`[ImpactedResourceDisplayName <String>]`: Display name for the impacted item.</span></span>
  - <span data-ttu-id="05ba7-207">`[ImpactedResourceId <String>]`: 영향을 받는 항목의 리소스 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-207">`[ImpactedResourceId <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>
  - <span data-ttu-id="05ba7-208">`[LastUpdatedTimestamp <String>]`: 경고가 마지막으로 업데이트 된 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-208">`[LastUpdatedTimestamp <String>]`: Timestamp when the alert was last updated.</span></span>
  - <span data-ttu-id="05ba7-209">`[Remediation <IDictionary[]>]`: 알림에 대 한 관리자의 쉬운 재구성 지침을 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-209">`[Remediation <IDictionary[]>]`: Gets or sets the admin friendly remediation instructions for the alert.</span></span>
  - <span data-ttu-id="05ba7-210">`[ResourceProviderRegistrationId <String>]`: 경고가 속한 서비스의 등록 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-210">`[ResourceProviderRegistrationId <String>]`: Gets or sets the registration ID of the service the alert belongs to.</span></span>
  - <span data-ttu-id="05ba7-211">`[ResourceRegistrationId <String>]`: 알림과 연결 된 리소스의 등록 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-211">`[ResourceRegistrationId <String>]`: Gets or sets the registration ID of the resource associated with the alert.</span></span> <span data-ttu-id="05ba7-212">경고가 리소스와 연결 되어 있지 않은 경우 리소스 등록 ID는 null입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-212">If the alert is not associated with a resource, the resource registration ID is null.</span></span>
  - <span data-ttu-id="05ba7-213">`[Severity <String>]`: 알림의 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-213">`[Severity <String>]`: Severity of the alert.</span></span>
  - <span data-ttu-id="05ba7-214">`[State <String>]`: 알림의 상태입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-214">`[State <String>]`: State of the alert.</span></span>
  - <span data-ttu-id="05ba7-215">`[Title <String>]`: 영향을 받는 항목의 리소스 ID를 가져오거나 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-215">`[Title <String>]`: Gets or sets the Resource ID for the impacted item.</span></span>

<span data-ttu-id="05ba7-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="05ba7-216">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="05ba7-217">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-217">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="05ba7-218">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="05ba7-218">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="05ba7-219">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="05ba7-219">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="05ba7-220">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-220">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="05ba7-221">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-221">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="05ba7-222">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-222">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="05ba7-223">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-223">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="05ba7-224">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-224">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="05ba7-225">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="05ba7-225">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="05ba7-226">관련 링크</span><span class="sxs-lookup"><span data-stu-id="05ba7-226">RELATED LINKS</span></span>

