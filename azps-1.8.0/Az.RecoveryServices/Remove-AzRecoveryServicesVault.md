---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: a0f21fc8cde4c64eaf1e8ea27bf05eff8d664c55
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699622"
---
# <span data-ttu-id="b176d-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b176d-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b176d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b176d-102">SYNOPSIS</span></span>
<span data-ttu-id="b176d-103">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b176d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b176d-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b176d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b176d-105">DESCRIPTION</span></span>
<span data-ttu-id="b176d-106">**AzRecoveryServicesVault** Cmdlet은 복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b176d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b176d-107">EXAMPLES</span></span>

### <span data-ttu-id="b176d-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b176d-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="b176d-109">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b176d-110">변수</span><span class="sxs-lookup"><span data-stu-id="b176d-110">PARAMETERS</span></span>

### <span data-ttu-id="b176d-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b176d-111">-DefaultProfile</span></span>
<span data-ttu-id="b176d-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b176d-113">-저장실</span><span class="sxs-lookup"><span data-stu-id="b176d-113">-Vault</span></span>
<span data-ttu-id="b176d-114">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="b176d-115">-확인</span><span class="sxs-lookup"><span data-stu-id="b176d-115">-Confirm</span></span>
<span data-ttu-id="b176d-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b176d-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b176d-117">-WhatIf</span></span>
<span data-ttu-id="b176d-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b176d-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b176d-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b176d-120">CommonParameters</span></span>
<span data-ttu-id="b176d-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b176d-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b176d-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b176d-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b176d-123">입력</span><span class="sxs-lookup"><span data-stu-id="b176d-123">INPUTS</span></span>

### <span data-ttu-id="b176d-124">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="b176d-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b176d-125">출력</span><span class="sxs-lookup"><span data-stu-id="b176d-125">OUTPUTS</span></span>

### <span data-ttu-id="b176d-126">VaultOperationOutput를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="b176d-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="b176d-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b176d-127">NOTES</span></span>

## <span data-ttu-id="b176d-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b176d-128">RELATED LINKS</span></span>

[<span data-ttu-id="b176d-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b176d-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b176d-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b176d-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b176d-131">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b176d-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


