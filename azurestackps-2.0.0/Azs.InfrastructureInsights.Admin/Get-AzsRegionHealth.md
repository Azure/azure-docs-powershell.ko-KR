---
external help file: ''
Module Name: Azs.InfrastructureInsights.Admin
online version: https://docs.microsoft.com/powershell/module/azs.infrastructureinsights.admin/get-azsregionhealth
schema: 2.0.0
ms.openlocfilehash: 6f5fa25f1b35ac03d27688eced71919cb409d1cb
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93877167"
---
# <span data-ttu-id="2b4b9-101">Get-AzsRegionHealth</span><span class="sxs-lookup"><span data-stu-id="2b4b9-101">Get-AzsRegionHealth</span></span>

## <span data-ttu-id="2b4b9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2b4b9-102">SYNOPSIS</span></span>
<span data-ttu-id="2b4b9-103">영역의 요청 된 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-103">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="2b4b9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2b4b9-104">SYNTAX</span></span>

### <span data-ttu-id="2b4b9-105">Get (기본값)</span><span class="sxs-lookup"><span data-stu-id="2b4b9-105">Get (Default)</span></span>
```
Get-AzsRegionHealth [-Location <String>] [-ResourceGroupName <String>] [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

### <span data-ttu-id="2b4b9-106">GetViaIdentity</span><span class="sxs-lookup"><span data-stu-id="2b4b9-106">GetViaIdentity</span></span>
```
Get-AzsRegionHealth -InputObject <IInfrastructureInsightsAdminIdentity> [-DefaultProfile <PSObject>]
 [<CommonParameters>]
```

### <span data-ttu-id="2b4b9-107">목록</span><span class="sxs-lookup"><span data-stu-id="2b4b9-107">List</span></span>
```
Get-AzsRegionHealth [-ResourceGroupName <String>] [-SubscriptionId <String[]>] [-Filter <String>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="2b4b9-108">설명은</span><span class="sxs-lookup"><span data-stu-id="2b4b9-108">DESCRIPTION</span></span>
<span data-ttu-id="2b4b9-109">영역의 요청 된 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-109">Returns the requested health status of a region.</span></span>

## <span data-ttu-id="2b4b9-110">예제의</span><span class="sxs-lookup"><span data-stu-id="2b4b9-110">EXAMPLES</span></span>

### <span data-ttu-id="2b4b9-111">예제 1:</span><span class="sxs-lookup"><span data-stu-id="2b4b9-111">Example 1:</span></span>
```powershell
PS C:\> Get-AzsRegionHealth
```

<span data-ttu-id="2b4b9-112">영역의 상태 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-112">Returns a list of region's health status.</span></span>

## <span data-ttu-id="2b4b9-113">변수</span><span class="sxs-lookup"><span data-stu-id="2b4b9-113">PARAMETERS</span></span>

### <span data-ttu-id="2b4b9-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2b4b9-114">-DefaultProfile</span></span>
<span data-ttu-id="2b4b9-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="2b4b9-116">-필터</span><span class="sxs-lookup"><span data-stu-id="2b4b9-116">-Filter</span></span>
<span data-ttu-id="2b4b9-117">OData 필터 매개 변수입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-117">OData filter parameter.</span></span>

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

### <span data-ttu-id="2b4b9-118">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2b4b9-118">-InputObject</span></span>
<span data-ttu-id="2b4b9-119">생성할 id 매개 변수는 INPUTOBJECT 속성에 대 한 참고 섹션을 참조 하 고 해시 테이블을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-119">Identity Parameter To construct, see NOTES section for INPUTOBJECT properties and create a hash table.</span></span>

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

### <span data-ttu-id="2b4b9-120">-위치</span><span class="sxs-lookup"><span data-stu-id="2b4b9-120">-Location</span></span>
<span data-ttu-id="2b4b9-121">지역 이름</span><span class="sxs-lookup"><span data-stu-id="2b4b9-121">Name of the region</span></span>

```yaml
Type: System.String
Parameter Sets: Get
Aliases:

Required: False
Position: Named
Default value: (Get-AzLocation)[0].Location
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="2b4b9-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2b4b9-122">-ResourceGroupName</span></span>
<span data-ttu-id="2b4b9-123">리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-123">The name of the resource group.</span></span>

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

### <span data-ttu-id="2b4b9-124">-SubscriptionId</span><span class="sxs-lookup"><span data-stu-id="2b4b9-124">-SubscriptionId</span></span>
<span data-ttu-id="2b4b9-125">Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-125">Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span>
<span data-ttu-id="2b4b9-126">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-126">The subscription ID forms part of the URI for every service call.</span></span>

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

### <span data-ttu-id="2b4b9-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2b4b9-127">CommonParameters</span></span>
<span data-ttu-id="2b4b9-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2b4b9-129">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-129">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2b4b9-130">입력</span><span class="sxs-lookup"><span data-stu-id="2b4b9-130">INPUTS</span></span>

### <span data-ttu-id="2b4b9-131">InfrastructureInsightsAdmin. IInfrastructureInsightsAdminIdentity에 대 한 Microsoft PowerShell</span><span class="sxs-lookup"><span data-stu-id="2b4b9-131">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.IInfrastructureInsightsAdminIdentity</span></span>

## <span data-ttu-id="2b4b9-132">출력</span><span class="sxs-lookup"><span data-stu-id="2b4b9-132">OUTPUTS</span></span>

### <span data-ttu-id="2b4b9-133">InfrastructureInsightsAdmin. Api20160501. .Exe 지역/국가 상태</span><span class="sxs-lookup"><span data-stu-id="2b4b9-133">Microsoft.Azure.PowerShell.Cmdlets.InfrastructureInsightsAdmin.Models.Api20160501.IRegionHealth</span></span>



## <span data-ttu-id="2b4b9-134">상속자</span><span class="sxs-lookup"><span data-stu-id="2b4b9-134">NOTES</span></span>

<span data-ttu-id="2b4b9-135">복잡 한 매개 변수 속성 아래 설명 된 매개 변수를 만들려면 적절 한 속성을 포함 하는 해시 테이블을 생성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-135">COMPLEX PARAMETER PROPERTIES To create the parameters described below, construct a hash table containing the appropriate properties.</span></span> <span data-ttu-id="2b4b9-136">해시 테이블에 대 한 자세한 내용은 Get-Help about_Hash_Tables를 실행 하세요.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-136">For information on hash tables, run Get-Help about_Hash_Tables.</span></span>

<span data-ttu-id="2b4b9-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity> : Identity 매개 변수</span><span class="sxs-lookup"><span data-stu-id="2b4b9-137">INPUTOBJECT <IInfrastructureInsightsAdminIdentity>: Identity Parameter</span></span>
  - <span data-ttu-id="2b4b9-138">`[AlertName <String>]`: 경고의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-138">`[AlertName <String>]`: Name of the alert.</span></span>
  - <span data-ttu-id="2b4b9-139">`[Id <String>]`: 리소스 id 경로</span><span class="sxs-lookup"><span data-stu-id="2b4b9-139">`[Id <String>]`: Resource identity path</span></span>
  - <span data-ttu-id="2b4b9-140">`[Location <String>]`: 지역 이름</span><span class="sxs-lookup"><span data-stu-id="2b4b9-140">`[Location <String>]`: Name of the region</span></span>
  - <span data-ttu-id="2b4b9-141">`[ResourceGroupName <String>]`: 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-141">`[ResourceGroupName <String>]`: The name of the resource group.</span></span>
  - <span data-ttu-id="2b4b9-142">`[ResourceRegistrationId <String>]`: 리소스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-142">`[ResourceRegistrationId <String>]`: Resource registration ID.</span></span>
  - <span data-ttu-id="2b4b9-143">`[ServiceHealth <String>]`: 서비스 상태 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-143">`[ServiceHealth <String>]`: Service Health name.</span></span>
  - <span data-ttu-id="2b4b9-144">`[ServiceRegistrationId <String>]`: 서비스 등록 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-144">`[ServiceRegistrationId <String>]`: Service registration ID.</span></span>
  - <span data-ttu-id="2b4b9-145">`[SubscriptionId <String>]`: Microsoft Azure 구독을 고유 하 게 식별 하는 구독 자격 증명입니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-145">`[SubscriptionId <String>]`: Subscription credentials that uniquely identify Microsoft Azure subscription.</span></span> <span data-ttu-id="2b4b9-146">구독 ID는 모든 서비스 호출에 대 한 URI의 일부를 형성 합니다.</span><span class="sxs-lookup"><span data-stu-id="2b4b9-146">The subscription ID forms part of the URI for every service call.</span></span>

## <span data-ttu-id="2b4b9-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2b4b9-147">RELATED LINKS</span></span>

