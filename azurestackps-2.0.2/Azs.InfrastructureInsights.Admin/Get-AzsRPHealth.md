---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsrphealth
schema: 2.0.0
ms.openlocfilehash: 50b71b6804ea5d57e18fbbd2774c0ff9306a829d
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046827"
---
# <span data-ttu-id="d1397-101">Get-AzsRPHealth</span><span class="sxs-lookup"><span data-stu-id="d1397-101">Get-AzsRPHealth</span></span>

## <span data-ttu-id="d1397-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d1397-102">SYNOPSIS</span></span>
<span data-ttu-id="d1397-103">요청 된 서비스 상태 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-103">Returns the requested service health object.</span></span>

## <span data-ttu-id="d1397-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d1397-104">SYNTAX</span></span>

### <span data-ttu-id="d1397-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="d1397-105">List (Default)</span></span>
```
Get-AzsRPHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1397-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="d1397-106">Get</span></span>
```
Get-AzsRPHealth -ServiceHealth <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="d1397-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="d1397-107">GetViaIdentity</span></span>
```
Get-AzsRPHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

## <span data-ttu-id="d1397-108">설명은</span><span class="sxs-lookup"><span data-stu-id="d1397-108">DESCRIPTION</span></span>
<span data-ttu-id="d1397-109">요청 된 서비스 상태 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-109">Returns the requested service health object.</span></span>

## <span data-ttu-id="d1397-110">예제의</span><span class="sxs-lookup"><span data-stu-id="d1397-110">EXAMPLES</span></span>

### <span data-ttu-id="d1397-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="d1397-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRPHealth
```

<span data-ttu-id="d1397-112">각 서비스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-112">Returns a list of each service's health.</span></span>

### <span data-ttu-id="d1397-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="d1397-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth -Name "e56bc7b8-c8b5-4e25-b00c-4f951effb22c"
```

<span data-ttu-id="d1397-114">서비스의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-114">Returns a service's health.</span></span>

## <span data-ttu-id="d1397-115">변수</span><span class="sxs-lookup"><span data-stu-id="d1397-115">PARAMETERS</span></span>

### <span data-ttu-id="d1397-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d1397-116">-DefaultProfile</span></span>
<span data-ttu-id="d1397-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d1397-118">-필터</span><span class="sxs-lookup"><span data-stu-id="d1397-118">-Filter</span></span>
<span data-ttu-id="d1397-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-119">OData filter parameter.</span></span>

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

### <span data-ttu-id="d1397-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d1397-120">-InputObject</span></span>
<span data-ttu-id="d1397-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="d1397-122">-위치</span><span class="sxs-lookup"><span data-stu-id="d1397-122">-Location</span></span>
<span data-ttu-id="d1397-123">지역 이름</span><span class="sxs-lookup"><span data-stu-id="d1397-123">Name of the region</span></span>

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

### <span data-ttu-id="d1397-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d1397-124">-ResourceGroupName</span></span>
<span data-ttu-id="d1397-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="d1397-126">-ServiceHealth</span><span class="sxs-lookup"><span data-stu-id="d1397-126">-ServiceHealth</span></span>
<span data-ttu-id="d1397-127">서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-127">Service Health name.</span></span>

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

### <span data-ttu-id="d1397-128">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="d1397-128">-SubscriptionId</span></span>
<span data-ttu-id="d1397-129">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-129">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="d1397-130">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-130">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="d1397-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d1397-131">CommonParameters</span></span>
<span data-ttu-id="d1397-132">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d1397-133">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1397-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d1397-134">입력</span><span class="sxs-lookup"><span data-stu-id="d1397-134">INPUTS</span></span>

### <span data-ttu-id="d1397-135">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="d1397-135">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="d1397-136">출력</span><span class="sxs-lookup"><span data-stu-id="d1397-136">OUTPUTS</span></span>

### <span data-ttu-id="d1397-137">InfrastructureInsightsAdmin. PowerShell. Api20160501. IServiceHealth</span><span class="sxs-lookup"><span data-stu-id="d1397-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IServiceHealth</span></span>



## <span data-ttu-id="d1397-138">상속자</span><span class="sxs-lookup"><span data-stu-id="d1397-138">NOTES</span></span>

<span data-ttu-id="d1397-139">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-139">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="d1397-140">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="d1397-140">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="d1397-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="d1397-141">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="d1397-142">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-142">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="d1397-143">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="d1397-143">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="d1397-144">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="d1397-144">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="d1397-145">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-145">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="d1397-146">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-146">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="d1397-147">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-147">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="d1397-148">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-148">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="d1397-149">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-149">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="d1397-150">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="d1397-150">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="d1397-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d1397-151">RELATED LINKS</span></span>

