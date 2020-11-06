---
external help file: Microsoft.Azure.Commands.SiteRecovery.dll-Help.xml
Module Name: AzureRM
ms.assetid: 133668A0-0D11-4034-A743-4C0D3CE0FAF1
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.siterecovery/set-azurermsiterecoveryvaultsettings
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/SiteRecovery/Commands.SiteRecovery/help/Set-AzureRmSiteRecoveryVaultSettings.md
ms.openlocfilehash: b6016857054d2560602c7ea37a508317ff895d37
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529710"
---
# <span data-ttu-id="4d8f1-101">Set-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4d8f1-101">Set-AzureRmSiteRecoveryVaultSettings</span></span>

## <span data-ttu-id="4d8f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4d8f1-102">SYNOPSIS</span></span>
<span data-ttu-id="4d8f1-103">추가 작업을 위해 사이트 복구 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-103">Sets the Site Recovery vault context for further operations.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="4d8f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4d8f1-104">SYNTAX</span></span>

### <span data-ttu-id="4d8f1-105">AzureSiteRecoveryVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-105">AzureSiteRecoveryVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ASRVault <ASRVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4d8f1-106">AzureRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-106">AzureRecoveryServicesVault</span></span>
```
Set-AzureRmSiteRecoveryVaultSettings -ARSVault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="4d8f1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="4d8f1-107">DESCRIPTION</span></span>
<span data-ttu-id="4d8f1-108">**AzureRmSiteRecoveryVaultSettings** cmdlet은 추가 작업을 위해 Azure Site Recovery 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-108">The **Set-AzureRmSiteRecoveryVaultSettings** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>
<span data-ttu-id="4d8f1-109">복구 서비스 자격 증명 모음에는 적용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-109">This does not apply to recovery services vaults.</span></span>

## <span data-ttu-id="4d8f1-110">예제의</span><span class="sxs-lookup"><span data-stu-id="4d8f1-110">EXAMPLES</span></span>

## <span data-ttu-id="4d8f1-111">변수</span><span class="sxs-lookup"><span data-stu-id="4d8f1-111">PARAMETERS</span></span>

### <span data-ttu-id="4d8f1-112">-ARSVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-112">-ARSVault</span></span>
<span data-ttu-id="4d8f1-113">**ARSVault** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-113">Specifies an **ARSVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: AzureRecoveryServicesVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8f1-114">-ASRVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-114">-ASRVault</span></span>
<span data-ttu-id="4d8f1-115">**Asrvault** 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-115">Specifies an **ASRVault** object.</span></span>

```yaml
Type: ASRVault
Parameter Sets: AzureSiteRecoveryVault
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="4d8f1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4d8f1-116">-DefaultProfile</span></span>
<span data-ttu-id="4d8f1-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4d8f1-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4d8f1-118">CommonParameters</span></span>
<span data-ttu-id="4d8f1-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4d8f1-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4d8f1-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4d8f1-121">입력</span><span class="sxs-lookup"><span data-stu-id="4d8f1-121">INPUTS</span></span>

### <span data-ttu-id="4d8f1-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-122">ARSVault</span></span>
<span data-ttu-id="4d8f1-123">' ARSVault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-123">Parameter 'ARSVault' accepts value of type 'ARSVault' from the pipeline</span></span>

### <span data-ttu-id="4d8f1-124">ASRVault</span><span class="sxs-lookup"><span data-stu-id="4d8f1-124">ASRVault</span></span>
<span data-ttu-id="4d8f1-125">' ASRVault ' 매개 변수는 파이프라인에서 ' ASRVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4d8f1-125">Parameter 'ASRVault' accepts value of type 'ASRVault' from the pipeline</span></span>

## <span data-ttu-id="4d8f1-126">출력</span><span class="sxs-lookup"><span data-stu-id="4d8f1-126">OUTPUTS</span></span>

### <span data-ttu-id="4d8f1-127">SiteRecovery. ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4d8f1-127">Microsoft.Azure.Commands.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4d8f1-128">상속자</span><span class="sxs-lookup"><span data-stu-id="4d8f1-128">NOTES</span></span>

## <span data-ttu-id="4d8f1-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4d8f1-129">RELATED LINKS</span></span>

[<span data-ttu-id="4d8f1-130">Get-AzureRmSiteRecoveryVaultSettings</span><span class="sxs-lookup"><span data-stu-id="4d8f1-130">Get-AzureRmSiteRecoveryVaultSettings</span></span>](./Get-AzureRmSiteRecoveryVaultSettings.md)
