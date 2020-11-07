---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 3F827EA0-7CF9-49F8-93BB-B15078A8BBB7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Resume-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 5514d7cec58c2ecad7a4b9c79b3d4d2ad77a5ef3
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703310"
---
# <span data-ttu-id="8a888-101">Resume-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8a888-101">Resume-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="8a888-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8a888-102">SYNOPSIS</span></span>
<span data-ttu-id="8a888-103">일시 중단 된 사이트 복구 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-103">Resumes a suspended Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="8a888-104">구문과</span><span class="sxs-lookup"><span data-stu-id="8a888-104">SYNTAX</span></span>

### <span data-ttu-id="8a888-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="8a888-105">ByObject (Default)</span></span>
```
Resume-AzureRmSiteRecoveryJob -Job <ASRJob> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="8a888-106">ByName</span><span class="sxs-lookup"><span data-stu-id="8a888-106">ByName</span></span>
```
Resume-AzureRmSiteRecoveryJob -Name <String> [-Comments <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="8a888-107">설명은</span><span class="sxs-lookup"><span data-stu-id="8a888-107">DESCRIPTION</span></span>
<span data-ttu-id="8a888-108">**AzureRmSiteRecoveryJob** cmdlet은 일시 중단 된 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-108">The **Resume-AzureRmSiteRecoveryJob** cmdlet resumes a suspended Azure Site Recovery job.</span></span>

## <span data-ttu-id="8a888-109">예제의</span><span class="sxs-lookup"><span data-stu-id="8a888-109">EXAMPLES</span></span>

## <span data-ttu-id="8a888-110">변수</span><span class="sxs-lookup"><span data-stu-id="8a888-110">PARAMETERS</span></span>

### <span data-ttu-id="8a888-111">-메모</span><span class="sxs-lookup"><span data-stu-id="8a888-111">-Comments</span></span>
<span data-ttu-id="8a888-112">작업 로그에 대 한 메모를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-112">Specifies the comments for the job log.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a888-113">-작업</span><span class="sxs-lookup"><span data-stu-id="8a888-113">-Job</span></span>
<span data-ttu-id="8a888-114">사이트 복구 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-114">Specifies the Site Recovery job object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRJob
Parameter Sets: ByObject
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="8a888-115">-이름</span><span class="sxs-lookup"><span data-stu-id="8a888-115">-Name</span></span>
<span data-ttu-id="8a888-116">작업의 고유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-116">Specifies the unique name for the job.</span></span>

```yaml
Type: System.String
Parameter Sets: ByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="8a888-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8a888-117">-DefaultProfile</span></span>
<span data-ttu-id="8a888-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="8a888-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8a888-119">CommonParameters</span></span>
<span data-ttu-id="8a888-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8a888-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="8a888-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8a888-122">입력</span><span class="sxs-lookup"><span data-stu-id="8a888-122">INPUTS</span></span>

### <span data-ttu-id="8a888-123">ASRJob</span><span class="sxs-lookup"><span data-stu-id="8a888-123">ASRJob</span></span>
<span data-ttu-id="8a888-124">' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="8a888-124">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="8a888-125">출력</span><span class="sxs-lookup"><span data-stu-id="8a888-125">OUTPUTS</span></span>

### <span data-ttu-id="8a888-126">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="8a888-126">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="8a888-127">상속자</span><span class="sxs-lookup"><span data-stu-id="8a888-127">NOTES</span></span>

## <span data-ttu-id="8a888-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8a888-128">RELATED LINKS</span></span>

[<span data-ttu-id="8a888-129">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8a888-129">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8a888-130">다시 시작-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8a888-130">Restart-AzureRmSiteRecoveryJob</span></span>](./Restart-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="8a888-131">중지-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="8a888-131">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
