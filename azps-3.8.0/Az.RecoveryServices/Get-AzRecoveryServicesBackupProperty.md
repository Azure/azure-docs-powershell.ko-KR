---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94034346"
---
# <span data-ttu-id="5159b-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="5159b-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="5159b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5159b-102">SYNOPSIS</span></span>
<span data-ttu-id="5159b-103">백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-103">Gets Backup properties.</span></span>

## <span data-ttu-id="5159b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="5159b-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="5159b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="5159b-105">DESCRIPTION</span></span>
<span data-ttu-id="5159b-106">**AzRecoveryServicesBackupProperty** Cmdlet은 복구 서비스 자격 증명 모음에 대 한 백업 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="5159b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="5159b-107">EXAMPLES</span></span>

### <span data-ttu-id="5159b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="5159b-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="5159b-109">자격 증명 모음에 대 한 백업 자격 증명 모음 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="5159b-110">변수</span><span class="sxs-lookup"><span data-stu-id="5159b-110">PARAMETERS</span></span>

### <span data-ttu-id="5159b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5159b-111">-DefaultProfile</span></span>
<span data-ttu-id="5159b-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5159b-113">-저장실</span><span class="sxs-lookup"><span data-stu-id="5159b-113">-Vault</span></span>
<span data-ttu-id="5159b-114">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="5159b-115">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="5159b-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5159b-116">CommonParameters</span></span>
<span data-ttu-id="5159b-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="5159b-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5159b-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="5159b-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5159b-119">입력</span><span class="sxs-lookup"><span data-stu-id="5159b-119">INPUTS</span></span>

### <span data-ttu-id="5159b-120">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="5159b-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="5159b-121">출력</span><span class="sxs-lookup"><span data-stu-id="5159b-121">OUTPUTS</span></span>

### <span data-ttu-id="5159b-122">ASRVaultBackupProperties를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="5159b-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="5159b-123">상속자</span><span class="sxs-lookup"><span data-stu-id="5159b-123">NOTES</span></span>

## <span data-ttu-id="5159b-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5159b-124">RELATED LINKS</span></span>
