---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/remove-azrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Remove-AzRecoveryServicesVault.md
ms.openlocfilehash: 4e6dab95f110e25f24781b2ffbd01a016bdaa9fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94043541"
---
# <span data-ttu-id="b2caa-101">Remove-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2caa-101">Remove-AzRecoveryServicesVault</span></span>

## <span data-ttu-id="b2caa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b2caa-102">SYNOPSIS</span></span>
<span data-ttu-id="b2caa-103">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-103">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b2caa-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b2caa-104">SYNTAX</span></span>

```
Remove-AzRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b2caa-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b2caa-105">DESCRIPTION</span></span>
<span data-ttu-id="b2caa-106">**AzRecoveryServicesVault** Cmdlet은 복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-106">The **Remove-AzRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b2caa-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b2caa-107">EXAMPLES</span></span>

### <span data-ttu-id="b2caa-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="b2caa-108">Example 1</span></span>
```
PS C:\> Remove-AzRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="b2caa-109">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="b2caa-110">변수</span><span class="sxs-lookup"><span data-stu-id="b2caa-110">PARAMETERS</span></span>

### <span data-ttu-id="b2caa-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b2caa-111">-DefaultProfile</span></span>
<span data-ttu-id="b2caa-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b2caa-113">-저장실</span><span class="sxs-lookup"><span data-stu-id="b2caa-113">-Vault</span></span>
<span data-ttu-id="b2caa-114">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-114">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="b2caa-115">-확인</span><span class="sxs-lookup"><span data-stu-id="b2caa-115">-Confirm</span></span>
<span data-ttu-id="b2caa-116">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-116">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b2caa-117">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b2caa-117">-WhatIf</span></span>
<span data-ttu-id="b2caa-118">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-118">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b2caa-119">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-119">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b2caa-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b2caa-120">CommonParameters</span></span>
<span data-ttu-id="b2caa-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b2caa-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b2caa-122">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="b2caa-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b2caa-123">입력</span><span class="sxs-lookup"><span data-stu-id="b2caa-123">INPUTS</span></span>

### <span data-ttu-id="b2caa-124">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="b2caa-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="b2caa-125">출력</span><span class="sxs-lookup"><span data-stu-id="b2caa-125">OUTPUTS</span></span>

### <span data-ttu-id="b2caa-126">VaultOperationOutput를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="b2caa-126">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="b2caa-127">상속자</span><span class="sxs-lookup"><span data-stu-id="b2caa-127">NOTES</span></span>

## <span data-ttu-id="b2caa-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b2caa-128">RELATED LINKS</span></span>

[<span data-ttu-id="b2caa-129">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2caa-129">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="b2caa-130">Get-AzRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="b2caa-130">Get-AzRecoveryServicesVaultSettingsFile</span></span>](./Get-AzRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="b2caa-131">새로운 AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="b2caa-131">New-AzRecoveryServicesVault</span></span>](./New-AzRecoveryServicesVault.md)


