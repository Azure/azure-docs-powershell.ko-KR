---
external help file: Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.dll-Help.xml
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices.SiteRecovery/Commands.RecoveryServices.SiteRecovery/help/Set-AzureRmRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: f8d55ec80c6120f2159969ae6a58a531bea50b20
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93529191"
---
# <span data-ttu-id="7f70f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="7f70f-101">Set-AzureRmRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="7f70f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7f70f-102">SYNOPSIS</span></span>
<span data-ttu-id="7f70f-103">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업에 사용할 복구 서비스 자격 증명 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7f70f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="7f70f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesAsrVaultContext -Vault <ARSVault> [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="7f70f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="7f70f-105">DESCRIPTION</span></span>
<span data-ttu-id="7f70f-106">**AzureRmRecoveryServicesAsrVaultContext** cmdlet은 추가 작업을 위해 Azure Site Recovery 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-106">The **Set-AzureRmRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="7f70f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="7f70f-107">EXAMPLES</span></span>

### <span data-ttu-id="7f70f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="7f70f-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzureRmRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="7f70f-109">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업을 위해 자격 증명 모음 컨텍스트를 지정 된 복구 서비스 자격 증명 모음으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="7f70f-110">변수</span><span class="sxs-lookup"><span data-stu-id="7f70f-110">PARAMETERS</span></span>

### <span data-ttu-id="7f70f-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="7f70f-111">-Vault</span></span>
<span data-ttu-id="7f70f-112">복구 서비스 자격 증명 모음에 해당 하는 Recovery Services 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-112">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="7f70f-113">-확인</span><span class="sxs-lookup"><span data-stu-id="7f70f-113">-Confirm</span></span>
<span data-ttu-id="7f70f-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-114">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f70f-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="7f70f-115">-WhatIf</span></span>
<span data-ttu-id="7f70f-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-116">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="7f70f-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-117">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7f70f-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7f70f-118">CommonParameters</span></span>
<span data-ttu-id="7f70f-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="7f70f-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7f70f-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7f70f-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7f70f-121">입력</span><span class="sxs-lookup"><span data-stu-id="7f70f-121">INPUTS</span></span>

### <span data-ttu-id="7f70f-122">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="7f70f-122">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7f70f-123">출력</span><span class="sxs-lookup"><span data-stu-id="7f70f-123">OUTPUTS</span></span>

### <span data-ttu-id="7f70f-124">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="7f70f-124">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="7f70f-125">상속자</span><span class="sxs-lookup"><span data-stu-id="7f70f-125">NOTES</span></span>

## <span data-ttu-id="7f70f-126">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7f70f-126">RELATED LINKS</span></span>

