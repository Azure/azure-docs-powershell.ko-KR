---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: AE26EA0F-9D92-4FDF-92EF-CA33BF06C0DB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 68a97359e5181bbc27183c0c1dbb6f526fa2e529
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046076"
---
# <span data-ttu-id="53c9f-101">Restart-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="53c9f-101">Restart-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="53c9f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="53c9f-102">SYNOPSIS</span></span>
<span data-ttu-id="53c9f-103">사이트 복구 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-103">Restarts a Site Recovery job.</span></span>

## <span data-ttu-id="53c9f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="53c9f-104">SYNTAX</span></span>

### <span data-ttu-id="53c9f-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="53c9f-105">ByObject (Default)</span></span>
```
Restart-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="53c9f-106">ById</span><span class="sxs-lookup"><span data-stu-id="53c9f-106">ById</span></span>
```
Restart-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="53c9f-107">설명은</span><span class="sxs-lookup"><span data-stu-id="53c9f-107">DESCRIPTION</span></span>
<span data-ttu-id="53c9f-108">**AzureSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-108">The **Restart-AzureSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="53c9f-109">예제의</span><span class="sxs-lookup"><span data-stu-id="53c9f-109">EXAMPLES</span></span>

### <span data-ttu-id="53c9f-110">예제 1: 작업 다시 시작</span><span class="sxs-lookup"><span data-stu-id="53c9f-110">Example 1: Restart a job</span></span>
```
PS C:\> Restart-AzureSiteRecoveryJob -Id "bbf0b839-9aaa-49e1-8354-601c9145966d"
ID               : bbf0b839-9aaa-49e1-8354-601c9145966d
ClientRequestId  : ef42c8b0-640c-4442-960b-349f83d161a5-2014-24-06 14:24:04Z-P
State            : Failed
StateDescription : Failed
StartTime        : 10/6/2014 9:41:08 AM
EndTime          : 10/6/2014 9:41:21 AM
AllowedActions   : {Cancel, Restart}
Name             : Enable protection
Tasks            : {Prerequisites check for enabling protection , Identifying replication target, Enable replication, 
                   Starting initial replication...} 
Errors           : {CreateProtectionTargetTask}
```

<span data-ttu-id="53c9f-111">이 명령은 지정 된 ID를 가진 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-111">This command restarts the job that has the specified ID.</span></span>

## <span data-ttu-id="53c9f-112">변수</span><span class="sxs-lookup"><span data-stu-id="53c9f-112">PARAMETERS</span></span>

### <span data-ttu-id="53c9f-113">-Id</span><span class="sxs-lookup"><span data-stu-id="53c9f-113">-Id</span></span>
<span data-ttu-id="53c9f-114">다시 시작할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-114">Specifies the ID of the job to restart.</span></span>

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

### <span data-ttu-id="53c9f-115">-작업</span><span class="sxs-lookup"><span data-stu-id="53c9f-115">-Job</span></span>
<span data-ttu-id="53c9f-116">다시 시작할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-116">Specifies the job to restart.</span></span>

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

### <span data-ttu-id="53c9f-117">-프로필</span><span class="sxs-lookup"><span data-stu-id="53c9f-117">-Profile</span></span>
<span data-ttu-id="53c9f-118">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-118">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="53c9f-119">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-119">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="53c9f-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="53c9f-120">CommonParameters</span></span>
<span data-ttu-id="53c9f-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="53c9f-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="53c9f-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="53c9f-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="53c9f-123">입력</span><span class="sxs-lookup"><span data-stu-id="53c9f-123">INPUTS</span></span>

## <span data-ttu-id="53c9f-124">출력</span><span class="sxs-lookup"><span data-stu-id="53c9f-124">OUTPUTS</span></span>

## <span data-ttu-id="53c9f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="53c9f-125">NOTES</span></span>

## <span data-ttu-id="53c9f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="53c9f-126">RELATED LINKS</span></span>

[<span data-ttu-id="53c9f-127">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="53c9f-127">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="53c9f-128">이력서-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="53c9f-128">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)

[<span data-ttu-id="53c9f-129">중지-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="53c9f-129">Stop-AzureSiteRecoveryJob</span></span>](./Stop-AzureSiteRecoveryJob.md)


