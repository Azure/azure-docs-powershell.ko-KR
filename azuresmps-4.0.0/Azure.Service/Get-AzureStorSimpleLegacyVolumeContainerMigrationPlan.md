---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: E4F6D096-E265-49CF-AA73-E9C807F8383B
online version: ''
schema: 2.0.0
ms.openlocfilehash: b0207d4b7eddfe56a8e4e86aac6899d19c10f44e
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045556"
---
# <span data-ttu-id="04200-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="04200-101">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="04200-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="04200-102">SYNOPSIS</span></span>
<span data-ttu-id="04200-103">레거시 컨테이너에 대 한 마이그레이션 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04200-103">Gets migration plans for legacy containers.</span></span>

## <span data-ttu-id="04200-104">구문과</span><span class="sxs-lookup"><span data-stu-id="04200-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan [-LegacyConfigId <String>]
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="04200-105">설명은</span><span class="sxs-lookup"><span data-stu-id="04200-105">DESCRIPTION</span></span>
<span data-ttu-id="04200-106">**Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet은 레거시 컨테이너에 대 한 마이그레이션 계획을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04200-106">The **Get-AzureStorSimpleLEgacyVolumeContainerMigrationPlan** cmdlet gets migration plans for legacy containers.</span></span>
<span data-ttu-id="04200-107">레거시 구성 ID를 기준으로 마이그레이션 계획을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-107">Specify a migration plan by its legacy configuration ID.</span></span>
<span data-ttu-id="04200-108">마이그레이션 계획 만들기가 아직 진행 중인 경우이 cmdlet은 마이그레이션 계획의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04200-108">If creation of the migration plan is still in progress, this cmdlet gets the status of the migration plan.</span></span>
<span data-ttu-id="04200-109">마이그레이션 계획이 완료 되 면이 cmdlet은 레거시 컨테이너 집합에 대 한 실제 마이그레이션 계획을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-109">If the migration plan is completed, this cmdlet returns the actual migration plan for the set of legacy containers.</span></span>
<span data-ttu-id="04200-110">*LegacyConfigId* 매개 변수를 지정 하지 않으면이 cmdlet은 구성 id 목록을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-110">If you do not specify the *LegacyConfigId* parameter, this cmdlet returns a list of configuration IDs.</span></span>

## <span data-ttu-id="04200-111">예제의</span><span class="sxs-lookup"><span data-stu-id="04200-111">EXAMPLES</span></span>

### <span data-ttu-id="04200-112">예제 1: 계획의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="04200-112">Example 1: Get the status of a plan</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 51e413fd-c2c9-4108-88cd-a0e792eab80a_PS
VERBOSE: 2015-04-08 13:48:05 ClientRequestId: 4c6398ef-35a0-4d1c-931e-d9d45599a97a_PS
VERBOSE: 2015-04-08 13:48:17 ClientRequestId: ef7a7e35-6dff-46cd-9df3-cb5fa25d149e_PS
VERBOSE: Request Id : fd7e502f273885468f633a44567bcb3f, HttpResponse OK
VERBOSE: List of volume containers: 


LegacyConfigId                    : f16463bd-94a9-4c3c-91c2-7a3ba7120087
DeviceName                        : ARUNKM-N4
MigrationTimeEstimationCompleted  : CloudConfigurationName        : OneSDKAzureCloud
                                    EstimatedTimeForLatestBackup  : 15Minutes
                                    EstimatedTimeForAllBackups    : 15Minutes
                                    These estimates are assuming 20 MBps bandwidth. Refer to migration guide to re-calculate for lower bandwidths. 



MigrationTimeEstimationInProgress : None
MigrationTimeEstimationFailed     : None
MigrationTimeEstimationNotStarted : None
```

<span data-ttu-id="04200-113">이 명령은 마이그레이션 계획의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04200-113">This command gets the status of the migration plan.</span></span>
<span data-ttu-id="04200-114">상태에는 가정 된 대역폭, 예상 시간 및 관련 정보가 포함 됩니다.</span><span class="sxs-lookup"><span data-stu-id="04200-114">The status includes assumed bandwidth, estimated time and, related information.</span></span>

### <span data-ttu-id="04200-115">예제 2: 기존 요금제의 Id 가져오기</span><span class="sxs-lookup"><span data-stu-id="04200-115">Example 2: Get the IDs of existing plans</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 813da56c-0cfc-4325-80db-08ef32bdde1e_PS
VERBOSE: 2015-04-08 13:46:51 ClientRequestId: 9e7cf244-1894-490a-be02-749834a99318_PS
VERBOSE: List of LegacyConfig Ids on the resource: 

LegacyConfigId                                              DeviceName
--------------                                              ----------
1e1f10a0-3dff-4249-b847-4930061cd87a                        ARUNKM-N4
26d4096d-49b6-4102-b188-0446ece73c8b                        ARUNKM-N4
```

<span data-ttu-id="04200-116">이 명령은 마이그레이션 계획의 모든 구성 Id를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="04200-116">This command gets all the configuration IDs of migration plans.</span></span>

## <span data-ttu-id="04200-117">변수</span><span class="sxs-lookup"><span data-stu-id="04200-117">PARAMETERS</span></span>

### <span data-ttu-id="04200-118">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="04200-118">-LegacyConfigId</span></span>
<span data-ttu-id="04200-119">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-119">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04200-120">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="04200-120">-LegacyContainerNames</span></span>
<span data-ttu-id="04200-121">이 cmdlet이 마이그레이션 계획을 가져오는 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-121">Specifies an array of volume container names for which this cmdlet gets a migration plan.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04200-122">-프로필</span><span class="sxs-lookup"><span data-stu-id="04200-122">-Profile</span></span>
<span data-ttu-id="04200-123">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-123">Specifies an Azure profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="04200-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="04200-124">CommonParameters</span></span>
<span data-ttu-id="04200-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="04200-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="04200-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="04200-127">입력</span><span class="sxs-lookup"><span data-stu-id="04200-127">INPUTS</span></span>

### <span data-ttu-id="04200-128">않아야</span><span class="sxs-lookup"><span data-stu-id="04200-128">None</span></span>

## <span data-ttu-id="04200-129">출력</span><span class="sxs-lookup"><span data-stu-id="04200-129">OUTPUTS</span></span>

### <span data-ttu-id="04200-130">MigrationPlanMsg</span><span class="sxs-lookup"><span data-stu-id="04200-130">MigrationPlanMsg</span></span>
<span data-ttu-id="04200-131">이 cmdlet은 마이그레이션 계획 작업의 상태, 초당 메가 비트의 가정 된 대역폭, 예상 시간 (분)을 포함 하는 **MigrationPlanMsg** 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="04200-131">This cmdlet returns a **MigrationPlanMsg** object that contains the status of the migration plan job, assumed bandwidth in megabits per second, and estimated time in minutes.</span></span>

## <span data-ttu-id="04200-132">상속자</span><span class="sxs-lookup"><span data-stu-id="04200-132">NOTES</span></span>

## <span data-ttu-id="04200-133">관련 링크</span><span class="sxs-lookup"><span data-stu-id="04200-133">RELATED LINKS</span></span>

[<span data-ttu-id="04200-134">시작-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="04200-134">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


