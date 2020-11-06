---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/resume-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: aae0bf7c2ec4a166d48edb032d6c21918dc3ae6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529714"
---
# <span data-ttu-id="90cf6-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="90cf6-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="90cf6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="90cf6-102">SYNOPSIS</span></span>
<span data-ttu-id="90cf6-103">일시 중단 된 사이트 복구 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="90cf6-104">구문과</span><span class="sxs-lookup"><span data-stu-id="90cf6-104">SYNTAX</span></span>

### <span data-ttu-id="90cf6-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="90cf6-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="90cf6-106">ByName</span><span class="sxs-lookup"><span data-stu-id="90cf6-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="90cf6-107">설명은</span><span class="sxs-lookup"><span data-stu-id="90cf6-107">DESCRIPTION</span></span>
<span data-ttu-id="90cf6-108">**AzureRmSiteRecoveryJob** cmdlet은 일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="90cf6-109">예제의</span><span class="sxs-lookup"><span data-stu-id="90cf6-109">EXAMPLES</span></span>

## <span data-ttu-id="90cf6-110">변수</span><span class="sxs-lookup"><span data-stu-id="90cf6-110">PARAMETERS</span></span>

### <span data-ttu-id="90cf6-111">-메모</span><span class="sxs-lookup"><span data-stu-id="90cf6-111">-Comments</span></span>
<span data-ttu-id="90cf6-112">작업 로그에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-112">Specifies the comments for the job log.</span></span>

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

### <span data-ttu-id="90cf6-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="90cf6-113">-DefaultProfile</span></span>
<span data-ttu-id="90cf6-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cf6-115">-작업</span><span class="sxs-lookup"><span data-stu-id="90cf6-115">-Job</span></span>
<span data-ttu-id="90cf6-116">사이트 복구 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-116">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="90cf6-117">-이름</span><span class="sxs-lookup"><span data-stu-id="90cf6-117">-Name</span></span>
<span data-ttu-id="90cf6-118">작업의 고유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-118">Specifies the unique name for the job.</span></span>

```yaml
Type: String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="90cf6-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="90cf6-119">CommonParameters</span></span>
<span data-ttu-id="90cf6-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="90cf6-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="90cf6-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="90cf6-122">입력</span><span class="sxs-lookup"><span data-stu-id="90cf6-122">INPUTS</span></span>

### <span data-ttu-id="90cf6-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="90cf6-123">ASRJob</span></span>
<span data-ttu-id="90cf6-124">' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="90cf6-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="90cf6-125">출력</span><span class="sxs-lookup"><span data-stu-id="90cf6-125">OUTPUTS</span></span>

### <span data-ttu-id="90cf6-126">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="90cf6-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="90cf6-127">상속자</span><span class="sxs-lookup"><span data-stu-id="90cf6-127">NOTES</span></span>

## <span data-ttu-id="90cf6-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="90cf6-128">RELATED LINKS</span></span>

[<span data-ttu-id="90cf6-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="90cf6-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="90cf6-130">다시 시작-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="90cf6-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="90cf6-131">중지-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="90cf6-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
