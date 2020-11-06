---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: AzureRM.RecoveryServices.SiteRecovery
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices.siterecovery/get-azurermrecoveryservicesasrevent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrEvent.md
ms.openlocfilehash: e32f0b1d12b1cb0399ddef04623ac76557c809b5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532684"
---
# <span data-ttu-id="d178c-101">Get-AzureRmRecoveryServicesAsrEvent</span><span class="sxs-lookup"><span data-stu-id="d178c-101">Get-AzureRmRecoveryServicesAsrEvent</span></span>

## <span data-ttu-id="d178c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d178c-102">SYNOPSIS</span></span>
<span data-ttu-id="d178c-103">자격 증명 모음에 있는 Azure Site Recovery 이벤트의 세부 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-103">Gets details of Azure Site Recovery events in the vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d178c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d178c-104">SYNTAX</span></span>

### <span data-ttu-id="d178c-105">ByParam (기본값)</span><span class="sxs-lookup"><span data-stu-id="d178c-105">ByParam (Default)</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent [-AffectedObjectFriendlyName <String>] [-Fabric <ASRFabric>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d178c-106">ByResourceId</span><span class="sxs-lookup"><span data-stu-id="d178c-106">ByResourceId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -ResourceId <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="d178c-107">ByFabricId</span><span class="sxs-lookup"><span data-stu-id="d178c-107">ByFabricId</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -FabricId <String> [-AffectedObjectFriendlyName <String>]
 [-Severity <String>] [-StartTime <DateTime>] [-EndTime <DateTime>] [-EventType <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="d178c-108">ByName</span><span class="sxs-lookup"><span data-stu-id="d178c-108">ByName</span></span>
```
Get-AzureRmRecoveryServicesAsrEvent -Name <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="d178c-109">설명은</span><span class="sxs-lookup"><span data-stu-id="d178c-109">DESCRIPTION</span></span>
<span data-ttu-id="d178c-110">**Get-AzureRmRecoveryServicesAsrEvent** 는 지정 된 선택 필터에 따라 자격 증명 모음에 있는 이벤트 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-110">The **Get-AzureRmRecoveryServicesAsrEvent** gets the list of events in the vault based on the specified selection filters.</span></span>

## <span data-ttu-id="d178c-111">예제의</span><span class="sxs-lookup"><span data-stu-id="d178c-111">EXAMPLES</span></span>

### <span data-ttu-id="d178c-112">예제 1</span><span class="sxs-lookup"><span data-stu-id="d178c-112">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent
```

<span data-ttu-id="d178c-113">모든 이벤트의 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-113">List of all events.</span></span>

### <span data-ttu-id="d178c-114">예제 2</span><span class="sxs-lookup"><span data-stu-id="d178c-114">Example 2</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -EventName "VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f"


AffectedObjectFriendlyName   : V2A-W2K12-400
Description                  : Virtual machine health is in Critical state.
EventCode                    : SRSVMHealthChanged
EventSpecificDetails         :
EventType                    : AgentHealth
FabricId                     : /Subscriptions/xxxxxxxxxxxxxxxxx/resourceGroups/xxxxxxxxxxxx/providers/Microsoft.RecoveryServices/vaults/xxxxxxxxxxxxxxxx/replicationFabrics/xxxxxxxxxxxx
HealthErrors                 : {}
Name                         : VmMonitoringEvent;9091897569816476200_84576304-bafc-4714-8ba6-197a5d09d84f
ProviderSpecificEventDetails : Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRInMageAzureV2EventDetails
Severity                     : Critical
TimeOfOccurence              : 8/17/2017 12:31:43 PM
```

<span data-ttu-id="d178c-115">이름을 기준으로 이벤트를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-115">Get event by name.</span></span>

### <span data-ttu-id="d178c-116">예제 3</span><span class="sxs-lookup"><span data-stu-id="d178c-116">Example 3</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxxx
```

<span data-ttu-id="d178c-117">영향을 받는 개체에 대 한 이벤트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-117">List of event for affected Object.</span></span>

### <span data-ttu-id="d178c-118">예제 4</span><span class="sxs-lookup"><span data-stu-id="d178c-118">Example 4</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesAsrEvent -AffectedObjectName xxxxxxxxxxxx -StartTime "8/17/2017 12:31:40 PM" -EndTime "8/17/2017 12:31:44 PM" -Severity Critical -EventType VmHealth
```

<span data-ttu-id="d178c-119">시간 시작 시간 및 종료 시간, 심각도 위험 및 상태 유형 VmHealth 사이의 이벤트 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-119">List of event between time start time and end time , severity critical and health type VmHealth.</span></span>

## <span data-ttu-id="d178c-120">변수</span><span class="sxs-lookup"><span data-stu-id="d178c-120">PARAMETERS</span></span>

### <span data-ttu-id="d178c-121">-AffectedObjectFriendlyName</span><span class="sxs-lookup"><span data-stu-id="d178c-121">-AffectedObjectFriendlyName</span></span>
<span data-ttu-id="d178c-122">검색에 대 한 AffectedObject FriendlyName을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-122">Specifies AffectedObject FriendlyName for the search.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d178c-123">-DefaultProfile</span></span>
<span data-ttu-id="d178c-124">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-124">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-125">-EndTime</span><span class="sxs-lookup"><span data-stu-id="d178c-125">-EndTime</span></span>
<span data-ttu-id="d178c-126">검색 창의 종료 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-126">Specifies the end time of the search window.</span></span> <span data-ttu-id="d178c-127">이 매개 변수를 사용 하 여 지정 된 시간 이전에 발생 한 이벤트만 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-127">Use this parameter to get only those events that have occurred before the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-128">-EventType</span><span class="sxs-lookup"><span data-stu-id="d178c-128">-EventType</span></span>
<span data-ttu-id="d178c-129">이벤트 유형별로 이벤트를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-129">Filter events by the event type.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: VmHealth, ServerHealth, AgentHealth

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-130">-패브릭</span><span class="sxs-lookup"><span data-stu-id="d178c-130">-Fabric</span></span>
<span data-ttu-id="d178c-131">지정 된 패브릭에 따라 이벤트를 필터링 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-131">Filter events by the specified fabric.</span></span>

```yaml
Type: ASRFabric
Parameter Sets: ByParam
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-132">-FabricId</span><span class="sxs-lookup"><span data-stu-id="d178c-132">-FabricId</span></span>
<span data-ttu-id="d178c-133">필터링 할 fabricId를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-133">Specifies the fabricId to filter.</span></span>

```yaml
Type: String
Parameter Sets: ByFabricId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-134">-이름</span><span class="sxs-lookup"><span data-stu-id="d178c-134">-Name</span></span>
<span data-ttu-id="d178c-135">검색할 이벤트의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-135">Specifies name of the event for search.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-136">-ResourceId</span><span class="sxs-lookup"><span data-stu-id="d178c-136">-ResourceId</span></span>
<span data-ttu-id="d178c-137">이벤트에 대 한 이벤트의 ReourceId를 발생 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-137">Specifes the event ReourceId of event.</span></span>

```yaml
Type: String
Parameter Sets: ByResourceId
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-138">-심각도</span><span class="sxs-lookup"><span data-stu-id="d178c-138">-Severity</span></span>
<span data-ttu-id="d178c-139">필터링 할 이벤트 심각도입니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-139">Event severity to filter on.</span></span>

```yaml
Type: String
Parameter Sets: ByParam, ByFabricId
Aliases:
Accepted values: Critical, Warning, OK, Unknown

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-140">-StartTime</span><span class="sxs-lookup"><span data-stu-id="d178c-140">-StartTime</span></span>
<span data-ttu-id="d178c-141">검색 창의 시작 시간을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-141">Specifies the start time of the search window.</span></span> <span data-ttu-id="d178c-142">이 매개 변수를 사용 하 여 지정 된 시간 이후에 발생 한 이벤트만 가져올 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-142">Use this parameter to get only those events that have occurred after the specified time.</span></span>

```yaml
Type: DateTime
Parameter Sets: ByParam, ByFabricId
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d178c-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d178c-143">CommonParameters</span></span>
<span data-ttu-id="d178c-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d178c-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d178c-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d178c-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d178c-146">입력</span><span class="sxs-lookup"><span data-stu-id="d178c-146">INPUTS</span></span>

### <span data-ttu-id="d178c-147">SiteRecovery. r m m a m</span><span class="sxs-lookup"><span data-stu-id="d178c-147">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRFabric</span></span>

## <span data-ttu-id="d178c-148">출력</span><span class="sxs-lookup"><span data-stu-id="d178c-148">OUTPUTS</span></span>

### <span data-ttu-id="d178c-149">System.webserver. t e 1 [[SiteRecovery] [[Microsoft Azure. ASREvent, SiteRecovery, Version = 0.1.0.0, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="d178c-149">System.Collections.Generic.IEnumerable\`1[[Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASREvent, Microsoft.Azure.Commands.RecoveryServices.SiteRecovery, Version=0.1.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="d178c-150">상속자</span><span class="sxs-lookup"><span data-stu-id="d178c-150">NOTES</span></span>

## <span data-ttu-id="d178c-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d178c-151">RELATED LINKS</span></span>
