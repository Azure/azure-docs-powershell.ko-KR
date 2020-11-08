---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsidentityhealthreport
schema: 2.0.0
ms.openlocfilehash: 995ddf191f870fee9d27438ebea6d29729ca4c9f
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047117"
---
# <span data-ttu-id="884e1-101">Get-AzsIdentityHealthReport</span><span class="sxs-lookup"><span data-stu-id="884e1-101">Get-AzsIdentityHealthReport</span></span>

## <span data-ttu-id="884e1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="884e1-102">SYNOPSIS</span></span>
<span data-ttu-id="884e1-103">Id 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-103">Checks the identity health</span></span>

## <span data-ttu-id="884e1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="884e1-104">SYNTAX</span></span>

### <span data-ttu-id="884e1-105">선택 (기본값)</span><span class="sxs-lookup"><span data-stu-id="884e1-105">Check (Default)</span></span>
```
Get-AzsIdentityHealthReport [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [-Confirm] [-WhatIf]
 [<CommonParameters>]
```

### <span data-ttu-id="884e1-106">CheckViaIdentity</span><span class="sxs-lookup"><span data-stu-id="884e1-106">CheckViaIdentity</span></span>
```
Get-AzsIdentityHealthReport -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="884e1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="884e1-107">DESCRIPTION</span></span>
<span data-ttu-id="884e1-108">Id 상태를 확인 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-108">Checks the identity health</span></span>

## <span data-ttu-id="884e1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="884e1-109">EXAMPLES</span></span>

### <span data-ttu-id="884e1-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="884e1-110">Example 1</span></span>
```powershell
PS C:\> Get-AzsIdentityHealthReport

ReportEndTimeUtc      ReportStartTimeUtc    Status 
----------------      ------------------    ------ 
3/12/2020 11:41:08 PM 3/12/2020 11:40:50 PM Healthy
```

<span data-ttu-id="884e1-111">Id 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-111">Get the status of the Identity Health.</span></span>

## <span data-ttu-id="884e1-112">변수</span><span class="sxs-lookup"><span data-stu-id="884e1-112">PARAMETERS</span></span>

### <span data-ttu-id="884e1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="884e1-113">-DefaultProfile</span></span>
<span data-ttu-id="884e1-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="884e1-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="884e1-115">-InputObject</span></span>
<span data-ttu-id="884e1-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: CheckViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="884e1-117">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="884e1-117">-SubscriptionId</span></span>
<span data-ttu-id="884e1-118">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-118">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Check
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="884e1-119">-확인</span><span class="sxs-lookup"><span data-stu-id="884e1-119">-Confirm</span></span>
<span data-ttu-id="884e1-120">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="884e1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="884e1-121">-WhatIf</span></span>
<span data-ttu-id="884e1-122">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="884e1-123">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="884e1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="884e1-124">CommonParameters</span></span>
<span data-ttu-id="884e1-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="884e1-126">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="884e1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="884e1-127">입력</span><span class="sxs-lookup"><span data-stu-id="884e1-127">INPUTS</span></span>

### <span data-ttu-id="884e1-128">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="884e1-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="884e1-129">출력</span><span class="sxs-lookup"><span data-stu-id="884e1-129">OUTPUTS</span></span>

### <span data-ttu-id="884e1-130">SubscriptionsAdmin. Api20151101. IIdentityHealthCheckReportDefinition에 대 한</span><span class="sxs-lookup"><span data-stu-id="884e1-130">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.IIdentityHealthCheckReportDefinition</span></span>

<span data-ttu-id="884e1-131">별칭과</span><span class="sxs-lookup"><span data-stu-id="884e1-131">ALIASES</span></span>

## <span data-ttu-id="884e1-132">상속자</span><span class="sxs-lookup"><span data-stu-id="884e1-132">NOTES</span></span>

<span data-ttu-id="884e1-133">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-133">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="884e1-134">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="884e1-134">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="884e1-135">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="884e1-135">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="884e1-136">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-136">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="884e1-137">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-137">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="884e1-138">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="884e1-138">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="884e1-139">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-139">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="884e1-140">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-140">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="884e1-141">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-141">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="884e1-142">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-142">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="884e1-143">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-143">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="884e1-144">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-144">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="884e1-145">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="884e1-145">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="884e1-146">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-146">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="884e1-147">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-147">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="884e1-148">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-148">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="884e1-149">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-149">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="884e1-150">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="884e1-150">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="884e1-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="884e1-151">RELATED LINKS</span></span>

