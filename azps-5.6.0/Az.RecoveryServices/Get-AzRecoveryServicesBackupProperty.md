---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/get-azrecoveryservicesbackupproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesBackupProperty.md
ms.openlocfilehash: 2cabaaedbd384237cd8be1469ea5f28cbc1e951f
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101984208"
---
# <span data-ttu-id="c2b6c-101">Get-AzRecoveryServicesBackupProperty</span><span class="sxs-lookup"><span data-stu-id="c2b6c-101">Get-AzRecoveryServicesBackupProperty</span></span>

## <span data-ttu-id="c2b6c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2b6c-102">SYNOPSIS</span></span>
<span data-ttu-id="c2b6c-103">Backup 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-103">Gets Backup properties.</span></span>

## <span data-ttu-id="c2b6c-104">구문</span><span class="sxs-lookup"><span data-stu-id="c2b6c-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesBackupProperty -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c2b6c-105">설명</span><span class="sxs-lookup"><span data-stu-id="c2b6c-105">DESCRIPTION</span></span>
<span data-ttu-id="c2b6c-106">**Get-AzRecoveryServicesBackupProperty** cmdlet은 Recovery Services 자격 증명 모음에 대한 백업 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-106">The **Get-AzRecoveryServicesBackupProperty** cmdlet gets backup properties for a Recovery Services vault.</span></span>

## <span data-ttu-id="c2b6c-107">예제</span><span class="sxs-lookup"><span data-stu-id="c2b6c-107">EXAMPLES</span></span>

### <span data-ttu-id="c2b6c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="c2b6c-108">Example 1</span></span>
```
PS C:\> Get-AzRecoveryServicesBackupProperty -Vault $vault
```

<span data-ttu-id="c2b6c-109">자격 증명 모음에 대한 백업 자격 증명 모음 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-109">Get the backup vault property for vault.</span></span>

## <span data-ttu-id="c2b6c-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="c2b6c-110">PARAMETERS</span></span>

### <span data-ttu-id="c2b6c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2b6c-111">-DefaultProfile</span></span>
<span data-ttu-id="c2b6c-112">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c2b6c-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="c2b6c-113">-Vault</span></span>
<span data-ttu-id="c2b6c-114">자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="c2b6c-115">자격 증명 모음은 **AzureRmRecoveryServicesVault 개체가 되어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="c2b6c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2b6c-116">CommonParameters</span></span>
<span data-ttu-id="c2b6c-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="c2b6c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2b6c-118">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="c2b6c-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2b6c-119">입력</span><span class="sxs-lookup"><span data-stu-id="c2b6c-119">INPUTS</span></span>

### <span data-ttu-id="c2b6c-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="c2b6c-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="c2b6c-121">출력</span><span class="sxs-lookup"><span data-stu-id="c2b6c-121">OUTPUTS</span></span>

### <span data-ttu-id="c2b6c-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span><span class="sxs-lookup"><span data-stu-id="c2b6c-122">Microsoft.Azure.Commands.RecoveryServices.ASRVaultBackupProperties</span></span>

## <span data-ttu-id="c2b6c-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="c2b6c-123">NOTES</span></span>

## <span data-ttu-id="c2b6c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="c2b6c-124">RELATED LINKS</span></span>
