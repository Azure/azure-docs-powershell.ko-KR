---
external help file: Microsoft.Azure.Commands.AzureBackup.dll-Help.xml
Module Name: AzureRM.Backup
ms.assetid: C5126E20-0A93-4ACE-8297-F1E8E17BEF53
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBackup/Commands.AzureBackup/help/Wait-AzureRmBackupJob.md
ms.openlocfilehash: 6ee1319881b200b3fcae56e433f81460bfc90274
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535023"
---
# <span data-ttu-id="b5aea-101">Wait-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b5aea-101">Wait-AzureRmBackupJob</span></span>

## <span data-ttu-id="b5aea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b5aea-102">SYNOPSIS</span></span>
<span data-ttu-id="b5aea-103">백업 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-103">Waits for a Backup job to finish.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b5aea-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b5aea-104">SYNTAX</span></span>

```
Wait-AzureRmBackupJob -Job <Object> [-TimeOut <Int64>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b5aea-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b5aea-105">DESCRIPTION</span></span>
<span data-ttu-id="b5aea-106">**AzureRmBackupJob** Cmdlet은 Azure Backup 작업이 완료 될 때까지 기다립니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-106">The **Wait-AzureRmBackupJob** cmdlet waits for an Azure Backup job to finish.</span></span>
<span data-ttu-id="b5aea-107">백업 작업에는 시간이 오래 걸릴 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-107">Backup jobs can take a long time.</span></span>
<span data-ttu-id="b5aea-108">스크립트의 일부로 백업 작업을 실행 하는 경우 스크립트에서 작업이 완료 될 때까지 기다렸다가 다른 작업을 계속 하도록 할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-108">If you run a backup job as part of a script, you may want to force the script to wait for job to finish before it continues to other tasks.</span></span>

<span data-ttu-id="b5aea-109">이 cmdlet을 포함 하는 스크립트는 작업 상태에 대 한 백업 서비스를 폴링하는 것 보다 더 간단 하 게 사용할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-109">A script that includes this cmdlet can be simpler than one that polls the Backup service for the job status.</span></span>

## <span data-ttu-id="b5aea-110">예제의</span><span class="sxs-lookup"><span data-stu-id="b5aea-110">EXAMPLES</span></span>

## <span data-ttu-id="b5aea-111">변수</span><span class="sxs-lookup"><span data-stu-id="b5aea-111">PARAMETERS</span></span>

### <span data-ttu-id="b5aea-112">-작업</span><span class="sxs-lookup"><span data-stu-id="b5aea-112">-Job</span></span>
<span data-ttu-id="b5aea-113">이 cmdlet이 취소 하는 작업을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-113">Specifies a job that this cmdlet cancels.</span></span>
<span data-ttu-id="b5aea-114">**AzureRmBackupJob** 개체를 가져오려면 Get-AzureRmBackupJob cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-114">To obtain an **AzureRmBackupJob** object, use the Get-AzureRmBackupJob cmdlet.</span></span>

```yaml
Type: System.Object
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="b5aea-115">-시간 제한</span><span class="sxs-lookup"><span data-stu-id="b5aea-115">-TimeOut</span></span>
<span data-ttu-id="b5aea-116">작업이 완료 될 때까지이 cmdlet이 대기 하는 최대 시간 (초)을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-116">Specifies the maximum time, in seconds, that this cmdlet waits for the job to finish.</span></span>
<span data-ttu-id="b5aea-117">시간 초과 값을 지정 하는 것이 좋습니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-117">We recommend that you specify a time-out value.</span></span>

```yaml
Type: System.Nullable`1[System.Int64]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aea-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b5aea-118">-DefaultProfile</span></span>
<span data-ttu-id="b5aea-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b5aea-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b5aea-120">CommonParameters</span></span>
<span data-ttu-id="b5aea-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b5aea-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b5aea-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b5aea-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b5aea-123">입력</span><span class="sxs-lookup"><span data-stu-id="b5aea-123">INPUTS</span></span>

### <span data-ttu-id="b5aea-124">AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b5aea-124">AzureRmBackupJob</span></span>

## <span data-ttu-id="b5aea-125">출력</span><span class="sxs-lookup"><span data-stu-id="b5aea-125">OUTPUTS</span></span>

### <span data-ttu-id="b5aea-126">AzureRmBackupJob[]</span><span class="sxs-lookup"><span data-stu-id="b5aea-126">AzureRmBackupJob[]</span></span>

## <span data-ttu-id="b5aea-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b5aea-127">NOTES</span></span>

## <span data-ttu-id="b5aea-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b5aea-128">RELATED LINKS</span></span>

[<span data-ttu-id="b5aea-129">Get-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b5aea-129">Get-AzureRmBackupJob</span></span>](./Get-AzureRmBackupJob.md)

[<span data-ttu-id="b5aea-130">중지-AzureRmBackupJob</span><span class="sxs-lookup"><span data-stu-id="b5aea-130">Stop-AzureRmBackupJob</span></span>](./Stop-AzureRmBackupJob.md)


