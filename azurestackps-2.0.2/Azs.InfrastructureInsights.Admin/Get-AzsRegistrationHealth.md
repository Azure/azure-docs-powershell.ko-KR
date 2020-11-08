---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregistrationhealth
schema: 2.0.0
ms.openlocfilehash: 1395840cab5d0500dcaf1d4e5e8abafee026daa7
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94046706"
---
# <span data-ttu-id="6e3a6-101">Get-AzsRegistrationHealth</span><span class="sxs-lookup"><span data-stu-id="6e3a6-101">Get-AzsRegistrationHealth</span></span>

## <span data-ttu-id="6e3a6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e3a6-102">SYNOPSIS</span></span>
<span data-ttu-id="6e3a6-103">자원에 대 한 요청 된 상태 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-103">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="6e3a6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6e3a6-104">SYNTAX</span></span>

### <span data-ttu-id="6e3a6-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="6e3a6-105">List (Default)</span></span>
```
Get-AzsRegistrationHealth -ServiceRegistrationId <String> [-Location <String>] [-ResourceGroupName <String>]
 [-SubscriptionId <String[]>] [-Filter <String>] [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e3a6-106">가져오기</span><span class="sxs-lookup"><span data-stu-id="6e3a6-106">Get</span></span>
```
Get-AzsRegistrationHealth -ResourceRegistrationId <String> -ServiceRegistrationId <String>
 [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="6e3a6-107">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="6e3a6-107">GetViaIdentity</span></span>
```
Get-AzsRegistrationHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="6e3a6-108">설명은</span><span class="sxs-lookup"><span data-stu-id="6e3a6-108">DESCRIPTION</span></span>
<span data-ttu-id="6e3a6-109">자원에 대 한 요청 된 상태 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-109">Returns the requested health information about a resource.</span></span>

## <span data-ttu-id="6e3a6-110">예제의</span><span class="sxs-lookup"><span data-stu-id="6e3a6-110">EXAMPLES</span></span>

### <span data-ttu-id="6e3a6-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="6e3a6-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegistrationHealth -ServiceRegistrationName e56bc7b8-c8b5-4e25-b00c-4f951effb22c
```

<span data-ttu-id="6e3a6-112">서비스 아래에 각 리소스의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-112">Returns a list of each resource's health under a service.</span></span>

### <span data-ttu-id="6e3a6-113">예제 2:</span><span class="sxs-lookup"><span data-stu-id="6e3a6-113">Example 2:</span></span>
```powershell
PS C:\> Get-AzsRPHealth | Where {$_.NamespaceProperty -eq 'Microsoft.Fabric.Admin'} | % { Get-AzsRegistrationHealth -ServiceRegistrationName $_.RegistrationId } | select ResourceName, HealthState
```

<span data-ttu-id="6e3a6-114">관리자의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-114">Returns health status under a for Microsoft.Fabric.Admin.</span></span>

## <span data-ttu-id="6e3a6-115">변수</span><span class="sxs-lookup"><span data-stu-id="6e3a6-115">PARAMETERS</span></span>

### <span data-ttu-id="6e3a6-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e3a6-116">-DefaultProfile</span></span>
<span data-ttu-id="6e3a6-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e3a6-118">-필터</span><span class="sxs-lookup"><span data-stu-id="6e3a6-118">-Filter</span></span>
<span data-ttu-id="6e3a6-119">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-119">OData filter parameter.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e3a6-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="6e3a6-120">-InputObject</span></span>
<span data-ttu-id="6e3a6-121">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-121">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="6e3a6-122">-위치</span><span class="sxs-lookup"><span data-stu-id="6e3a6-122">-Location</span></span>
<span data-ttu-id="6e3a6-123">지역 이름</span><span class="sxs-lookup"><span data-stu-id="6e3a6-123">Name of the region</span></span>

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

### <span data-ttu-id="6e3a6-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6e3a6-124">-ResourceGroupName</span></span>
<span data-ttu-id="6e3a6-125">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-125">The name of the resource group.</span></span>

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

### <span data-ttu-id="6e3a6-126">-ResourceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6e3a6-126">-ResourceRegistrationId</span></span>
<span data-ttu-id="6e3a6-127">리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-127">Resource registration ID.</span></span>

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

### <span data-ttu-id="6e3a6-128">-ServiceRegistrationId</span><span class="sxs-lookup"><span data-stu-id="6e3a6-128">-ServiceRegistrationId</span></span>
<span data-ttu-id="6e3a6-129">서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-129">Service registration ID.</span></span>

```yaml
Type: System.String
Parameter Sets: Get, List
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="6e3a6-130">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="6e3a6-130">-SubscriptionId</span></span>
<span data-ttu-id="6e3a6-131">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-131">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="6e3a6-132">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-132">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="6e3a6-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e3a6-133">CommonParameters</span></span>
<span data-ttu-id="6e3a6-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e3a6-135">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-135">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e3a6-136">입력</span><span class="sxs-lookup"><span data-stu-id="6e3a6-136">INPUTS</span></span>

### <span data-ttu-id="6e3a6-137">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="6e3a6-137">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="6e3a6-138">출력</span><span class="sxs-lookup"><span data-stu-id="6e3a6-138">OUTPUTS</span></span>

### <span data-ttu-id="6e3a6-139">InfrastructureInsightsAdmin. Api20160501. i a Nsourcehealth</span><span class="sxs-lookup"><span data-stu-id="6e3a6-139">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IResourceHealth</span></span>



## <span data-ttu-id="6e3a6-140">상속자</span><span class="sxs-lookup"><span data-stu-id="6e3a6-140">NOTES</span></span>

<span data-ttu-id="6e3a6-141">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-141">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="6e3a6-142">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-142">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="6e3a6-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e3a6-143">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="6e3a6-144">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-144">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="6e3a6-145">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="6e3a6-145">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="6e3a6-146">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="6e3a6-146">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="6e3a6-147">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-147">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="6e3a6-148">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-148">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="6e3a6-149">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-149">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="6e3a6-150">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-150">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="6e3a6-151">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-151">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="6e3a6-152">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e3a6-152">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="6e3a6-153">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e3a6-153">RELATED LINKS</span></span>

