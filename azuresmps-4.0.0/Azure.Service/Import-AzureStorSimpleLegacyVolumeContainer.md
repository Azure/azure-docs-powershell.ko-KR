---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 23272A36-8F55-41A8-AFC9-2EEE0FA55DA3
online version: ''
schema: 2.0.0
ms.openlocfilehash: bd341437019b6adbe6c2a5a93076baff61e1f0d7
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046258"
---
# <span data-ttu-id="d889e-101">Import-AzureStorSimpleLegacyVolumeContainer</span><span class="sxs-lookup"><span data-stu-id="d889e-101">Import-AzureStorSimpleLegacyVolumeContainer</span></span>

## <span data-ttu-id="d889e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d889e-102">SYNOPSIS</span></span>
<span data-ttu-id="d889e-103">볼륨 컨테이너의 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-103">Starts the migration of volume containers.</span></span>

## <span data-ttu-id="d889e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d889e-104">SYNTAX</span></span>

### <span data-ttu-id="d889e-105">MigrateSpecificContainer</span><span class="sxs-lookup"><span data-stu-id="d889e-105">MigrateSpecificContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> -LegacyContainerNames <String[]>
 [-SkipACRs] [-Force] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="d889e-106">MigrateAllContainer</span><span class="sxs-lookup"><span data-stu-id="d889e-106">MigrateAllContainer</span></span>
```
Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId <String> [-All] [-SkipACRs] [-Force]
 [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="d889e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="d889e-107">DESCRIPTION</span></span>
<span data-ttu-id="d889e-108">**AzureStorSimpleLegacyVolumeContainer** cmdlet은 레거시 기기에서 대상 기기로 볼륨 컨테이너의 마이그레이션을 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-108">The **Import-AzureStorSimpleLegacyVolumeContainer** cmdlet starts the migration of volume containers from a legacy appliance to the target appliance.</span></span>

## <span data-ttu-id="d889e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="d889e-109">EXAMPLES</span></span>

### <span data-ttu-id="d889e-110">예제 1: 레거시 볼륨 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="d889e-110">Example 1: Import a legacy volume container</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -LegacyContainerNames "OneSDKAzureCloud"
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="d889e-111">이 명령은 명명 된 컨테이너에 대 한 레거시 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-111">This command imports a legacy volume container for the named container.</span></span>
<span data-ttu-id="d889e-112">Cmdlet에서 가져오기를 시작한 다음 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-112">The cmdlet starts the import, and then returns a message.</span></span>

### <span data-ttu-id="d889e-113">예제 2: 모든 레거시 볼륨 컨테이너 가져오기</span><span class="sxs-lookup"><span data-stu-id="d889e-113">Example 2: Import all legacy volume containers</span></span>
```
PS C:\>Import-AzureStorSimpleLegacyVolumeContainer -LegacyConfigId "c5a831e1-7888-44f4-adf1-92994be630c3" -All
Import started, Please check status with Get-AzureStorSimpleLegacyVolumeContainerStatus commandlet
```

<span data-ttu-id="d889e-114">이 명령은 가져온 구성 파일에서 모든 레거시 볼륨 컨테이너를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-114">This command imports all legacy volume containers from configuration file imported.</span></span>
<span data-ttu-id="d889e-115">Cmdlet에서 가져오기를 시작한 다음 메시지를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-115">The cmdlet starts the import, and then returns a message.</span></span>

## <span data-ttu-id="d889e-116">변수</span><span class="sxs-lookup"><span data-stu-id="d889e-116">PARAMETERS</span></span>

### <span data-ttu-id="d889e-117">-All</span><span class="sxs-lookup"><span data-stu-id="d889e-117">-All</span></span>
<span data-ttu-id="d889e-118">이 cmdlet이 가져온 구성 파일의 모든 볼륨 컨테이너를 대상 장치로 가져오도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-118">Indicates that this cmdlet imports all volume containers in the imported configuration file to the target device.</span></span>

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

### <span data-ttu-id="d889e-119">-Force</span><span class="sxs-lookup"><span data-stu-id="d889e-119">-Force</span></span>
<span data-ttu-id="d889e-120">다른 장치에서 볼륨 컨테이너를 가져온 경우에도이 cmdlet이 다른 디바이스의 볼륨 컨테이너를 가져오도록 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-120">Indicates that this cmdlet imports volume container on a different device, even if volume container has been imported on a different device.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d889e-121">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="d889e-121">-LegacyConfigId</span></span>
<span data-ttu-id="d889e-122">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-122">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="d889e-123">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="d889e-123">-LegacyContainerNames</span></span>
<span data-ttu-id="d889e-124">마이그레이션 계획이 적용 되는 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-124">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="d889e-125">-프로필</span><span class="sxs-lookup"><span data-stu-id="d889e-125">-Profile</span></span>
<span data-ttu-id="d889e-126">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-126">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="d889e-127">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-127">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="d889e-128">-SkipACRs</span><span class="sxs-lookup"><span data-stu-id="d889e-128">-SkipACRs</span></span>
<span data-ttu-id="d889e-129">가져오기 프로세스가 마이그레이션에 대 한 액세스 제어 레코드를 생략 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-129">Indicates that the import process skips access control records for migration.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d889e-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d889e-130">CommonParameters</span></span>
<span data-ttu-id="d889e-131">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d889e-132">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d889e-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d889e-133">입력</span><span class="sxs-lookup"><span data-stu-id="d889e-133">INPUTS</span></span>

## <span data-ttu-id="d889e-134">출력</span><span class="sxs-lookup"><span data-stu-id="d889e-134">OUTPUTS</span></span>

### <span data-ttu-id="d889e-135">이름</span><span class="sxs-lookup"><span data-stu-id="d889e-135">String</span></span>
<span data-ttu-id="d889e-136">이 명령은 기기에서 성공적으로 시작 되 면 마이그레이션 볼륨 컨테이너 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="d889e-136">This command returns the status of the migration import volume container job if it has been successfully started in the appliance.</span></span>

## <span data-ttu-id="d889e-137">상속자</span><span class="sxs-lookup"><span data-stu-id="d889e-137">NOTES</span></span>

## <span data-ttu-id="d889e-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d889e-138">RELATED LINKS</span></span>

[<span data-ttu-id="d889e-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="d889e-139">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="d889e-140">가져오기-AzureStorSimpleLegacyApplianceConfig</span><span class="sxs-lookup"><span data-stu-id="d889e-140">Import-AzureStorSimpleLegacyApplianceConfig</span></span>](./Import-AzureStorSimpleLegacyApplianceConfig.md)


