---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 466F6B7C-BA7E-4DFD-8504-5A196A335231
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/remove-azurermrecoveryservicesvault
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Remove-AzureRmRecoveryServicesVault.md
ms.openlocfilehash: e6ac59a84e4244cb6d6815f8e3256618cccd661c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535663"
---
# <span data-ttu-id="bea95-101">Remove-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bea95-101">Remove-AzureRmRecoveryServicesVault</span></span>

## <span data-ttu-id="bea95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bea95-102">SYNOPSIS</span></span>
<span data-ttu-id="bea95-103">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-103">Deletes a Recovery Services vault.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bea95-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bea95-104">SYNTAX</span></span>

```
Remove-AzureRmRecoveryServicesVault -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bea95-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bea95-105">DESCRIPTION</span></span>
<span data-ttu-id="bea95-106">**AzureRmRecoveryServicesVault** Cmdlet은 복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-106">The **Remove-AzureRmRecoveryServicesVault** cmdlet deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="bea95-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bea95-107">EXAMPLES</span></span>

### <span data-ttu-id="bea95-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="bea95-108">Example 1</span></span>
```
PS C:\> Remove-AzureRmRecoveryServicesVault -Vault $vault
```

<span data-ttu-id="bea95-109">복구 서비스 자격 증명 모음을 삭제 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-109">Deletes a Recovery Services vault.</span></span>

## <span data-ttu-id="bea95-110">변수</span><span class="sxs-lookup"><span data-stu-id="bea95-110">PARAMETERS</span></span>

### <span data-ttu-id="bea95-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="bea95-111">-Vault</span></span>
<span data-ttu-id="bea95-112">Azure Site Recovery 자격 증명 모음 개체를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-112">Specifies an Azure Site Recovery vault object.</span></span>

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

### <span data-ttu-id="bea95-113">-확인</span><span class="sxs-lookup"><span data-stu-id="bea95-113">-Confirm</span></span>
<span data-ttu-id="bea95-114">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-114">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bea95-115">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bea95-115">-WhatIf</span></span>
<span data-ttu-id="bea95-116">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-116">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="bea95-117">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-117">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bea95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bea95-118">-DefaultProfile</span></span>
<span data-ttu-id="bea95-119">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bea95-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bea95-120">CommonParameters</span></span>
<span data-ttu-id="bea95-121">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bea95-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bea95-122">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bea95-122">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bea95-123">입력</span><span class="sxs-lookup"><span data-stu-id="bea95-123">INPUTS</span></span>

### <span data-ttu-id="bea95-124">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="bea95-124">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="bea95-125">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="bea95-125">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="bea95-126">출력</span><span class="sxs-lookup"><span data-stu-id="bea95-126">OUTPUTS</span></span>

### <span data-ttu-id="bea95-127">VaultOperationOutput를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="bea95-127">Microsoft.Azure.Commands.RecoveryServices.VaultOperationOutput</span></span>

## <span data-ttu-id="bea95-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bea95-128">NOTES</span></span>

## <span data-ttu-id="bea95-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bea95-129">RELATED LINKS</span></span>

[<span data-ttu-id="bea95-130">Get-AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bea95-130">Get-AzureRmRecoveryServicesVault</span></span>](./Get-AzureRmRecoveryServicesVault.md)

[<span data-ttu-id="bea95-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span><span class="sxs-lookup"><span data-stu-id="bea95-131">Get-AzureRmRecoveryServicesVaultSettingsFile</span></span>](./Get-AzureRmRecoveryServicesVaultSettingsFile.md)

[<span data-ttu-id="bea95-132">새로운 AzureRmRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="bea95-132">New-AzureRmRecoveryServicesVault</span></span>](./New-AzureRmRecoveryServicesVault.md)


