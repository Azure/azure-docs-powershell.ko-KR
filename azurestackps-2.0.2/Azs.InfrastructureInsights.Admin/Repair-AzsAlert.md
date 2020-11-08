---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/repair-azsalert
schema: 2.0.0
ms.openlocfilehash: b4017fdcabf1c7d955e8e2a754c3fca989448aa6
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046856"
---
# <span data-ttu-id="061b3-101">Repair-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="061b3-101">Repair-AzsAlert</span></span>

## <span data-ttu-id="061b3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="061b3-102">SYNOPSIS</span></span>
<span data-ttu-id="061b3-103">알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-103">Repairs an alert.</span></span>

## <span data-ttu-id="061b3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="061b3-104">SYNTAX</span></span>

### <span data-ttu-id="061b3-105">복구 (기본값)</span><span class="sxs-lookup"><span data-stu-id="061b3-105">Repair (Default)</span></span>
```
Repair-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-AsJob] [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="061b3-106">RepairViaIdentity</span><span class="sxs-lookup"><span data-stu-id="061b3-106">RepairViaIdentity</span></span>
```
Repair-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>] [-AsJob]
 [-NoWait] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="061b3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="061b3-107">DESCRIPTION</span></span>
<span data-ttu-id="061b3-108">알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-108">Repairs an alert.</span></span>

## <span data-ttu-id="061b3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="061b3-109">EXAMPLES</span></span>

### <span data-ttu-id="061b3-110">예제 1:</span><span class="sxs-lookup"><span data-stu-id="061b3-110">Example 1:</span></span>
```powershell
PS C:\> Repair-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0
```

<span data-ttu-id="061b3-111">이름으로 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-111">Repairs an alert by Name.</span></span>

### <span data-ttu-id="061b3-112">예제 2:</span><span class="sxs-lookup"><span data-stu-id="061b3-112">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name f2147f3d-42ac-4316-8cbc-f0f9c18888b0 | Repair-AzsAlert
```

<span data-ttu-id="061b3-113">파이핑을 통해 알림을 복구 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-113">Repairs an alert through piping.</span></span>

## <span data-ttu-id="061b3-114">변수</span><span class="sxs-lookup"><span data-stu-id="061b3-114">PARAMETERS</span></span>

### <span data-ttu-id="061b3-115">-AsJob</span><span class="sxs-lookup"><span data-stu-id="061b3-115">-AsJob</span></span>
<span data-ttu-id="061b3-116">작업으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="061b3-116">Run the command as a job</span></span>

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

### <span data-ttu-id="061b3-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="061b3-117">-DefaultProfile</span></span>
<span data-ttu-id="061b3-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-118">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="061b3-119">-InputObject</span><span class="sxs-lookup"><span data-stu-id="061b3-119">-InputObject</span></span>
<span data-ttu-id="061b3-120">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-120">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: RepairViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="061b3-121">-위치</span><span class="sxs-lookup"><span data-stu-id="061b3-121">-Location</span></span>
<span data-ttu-id="061b3-122">지역 이름</span><span class="sxs-lookup"><span data-stu-id="061b3-122">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="061b3-123">-이름</span><span class="sxs-lookup"><span data-stu-id="061b3-123">-Name</span></span>
<span data-ttu-id="061b3-124">경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-124">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="061b3-125">-NoWait</span><span class="sxs-lookup"><span data-stu-id="061b3-125">-NoWait</span></span>
<span data-ttu-id="061b3-126">비동기적으로 명령 실행</span><span class="sxs-lookup"><span data-stu-id="061b3-126">Run the command asynchronously</span></span>

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

### <span data-ttu-id="061b3-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="061b3-127">-PassThru</span></span>
<span data-ttu-id="061b3-128">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-128">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="061b3-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="061b3-129">-ResourceGroupName</span></span>
<span data-ttu-id="061b3-130">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-130">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="061b3-131">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="061b3-131">-SubscriptionId</span></span>
<span data-ttu-id="061b3-132">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-132">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="061b3-133">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-133">The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Repair
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="061b3-134">-확인</span><span class="sxs-lookup"><span data-stu-id="061b3-134">-Confirm</span></span>
<span data-ttu-id="061b3-135">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="061b3-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="061b3-136">-WhatIf</span></span>
<span data-ttu-id="061b3-137">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="061b3-138">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="061b3-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="061b3-139">CommonParameters</span></span>
<span data-ttu-id="061b3-140">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="061b3-141">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="061b3-141">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="061b3-142">입력</span><span class="sxs-lookup"><span data-stu-id="061b3-142">INPUTS</span></span>

### <span data-ttu-id="061b3-143">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="061b3-143">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="061b3-144">출력</span><span class="sxs-lookup"><span data-stu-id="061b3-144">OUTPUTS</span></span>

### <span data-ttu-id="061b3-145">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="061b3-145">System.Boolean</span></span>



## <span data-ttu-id="061b3-146">상속자</span><span class="sxs-lookup"><span data-stu-id="061b3-146">NOTES</span></span>

<span data-ttu-id="061b3-147">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-147">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="061b3-148">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="061b3-148">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="061b3-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="061b3-149">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="061b3-150">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-150">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="061b3-151">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="061b3-151">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="061b3-152">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="061b3-152">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="061b3-153">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-153">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="061b3-154">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-154">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="061b3-155">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-155">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="061b3-156">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-156">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="061b3-157">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-157">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="061b3-158">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="061b3-158">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="061b3-159">관련 링크</span><span class="sxs-lookup"><span data-stu-id="061b3-159">RELATED LINKS</span></span>

