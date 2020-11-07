---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 31eda861294d4c678e141da8f40d1f5d6c5a4ca1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703613"
---
# <span data-ttu-id="dbb3d-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="dbb3d-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="dbb3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dbb3d-102">SYNOPSIS</span></span>
<span data-ttu-id="dbb3d-103">Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dbb3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="dbb3d-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dbb3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="dbb3d-105">DESCRIPTION</span></span>
<span data-ttu-id="dbb3d-106">**업데이트 AzureRmSiteRecoveryServicesProvider** Cmdlet은 Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="dbb3d-107">이 cmdlet을 사용 하 여 복구 서비스 공급자 로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="dbb3d-108">예제의</span><span class="sxs-lookup"><span data-stu-id="dbb3d-108">EXAMPLES</span></span>

## <span data-ttu-id="dbb3d-109">변수</span><span class="sxs-lookup"><span data-stu-id="dbb3d-109">PARAMETERS</span></span>

### <span data-ttu-id="dbb3d-110">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="dbb3d-110">-ServicesProvider</span></span>
<span data-ttu-id="dbb3d-111">Azure Site Recovery 서비스 공급자 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-111">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="dbb3d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dbb3d-112">-DefaultProfile</span></span>
<span data-ttu-id="dbb3d-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="dbb3d-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dbb3d-114">CommonParameters</span></span>
<span data-ttu-id="dbb3d-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dbb3d-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dbb3d-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dbb3d-117">입력</span><span class="sxs-lookup"><span data-stu-id="dbb3d-117">INPUTS</span></span>

### <span data-ttu-id="dbb3d-118">Asrrecovery서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="dbb3d-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="dbb3d-119">' 서비스 공급자 ' 매개 변수는 파이프라인에서 ' Asrrecovery서비스 공급자 '의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="dbb3d-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="dbb3d-120">출력</span><span class="sxs-lookup"><span data-stu-id="dbb3d-120">OUTPUTS</span></span>

## <span data-ttu-id="dbb3d-121">상속자</span><span class="sxs-lookup"><span data-stu-id="dbb3d-121">NOTES</span></span>

## <span data-ttu-id="dbb3d-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="dbb3d-122">RELATED LINKS</span></span>

[<span data-ttu-id="dbb3d-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="dbb3d-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="dbb3d-124">제거-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="dbb3d-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
