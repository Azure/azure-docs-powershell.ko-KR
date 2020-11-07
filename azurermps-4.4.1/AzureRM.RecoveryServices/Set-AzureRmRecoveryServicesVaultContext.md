---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: d8743b12757d5845107d6a38689059b90bf1e287
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93710968"
---
# <span data-ttu-id="69533-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="69533-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="69533-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="69533-102">SYNOPSIS</span></span>
<span data-ttu-id="69533-103">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="69533-104">구문과</span><span class="sxs-lookup"><span data-stu-id="69533-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="69533-105">설명은</span><span class="sxs-lookup"><span data-stu-id="69533-105">DESCRIPTION</span></span>
<span data-ttu-id="69533-106">**AzureRmRecoveryServicesVaultContext** Cmdlet은 Azure Site Recovery 서비스에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="69533-107">예제의</span><span class="sxs-lookup"><span data-stu-id="69533-107">EXAMPLES</span></span>

## <span data-ttu-id="69533-108">변수</span><span class="sxs-lookup"><span data-stu-id="69533-108">PARAMETERS</span></span>

### <span data-ttu-id="69533-109">-저장실</span><span class="sxs-lookup"><span data-stu-id="69533-109">-Vault</span></span>
<span data-ttu-id="69533-110">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="69533-111">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.RecoveryServices.ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="69533-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="69533-112">-DefaultProfile</span></span>
<span data-ttu-id="69533-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="69533-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="69533-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="69533-114">CommonParameters</span></span>
<span data-ttu-id="69533-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="69533-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="69533-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="69533-117">입력</span><span class="sxs-lookup"><span data-stu-id="69533-117">INPUTS</span></span>

### <span data-ttu-id="69533-118">ARSVault</span><span class="sxs-lookup"><span data-stu-id="69533-118">ARSVault</span></span>
<span data-ttu-id="69533-119">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="69533-119">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="69533-120">출력</span><span class="sxs-lookup"><span data-stu-id="69533-120">OUTPUTS</span></span>

## <span data-ttu-id="69533-121">상속자</span><span class="sxs-lookup"><span data-stu-id="69533-121">NOTES</span></span>

## <span data-ttu-id="69533-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="69533-122">RELATED LINKS</span></span>

