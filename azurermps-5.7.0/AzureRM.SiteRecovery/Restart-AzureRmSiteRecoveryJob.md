---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 5A70AC55-27B4-421E-8EB0-1C7B8DFD3537
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/restart-azurermsiterecoveryjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Restart-AzureRmSiteRecoveryJob.md
ms.openlocfilehash: 17486f4a22e488a147fcdd8a8e085c7900fc8147
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93524900"
---
# <span data-ttu-id="936f3-101">Restart-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="936f3-101">Restart-AzureRmSiteRecoveryJob</span></span>

## <span data-ttu-id="936f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="936f3-102">SYNOPSIS</span></span>
<span data-ttu-id="936f3-103">Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-103">Restarts an Azure Site Recovery job.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="936f3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="936f3-104">SYNTAX</span></span>

### <span data-ttu-id="936f3-105">ByObject (기본값)</span><span class="sxs-lookup"><span data-stu-id="936f3-105">ByObject (Default)</span></span>
```
Restart-AzureRmSiteRecoveryJob -Job <ASRJob> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="936f3-106">ByName</span><span class="sxs-lookup"><span data-stu-id="936f3-106">ByName</span></span>
```
Restart-AzureRmSiteRecoveryJob -Name <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="936f3-107">설명은</span><span class="sxs-lookup"><span data-stu-id="936f3-107">DESCRIPTION</span></span>
<span data-ttu-id="936f3-108">**AzureRmSiteRecoveryJob** Cmdlet은 Azure Site Recovery 작업을 다시 시작 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-108">The **Restart-AzureRmSiteRecoveryJob** cmdlet restarts an Azure Site Recovery job.</span></span>

## <span data-ttu-id="936f3-109">예제의</span><span class="sxs-lookup"><span data-stu-id="936f3-109">EXAMPLES</span></span>

## <span data-ttu-id="936f3-110">변수</span><span class="sxs-lookup"><span data-stu-id="936f3-110">PARAMETERS</span></span>

### <span data-ttu-id="936f3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="936f3-111">-DefaultProfile</span></span>
<span data-ttu-id="936f3-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="936f3-113">-작업</span><span class="sxs-lookup"><span data-stu-id="936f3-113">-Job</span></span>
<span data-ttu-id="936f3-114">사이트 복구 작업 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-114">Specifies the Site Recovery job object.</span></span>

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

### <span data-ttu-id="936f3-115">-이름</span><span class="sxs-lookup"><span data-stu-id="936f3-115">-Name</span></span>
<span data-ttu-id="936f3-116">작업의 고유 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-116">Specifies the unique name for the job.</span></span>

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

### <span data-ttu-id="936f3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="936f3-117">CommonParameters</span></span>
<span data-ttu-id="936f3-118">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="936f3-119">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="936f3-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="936f3-120">입력</span><span class="sxs-lookup"><span data-stu-id="936f3-120">INPUTS</span></span>

### <span data-ttu-id="936f3-121">ASRJob</span><span class="sxs-lookup"><span data-stu-id="936f3-121">ASRJob</span></span>
<span data-ttu-id="936f3-122">' Job ' 매개 변수는 파이프라인에서 ' ASRJob ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="936f3-122">Parameter 'Job' accepts value of type 'ASRJob' from the pipeline</span></span>

## <span data-ttu-id="936f3-123">출력</span><span class="sxs-lookup"><span data-stu-id="936f3-123">OUTPUTS</span></span>

### <span data-ttu-id="936f3-124">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="936f3-124">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="936f3-125">상속자</span><span class="sxs-lookup"><span data-stu-id="936f3-125">NOTES</span></span>

## <span data-ttu-id="936f3-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="936f3-126">RELATED LINKS</span></span>

[<span data-ttu-id="936f3-127">Get-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="936f3-127">Get-AzureRmSiteRecoveryJob</span></span>](./Get-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="936f3-128">이력서-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="936f3-128">Resume-AzureRmSiteRecoveryJob</span></span>](./Resume-AzureRmSiteRecoveryJob.md)

[<span data-ttu-id="936f3-129">중지-AzureRmSiteRecoveryJob</span><span class="sxs-lookup"><span data-stu-id="936f3-129">Stop-AzureRmSiteRecoveryJob</span></span>](./Stop-AzureRmSiteRecoveryJob.md)
