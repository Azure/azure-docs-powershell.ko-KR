---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212191"
---
# <span data-ttu-id="f5d0e-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="f5d0e-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="f5d0e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f5d0e-102">SYNOPSIS</span></span>
<span data-ttu-id="f5d0e-103">복구 서비스 자격 증명 모음에 대 한 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="f5d0e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f5d0e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f5d0e-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f5d0e-105">DESCRIPTION</span></span>
<span data-ttu-id="f5d0e-106">**AzRecoveryServicesAsrVaultContext** Cmdlet은 복구 서비스 자격 증명 모음과 관련 된 ASR vault 설정 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="f5d0e-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f5d0e-107">EXAMPLES</span></span>

### <span data-ttu-id="f5d0e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f5d0e-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="f5d0e-109">현재 활성 (PowerShell 세션) 복구 서비스 자격 증명 모음에 대 한 ASR vault 설정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="f5d0e-110">변수</span><span class="sxs-lookup"><span data-stu-id="f5d0e-110">PARAMETERS</span></span>

### <span data-ttu-id="f5d0e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f5d0e-111">-DefaultProfile</span></span>
<span data-ttu-id="f5d0e-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f5d0e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f5d0e-113">CommonParameters</span></span>
<span data-ttu-id="f5d0e-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f5d0e-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="f5d0e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f5d0e-116">입력</span><span class="sxs-lookup"><span data-stu-id="f5d0e-116">INPUTS</span></span>

### <span data-ttu-id="f5d0e-117">않아야</span><span class="sxs-lookup"><span data-stu-id="f5d0e-117">None</span></span>

## <span data-ttu-id="f5d0e-118">출력</span><span class="sxs-lookup"><span data-stu-id="f5d0e-118">OUTPUTS</span></span>

### <span data-ttu-id="f5d0e-119">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="f5d0e-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="f5d0e-120">상속자</span><span class="sxs-lookup"><span data-stu-id="f5d0e-120">NOTES</span></span>

## <span data-ttu-id="f5d0e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f5d0e-121">RELATED LINKS</span></span>
