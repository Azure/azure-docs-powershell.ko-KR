---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: b3df84865d29bbcf62074c1b1ed7f5586fb64fee
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703640"
---
# <span data-ttu-id="ef4b2-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef4b2-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="ef4b2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ef4b2-102">SYNOPSIS</span></span>
<span data-ttu-id="ef4b2-103">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ef4b2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="ef4b2-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ef4b2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="ef4b2-105">DESCRIPTION</span></span>
<span data-ttu-id="ef4b2-106">**AzureRmRecoveryServicesVault** Cmdlet은 복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="ef4b2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="ef4b2-107">EXAMPLES</span></span>

## <span data-ttu-id="ef4b2-108">변수</span><span class="sxs-lookup"><span data-stu-id="ef4b2-108">PARAMETERS</span></span>

### <span data-ttu-id="ef4b2-109">-저장실</span><span class="sxs-lookup"><span data-stu-id="ef4b2-109">-Vault</span></span>
<span data-ttu-id="ef4b2-110">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-110">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="ef4b2-111">-확인</span><span class="sxs-lookup"><span data-stu-id="ef4b2-111">-Confirm</span></span>
<span data-ttu-id="ef4b2-112">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-112">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ef4b2-113">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ef4b2-113">-WhatIf</span></span>
<span data-ttu-id="ef4b2-114">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-114">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ef4b2-115">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-115">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ef4b2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ef4b2-116">-DefaultProfile</span></span>
<span data-ttu-id="ef4b2-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ef4b2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ef4b2-118">CommonParameters</span></span>
<span data-ttu-id="ef4b2-119">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ef4b2-120">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ef4b2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ef4b2-121">입력</span><span class="sxs-lookup"><span data-stu-id="ef4b2-121">INPUTS</span></span>

### <span data-ttu-id="ef4b2-122">ARSVault</span><span class="sxs-lookup"><span data-stu-id="ef4b2-122">ARSVault</span></span>
<span data-ttu-id="ef4b2-123">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="ef4b2-123">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="ef4b2-124">출력</span><span class="sxs-lookup"><span data-stu-id="ef4b2-124">OUTPUTS</span></span>

### <span data-ttu-id="ef4b2-125">VaultOperationOutput를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="ef4b2-125">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="ef4b2-126">상속자</span><span class="sxs-lookup"><span data-stu-id="ef4b2-126">NOTES</span></span>

## <span data-ttu-id="ef4b2-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ef4b2-127">RELATED LINKS</span></span>

[<span data-ttu-id="ef4b2-128">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef4b2-128">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="ef4b2-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="ef4b2-129">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="ef4b2-130">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="ef4b2-130">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


