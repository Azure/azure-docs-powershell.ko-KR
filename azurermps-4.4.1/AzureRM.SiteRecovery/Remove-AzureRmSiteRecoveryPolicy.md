---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: C4C624DB-BBE8-4F94-BDC6-C012482F7271
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryPolicy.md
ms.openlocfilehash: 3b01e089271cc131af5a4258c46836a87104ef62
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702683"
---
# <span data-ttu-id="274ec-101">Remove-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="274ec-101">Remove-AzureRmSiteRecoveryPolicy</span></span>

## <span data-ttu-id="274ec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="274ec-102">SYNOPSIS</span></span>
<span data-ttu-id="274ec-103">사이트 복구 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-103">Removes a Site Recovery replication policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="274ec-104">구문과</span><span class="sxs-lookup"><span data-stu-id="274ec-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryPolicy -Policy <ASRPolicy> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="274ec-105">설명은</span><span class="sxs-lookup"><span data-stu-id="274ec-105">DESCRIPTION</span></span>
<span data-ttu-id="274ec-106">**AzureRMSiteRecoveryPolicy** Cmdlet은 Azure Site Recovery 복제 정책을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-106">The **Remove-AzureRMSiteRecoveryPolicy** cmdlet removes an Azure Site Recovery replication policy.</span></span>

## <span data-ttu-id="274ec-107">예제의</span><span class="sxs-lookup"><span data-stu-id="274ec-107">EXAMPLES</span></span>

## <span data-ttu-id="274ec-108">변수</span><span class="sxs-lookup"><span data-stu-id="274ec-108">PARAMETERS</span></span>

### <span data-ttu-id="274ec-109">-정책</span><span class="sxs-lookup"><span data-stu-id="274ec-109">-Policy</span></span>
<span data-ttu-id="274ec-110">사이트 복구 정책 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-110">Specifies the Site Recovery policy object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRPolicy
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="274ec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="274ec-111">-DefaultProfile</span></span>
<span data-ttu-id="274ec-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="274ec-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="274ec-113">CommonParameters</span></span>
<span data-ttu-id="274ec-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="274ec-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="274ec-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="274ec-116">입력</span><span class="sxs-lookup"><span data-stu-id="274ec-116">INPUTS</span></span>

### <span data-ttu-id="274ec-117">ASRPolicy</span><span class="sxs-lookup"><span data-stu-id="274ec-117">ASRPolicy</span></span>
<span data-ttu-id="274ec-118">' Policy ' 매개 변수는 파이프라인에서 ' ASRPolicy ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="274ec-118">Parameter 'Policy' accepts value of type 'ASRPolicy' from the pipeline</span></span>

## <span data-ttu-id="274ec-119">출력</span><span class="sxs-lookup"><span data-stu-id="274ec-119">OUTPUTS</span></span>

## <span data-ttu-id="274ec-120">상속자</span><span class="sxs-lookup"><span data-stu-id="274ec-120">NOTES</span></span>

## <span data-ttu-id="274ec-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="274ec-121">RELATED LINKS</span></span>

[<span data-ttu-id="274ec-122">Get-AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="274ec-122">Get-AzureRmSiteRecoveryPolicy</span></span>](./Get-AzureRmSiteRecoveryPolicy.md)

[<span data-ttu-id="274ec-123">새로운 AzureRmSiteRecoveryPolicy</span><span class="sxs-lookup"><span data-stu-id="274ec-123">New-AzureRmSiteRecoveryPolicy</span></span>](./New-AzureRmSiteRecoveryPolicy.md)
