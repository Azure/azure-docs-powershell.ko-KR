---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Get-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 0a809f9ef3d3c89edc7571b9bb7b7cc2f03e043b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711509"
---
# <span data-ttu-id="daf76-101">Get-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="daf76-101">Get-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="daf76-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="daf76-102">SYNOPSIS</span></span>
<span data-ttu-id="daf76-103">복구 서비스 자격 증명 모음에 대 한 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf76-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="daf76-104">구문과</span><span class="sxs-lookup"><span data-stu-id="daf76-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesAsrVaultContext [<CommonParameters>]
```

## <span data-ttu-id="daf76-105">설명은</span><span class="sxs-lookup"><span data-stu-id="daf76-105">DESCRIPTION</span></span>
<span data-ttu-id="daf76-106">**AzureRmRecoveryServicesAsrVaultContext** Cmdlet은 복구 서비스 자격 증명 모음과 관련 된 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf76-106">The **Get-AzureRmRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="daf76-107">예제의</span><span class="sxs-lookup"><span data-stu-id="daf76-107">EXAMPLES</span></span>

### <span data-ttu-id="daf76-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="daf76-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzureRmRecoveryServicesAsrVaultContext
```

<span data-ttu-id="daf76-109">현재 활성 (PowerShell 세션) 복구 서비스 자격 증명 모음에 대 한 ASR vault 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="daf76-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="daf76-110">변수</span><span class="sxs-lookup"><span data-stu-id="daf76-110">PARAMETERS</span></span>

### <span data-ttu-id="daf76-111">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="daf76-111">CommonParameters</span></span>
<span data-ttu-id="daf76-112">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="daf76-112">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="daf76-113">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="daf76-113">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="daf76-114">입력</span><span class="sxs-lookup"><span data-stu-id="daf76-114">INPUTS</span></span>

### <span data-ttu-id="daf76-115">않아야</span><span class="sxs-lookup"><span data-stu-id="daf76-115">None</span></span>

## <span data-ttu-id="daf76-116">출력</span><span class="sxs-lookup"><span data-stu-id="daf76-116">OUTPUTS</span></span>

### <span data-ttu-id="daf76-117">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="daf76-117">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="daf76-118">상속자</span><span class="sxs-lookup"><span data-stu-id="daf76-118">NOTES</span></span>

## <span data-ttu-id="daf76-119">관련 링크</span><span class="sxs-lookup"><span data-stu-id="daf76-119">RELATED LINKS</span></span>

