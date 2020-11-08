---
external help file: ''
Module Name: Azs.Subscriptions.Admin
online version: https://docs.microsoft.com/en-us/powershell/module/azs.subscriptions.admin/get-azsdelegatedprovider
schema: 2.0.0
ms.openlocfilehash: 2c6c87ce0b40fae228756d4a9dd452b49ce1aad2
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047121"
---
# <span data-ttu-id="8a92d-101">Get-AzsDelegatedProvider</span><span class="sxs-lookup"><span data-stu-id="8a92d-101">Get-AzsDelegatedProvider</span></span>

## <span data-ttu-id="8a92d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a92d-102">SYNOPSIS</span></span>
<span data-ttu-id="8a92d-103">지정 된 위임 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-103">Get the specified delegated provider.</span></span>

## <span data-ttu-id="8a92d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a92d-104">SYNTAX</span></span>

### <span data-ttu-id="8a92d-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a92d-105">List (Default)</span></span>
```
Get-AzsDelegatedProvider [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a92d-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="8a92d-106">Get</span></span>
```
Get-AzsDelegatedProvider -DelegatedProviderId <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="8a92d-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="8a92d-107">GetViaIdentity</span></span>
```
Get-AzsDelegatedProvider -InputObject <ISubscriptionsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a92d-108">설명은</span><span class="sxs-lookup"><span data-stu-id="8a92d-108">DESCRIPTION</span></span>
<span data-ttu-id="8a92d-109">지정 된 위임 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-109">Get the specified delegated provider.</span></span>

## <span data-ttu-id="8a92d-110">예제의</span><span class="sxs-lookup"><span data-stu-id="8a92d-110">EXAMPLES</span></span>

### <span data-ttu-id="8a92d-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="8a92d-111">Example 1</span></span>
```powershell
PS C:\> Get-AzsDelegatedProvider -DelegatedProviderId "ed3e275b-87d1-4e94-9962-b3700287bdbc" | fl *

DelegatedProviderSubscriptionId : d77ed1d7-cb62-4658-a777-386a8ae523dd
DisplayName                     : cnur4866tenantresellersubscription843
ExternalReferenceId             : 
Id                              : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/providers/Microsoft.Subscriptions.Admin/subscriptions/ed3e275b-87d1-4e94-9962-b3700287bdbc
OfferId                         : /subscriptions/d77ed1d7-cb62-4658-a777-386a8ae523dd/resourceGroups/cnur4866resellersubscrrg843/providers/Microsoft.Subscriptions.Admin/offers/cnur4866tenantsubsvcoffe
                                  r843
Owner                           : tenantadmin1@msazurestack.onmicrosoft.com
RoutingResourceManagerType      : Default
State                           : Enabled
SubscriptionId                  : ed3e275b-87d1-4e94-9962-b3700287bdbc
TenantId                        : 6ca57aaf-0074-498a-9c96-2b097515e8cb
```

<span data-ttu-id="8a92d-112">위임 된 특정 공급자를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-112">Get a specific delegated provider.</span></span>

## <span data-ttu-id="8a92d-113">변수</span><span class="sxs-lookup"><span data-stu-id="8a92d-113">PARAMETERS</span></span>

### <span data-ttu-id="8a92d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a92d-114">-DefaultProfile</span></span>
<span data-ttu-id="8a92d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="8a92d-116">-DelegatedProviderId</span><span class="sxs-lookup"><span data-stu-id="8a92d-116">-DelegatedProviderId</span></span>
<span data-ttu-id="8a92d-117">DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-117">DelegatedProvider identifier.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a92d-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="8a92d-118">-InputObject</span></span>
<span data-ttu-id="8a92d-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="8a92d-120">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="8a92d-120">-SubscriptionId</span></span>
<span data-ttu-id="8a92d-121">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-121">Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>

```yaml
Type: System.String[]
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="8a92d-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a92d-122">CommonParameters</span></span>
<span data-ttu-id="8a92d-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a92d-124">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a92d-124">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a92d-125">입력</span><span class="sxs-lookup"><span data-stu-id="8a92d-125">INPUTS</span></span>

### <span data-ttu-id="8a92d-126">SubscriptionsAdmin. ISubscriptionsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="8a92d-126">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.ISubscriptionsAdminIdentity</span></span>

## <span data-ttu-id="8a92d-127">출력</span><span class="sxs-lookup"><span data-stu-id="8a92d-127">OUTPUTS</span></span>

### <span data-ttu-id="8a92d-128">SubscriptionsAdmin. Api20151101. i a PowerShell. ISubscriptionDefinition</span><span class="sxs-lookup"><span data-stu-id="8a92d-128">Microsoft.Azure.PowerShell.Cmdlets.SubscriptionsAdmin.Models.Api20151101.ISubscriptionDefinition</span></span>

<span data-ttu-id="8a92d-129">별칭과</span><span class="sxs-lookup"><span data-stu-id="8a92d-129">ALIASES</span></span>

## <span data-ttu-id="8a92d-130">상속자</span><span class="sxs-lookup"><span data-stu-id="8a92d-130">NOTES</span></span>

<span data-ttu-id="8a92d-131">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-131">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="8a92d-132">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="8a92d-132">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="8a92d-133">INPUTOBJECT <ISubscriptionsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="8a92d-133">INPUTOBJECT <ISubscriptionsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="8a92d-134">`[DelegatedProvider <String>]`: DelegatedProvider 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-134">`[DelegatedProvider <String>]`: DelegatedProvider identifier.</span></span>
  - <span data-ttu-id="8a92d-135">`[DelegatedProviderSubscriptionId <String>]`: 위임 된 공급자 구독 식별자입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-135">`[DelegatedProviderSubscriptionId <String>]`: Delegated provider subscription identifier.</span></span>
  - <span data-ttu-id="8a92d-136">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="8a92d-136">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="8a92d-137">`[Location <String>]`: AzureStack 위치입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-137">`[Location <String>]`: The AzureStack location.</span></span>
  - <span data-ttu-id="8a92d-138">`[ManifestName <String>]`: 매니페스트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-138">`[ManifestName <String>]`: The manifest name.</span></span>
  - <span data-ttu-id="8a92d-139">`[Offer <String>]`: 제안의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-139">`[Offer <String>]`: Name of an offer.</span></span>
  - <span data-ttu-id="8a92d-140">`[OfferDelegationName <String>]`: 제안 위임의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-140">`[OfferDelegationName <String>]`: Name of a offer delegation.</span></span>
  - <span data-ttu-id="8a92d-141">`[OperationsStatusName <String>]`: 작업 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-141">`[OperationsStatusName <String>]`: The operation status name.</span></span>
  - <span data-ttu-id="8a92d-142">`[Plan <String>]`: 계획의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-142">`[Plan <String>]`: Name of the plan.</span></span>
  - <span data-ttu-id="8a92d-143">`[PlanAcquisitionId <String>]`: 계획 획득 식별자</span><span class="sxs-lookup"><span data-stu-id="8a92d-143">`[PlanAcquisitionId <String>]`: The plan acquisition Identifier</span></span>
  - <span data-ttu-id="8a92d-144">`[Quota <String>]`: 할당량의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-144">`[Quota <String>]`: Name of the quota.</span></span>
  - <span data-ttu-id="8a92d-145">`[ResourceGroupName <String>]`: 리소스 그룹이 아래에 있습니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-145">`[ResourceGroupName <String>]`: The resource group the resource is located under.</span></span>
  - <span data-ttu-id="8a92d-146">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다. 구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-146">`[SubscriptionId <String>]`: Subscription credentials which uniquely identify Microsoft Azure subscription.The subscription ID forms part of the URI for every service call.</span></span>
  - <span data-ttu-id="8a92d-147">`[TargetSubscriptionId <String>]`: 대상 구독 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-147">`[TargetSubscriptionId <String>]`: The target subscription ID.</span></span>
  - <span data-ttu-id="8a92d-148">`[Tenant <String>]`: 디렉터리 테 넌 트 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8a92d-148">`[Tenant <String>]`: Directory tenant name.</span></span>

## <span data-ttu-id="8a92d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a92d-149">RELATED LINKS</span></span>

