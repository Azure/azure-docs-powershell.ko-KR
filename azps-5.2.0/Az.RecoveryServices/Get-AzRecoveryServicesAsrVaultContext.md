---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: cc8f5028a5b2d4917e94ebc666c478ee8d04efa7
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98352557"
---
# <span data-ttu-id="b460e-101">Get-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="b460e-101">Get-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="b460e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b460e-102">SYNOPSIS</span></span>
<span data-ttu-id="b460e-103">Recovery Services 자격 증명 모음에 대한 ASR 자격 증명 모음 설정 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b460e-103">Gets ASR vault settings information for the Recovery Services vault.</span></span>

## <span data-ttu-id="b460e-104">구문</span><span class="sxs-lookup"><span data-stu-id="b460e-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesAsrVaultContext [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b460e-105">설명</span><span class="sxs-lookup"><span data-stu-id="b460e-105">DESCRIPTION</span></span>
<span data-ttu-id="b460e-106">**Get-AzRecoveryServicesAsrVaultContext** cmdlet은 Recovery Services 자격 증명 모음과 관련된 ASR 자격 증명 모음 설정 정보를 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b460e-106">The **Get-AzRecoveryServicesAsrVaultContext** cmdlet gets ASR vault settings information related to the Recovery Services vault.</span></span>

## <span data-ttu-id="b460e-107">예제</span><span class="sxs-lookup"><span data-stu-id="b460e-107">EXAMPLES</span></span>

### <span data-ttu-id="b460e-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b460e-108">Example 1</span></span>
```
PS C:\> $VaultSettings = Get-AzRecoveryServicesAsrVaultContext
```

<span data-ttu-id="b460e-109">현재 활성(PowerShell 세션에서) Recovery Services 자격 증명 모음에 대한 ASR 자격 증명 모음 설정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="b460e-109">Gets the ASR vault settings for the currently active(in the PowerShell session) Recovery Services vault.</span></span>

## <span data-ttu-id="b460e-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="b460e-110">PARAMETERS</span></span>

### <span data-ttu-id="b460e-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b460e-111">-DefaultProfile</span></span>
<span data-ttu-id="b460e-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b460e-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b460e-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b460e-113">CommonParameters</span></span>
<span data-ttu-id="b460e-114">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="b460e-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b460e-115">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="b460e-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b460e-116">입력</span><span class="sxs-lookup"><span data-stu-id="b460e-116">INPUTS</span></span>

### <span data-ttu-id="b460e-117">없음</span><span class="sxs-lookup"><span data-stu-id="b460e-117">None</span></span>

## <span data-ttu-id="b460e-118">출력</span><span class="sxs-lookup"><span data-stu-id="b460e-118">OUTPUTS</span></span>

### <span data-ttu-id="b460e-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="b460e-119">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="b460e-120">참고 사항</span><span class="sxs-lookup"><span data-stu-id="b460e-120">NOTES</span></span>

## <span data-ttu-id="b460e-121">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b460e-121">RELATED LINKS</span></span>
