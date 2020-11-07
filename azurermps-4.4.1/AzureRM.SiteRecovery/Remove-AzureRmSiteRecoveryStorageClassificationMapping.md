---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 441478B4-1453-4A11-AD52-53ADB85E194F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryStorageClassificationMapping.md
ms.openlocfilehash: 59ae0324a5e42e87192e655352fce074413907ae
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703315"
---
# <span data-ttu-id="95836-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="95836-101">Remove-AzureRmSiteRecoveryStorageClassificationMapping</span></span>

## <span data-ttu-id="95836-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="95836-102">SYNOPSIS</span></span>
<span data-ttu-id="95836-103">사이트 복구에서 저장소 분류 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95836-103">Removes a storage classification mapping from Site Recovery.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="95836-104">구문과</span><span class="sxs-lookup"><span data-stu-id="95836-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryStorageClassificationMapping
 -StorageClassificationMapping <ASRStorageClassificationMapping> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="95836-105">설명은</span><span class="sxs-lookup"><span data-stu-id="95836-105">DESCRIPTION</span></span>
<span data-ttu-id="95836-106">**AzureRmSiteRecoveryStorageClassificationMapping** Cmdlet은 Azure Site Recovery에서 저장소 분류 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="95836-106">The **Remove-AzureRmSiteRecoveryStorageClassificationMapping** cmdlet removes a storage classification mapping from Azure Site Recovery.</span></span>

## <span data-ttu-id="95836-107">예제의</span><span class="sxs-lookup"><span data-stu-id="95836-107">EXAMPLES</span></span>

## <span data-ttu-id="95836-108">변수</span><span class="sxs-lookup"><span data-stu-id="95836-108">PARAMETERS</span></span>

### <span data-ttu-id="95836-109">-StorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="95836-109">-StorageClassificationMapping</span></span>
<span data-ttu-id="95836-110">이 cmdlet이 제거 하는 저장소 분류 매핑을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="95836-110">Specifies a storage classification mapping that this cmdlet removes.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRStorageClassificationMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="95836-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="95836-111">-DefaultProfile</span></span>
<span data-ttu-id="95836-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="95836-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="95836-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="95836-113">CommonParameters</span></span>
<span data-ttu-id="95836-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="95836-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="95836-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="95836-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="95836-116">입력</span><span class="sxs-lookup"><span data-stu-id="95836-116">INPUTS</span></span>

### <span data-ttu-id="95836-117">ASRStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="95836-117">ASRStorageClassificationMapping</span></span>
<span data-ttu-id="95836-118">' StorageClassificationMapping ' 매개 변수는 파이프라인에서 ' ASRStorageClassificationMapping ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="95836-118">Parameter 'StorageClassificationMapping' accepts value of type 'ASRStorageClassificationMapping' from the pipeline</span></span>

## <span data-ttu-id="95836-119">출력</span><span class="sxs-lookup"><span data-stu-id="95836-119">OUTPUTS</span></span>

### <span data-ttu-id="95836-120">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="95836-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="95836-121">상속자</span><span class="sxs-lookup"><span data-stu-id="95836-121">NOTES</span></span>

## <span data-ttu-id="95836-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="95836-122">RELATED LINKS</span></span>

[<span data-ttu-id="95836-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="95836-123">Get-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./Get-AzureRmSiteRecoveryStorageClassificationMapping.md)

[<span data-ttu-id="95836-124">새로운 AzureRmSiteRecoveryStorageClassificationMapping</span><span class="sxs-lookup"><span data-stu-id="95836-124">New-AzureRmSiteRecoveryStorageClassificationMapping</span></span>](./New-AzureRmSiteRecoveryStorageClassificationMapping.md)
