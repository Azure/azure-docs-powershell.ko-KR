---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 3e93df0adfe1e1bc10d5ea74dd189bee60595824
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703642"
---
# <span data-ttu-id="48f88-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="48f88-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="48f88-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="48f88-102">SYNOPSIS</span></span>
<span data-ttu-id="48f88-103">백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="48f88-104">구문과</span><span class="sxs-lookup"><span data-stu-id="48f88-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="48f88-105">설명은</span><span class="sxs-lookup"><span data-stu-id="48f88-105">DESCRIPTION</span></span>
<span data-ttu-id="48f88-106">**AzureRmRecoveryServicesBackupProperty** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="48f88-107">예제의</span><span class="sxs-lookup"><span data-stu-id="48f88-107">EXAMPLES</span></span>

## <span data-ttu-id="48f88-108">변수</span><span class="sxs-lookup"><span data-stu-id="48f88-108">PARAMETERS</span></span>

### <span data-ttu-id="48f88-109">-저장실</span><span class="sxs-lookup"><span data-stu-id="48f88-109">-Vault</span></span>
<span data-ttu-id="48f88-110">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-110">Specifies the name of the vault.</span></span>
<span data-ttu-id="48f88-111">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-111">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="48f88-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="48f88-112">-DefaultProfile</span></span>
<span data-ttu-id="48f88-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="48f88-114">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="48f88-114">CommonParameters</span></span>
<span data-ttu-id="48f88-115">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="48f88-115">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="48f88-116">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="48f88-116">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="48f88-117">입력</span><span class="sxs-lookup"><span data-stu-id="48f88-117">INPUTS</span></span>

### <span data-ttu-id="48f88-118">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="48f88-118">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="48f88-119">출력</span><span class="sxs-lookup"><span data-stu-id="48f88-119">OUTPUTS</span></span>

### <span data-ttu-id="48f88-120">ASRVaultBackupProperties를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="48f88-120">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="48f88-121">상속자</span><span class="sxs-lookup"><span data-stu-id="48f88-121">NOTES</span></span>

## <span data-ttu-id="48f88-122">관련 링크</span><span class="sxs-lookup"><span data-stu-id="48f88-122">RELATED LINKS</span></span>

