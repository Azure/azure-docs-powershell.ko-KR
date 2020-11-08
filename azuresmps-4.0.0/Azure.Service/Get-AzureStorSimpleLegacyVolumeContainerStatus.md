---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: A736738A-C6B3-4E5A-B9BA-D6559A27A667
online version: ''
schema: 2.0.0
ms.openlocfilehash: a95e604c6c3f6766ccfc89bd9018dbe2241fb5b5
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046550"
---
# <span data-ttu-id="4be02-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="4be02-101">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="4be02-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4be02-102">SYNOPSIS</span></span>
<span data-ttu-id="4be02-103">볼륨 컨테이너의 마이그레이션 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-103">Gets the migration status of the volume containers.</span></span>

## <span data-ttu-id="4be02-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4be02-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> [-LegacyContainerNames <String[]>]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="4be02-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4be02-105">DESCRIPTION</span></span>
<span data-ttu-id="4be02-106">**Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet은 볼륨 컨테이너의 마이그레이션 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-106">The **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet gets the migration status of the volume containers.</span></span>
<span data-ttu-id="4be02-107">이 cmdlet은 볼륨 컨테이너 마이그레이션이 아직 진행 중이거나, 완료 되었거나, 실패 했는지 여부를 포함 하는 상태 정보를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-107">This cmdlet returns status information which includes whether the volume container migration is still in progress, completed, or failed.</span></span>

## <span data-ttu-id="4be02-108">예제의</span><span class="sxs-lookup"><span data-stu-id="4be02-108">EXAMPLES</span></span>

### <span data-ttu-id="4be02-109">예제 1: 실패 한 마이그레이션 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="4be02-109">Example 1: Get status for a failed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : No Cloud Configuration(s)  are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : Cloud Configuration Name: OneSDKAzureCloud
                       PercentageCompleted : 0
                       MigrationStatus : Failed
                       No Backup sets found
```

<span data-ttu-id="4be02-110">이 명령은 명명 된 레거시 컨테이너에 대 한 마이그레이션 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-110">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="4be02-111">결과에는 마이그레이션이 실패 한 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-111">The results show that the migration failed.</span></span>

### <span data-ttu-id="4be02-112">예제 2: 진행 중인 마이그레이션 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="4be02-112">Example 2: Get status for a migration in progress</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4" -LegacyContainerNames "OneSDKAzureCloud"
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : No Cloud Configuration(s) are found to be in Completed state of Migration
MigrationInprogress  : CloudConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 10
                       MigrationStatus : InProgress
                       BackupSets : 
                           Policy : OneSDKBackupPolicy, Status : InProgress
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="4be02-113">이 명령은 명명 된 레거시 컨테이너에 대 한 마이그레이션 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-113">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="4be02-114">결과에는 마이그레이션이 진행 되 고 있는 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-114">The results show that the migration is in progress.</span></span>

### <span data-ttu-id="4be02-115">예제 3: 완료 된 마이그레이션 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="4be02-115">Example 3: Get status for a completed migration</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId dcddbb51-2ab2-4d22-8204-fefdbd6b7ba4 -LegacyContainerNames OneSDKAzureCloud
ConfigId             : 5a83ec88-9e0a-4722-9fb0-9131caa7387a
MigrationCompleted   : Cloud ConfigurationName: OneSDKAzureCloud
                       PercentageCompleted : 100
                       MigrationStatus : Completed
                       BackupSets : 
                          Policy : vg1p1, Created On : 04/06/2015 11:22:00, Status : Completed
                          Policy : vg1p1, Created On : 03/30/2015 11:22:00, Status : Completed
                          Policy : c1v1-Auto-Daily-CloudSnapshot, Created On : 03/30/2015 03:30:00, Status : Completed
MigrationInprogress  : No Cloud Configuration(s) are found to be in InProgress state of Migration
MigrationNotStarted  : No Cloud Configuration(s) are found to be in NotStarted state of Migration
MigrationFailed      : No Cloud Configuration(s) are found to be in Failed state of Migration
```

<span data-ttu-id="4be02-116">이 명령은 명명 된 레거시 컨테이너에 대 한 마이그레이션 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-116">This command gets the migration status for the named legacy container.</span></span>
<span data-ttu-id="4be02-117">결과에는 마이그레이션이 완료 된 것으로 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-117">The results show that the migration is completed.</span></span>

## <span data-ttu-id="4be02-118">변수</span><span class="sxs-lookup"><span data-stu-id="4be02-118">PARAMETERS</span></span>

### <span data-ttu-id="4be02-119">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="4be02-119">-LegacyConfigId</span></span>
<span data-ttu-id="4be02-120">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-120">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4be02-121">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="4be02-121">-LegacyContainerNames</span></span>
<span data-ttu-id="4be02-122">마이그레이션 계획이 적용 되는 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-122">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="4be02-123">-프로필</span><span class="sxs-lookup"><span data-stu-id="4be02-123">-Profile</span></span>
<span data-ttu-id="4be02-124">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-124">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="4be02-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4be02-125">CommonParameters</span></span>
<span data-ttu-id="4be02-126">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4be02-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4be02-127">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4be02-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4be02-128">입력</span><span class="sxs-lookup"><span data-stu-id="4be02-128">INPUTS</span></span>

## <span data-ttu-id="4be02-129">출력</span><span class="sxs-lookup"><span data-stu-id="4be02-129">OUTPUTS</span></span>

## <span data-ttu-id="4be02-130">상속자</span><span class="sxs-lookup"><span data-stu-id="4be02-130">NOTES</span></span>

## <span data-ttu-id="4be02-131">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4be02-131">RELATED LINKS</span></span>

[<span data-ttu-id="4be02-132">확인-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="4be02-132">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="4be02-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="4be02-133">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)


