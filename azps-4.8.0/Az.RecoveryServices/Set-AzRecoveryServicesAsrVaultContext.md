---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.SiteRecovery.dll-Help.xml
Module Name: Az.RecoveryServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesasrvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesAsrVaultContext.md
ms.openlocfilehash: 493dea664ac603e3800c0dcdd47ddeb378c5f0a2
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94204923"
---
# <span data-ttu-id="26caa-101">Set-AzRecoveryServicesAsrVaultContext</span><span class="sxs-lookup"><span data-stu-id="26caa-101">Set-AzRecoveryServicesAsrVaultContext</span></span>

## <span data-ttu-id="26caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26caa-102">SYNOPSIS</span></span>
<span data-ttu-id="26caa-103">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업에 사용할 복구 서비스 자격 증명 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-103">Sets the Recovery Services vault context to be used for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="26caa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="26caa-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesAsrVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="26caa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="26caa-105">DESCRIPTION</span></span>
<span data-ttu-id="26caa-106">**AzRecoveryServicesAsrVaultContext** cmdlet은 추가 작업을 위해 Azure Site Recovery 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-106">The **Set-AzRecoveryServicesAsrVaultContext** cmdlet sets the Azure Site Recovery vault context for further operations.</span></span>

## <span data-ttu-id="26caa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="26caa-107">EXAMPLES</span></span>

### <span data-ttu-id="26caa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="26caa-108">Example 1</span></span>
```
PS C:\> $vaultSettings = Set-AzRecoveryServicesAsrVaultContext -Vault $RecoveryServicesVault
```

<span data-ttu-id="26caa-109">현재 PowerShell 세션에서 후속 Azure Site Recovery 작업을 위해 자격 증명 모음 컨텍스트를 지정 된 복구 서비스 자격 증명 모음으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-109">Sets the vault context to the specified Recovery Services vault for subsequent Azure Site Recovery operations in the current PowerShell session.</span></span>

## <span data-ttu-id="26caa-110">변수</span><span class="sxs-lookup"><span data-stu-id="26caa-110">PARAMETERS</span></span>

### <span data-ttu-id="26caa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26caa-111">-DefaultProfile</span></span>
<span data-ttu-id="26caa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="26caa-113">-저장실</span><span class="sxs-lookup"><span data-stu-id="26caa-113">-Vault</span></span>
<span data-ttu-id="26caa-114">복구 서비스 자격 증명 모음에 해당 하는 Recovery Services 자격 증명 모음 개체입니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-114">The Recovery Services vault object corresponding to the Recovery Services vault.</span></span>

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

### <span data-ttu-id="26caa-115">-확인</span><span class="sxs-lookup"><span data-stu-id="26caa-115">-Confirm</span></span>
<span data-ttu-id="26caa-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="26caa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="26caa-117">-WhatIf</span></span>
<span data-ttu-id="26caa-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-118">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="26caa-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="26caa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26caa-120">CommonParameters</span></span>
<span data-ttu-id="26caa-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="26caa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26caa-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="26caa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26caa-123">입력</span><span class="sxs-lookup"><span data-stu-id="26caa-123">INPUTS</span></span>

### <span data-ttu-id="26caa-124">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="26caa-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="26caa-125">출력</span><span class="sxs-lookup"><span data-stu-id="26caa-125">OUTPUTS</span></span>

### <span data-ttu-id="26caa-126">SiteRecovery. ASRVaultSettings에 대 한 서비스</span><span class="sxs-lookup"><span data-stu-id="26caa-126">Microsoft.Azure.Commands.RecoveryServices.SiteRecovery.ASRVaultSettings</span></span>

## <span data-ttu-id="26caa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="26caa-127">NOTES</span></span>

## <span data-ttu-id="26caa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26caa-128">RELATED LINKS</span></span>
