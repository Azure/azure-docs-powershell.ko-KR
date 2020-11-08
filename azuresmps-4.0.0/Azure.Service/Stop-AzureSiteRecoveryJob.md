---
external help file: Microsoft.Azure.Commands.RecoveryServicesRdfe.dll-Help.xml
ms.assetid: 8FF1362B-C7AB-4769-A88B-D1B6E214A006
online version: ''
schema: 2.0.0
ms.openlocfilehash: cf8275b8dfec4263c5ab7a8022dcb65edccb1171
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94046407"
---
# <span data-ttu-id="63984-101">Stop-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63984-101">Stop-AzureSiteRecoveryJob</span></span>

## <span data-ttu-id="63984-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="63984-102">SYNOPSIS</span></span>
<span data-ttu-id="63984-103">사이트 복구 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-103">Stops a Site Recovery job.</span></span>

## <span data-ttu-id="63984-104">구문과</span><span class="sxs-lookup"><span data-stu-id="63984-104">SYNTAX</span></span>

### <span data-ttu-id="63984-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="63984-105">ByObject (Default)</span></span>
```
Stop-AzureSiteRecoveryJob -Job <ASRJob> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

### <span data-ttu-id="63984-106">ById</span><span class="sxs-lookup"><span data-stu-id="63984-106">ById</span></span>
```
Stop-AzureSiteRecoveryJob -Id <String> [-Profile <AzureSMProfile>] [<CommonParameters>]
```

## <span data-ttu-id="63984-107">설명은</span><span class="sxs-lookup"><span data-stu-id="63984-107">DESCRIPTION</span></span>
<span data-ttu-id="63984-108">**AzureSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-108">The **Stop-AzureSiteRecoveryJob** cmdlet stops an Azure Site Recovery job.</span></span>

## <span data-ttu-id="63984-109">예제의</span><span class="sxs-lookup"><span data-stu-id="63984-109">EXAMPLES</span></span>

### <span data-ttu-id="63984-110">예제 1: 모든 작업 중지</span><span class="sxs-lookup"><span data-stu-id="63984-110">Example 1: Stop all jobs</span></span>
```
PS C:\>$Jobs = Get-AzureSiteRecoveryJob 
PS C:\> Stop-AzureSiteRecoveryJob -Job $Jobs
```

<span data-ttu-id="63984-111">첫 번째 명령은 **AzureSiteRecoveryJob** cmdlet을 사용 하 여 현재 Azure site recovery 자격 증명 모음에 대 한 Azure site recovery 작업을 가져온 다음 결과를 $Jobs 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-111">The first command gets the Azure Site Recovery jobs for the current Azure Site Recovery vault by using the **Get-AzureSiteRecoveryJob** cmdlet, and then stores the results in the $Jobs variable.</span></span>

<span data-ttu-id="63984-112">두 번째 명령은 $Jobs에 지정 된 작업을 중지 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-112">The second command stops the jobs specified by $Jobs.</span></span>

## <span data-ttu-id="63984-113">변수</span><span class="sxs-lookup"><span data-stu-id="63984-113">PARAMETERS</span></span>

### <span data-ttu-id="63984-114">-Id</span><span class="sxs-lookup"><span data-stu-id="63984-114">-Id</span></span>
<span data-ttu-id="63984-115">중지할 작업의 ID를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-115">Specifies the ID of the job to stop.</span></span>

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

### <span data-ttu-id="63984-116">-작업</span><span class="sxs-lookup"><span data-stu-id="63984-116">-Job</span></span>
<span data-ttu-id="63984-117">중지할 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-117">Specifies the job to stop.</span></span>

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

### <span data-ttu-id="63984-118">-프로필</span><span class="sxs-lookup"><span data-stu-id="63984-118">-Profile</span></span>
<span data-ttu-id="63984-119">이 cmdlet이 읽는 Azure 프로필을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-119">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="63984-120">프로필을 지정 하지 않으면이 cmdlet은 로컬 기본 프로필을 읽습니다.</span><span class="sxs-lookup"><span data-stu-id="63984-120">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="63984-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="63984-121">CommonParameters</span></span>
<span data-ttu-id="63984-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="63984-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="63984-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="63984-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="63984-124">입력</span><span class="sxs-lookup"><span data-stu-id="63984-124">INPUTS</span></span>

## <span data-ttu-id="63984-125">출력</span><span class="sxs-lookup"><span data-stu-id="63984-125">OUTPUTS</span></span>

## <span data-ttu-id="63984-126">상속자</span><span class="sxs-lookup"><span data-stu-id="63984-126">NOTES</span></span>

## <span data-ttu-id="63984-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="63984-127">RELATED LINKS</span></span>

[<span data-ttu-id="63984-128">Get-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63984-128">Get-AzureSiteRecoveryJob</span></span>](./Get-AzureSiteRecoveryJob.md)

[<span data-ttu-id="63984-129">다시 시작-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63984-129">Restart-AzureSiteRecoveryJob</span></span>](./Restart-AzureSiteRecoveryJob.md)

[<span data-ttu-id="63984-130">이력서-AzureSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="63984-130">Resume-AzureSiteRecoveryJob</span></span>](./Resume-AzureSiteRecoveryJob.md)


