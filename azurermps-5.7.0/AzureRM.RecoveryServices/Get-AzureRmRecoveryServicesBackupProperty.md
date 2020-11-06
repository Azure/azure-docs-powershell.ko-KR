---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: 19e443a4e7bca12a988e3a339fe9d568d81431b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93533680"
---
# <span data-ttu-id="a4d95-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="a4d95-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="a4d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a4d95-102">SYNOPSIS</span></span>
<span data-ttu-id="a4d95-103">백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a4d95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="a4d95-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a4d95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="a4d95-105">DESCRIPTION</span></span>
<span data-ttu-id="a4d95-106">**AzureRmRecoveryServicesBackupProperty** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="a4d95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="a4d95-107">EXAMPLES</span></span>

### <span data-ttu-id="a4d95-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="a4d95-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="a4d95-109">자격 증명 모음에 대 한 백업 자격 증명 모음 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="a4d95-110">변수</span><span class="sxs-lookup"><span data-stu-id="a4d95-110">PARAMETERS</span></span>

### <span data-ttu-id="a4d95-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="a4d95-111">-Vault</span></span>
<span data-ttu-id="a4d95-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="a4d95-113">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

```yaml
Type: ARSVault
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="a4d95-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a4d95-114">-DefaultProfile</span></span>
<span data-ttu-id="a4d95-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a4d95-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a4d95-116">CommonParameters</span></span>
<span data-ttu-id="a4d95-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="a4d95-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a4d95-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a4d95-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a4d95-119">입력</span><span class="sxs-lookup"><span data-stu-id="a4d95-119">INPUTS</span></span>

### <span data-ttu-id="a4d95-120">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="a4d95-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="a4d95-121">출력</span><span class="sxs-lookup"><span data-stu-id="a4d95-121">OUTPUTS</span></span>

### <span data-ttu-id="a4d95-122">ASRVaultBackupProperties를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="a4d95-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="a4d95-123">상속자</span><span class="sxs-lookup"><span data-stu-id="a4d95-123">NOTES</span></span>

## <span data-ttu-id="a4d95-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a4d95-124">RELATED LINKS</span></span>

