---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 48DCC0DC-1D59-4C30-9E1F-BBED7F94844F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/update-azurermsiterecoveryservicesprovider
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Update-AzureRmSiteRecoveryServicesProvider.md
ms.openlocfilehash: 7e1a043d1fd34ceae673111f2f7e0b892e419172
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532620"
---
# <span data-ttu-id="52799-101">Update-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="52799-101">Update-AzureRmSiteRecoveryServicesProvider</span></span>

## <span data-ttu-id="52799-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="52799-102">SYNOPSIS</span></span>
<span data-ttu-id="52799-103">Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52799-103">Updates the information received from the Azure Site Recovery Services Provider.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="52799-104">구문과</span><span class="sxs-lookup"><span data-stu-id="52799-104">SYNTAX</span></span>

```
Update-AzureRmSiteRecoveryServicesProvider -ServicesProvider <ASRRecoveryServicesProvider>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="52799-105">설명은</span><span class="sxs-lookup"><span data-stu-id="52799-105">DESCRIPTION</span></span>
<span data-ttu-id="52799-106">**업데이트 AzureRmSiteRecoveryServicesProvider** Cmdlet은 Azure Site Recovery 서비스 공급자 로부터 받은 정보를 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="52799-106">The **Update-AzureRmSiteRecoveryServicesProvider** cmdlet updates the information received from the Azure Site Recovery Services Provider.</span></span>
<span data-ttu-id="52799-107">이 cmdlet을 사용 하 여 복구 서비스 공급자 로부터 받은 정보의 새로 고침을 트리거할 수 있습니다.</span><span class="sxs-lookup"><span data-stu-id="52799-107">You can use this cmdlet to trigger a refresh of the information received from the Recovery Services Provider.</span></span>

## <span data-ttu-id="52799-108">예제의</span><span class="sxs-lookup"><span data-stu-id="52799-108">EXAMPLES</span></span>

## <span data-ttu-id="52799-109">변수</span><span class="sxs-lookup"><span data-stu-id="52799-109">PARAMETERS</span></span>

### <span data-ttu-id="52799-110">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="52799-110">-DefaultProfile</span></span>
<span data-ttu-id="52799-111">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="52799-111">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="52799-112">-서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="52799-112">-ServicesProvider</span></span>
<span data-ttu-id="52799-113">Azure Site Recovery 서비스 공급자 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="52799-113">Specifies the Azure Site Recovery Services Provider object.</span></span>

```yaml
Type: ASRRecoveryServicesProvider
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="52799-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="52799-114">CommonParameters</span></span>
<span data-ttu-id="52799-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="52799-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="52799-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="52799-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="52799-117">입력</span><span class="sxs-lookup"><span data-stu-id="52799-117">INPUTS</span></span>

### <span data-ttu-id="52799-118">Asrrecovery서비스 공급자</span><span class="sxs-lookup"><span data-stu-id="52799-118">ASRRecoveryServicesProvider</span></span>
<span data-ttu-id="52799-119">' 서비스 공급자 ' 매개 변수는 파이프라인에서 ' Asrrecovery서비스 공급자 '의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="52799-119">Parameter 'ServicesProvider' accepts value of type 'ASRRecoveryServicesProvider' from the pipeline</span></span>

## <span data-ttu-id="52799-120">출력</span><span class="sxs-lookup"><span data-stu-id="52799-120">OUTPUTS</span></span>

## <span data-ttu-id="52799-121">상속자</span><span class="sxs-lookup"><span data-stu-id="52799-121">NOTES</span></span>

## <span data-ttu-id="52799-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="52799-122">RELATED LINKS</span></span>

[<span data-ttu-id="52799-123">Get-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="52799-123">Get-AzureRmSiteRecoveryServicesProvider</span></span>](./Get-AzureRmSiteRecoveryServicesProvider.md)

[<span data-ttu-id="52799-124">제거-AzureRmSiteRecoveryServicesProvider</span><span class="sxs-lookup"><span data-stu-id="52799-124">Remove-AzureRmSiteRecoveryServicesProvider</span></span>](./Remove-AzureRmSiteRecoveryServicesProvider.md)
