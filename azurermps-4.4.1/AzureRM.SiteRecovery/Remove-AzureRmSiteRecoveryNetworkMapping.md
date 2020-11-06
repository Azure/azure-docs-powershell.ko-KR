---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM.SiteRecovery
ms.assetid: BDEA3F9D-AC23-402D-BA1F-AC617C7480A1
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Remove-AzureRmSiteRecoveryNetworkMapping.md
ms.openlocfilehash: 03bd15f1071ac223ba7460c27bcfd9ce96a55dda
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93530657"
---
# <span data-ttu-id="31b9c-101">Remove-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31b9c-101">Remove-AzureRmSiteRecoveryNetworkMapping</span></span>

## <span data-ttu-id="31b9c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="31b9c-102">SYNOPSIS</span></span>
<span data-ttu-id="31b9c-103">현재 사이트 복구 자격 증명 모음에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-103">Removes a network mapping from the current Site Recovery vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="31b9c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="31b9c-104">SYNTAX</span></span>

```
Remove-AzureRmSiteRecoveryNetworkMapping -NetworkMapping <ASRNetworkMapping>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="31b9c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="31b9c-105">DESCRIPTION</span></span>
<span data-ttu-id="31b9c-106">**AzureRMSiteRecoveryNetworkMapping** cmdlet은 현재 Azure Site Recovery 자격 증명 모음에서 네트워크 매핑을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-106">The **Remove-AzureRMSiteRecoveryNetworkMapping** cmdlet removes a network mapping from the current Azure Site Recovery vault.</span></span>

## <span data-ttu-id="31b9c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="31b9c-107">EXAMPLES</span></span>

## <span data-ttu-id="31b9c-108">변수</span><span class="sxs-lookup"><span data-stu-id="31b9c-108">PARAMETERS</span></span>

### <span data-ttu-id="31b9c-109">-NetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31b9c-109">-NetworkMapping</span></span>
<span data-ttu-id="31b9c-110">네트워크 매핑 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-110">Specifies the network mapping object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.SiteRecovery.ASRNetworkMapping
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="31b9c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="31b9c-111">-DefaultProfile</span></span>
<span data-ttu-id="31b9c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="31b9c-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="31b9c-113">CommonParameters</span></span>
<span data-ttu-id="31b9c-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="31b9c-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="31b9c-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="31b9c-116">입력</span><span class="sxs-lookup"><span data-stu-id="31b9c-116">INPUTS</span></span>

### <span data-ttu-id="31b9c-117">ASRNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31b9c-117">ASRNetworkMapping</span></span>
<span data-ttu-id="31b9c-118">' NetworkMapping ' 매개 변수는 파이프라인에서 ' ASRNetworkMapping ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="31b9c-118">Parameter 'NetworkMapping' accepts value of type 'ASRNetworkMapping' from the pipeline</span></span>

## <span data-ttu-id="31b9c-119">출력</span><span class="sxs-lookup"><span data-stu-id="31b9c-119">OUTPUTS</span></span>

### <span data-ttu-id="31b9c-120">SiteRecovery. r m m 작업</span><span class="sxs-lookup"><span data-stu-id="31b9c-120">Microsoft.Azure.Commands.SiteRecovery.ASRJob</span></span>

## <span data-ttu-id="31b9c-121">상속자</span><span class="sxs-lookup"><span data-stu-id="31b9c-121">NOTES</span></span>

## <span data-ttu-id="31b9c-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="31b9c-122">RELATED LINKS</span></span>

[<span data-ttu-id="31b9c-123">Get-AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31b9c-123">Get-AzureRmSiteRecoveryNetworkMapping</span></span>](./Get-AzureRmSiteRecoveryNetworkMapping.md)

[<span data-ttu-id="31b9c-124">새로운 AzureRmSiteRecoveryNetworkMapping</span><span class="sxs-lookup"><span data-stu-id="31b9c-124">New-AzureRmSiteRecoveryNetworkMapping</span></span>](./New-AzureRmSiteRecoveryNetworkMapping.md)
