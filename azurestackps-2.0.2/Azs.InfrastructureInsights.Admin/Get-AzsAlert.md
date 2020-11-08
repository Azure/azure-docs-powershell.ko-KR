---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsalert
schema: 2.0.0
ms.openlocfilehash: 097793edf89bed5193ef007b6bad0803a9082149
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046708"
---
# <span data-ttu-id="a97de-101">Get-AzsAlert</span><span class="sxs-lookup"><span data-stu-id="a97de-101">Get-AzsAlert</span></span>

## <span data-ttu-id="a97de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a97de-102">SYNOPSIS</span></span>
<span data-ttu-id="a97de-103">요청 된 알림을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-103">Returns the requested alert.</span></span>

## <span data-ttu-id="a97de-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a97de-104">SYNTAX</span></span>

### <span data-ttu-id="a97de-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="a97de-105">List (Default)</span></span>
```
Get-AzsAlert [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a97de-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="a97de-106">Get</span></span>
```
Get-AzsAlert -Name <String> [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="a97de-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="a97de-107">GetViaIdentity</span></span>
```
Get-AzsAlert -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="a97de-108">설명은</span><span class="sxs-lookup"><span data-stu-id="a97de-108">DESCRIPTION</span></span>
<span data-ttu-id="a97de-109">요청 된 알림을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-109">Returns the requested alert.</span></span>

## <span data-ttu-id="a97de-110">예제의</span><span class="sxs-lookup"><span data-stu-id="a97de-110">EXAMPLES</span></span>

### <span data-ttu-id="a97de-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="a97de-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsAlert -Name 7f58eb8b-e39f-45d0-8ae7-9920b8f22f5f
```

<span data-ttu-id="a97de-112">이름으로 알림을 받습니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-112">Get an alert by Name.</span></span>

### <span data-ttu-id="a97de-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="a97de-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsAlert | Where State -EQ 'active' | select FaultTypeId, Title
```

<span data-ttu-id="a97de-114">모든 활성 알림을 받고 해당 오류 및 직함을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-114">Get all active alerts and display their fault and title.</span></span>

## <span data-ttu-id="a97de-115">변수</span><span class="sxs-lookup"><span data-stu-id="a97de-115">PARAMETERS</span></span>

### <span data-ttu-id="a97de-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a97de-116">-DefaultProfile</span></span>
<span data-ttu-id="a97de-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a97de-118">-필터</span><span class="sxs-lookup"><span data-stu-id="a97de-118">-Filter</span></span>
<span data-ttu-id="a97de-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: List
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a97de-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="a97de-120">-InputObject</span></span>
<span data-ttu-id="a97de-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

```yaml
Type: Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity
Parameter Sets: GetViaIdentity
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False

```

### <span data-ttu-id="a97de-122">-위치</span><span class="sxs-lookup"><span data-stu-id="a97de-122">-Location</span></span>
<span data-ttu-id="a97de-123">지역 이름</span><span class="sxs-lookup"><span data-stu-id="a97de-123">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a97de-124">-이름</span><span class="sxs-lookup"><span data-stu-id="a97de-124">-Name</span></span>
<span data-ttu-id="a97de-125">경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-125">Name of the alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases: AlertName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a97de-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a97de-126">-ResourceGroupName</span></span>
<span data-ttu-id="a97de-127">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-127">The name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: False
Position: Named
Default value: -join("System.",(Get-AzLocation)[0].Location)
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="a97de-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="a97de-128">-SubscriptionId</span></span>
<span data-ttu-id="a97de-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="a97de-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="a97de-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a97de-131">CommonParameters</span></span>
<span data-ttu-id="a97de-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a97de-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="a97de-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a97de-134">입력</span><span class="sxs-lookup"><span data-stu-id="a97de-134">INPUTS</span></span>

### <span data-ttu-id="a97de-135">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="a97de-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="a97de-136">출력</span><span class="sxs-lookup"><span data-stu-id="a97de-136">OUTPUTS</span></span>

### <span data-ttu-id="a97de-137">InfrastructureInsightsAdmin Api20160501. i i m/. i i m Alert</span><span class="sxs-lookup"><span data-stu-id="a97de-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IAlert</span></span>



## <span data-ttu-id="a97de-138">상속자</span><span class="sxs-lookup"><span data-stu-id="a97de-138">NOTES</span></span>

<span data-ttu-id="a97de-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="a97de-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="a97de-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="a97de-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="a97de-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="a97de-142">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="a97de-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="a97de-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="a97de-144">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="a97de-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="a97de-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="a97de-146">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="a97de-147">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="a97de-148">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="a97de-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="a97de-150">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="a97de-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="a97de-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a97de-151">RELATED LINKS</span></span>

