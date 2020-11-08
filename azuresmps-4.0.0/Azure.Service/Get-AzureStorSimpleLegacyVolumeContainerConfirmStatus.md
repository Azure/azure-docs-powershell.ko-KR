---
external help file: Microsoft.WindowsAzure.Commands.StorSimple.dll-Help.xml
ms.assetid: 3B4630C1-9885-4BE4-B41E-D98AF5CCD7C3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 185072d1bc0d0895d4b6cfaea9470bac107d651a
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046553"
---
# <span data-ttu-id="7036a-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span><span class="sxs-lookup"><span data-stu-id="7036a-101">Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus</span></span>

## <span data-ttu-id="7036a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7036a-102">SYNOPSIS</span></span>
<span data-ttu-id="7036a-103">커밋 또는 롤백 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-103">Gets the status of a commit or rollback operation.</span></span>

## <span data-ttu-id="7036a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7036a-104">SYNTAX</span></span>

```
Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId <String>
 [-LegacyContainerNames <String[]>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="7036a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7036a-105">DESCRIPTION</span></span>
<span data-ttu-id="7036a-106">**Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet은 커밋 또는 롤백 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-106">The **Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus** cmdlet gets the status of the commit or rollback operation.</span></span>

## <span data-ttu-id="7036a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7036a-107">EXAMPLES</span></span>

### <span data-ttu-id="7036a-108">예제 1: 완료 된 커밋 작업의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="7036a-108">Example 1: Get the status of a completed commit operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Commit
                             PercentageCompleted    : 100
                             Messages               : 

CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : None
RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="7036a-109">이 명령은 명명 된 컨테이너에 대 한 커밋 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-109">This command gets the status of a commit operation for the named container.</span></span>
<span data-ttu-id="7036a-110">이 작업의 상태가 완료 됨입니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-110">This operation has a status of completed.</span></span>

### <span data-ttu-id="7036a-111">예제 2: 완료 된 롤백 작업의 상태 가져오기</span><span class="sxs-lookup"><span data-stu-id="7036a-111">Example 2: Get the status of a completed rollback operation</span></span>
```
PS C:\>Get-AzureStorSimpleLegacyVolumeContainerConfirmStatus -LegacyConfigId "f16463bd-94a9-4c3c-91c2-7a3ba7120087" -LegacyContainerNames "OneSDKAzureCloud"
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 2bda2b9b-1361-4787-bc04-1e081218ed76_PS
VERBOSE: 2015-04-08 13:51:01 ClientRequestId: 84bf18d8-c459-47a7-b4a8-f82ca8659672_PS
VERBOSE: 2015-04-08 13:51:12 ClientRequestId: e93f9cb7-df58-497e-bb9f-9a6a23e68925_PS


LegacyConfigId             : f16463bd-94a9-4c3c-91c2-7a3ba7120087
CommitComplete             : None
CommitInProgress           : None
CommitFailed               : None
RollbackComplete           : CloudConfigurationName : OneSDKAzureCloud
                             Operation              : Rollback
                             PercentageCompleted    : 100
                             Messages               : 

RollbackInProgress         : None
RollbackFailed             : None
CommitOrRollbackNotStarted : None
```

<span data-ttu-id="7036a-112">이 명령은 명명 된 컨테이너에 대 한 롤백 작업의 상태를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-112">This command gets the status of a rollback operation for the named container.</span></span>
<span data-ttu-id="7036a-113">이 작업의 상태가 완료 됨입니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-113">This operation has a status of completed.</span></span>

## <span data-ttu-id="7036a-114">변수</span><span class="sxs-lookup"><span data-stu-id="7036a-114">PARAMETERS</span></span>

### <span data-ttu-id="7036a-115">-LegacyConfigId</span><span class="sxs-lookup"><span data-stu-id="7036a-115">-LegacyConfigId</span></span>
<span data-ttu-id="7036a-116">레거시 기기의 구성에 대 한 고유 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-116">Specifies the unique ID of the configuration of the legacy appliance.</span></span>

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

### <span data-ttu-id="7036a-117">-LegacyContainerNames</span><span class="sxs-lookup"><span data-stu-id="7036a-117">-LegacyContainerNames</span></span>
<span data-ttu-id="7036a-118">마이그레이션 계획이 적용 되는 볼륨 컨테이너 이름의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-118">Specifies an array of volume container names for which the migration plan applies.</span></span>

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

### <span data-ttu-id="7036a-119">-프로필</span><span class="sxs-lookup"><span data-stu-id="7036a-119">-Profile</span></span>
<span data-ttu-id="7036a-120">Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-120">Specifies an Azure profile.</span></span>

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

### <span data-ttu-id="7036a-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7036a-121">CommonParameters</span></span>
<span data-ttu-id="7036a-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7036a-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7036a-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7036a-124">입력</span><span class="sxs-lookup"><span data-stu-id="7036a-124">INPUTS</span></span>

### <span data-ttu-id="7036a-125">않아야</span><span class="sxs-lookup"><span data-stu-id="7036a-125">None</span></span>

## <span data-ttu-id="7036a-126">출력</span><span class="sxs-lookup"><span data-stu-id="7036a-126">OUTPUTS</span></span>

### <span data-ttu-id="7036a-127">ConfirmMigrationStatusMsg</span><span class="sxs-lookup"><span data-stu-id="7036a-127">ConfirmMigrationStatusMsg</span></span>
<span data-ttu-id="7036a-128">이 cmdlet은 수행 되는 마이그레이션 확인 작업의 상태를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="7036a-128">This cmdlet returns the status of the confirm migration operation that is performed.</span></span>

## <span data-ttu-id="7036a-129">상속자</span><span class="sxs-lookup"><span data-stu-id="7036a-129">NOTES</span></span>

## <span data-ttu-id="7036a-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7036a-130">RELATED LINKS</span></span>

[<span data-ttu-id="7036a-131">확인-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="7036a-131">Confirm-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Confirm-AzureStorSimpleLegacyVolumeContainerStatus.md)

[<span data-ttu-id="7036a-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span><span class="sxs-lookup"><span data-stu-id="7036a-132">Get-AzureStorSimpleLegacyVolumeContainerStatus</span></span>](./Get-AzureStorSimpleLegacyVolumeContainerStatus.md)


