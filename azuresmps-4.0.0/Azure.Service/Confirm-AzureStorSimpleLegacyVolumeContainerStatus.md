---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 97AC691F-3835-4CEE-B47E-430BE9962AF9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 26fcee5f6cb669ef49993a009aa76e9c9522b180
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045700"
---
# <span data-ttu-id="b0a6e-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="b0a6e-101">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>

## <span data-ttu-id="b0a6e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b0a6e-102">SYNOPSIS</span></span>
<span data-ttu-id="b0a6e-103">마이그레이션된 볼륨 컨테이너의 커밋 또는 롤백을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-103">Initiates the commit or rollback of the volume containers that are migrated.</span></span>

## <span data-ttu-id="b0a6e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b0a6e-104">SYNTAX</span></span>

### <span data-ttu-id="b0a6e-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="b0a6e-105">MigrateSpecificContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="b0a6e-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="b0a6e-106">MigrateAllContainer</span></span>
```
Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId <String> -MigrationOperation <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="b0a6e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="b0a6e-107">DESCRIPTION</span></span>
<span data-ttu-id="b0a6e-108">**AzureStorSimpleLegacyVolumeContainerStatus** cmdlet은 레거시 마이그레이션의 일부로 마이그레이션된 볼륨 컨테이너의 커밋 또는 롤백을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-108">The **Confirm-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet initiates the commit or rollback of the volume containers that are migrated as part of a legacy migration.</span></span>
<span data-ttu-id="b0a6e-109">롤백은 기기를 원래 소유권으로 복원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-109">The rollback restores the appliance to the original ownership.</span></span>
<span data-ttu-id="b0a6e-110">커밋은 대상 기기에 소유권을 할당 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-110">The commit assigns the ownership to the target appliance.</span></span>

## <span data-ttu-id="b0a6e-111">예제의</span><span class="sxs-lookup"><span data-stu-id="b0a6e-111">EXAMPLES</span></span>

### <span data-ttu-id="b0a6e-112">예제 1: 특정 볼륨 컨테이너에서 커밋 작업 시작</span><span class="sxs-lookup"><span data-stu-id="b0a6e-112">Example 1: Initiate a commit operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Commit
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="b0a6e-113">이 명령은 지정 된 레거시 구성 ID에 대해 지정 된 볼륨 컨테이너에서 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-113">This command initiates a commit operation on the specified volume container for the specified legacy configuration ID.</span></span>
<span data-ttu-id="b0a6e-114">작업 상태를 확인 하려면 **AzureStorSimpleLegacyVolumeContainerStatus** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-114">To see the status of the operation, use the **Get-AzureStorSimpleLegacyVolumeContainerStatus** cmdlet.</span></span>

### <span data-ttu-id="b0a6e-115">예제 2: 특정 볼륨 컨테이너에서 롤백 작업 시작</span><span class="sxs-lookup"><span data-stu-id="b0a6e-115">Example 2: Initiate a rollback operation on a specific volume container</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud" -MigrationOperation Rollback
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="b0a6e-116">이 명령은 지정 된 레거시 구성 ID에 대해 지정 된 볼륨 컨테이너에서 롤백 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-116">This command initiates a rollback operation on the specified volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="b0a6e-117">예제 3: 모든 볼륨 컨테이너에서 커밋 작업 시작</span><span class="sxs-lookup"><span data-stu-id="b0a6e-117">Example 3: Initiate a commit operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Commit -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="b0a6e-118">이 명령은 모든 볼륨 컨테이너에서 지정 된 레거시 구성 ID에 대 한 커밋 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-118">This command initiates a commit operation on all volume container for the specified legacy configuration ID.</span></span>

### <span data-ttu-id="b0a6e-119">예제 4: 모든 볼륨 컨테이너에서 롤백 작업 시작</span><span class="sxs-lookup"><span data-stu-id="b0a6e-119">Example 4: Initiate a rollback operation on all volume containers</span></span>
```
PS C:\>Confirm-AzureStorSimpleLegacyVolumeContainerStatus -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -MigrationOperation Rollback -All
Please check the commit/discard status using Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus
```

<span data-ttu-id="b0a6e-120">이 명령은 모든 볼륨 컨테이너에서 지정 된 레거시 구성 ID에 대 한 롤백 작업을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-120">This command initiates a rollback operation on all volume containers for the specified legacy configuration ID.</span></span>

## <span data-ttu-id="b0a6e-121">변수</span><span class="sxs-lookup"><span data-stu-id="b0a6e-121">PARAMETERS</span></span>

### <span data-ttu-id="b0a6e-122">-All</span><span class="sxs-lookup"><span data-stu-id="b0a6e-122">-All</span></span>
<span data-ttu-id="b0a6e-123">이 cmdlet이 가져온 구성 파일의 모든 볼륨 컨테이너에 대해 롤백 또는 커밋 작업을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-123">Indicates that this cmdlet initiates a roll back or commit operation on all volume containers in the imported configuration file.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: MigrateAllContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a6e-124">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="b0a6e-124">-LegacyConfigId</span></span>
<span data-ttu-id="b0a6e-125">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-125">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="b0a6e-126">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="b0a6e-126">-LegacyContainerNames</span></span>
<span data-ttu-id="b0a6e-127">마이그레이션 계획이 적용 되는 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-127">Specifies an array of volume container names for which the migration plan applies.</span></span>

```yaml
Type: String[]
Parameter Sets: MigrateSpecificContainer
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b0a6e-128">-MigrationOperation</span><span class="sxs-lookup"><span data-stu-id="b0a6e-128">-MigrationOperation</span></span>
<span data-ttu-id="b0a6e-129">이 cmdlet이 커밋 또는 롤백을 수행할지 여부를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-129">Specifies whether this cmdlet performs a commit or rollback.</span></span>
<span data-ttu-id="b0a6e-130">유효한 값은 Commit 및 Rollback입니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-130">Valid values are: Commit and Rollback.</span></span>

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

### <span data-ttu-id="b0a6e-131">-프로필</span><span class="sxs-lookup"><span data-stu-id="b0a6e-131">-Profile</span></span>
<span data-ttu-id="b0a6e-132">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-132">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b0a6e-133">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-133">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b0a6e-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b0a6e-134">CommonParameters</span></span>
<span data-ttu-id="b0a6e-135">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b0a6e-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b0a6e-136">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b0a6e-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b0a6e-137">입력</span><span class="sxs-lookup"><span data-stu-id="b0a6e-137">INPUTS</span></span>

## <span data-ttu-id="b0a6e-138">출력</span><span class="sxs-lookup"><span data-stu-id="b0a6e-138">OUTPUTS</span></span>

## <span data-ttu-id="b0a6e-139">상속자</span><span class="sxs-lookup"><span data-stu-id="b0a6e-139">NOTES</span></span>

## <span data-ttu-id="b0a6e-140">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b0a6e-140">RELATED LINKS</span></span>

[<span data-ttu-id="b0a6e-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="b0a6e-141">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="b0a6e-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="b0a6e-142">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus.md)

[<span data-ttu-id="b0a6e-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="b0a6e-143">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


