---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: da541e9f019dfb82efc496ce60ab300229e36ac0
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100192924"
---
# <span data-ttu-id="e47a3-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="e47a3-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="e47a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e47a3-102">SYNOPSIS</span></span>
<span data-ttu-id="e47a3-103">Recovery Services 자격 증명 모음의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="e47a3-104">구문</span><span class="sxs-lookup"><span data-stu-id="e47a3-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="e47a3-105">설명</span><span class="sxs-lookup"><span data-stu-id="e47a3-105">DESCRIPTION</span></span>
<span data-ttu-id="e47a3-106">**Get-AzRecoveryServicesVaultProperty** cmdlet은 Recovery Services 자격 증명 모음의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="e47a3-107">예제</span><span class="sxs-lookup"><span data-stu-id="e47a3-107">EXAMPLES</span></span>

### <span data-ttu-id="e47a3-108">예제 1: 자격 증명 모음의 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="e47a3-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -ResourceGroupName "resourceGroup" -Name "vaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
PS C:\> $encryption.encryptionProperties
```

<span data-ttu-id="e47a3-109">첫 번째 명령은 자격 증명 모음 개체를 인용한 다음, 자격 증명 모음 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="e47a3-110">두 번째 명령은 자격 증명 모음 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-110">The second command Gets the Vault Properties.</span></span> <span data-ttu-id="e47a3-111">다음으로 자격 증명 모음의 encryptionProperties에 액세스합니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-111">Next we access the encryptionProperties of the vault.</span></span>

## <span data-ttu-id="e47a3-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="e47a3-112">PARAMETERS</span></span>

### <span data-ttu-id="e47a3-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e47a3-113">-DefaultProfile</span></span>
<span data-ttu-id="e47a3-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e47a3-115">-VaultId</span><span class="sxs-lookup"><span data-stu-id="e47a3-115">-VaultId</span></span>
<span data-ttu-id="e47a3-116">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-116">ARM ID of the Recovery Services Vault.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="e47a3-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e47a3-117">CommonParameters</span></span>
<span data-ttu-id="e47a3-118">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="e47a3-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e47a3-119">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="e47a3-119">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e47a3-120">입력</span><span class="sxs-lookup"><span data-stu-id="e47a3-120">INPUTS</span></span>

### <span data-ttu-id="e47a3-121">System.String</span><span class="sxs-lookup"><span data-stu-id="e47a3-121">System.String</span></span>

## <span data-ttu-id="e47a3-122">출력</span><span class="sxs-lookup"><span data-stu-id="e47a3-122">OUTPUTS</span></span>

### <span data-ttu-id="e47a3-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="e47a3-123">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="e47a3-124">참고 사항</span><span class="sxs-lookup"><span data-stu-id="e47a3-124">NOTES</span></span>

## <span data-ttu-id="e47a3-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="e47a3-125">RELATED LINKS</span></span>

[<span data-ttu-id="e47a3-126">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="e47a3-126">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="e47a3-127">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="e47a3-127">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
