---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 6F31F2B4-6131-4B11-B074-CA05CE3A56F1
online version: ''
schema: 2.0.0
ms.openlocfilehash: f928ecba8f92badc1eb87e47aee16515f1684fce
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94045773"
---
# <span data-ttu-id="39ce4-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="39ce4-101">Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>

## <span data-ttu-id="39ce4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="39ce4-102">SYNOPSIS</span></span>
<span data-ttu-id="39ce4-103">마이그레이션 계획 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-103">Starts the creation of a migration plan.</span></span>

## <span data-ttu-id="39ce4-104">구문과</span><span class="sxs-lookup"><span data-stu-id="39ce4-104">SYNTAX</span></span>

### <span data-ttu-id="39ce4-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="39ce4-105">MigrateSpecificContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String>
 -LegacyContainerNames <String[]> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="39ce4-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="39ce4-106">MigrateAllContainer</span></span>
```
Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId <String> [-All]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="39ce4-107">설명은</span><span class="sxs-lookup"><span data-stu-id="39ce4-107">DESCRIPTION</span></span>
<span data-ttu-id="39ce4-108">**AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet은 마이그레이션 계획 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-108">The **Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet starts the creation of a migration plan.</span></span>
<span data-ttu-id="39ce4-109">마이그레이션 계획 만들기는 비동기입니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-109">The creation of a migration plan is asynchronous.</span></span>
<span data-ttu-id="39ce4-110">마이그레이션 계획의 상태를 보려면 **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-110">To see the status of the migration plan, use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet.</span></span>

## <span data-ttu-id="39ce4-111">예제의</span><span class="sxs-lookup"><span data-stu-id="39ce4-111">EXAMPLES</span></span>

### <span data-ttu-id="39ce4-112">예제 1: 마이그레이션 계획 시작</span><span class="sxs-lookup"><span data-stu-id="39ce4-112">Example 1: Start a migration plan</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="39ce4-113">이 명령은 OneSDKAzureCloud 이라는 레거시 컨테이너에 대 한 마이그레이션 계획 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-113">This command starts creation of a migration plan for the legacy container named OneSDKAzureCloud.</span></span>
<span data-ttu-id="39ce4-114">이 명령은 계획의 상태에 대 한 메시지를 반환 하 고 최신 정보에 대 한 **AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-114">The command returns a message about the status of the plan, and to use the **Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan** cmdlet for up to date information.</span></span>

### <span data-ttu-id="39ce4-115">예제 2: 모든 볼륨 컨테이너에 대 한 마이그레이션 계획 시작</span><span class="sxs-lookup"><span data-stu-id="39ce4-115">Example 2: Start migration plan for all volume containers</span></span>
```
PS C:\>Start-AzureStorSimpleLegacyVolumeContainerMigrationPlan -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Successfully started estimating the Migration Plan. Please check details with Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan
```

<span data-ttu-id="39ce4-116">이 명령은 가져온 구성 파일의 모든 레거시 볼륨 컨테이너에 대 한 마이그레이션 계획 만들기를 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-116">This command starts creation of migration plan for all legacy volume containers in the configuration file that is imported.</span></span>

## <span data-ttu-id="39ce4-117">변수</span><span class="sxs-lookup"><span data-stu-id="39ce4-117">PARAMETERS</span></span>

### <span data-ttu-id="39ce4-118">-All</span><span class="sxs-lookup"><span data-stu-id="39ce4-118">-All</span></span>
<span data-ttu-id="39ce4-119">이 cmdlet이 가져온 구성 파일의 모든 볼륨 컨테이너에 대 한 마이그레이션 시간 예상을 시작 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-119">Indicates that this cmdlet starts migration time estimates for all volume containers in the imported configuration file.</span></span>

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

### <span data-ttu-id="39ce4-120">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="39ce4-120">-LegacyConfigId</span></span>
<span data-ttu-id="39ce4-121">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-121">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="39ce4-122">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="39ce4-122">-LegacyContainerNames</span></span>
<span data-ttu-id="39ce4-123">마이그레이션 계획을 만들 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-123">Specifies an array of volume container names for which to create a migration plan.</span></span>

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

### <span data-ttu-id="39ce4-124">-프로필</span><span class="sxs-lookup"><span data-stu-id="39ce4-124">-Profile</span></span>
<span data-ttu-id="39ce4-125">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-125">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="39ce4-126">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-126">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="39ce4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="39ce4-127">CommonParameters</span></span>
<span data-ttu-id="39ce4-128">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="39ce4-129">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="39ce4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="39ce4-130">입력</span><span class="sxs-lookup"><span data-stu-id="39ce4-130">INPUTS</span></span>

### <span data-ttu-id="39ce4-131">않아야</span><span class="sxs-lookup"><span data-stu-id="39ce4-131">None</span></span>

## <span data-ttu-id="39ce4-132">출력</span><span class="sxs-lookup"><span data-stu-id="39ce4-132">OUTPUTS</span></span>

### <span data-ttu-id="39ce4-133">이름</span><span class="sxs-lookup"><span data-stu-id="39ce4-133">String</span></span>
<span data-ttu-id="39ce4-134">이 cmdlet은 기기에서 성공적으로 시작 된 마이그레이션 계획 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="39ce4-134">This cmdlet returns the status of the migration plan job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="39ce4-135">상속자</span><span class="sxs-lookup"><span data-stu-id="39ce4-135">NOTES</span></span>

## <span data-ttu-id="39ce4-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="39ce4-136">RELATED LINKS</span></span>

[<span data-ttu-id="39ce4-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span><span class="sxs-lookup"><span data-stu-id="39ce4-137">Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerMigrationPlan.md)


