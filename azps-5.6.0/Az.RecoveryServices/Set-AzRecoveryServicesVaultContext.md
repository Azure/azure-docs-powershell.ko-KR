---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 04fa3c9a7024b8a9e1f525a4ef131ae151f25804
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101997397"
---
# <span data-ttu-id="239b4-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="239b4-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="239b4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="239b4-102">SYNOPSIS</span></span>

<span data-ttu-id="239b4-103">자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-103">Sets vault context.</span></span>

## <span data-ttu-id="239b4-104">구문</span><span class="sxs-lookup"><span data-stu-id="239b4-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="239b4-105">설명</span><span class="sxs-lookup"><span data-stu-id="239b4-105">DESCRIPTION</span></span>

<span data-ttu-id="239b4-106">**Set-AzRecoveryServicesVaultContext** cmdlet은 Azure Site Recovery 서비스에 대한 자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

<span data-ttu-id="239b4-107">경고: 이 cmdlet은 향후 중단되는 변경 릴리스에서 사용되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-107">Warning: This cmdlet is being deprecated in a future breaking change release.</span></span> <span data-ttu-id="239b4-108">대체할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-108">There will be no replacement for it.</span></span> <span data-ttu-id="239b4-109">앞으로 모든 Recovery Services 명령에서 -VaultId 매개 변수를 사용하시기 바랍니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-109">Please use the -VaultId parameter in all Recovery Services commands going forward.</span></span>

## <span data-ttu-id="239b4-110">예제</span><span class="sxs-lookup"><span data-stu-id="239b4-110">EXAMPLES</span></span>

### <span data-ttu-id="239b4-111">예제 1</span><span class="sxs-lookup"><span data-stu-id="239b4-111">Example 1</span></span>

```powershell
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="239b4-112">자격 증명 모음 컨텍스트를 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-112">Sets vault context.</span></span>

## <span data-ttu-id="239b4-113">매개 변수</span><span class="sxs-lookup"><span data-stu-id="239b4-113">PARAMETERS</span></span>

### <span data-ttu-id="239b4-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="239b4-114">-DefaultProfile</span></span>

<span data-ttu-id="239b4-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="239b4-116">-Vault</span><span class="sxs-lookup"><span data-stu-id="239b4-116">-Vault</span></span>

<span data-ttu-id="239b4-117">자격 증명 모음의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-117">Specifies the name of the vault.</span></span>
<span data-ttu-id="239b4-118">자격 증명 모음은 **AzureRmRecoveryServicesVault 개체가 되어야** 합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-118">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="239b4-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="239b4-119">CommonParameters</span></span>
<span data-ttu-id="239b4-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="239b4-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="239b4-121">자세한 내용은 를 [about_CommonParameters.](http://go.microsoft.com/fwlink/?LinkID=113216)</span><span class="sxs-lookup"><span data-stu-id="239b4-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="239b4-122">입력</span><span class="sxs-lookup"><span data-stu-id="239b4-122">INPUTS</span></span>

### <span data-ttu-id="239b4-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span><span class="sxs-lookup"><span data-stu-id="239b4-123">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="239b4-124">출력</span><span class="sxs-lookup"><span data-stu-id="239b4-124">OUTPUTS</span></span>

### <span data-ttu-id="239b4-125">System.Void</span><span class="sxs-lookup"><span data-stu-id="239b4-125">System.Void</span></span>

## <span data-ttu-id="239b4-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="239b4-126">NOTES</span></span>

## <span data-ttu-id="239b4-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="239b4-127">RELATED LINKS</span></span>
