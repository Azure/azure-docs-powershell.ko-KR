---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: e5bb8a19cb616c9696ec224d8f1d9d25678d9e47
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93872718"
---
# <span data-ttu-id="4e1b0-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="4e1b0-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="4e1b0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4e1b0-102">SYNOPSIS</span></span>
<span data-ttu-id="4e1b0-103">복구 서비스 자격 증명 모음에 대 한 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="4e1b0-104">구문과</span><span class="sxs-lookup"><span data-stu-id="4e1b0-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4e1b0-105">설명은</span><span class="sxs-lookup"><span data-stu-id="4e1b0-105">DESCRIPTION</span></span>
<span data-ttu-id="4e1b0-106">**AzRecoveryServicesAsrVaultContext** Cmdlet은 복구 서비스 자격 증명 모음과 관련 된 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="4e1b0-107">예제의</span><span class="sxs-lookup"><span data-stu-id="4e1b0-107">EXAMPLES</span></span>

### <span data-ttu-id="4e1b0-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="4e1b0-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="4e1b0-109">현재 활성 (PowerShell 세션) 복구 서비스 자격 증명 모음에 대 한 ASR vault 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="4e1b0-110">변수</span><span class="sxs-lookup"><span data-stu-id="4e1b0-110">PARAMETERS</span></span>

### <span data-ttu-id="4e1b0-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4e1b0-111">-DefaultProfile</span></span>
<span data-ttu-id="4e1b0-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="4e1b0-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4e1b0-113">CommonParameters</span></span>
<span data-ttu-id="4e1b0-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="4e1b0-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4e1b0-115">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4e1b0-115">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4e1b0-116">입력</span><span class="sxs-lookup"><span data-stu-id="4e1b0-116">INPUTS</span></span>

### <span data-ttu-id="4e1b0-117">않아야</span><span class="sxs-lookup"><span data-stu-id="4e1b0-117">None</span></span>

## <span data-ttu-id="4e1b0-118">출력</span><span class="sxs-lookup"><span data-stu-id="4e1b0-118">OUTPUTS</span></span>

### <span data-ttu-id="4e1b0-119">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="4e1b0-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="4e1b0-120">상속자</span><span class="sxs-lookup"><span data-stu-id="4e1b0-120">NOTES</span></span>

## <span data-ttu-id="4e1b0-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4e1b0-121">RELATED LINKS</span></span>
