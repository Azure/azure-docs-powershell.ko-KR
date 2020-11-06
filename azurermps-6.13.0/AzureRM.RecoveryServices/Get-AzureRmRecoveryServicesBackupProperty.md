---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/get-azurermrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Get-AzureRmRecoveryServicesBackupProperty.md
ms.openlocfilehash: d900da862572c0e3a51f288a7e6bec948f7aeba4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529432"
---
# <span data-ttu-id="6aa38-101">Get-AzureRmRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="6aa38-101">Get-AzureRmRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="6aa38-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6aa38-102">SYNOPSIS</span></span>
<span data-ttu-id="6aa38-103">백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-103">Gets Backup properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6aa38-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6aa38-104">SYNTAX</span></span>

```
Get-AzureRmRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6aa38-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6aa38-105">DESCRIPTION</span></span>
<span data-ttu-id="6aa38-106">**AzureRmRecoveryServicesBackupProperty** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-106">The **Get-AzureRmRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="6aa38-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6aa38-107">EXAMPLES</span></span>

### <span data-ttu-id="6aa38-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="6aa38-108">Example 1</span></span>
```
PS C:\> Get-AzureRmRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="6aa38-109">자격 증명 모음에 대 한 백업 자격 증명 모음 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="6aa38-110">변수</span><span class="sxs-lookup"><span data-stu-id="6aa38-110">PARAMETERS</span></span>

### <span data-ttu-id="6aa38-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="6aa38-111">-Vault</span></span>
<span data-ttu-id="6aa38-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="6aa38-113">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="6aa38-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6aa38-114">-DefaultProfile</span></span>
<span data-ttu-id="6aa38-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6aa38-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6aa38-116">CommonParameters</span></span>
<span data-ttu-id="6aa38-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6aa38-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6aa38-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6aa38-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6aa38-119">입력</span><span class="sxs-lookup"><span data-stu-id="6aa38-119">INPUTS</span></span>

### <span data-ttu-id="6aa38-120">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="6aa38-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="6aa38-121">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="6aa38-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="6aa38-122">출력</span><span class="sxs-lookup"><span data-stu-id="6aa38-122">OUTPUTS</span></span>

### <span data-ttu-id="6aa38-123">ASRVaultBackupProperties를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="6aa38-123">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="6aa38-124">상속자</span><span class="sxs-lookup"><span data-stu-id="6aa38-124">NOTES</span></span>

## <span data-ttu-id="6aa38-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6aa38-125">RELATED LINKS</span></span>
