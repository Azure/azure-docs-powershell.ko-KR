---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 1b17284a5b0dfbdc8ee031df714c9f9f03533697
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532915"
---
# <span data-ttu-id="c2c13-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c2c13-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="c2c13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2c13-102">SYNOPSIS</span></span>
<span data-ttu-id="c2c13-103">Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c2c13-104">구문과</span><span class="sxs-lookup"><span data-stu-id="c2c13-104">SYNTAX</span></span>

### <span data-ttu-id="c2c13-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="c2c13-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c2c13-106">ByName</span><span class="sxs-lookup"><span data-stu-id="c2c13-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c2c13-107">설명은</span><span class="sxs-lookup"><span data-stu-id="c2c13-107">DESCRIPTION</span></span>
<span data-ttu-id="c2c13-108">**AzureRmSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="c2c13-109">예제의</span><span class="sxs-lookup"><span data-stu-id="c2c13-109">EXAMPLES</span></span>

## <span data-ttu-id="c2c13-110">변수</span><span class="sxs-lookup"><span data-stu-id="c2c13-110">PARAMETERS</span></span>

### <span data-ttu-id="c2c13-111">-작업</span><span class="sxs-lookup"><span data-stu-id="c2c13-111">-Job</span></span>
<span data-ttu-id="c2c13-112">사이트 복구 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-112">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="c2c13-113">-이름</span><span class="sxs-lookup"><span data-stu-id="c2c13-113">-Name</span></span>
<span data-ttu-id="c2c13-114">작업의 고유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-114">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="c2c13-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2c13-115">-DefaultProfile</span></span>
<span data-ttu-id="c2c13-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2c13-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2c13-117">CommonParameters</span></span>
<span data-ttu-id="c2c13-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2c13-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c2c13-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2c13-120">입력</span><span class="sxs-lookup"><span data-stu-id="c2c13-120">INPUTS</span></span>

### <span data-ttu-id="c2c13-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="c2c13-121">ASRJob</span></span>
<span data-ttu-id="c2c13-122">' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2c13-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="c2c13-123">출력</span><span class="sxs-lookup"><span data-stu-id="c2c13-123">OUTPUTS</span></span>

### <span data-ttu-id="c2c13-124">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="c2c13-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="c2c13-125">상속자</span><span class="sxs-lookup"><span data-stu-id="c2c13-125">NOTES</span></span>

## <span data-ttu-id="c2c13-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2c13-126">RELATED LINKS</span></span>

[<span data-ttu-id="c2c13-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c2c13-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="c2c13-128">이력서-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c2c13-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="c2c13-129">중지-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="c2c13-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
