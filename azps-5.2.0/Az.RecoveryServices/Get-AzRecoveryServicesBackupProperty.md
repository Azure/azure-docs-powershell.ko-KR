---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: efe463bab4195dfb09692f76d0e02e3aeaa59344
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98356030"
---
# <span data-ttu-id="61fec-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="61fec-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="61fec-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="61fec-102">SYNOPSIS</span></span>
<span data-ttu-id="61fec-103">Backup 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-103">Gets Backup properties.</span></span>

## <span data-ttu-id="61fec-104">구문</span><span class="sxs-lookup"><span data-stu-id="61fec-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="61fec-105">설명</span><span class="sxs-lookup"><span data-stu-id="61fec-105">DESCRIPTION</span></span>
<span data-ttu-id="61fec-106">**Get-AzRecoveryServicesBackupProperty** cmdlet은 Recovery Services 자격 증명 모음에 대한 백업 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="61fec-107">예제</span><span class="sxs-lookup"><span data-stu-id="61fec-107">EXAMPLES</span></span>

### <span data-ttu-id="61fec-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="61fec-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="61fec-109">자격 증명 모음에 대한 백업 자격 증명 모음 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="61fec-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="61fec-110">PARAMETERS</span></span>

### <span data-ttu-id="61fec-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="61fec-111">-DefaultProfile</span></span>
<span data-ttu-id="61fec-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="61fec-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="61fec-113">-Vault</span></span>
<span data-ttu-id="61fec-114">자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="61fec-115">자격 증명 모음은 **AzureRmRecoveryServicesVault 개체가 되어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="61fec-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="61fec-116">CommonParameters</span></span>
<span data-ttu-id="61fec-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="61fec-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="61fec-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="61fec-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="61fec-119">입력</span><span class="sxs-lookup"><span data-stu-id="61fec-119">INPUTS</span></span>

### <span data-ttu-id="61fec-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="61fec-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="61fec-121">출력</span><span class="sxs-lookup"><span data-stu-id="61fec-121">OUTPUTS</span></span>

### <span data-ttu-id="61fec-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="61fec-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="61fec-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="61fec-123">NOTES</span></span>

## <span data-ttu-id="61fec-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="61fec-124">RELATED LINKS</span></span>
