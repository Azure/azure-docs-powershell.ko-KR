---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337658"
---
# <span data-ttu-id="f914b-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f914b-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="f914b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f914b-102">SYNOPSIS</span></span>
<span data-ttu-id="f914b-103">Recovery Services 자격 증명 모음을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f914b-104">구문</span><span class="sxs-lookup"><span data-stu-id="f914b-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f914b-105">설명</span><span class="sxs-lookup"><span data-stu-id="f914b-105">DESCRIPTION</span></span>
<span data-ttu-id="f914b-106">**Remove-AzRecoveryServicesVault** cmdlet은 Recovery Services 자격 증명 모음을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f914b-107">예제</span><span class="sxs-lookup"><span data-stu-id="f914b-107">EXAMPLES</span></span>

### <span data-ttu-id="f914b-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="f914b-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="f914b-109">Recovery Services 자격 증명 모음을 삭제합니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="f914b-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="f914b-110">PARAMETERS</span></span>

### <span data-ttu-id="f914b-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f914b-111">-DefaultProfile</span></span>
<span data-ttu-id="f914b-112">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f914b-113">-Vault</span><span class="sxs-lookup"><span data-stu-id="f914b-113">-Vault</span></span>
<span data-ttu-id="f914b-114">Azure Site Recovery 자격 증명 모음 개체를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="f914b-115">-Confirm</span><span class="sxs-lookup"><span data-stu-id="f914b-115">-Confirm</span></span>
<span data-ttu-id="f914b-116">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f914b-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f914b-117">-WhatIf</span></span>
<span data-ttu-id="f914b-118">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="f914b-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f914b-119">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f914b-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f914b-120">CommonParameters</span></span>
<span data-ttu-id="f914b-121">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f914b-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f914b-122">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="f914b-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f914b-123">입력</span><span class="sxs-lookup"><span data-stu-id="f914b-123">INPUTS</span></span>

### <span data-ttu-id="f914b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="f914b-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="f914b-125">출력</span><span class="sxs-lookup"><span data-stu-id="f914b-125">OUTPUTS</span></span>

### <span data-ttu-id="f914b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span><span class="sxs-lookup"><span data-stu-id="f914b-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="f914b-127">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f914b-127">NOTES</span></span>

## <span data-ttu-id="f914b-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f914b-128">RELATED LINKS</span></span>

[<span data-ttu-id="f914b-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f914b-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="f914b-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="f914b-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="f914b-131">New-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="f914b-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


