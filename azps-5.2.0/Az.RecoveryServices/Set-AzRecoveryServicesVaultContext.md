---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 48454b3b6bda283763b05657b0bc652fa9973233
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98368103"
---
# <span data-ttu-id="7587e-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="7587e-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="7587e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7587e-102">SYNOPSIS</span></span>

<span data-ttu-id="7587e-103">자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-103">Sets vault context.</span></span>

## <span data-ttu-id="7587e-104">구문</span><span class="sxs-lookup"><span data-stu-id="7587e-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7587e-105">설명</span><span class="sxs-lookup"><span data-stu-id="7587e-105">DESCRIPTION</span></span>

<span data-ttu-id="7587e-106">**Set-AzRecoveryServicesVaultContext** cmdlet은 Azure Site Recovery 서비스에 대한 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="7587e-107">경고: 이 cmdlet은 향후 중단되는 변경 릴리스에서 더 이상 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="7587e-108">대체할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-108">There will be no replacement for it.</span></span> <span data-ttu-id="7587e-109">앞으로 모든 Recovery Services 명령에서 -VaultId 매개 변수를 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="7587e-110">예제</span><span class="sxs-lookup"><span data-stu-id="7587e-110">EXAMPLES</span></span>

### <span data-ttu-id="7587e-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="7587e-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="7587e-112">자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-112">Sets vault context.</span></span>

## <span data-ttu-id="7587e-113">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7587e-113">PARAMETERS</span></span>

### <span data-ttu-id="7587e-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7587e-114">-DefaultProfile</span></span>

<span data-ttu-id="7587e-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7587e-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="7587e-116">-Vault</span></span>

<span data-ttu-id="7587e-117">자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="7587e-118">자격 증명 모음은 **AzureRmRecoveryServicesVault 개체가 되어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="7587e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7587e-119">CommonParameters</span></span>
<span data-ttu-id="7587e-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7587e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7587e-121">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7587e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7587e-122">입력</span><span class="sxs-lookup"><span data-stu-id="7587e-122">INPUTS</span></span>

### <span data-ttu-id="7587e-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="7587e-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="7587e-124">출력</span><span class="sxs-lookup"><span data-stu-id="7587e-124">OUTPUTS</span></span>

### <span data-ttu-id="7587e-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="7587e-125">System.Void</span></span>

## <span data-ttu-id="7587e-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7587e-126">NOTES</span></span>

## <span data-ttu-id="7587e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7587e-127">RELATED LINKS</span></span>
