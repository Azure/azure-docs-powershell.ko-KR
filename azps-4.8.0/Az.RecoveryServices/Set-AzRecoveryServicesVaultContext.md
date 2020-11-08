---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94214016"
---
# <span data-ttu-id="1d708-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="1d708-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="1d708-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1d708-102">SYNOPSIS</span></span>

<span data-ttu-id="1d708-103">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-103">Sets vault context.</span></span>

## <span data-ttu-id="1d708-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1d708-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1d708-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1d708-105">DESCRIPTION</span></span>

<span data-ttu-id="1d708-106">**AzRecoveryServicesVaultContext** Cmdlet은 Azure Site Recovery 서비스에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="1d708-107">경고:이 cmdlet은 향후 주요 변경 릴리스에서 더 이상 사용 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="1d708-108">여기에는 대체 방법이 없습니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-108">There will be no replacement for it.</span></span> <span data-ttu-id="1d708-109">모든 복구 서비스 명령에-VaultId 매개 변수를 사용 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d708-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="1d708-110">예제의</span><span class="sxs-lookup"><span data-stu-id="1d708-110">EXAMPLES</span></span>

### <span data-ttu-id="1d708-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="1d708-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="1d708-112">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-112">Sets vault context.</span></span>

## <span data-ttu-id="1d708-113">변수</span><span class="sxs-lookup"><span data-stu-id="1d708-113">PARAMETERS</span></span>

### <span data-ttu-id="1d708-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1d708-114">-DefaultProfile</span></span>

<span data-ttu-id="1d708-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1d708-116">-저장실</span><span class="sxs-lookup"><span data-stu-id="1d708-116">-Vault</span></span>

<span data-ttu-id="1d708-117">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="1d708-118">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="1d708-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1d708-119">CommonParameters</span></span>
<span data-ttu-id="1d708-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1d708-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1d708-121">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="1d708-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1d708-122">입력</span><span class="sxs-lookup"><span data-stu-id="1d708-122">INPUTS</span></span>

### <span data-ttu-id="1d708-123">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="1d708-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1d708-124">출력</span><span class="sxs-lookup"><span data-stu-id="1d708-124">OUTPUTS</span></span>

### <span data-ttu-id="1d708-125">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1d708-125">System.Void</span></span>

## <span data-ttu-id="1d708-126">상속자</span><span class="sxs-lookup"><span data-stu-id="1d708-126">NOTES</span></span>

## <span data-ttu-id="1d708-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1d708-127">RELATED LINKS</span></span>
