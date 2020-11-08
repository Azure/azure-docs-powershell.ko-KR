---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: E214AFEB-90A6-4553-94D4-FBEA6ADE572E
online version: ''
schema: 2.0.0
ms.openlocfilehash: 7ee340c2302670628bb8a3893567d7f8a2da754f
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046440"
---
# <span data-ttu-id="81c96-101">Resume-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="81c96-101">Resume-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="81c96-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="81c96-102">SYNOPSIS</span></span>
<span data-ttu-id="81c96-103">일시 중단 된 사이트 복구 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-103">Resumes a suspended Site Recovery job.</span></span>

## <span data-ttu-id="81c96-104">구문과</span><span class="sxs-lookup"><span data-stu-id="81c96-104">SYNTAX</span></span>

### <span data-ttu-id="81c96-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="81c96-105">ByObject (Default)</span></span>
```
Resume-AzureSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="81c96-106">ById</span><span class="sxs-lookup"><span data-stu-id="81c96-106">ById</span></span>
```
Resume-AzureSiteRecoveryJob -Id <String> [-Comments <String>] [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="81c96-107">설명은</span><span class="sxs-lookup"><span data-stu-id="81c96-107">DESCRIPTION</span></span>
<span data-ttu-id="81c96-108">**AzureSiteRecoveryJob** cmdlet은 일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-108">The **Resume-AzureSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="81c96-109">예제의</span><span class="sxs-lookup"><span data-stu-id="81c96-109">EXAMPLES</span></span>

### <span data-ttu-id="81c96-110">예제 1: 모든 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="81c96-110">Example 1: Resume all jobs</span></span>
```
PS C:\> $Jobs = Get-AzureSiteRecoveryJob  
PS C:\> Resume-AzureSiteRecoveryJob -Job $Jobs
ID               : d16397fb-cdf1-4972-b677-c333f3c557b4
ClientRequestId  : 32ace403-0916-4967-83a1-529176bd6e88-2014-49-06 15:49:24Z-P
State            : Suspended
StateDescription : WaitingForManualAction
StartTime        : 10/6/2014 10:19:28 AM
EndTime          : 10/6/2014 10:19:31 AM
AllowedActions   : {Cancel, RestartTestFailoverCleanup}
Name             : Test failover
Tasks            : {Recovery plan preflight checks, Create test environment, All groups failover: Pre steps (1), 
                   Recovery plan failover...} 
Errors           : {}
```

<span data-ttu-id="81c96-111">첫 번째 명령은 **AzureSiteRecoveryJob** cmdlet을 사용 하 여 현재 사이트 복구 자격 증명 모음에 대 한 Azure Site recovery 작업을 모두 가져온 다음 결과를 $Jobs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-111">The first command gets all the Azure Site Recovery jobs for the current Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="81c96-112">두 번째 명령은 $Jobs에서 지정한 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-112">The second command resumes the job specified by $Jobs.</span></span>

## <span data-ttu-id="81c96-113">변수</span><span class="sxs-lookup"><span data-stu-id="81c96-113">PARAMETERS</span></span>

### <span data-ttu-id="81c96-114">-메모</span><span class="sxs-lookup"><span data-stu-id="81c96-114">-Comments</span></span>
<span data-ttu-id="81c96-115">작업 로그에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-115">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="81c96-116">-Id</span><span class="sxs-lookup"><span data-stu-id="81c96-116">-Id</span></span>
<span data-ttu-id="81c96-117">다시 시작할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-117">Specifies the ID of a job to resume.</span></span>

```yaml
Type: String
Parameter Sets: ById
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="81c96-118">-작업</span><span class="sxs-lookup"><span data-stu-id="81c96-118">-Job</span></span>
<span data-ttu-id="81c96-119">다시 시작할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-119">Specifies the job to resume.</span></span>

```yaml
Type: ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="81c96-120">-프로필</span><span class="sxs-lookup"><span data-stu-id="81c96-120">-Profile</span></span>
<span data-ttu-id="81c96-121">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-121">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="81c96-122">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-122">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="81c96-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="81c96-123">CommonParameters</span></span>
<span data-ttu-id="81c96-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="81c96-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="81c96-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="81c96-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="81c96-126">입력</span><span class="sxs-lookup"><span data-stu-id="81c96-126">INPUTS</span></span>

## <span data-ttu-id="81c96-127">출력</span><span class="sxs-lookup"><span data-stu-id="81c96-127">OUTPUTS</span></span>

## <span data-ttu-id="81c96-128">상속자</span><span class="sxs-lookup"><span data-stu-id="81c96-128">NOTES</span></span>

## <span data-ttu-id="81c96-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="81c96-129">RELATED LINKS</span></span>

[<span data-ttu-id="81c96-130">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="81c96-130">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="81c96-131">다시 시작-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="81c96-131">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="81c96-132">중지-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="81c96-132">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


