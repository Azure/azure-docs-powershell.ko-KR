---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/remove-azsplan
schema: 2.0.0
ms.openlocfilehash: fca0ab39b587bea05228da3a053fd1575b3e7e98
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046928"
---
# <span data-ttu-id="aaf18-101">Remove-AzsPlan</span><span class="sxs-lookup"><span data-stu-id="aaf18-101">Remove-AzsPlan</span></span>

## <span data-ttu-id="aaf18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aaf18-102">SYNOPSIS</span></span>
<span data-ttu-id="aaf18-103">지정 된 요금제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-103">Delete the specified plan.</span></span>

## <span data-ttu-id="aaf18-104">구문과</span><span class="sxs-lookup"><span data-stu-id="aaf18-104">SYNTAX</span></span>

### <span data-ttu-id="aaf18-105">삭제 (기본값)</span><span class="sxs-lookup"><span data-stu-id="aaf18-105">Delete (Default)</span></span>
```
Remove-AzsPlan -Name <String> -ResourceGroupName <String> [-SubscriptionId <String>]
 [-DefaultProfile <PSObject>] [-PassThru] [-Confirm] [-WhatIf] [<CommonParameters>]
```

### <span data-ttu-id="aaf18-106">DeleteViaIdentity</span><span class="sxs-lookup"><span data-stu-id="aaf18-106">DeleteViaIdentity</span></span>
```
Remove-AzsPlan -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>] [-PassThru] [-Confirm]
 [-WhatIf] [<CommonParameters>]
```

## <span data-ttu-id="aaf18-107">설명은</span><span class="sxs-lookup"><span data-stu-id="aaf18-107">DESCRIPTION</span></span>
<span data-ttu-id="aaf18-108">지정 된 요금제를 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-108">Delete the specified plan.</span></span>

## <span data-ttu-id="aaf18-109">예제의</span><span class="sxs-lookup"><span data-stu-id="aaf18-109">EXAMPLES</span></span>

### <span data-ttu-id="aaf18-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="aaf18-110">Example 1</span></span>
```powershell
PS C:\> Remove-AzsPlan -Name "testplan" -ResourceGroupName "testrg"

```

<span data-ttu-id="aaf18-111">지정 된 계획 삭제</span><span class="sxs-lookup"><span data-stu-id="aaf18-111">Delete the specified plan</span></span>

## <span data-ttu-id="aaf18-112">변수</span><span class="sxs-lookup"><span data-stu-id="aaf18-112">PARAMETERS</span></span>

### <span data-ttu-id="aaf18-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aaf18-113">-DefaultProfile</span></span>
<span data-ttu-id="aaf18-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aaf18-115">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aaf18-115">-InputObject</span></span>
<span data-ttu-id="aaf18-116">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-116">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: DeleteViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="aaf18-117">-이름</span><span class="sxs-lookup"><span data-stu-id="aaf18-117">-Name</span></span>
<span data-ttu-id="aaf18-118">계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-118">Name of the plan.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aaf18-119">-PassThru</span><span class="sxs-lookup"><span data-stu-id="aaf18-119">-PassThru</span></span>
<span data-ttu-id="aaf18-120">명령이 성공 하면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-120">Returns true when the command succeeds</span></span>

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

### <span data-ttu-id="aaf18-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="aaf18-121">-ResourceGroupName</span></span>
<span data-ttu-id="aaf18-122">리소스가 있는 리소스 그룹입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-122">The resource group the resource is located under.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aaf18-123">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="aaf18-123">-SubscriptionId</span></span>
<span data-ttu-id="aaf18-124">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-124">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String
Parameter Sets: Delete
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="aaf18-125">-확인</span><span class="sxs-lookup"><span data-stu-id="aaf18-125">-Confirm</span></span>
<span data-ttu-id="aaf18-126">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-126">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aaf18-127">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aaf18-127">-WhatIf</span></span>
<span data-ttu-id="aaf18-128">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-128">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aaf18-129">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-129">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aaf18-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aaf18-130">CommonParameters</span></span>
<span data-ttu-id="aaf18-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aaf18-132">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="aaf18-132">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aaf18-133">입력</span><span class="sxs-lookup"><span data-stu-id="aaf18-133">INPUTS</span></span>

### <span data-ttu-id="aaf18-134">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="aaf18-134">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="aaf18-135">출력</span><span class="sxs-lookup"><span data-stu-id="aaf18-135">OUTPUTS</span></span>

### <span data-ttu-id="aaf18-136">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="aaf18-136">System.Boolean</span></span>

<span data-ttu-id="aaf18-137">별칭과</span><span class="sxs-lookup"><span data-stu-id="aaf18-137">ALIASES</span></span>

## <span data-ttu-id="aaf18-138">상속자</span><span class="sxs-lookup"><span data-stu-id="aaf18-138">NOTES</span></span>

<span data-ttu-id="aaf18-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="aaf18-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="aaf18-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="aaf18-141">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="aaf18-141">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="aaf18-142">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-142">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="aaf18-143">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-143">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="aaf18-144">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="aaf18-144">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="aaf18-145">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-145">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="aaf18-146">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-146">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="aaf18-147">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-147">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="aaf18-148">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-148">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="aaf18-149">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-149">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="aaf18-150">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-150">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="aaf18-151">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="aaf18-151">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="aaf18-152">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-152">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="aaf18-153">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-153">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="aaf18-154">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-154">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="aaf18-155">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-155">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="aaf18-156">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="aaf18-156">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="aaf18-157">관련 링크</span><span class="sxs-lookup"><span data-stu-id="aaf18-157">RELATED LINKS</span></span>

