---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98326206"
---
# <span data-ttu-id="49b3d-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="49b3d-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="49b3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="49b3d-102">SYNOPSIS</span></span>
<span data-ttu-id="49b3d-103">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업에 사용할 Recovery Services 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="49b3d-104">구문</span><span class="sxs-lookup"><span data-stu-id="49b3d-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="49b3d-105">설명</span><span class="sxs-lookup"><span data-stu-id="49b3d-105">DESCRIPTION</span></span>
<span data-ttu-id="49b3d-106">**Set-AzRecoveryServicesAsrVaultContext** cmdlet은 추가 작업을 위해 Azure Site Recovery 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="49b3d-107">예제</span><span class="sxs-lookup"><span data-stu-id="49b3d-107">EXAMPLES</span></span>

### <span data-ttu-id="49b3d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="49b3d-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="49b3d-109">자격 증명 모음 컨텍스트를 현재 PowerShell 세션의 후속 Azure Site Recovery 작업에 대해 지정된 Recovery Services 자격 증명 모음으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="49b3d-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="49b3d-110">PARAMETERS</span></span>

### <span data-ttu-id="49b3d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="49b3d-111">-DefaultProfile</span></span>
<span data-ttu-id="49b3d-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="49b3d-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="49b3d-113">-Vault</span></span>
<span data-ttu-id="49b3d-114">Recovery Services 자격 증명 모음에 해당하는 Recovery Services 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="49b3d-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="49b3d-115">-Confirm</span></span>
<span data-ttu-id="49b3d-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-116">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b3d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="49b3d-117">-WhatIf</span></span>
<span data-ttu-id="49b3d-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="49b3d-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="49b3d-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-119">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="49b3d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="49b3d-120">CommonParameters</span></span>
<span data-ttu-id="49b3d-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="49b3d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="49b3d-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="49b3d-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="49b3d-123">입력</span><span class="sxs-lookup"><span data-stu-id="49b3d-123">INPUTS</span></span>

### <span data-ttu-id="49b3d-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="49b3d-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="49b3d-125">출력</span><span class="sxs-lookup"><span data-stu-id="49b3d-125">OUTPUTS</span></span>

### <span data-ttu-id="49b3d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span><span class="sxs-lookup"><span data-stu-id="49b3d-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="49b3d-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="49b3d-127">NOTES</span></span>

## <span data-ttu-id="49b3d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="49b3d-128">RELATED LINKS</span></span>
