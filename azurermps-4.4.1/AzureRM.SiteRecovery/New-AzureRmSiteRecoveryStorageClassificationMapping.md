---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 4B4CB198-ABD3-4926-808D-2087151EA06B
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/New-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 2520dd90eed1362f4d499eb88ce88dec33f1338c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527263"
---
# <span data-ttu-id="bd289-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd289-101">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="bd289-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bd289-102">SYNOPSIS</span></span>
<span data-ttu-id="bd289-103">사이트 복구에서 저장소 분류 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-103">Creates a storage classification mapping in Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bd289-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bd289-104">SYNTAX</span></span>

```
New-AzureRmSiteRecoveryStorageClassificationMapping [-Name <String>]
 -PrimaryStorageClassification <ASRStorageClassification>
 -RecoveryStorageClassification <ASRStorageClassification> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="bd289-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bd289-105">DESCRIPTION</span></span>
<span data-ttu-id="bd289-106">**AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet은 Azure Site Recovery에서 저장소 분류 매핑을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-106">The **New-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet creates a storage classification mapping in Azure Site Recovery.</span></span>

## <span data-ttu-id="bd289-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bd289-107">EXAMPLES</span></span>

## <span data-ttu-id="bd289-108">변수</span><span class="sxs-lookup"><span data-stu-id="bd289-108">PARAMETERS</span></span>

### <span data-ttu-id="bd289-109">-이름</span><span class="sxs-lookup"><span data-stu-id="bd289-109">-Name</span></span>
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

### <span data-ttu-id="bd289-110">-PrimaryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="bd289-110">-PrimaryStorageClassification</span></span>
<span data-ttu-id="bd289-111">기본 저장소 분류 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-111">Specifies the primary storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="bd289-112">-RecoveryStorageClassification</span><span class="sxs-lookup"><span data-stu-id="bd289-112">-RecoveryStorageClassification</span></span>
<span data-ttu-id="bd289-113">복구 저장소 분류 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-113">Specifies a recovery storage classification mapping.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassification
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bd289-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bd289-114">-DefaultProfile</span></span>
<span data-ttu-id="bd289-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bd289-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bd289-116">CommonParameters</span></span>
<span data-ttu-id="bd289-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bd289-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bd289-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bd289-119">입력</span><span class="sxs-lookup"><span data-stu-id="bd289-119">INPUTS</span></span>

### <span data-ttu-id="bd289-120">ASRStorageClassification</span><span class="sxs-lookup"><span data-stu-id="bd289-120">ASRStorageClassification</span></span>
<span data-ttu-id="bd289-121">' PrimaryStorageClassification ' 매개 변수는 파이프라인에서 ' ASRStorageClassification ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bd289-121">Parameter 'PrimaryStorageClassification' accepts value of type 'ASRStorageClassification' from the pipeline</span></span>

## <span data-ttu-id="bd289-122">출력</span><span class="sxs-lookup"><span data-stu-id="bd289-122">OUTPUTS</span></span>

### <span data-ttu-id="bd289-123">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="bd289-123">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="bd289-124">상속자</span><span class="sxs-lookup"><span data-stu-id="bd289-124">NOTES</span></span>

## <span data-ttu-id="bd289-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bd289-125">RELATED LINKS</span></span>

[<span data-ttu-id="bd289-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd289-126">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="bd289-127">제거-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="bd289-127">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Remove-AzureRmSiteRecoveryStorageClassificationMapping.md)
