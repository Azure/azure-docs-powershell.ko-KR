---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98337761"
---
# <span data-ttu-id="7674a-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="7674a-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="7674a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7674a-102">SYNOPSIS</span></span>
<span data-ttu-id="7674a-103">Recovery Services 자격 증명 모음의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="7674a-104">구문</span><span class="sxs-lookup"><span data-stu-id="7674a-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7674a-105">설명</span><span class="sxs-lookup"><span data-stu-id="7674a-105">DESCRIPTION</span></span>
<span data-ttu-id="7674a-106">**Get-AzRecoveryServicesVaultProperty** cmdlet은 Recovery Services 자격 증명 모음의 속성을 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="7674a-107">예제</span><span class="sxs-lookup"><span data-stu-id="7674a-107">EXAMPLES</span></span>

### <span data-ttu-id="7674a-108">예제 1: 자격 증명 모음의 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="7674a-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="7674a-109">첫 번째 명령은 자격 증명 모음 개체를 인용한 다음, 자격 증명 모음 $vault 저장합니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="7674a-110">두 번째 명령은 자격 증명 모음 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="7674a-111">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="7674a-111">PARAMETERS</span></span>

### <span data-ttu-id="7674a-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7674a-112">-DefaultProfile</span></span>
<span data-ttu-id="7674a-113">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7674a-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="7674a-114">-VaultId</span></span>
<span data-ttu-id="7674a-115">ARM 자격 증명 모음의 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="7674a-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7674a-116">CommonParameters</span></span>
<span data-ttu-id="7674a-117">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="7674a-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7674a-118">자세한 내용은 [다음](http://go.microsoft.com/fwlink/?LinkID=113216)about_CommonParameters.</span><span class="sxs-lookup"><span data-stu-id="7674a-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7674a-119">입력</span><span class="sxs-lookup"><span data-stu-id="7674a-119">INPUTS</span></span>

### <span data-ttu-id="7674a-120">System.String</span><span class="sxs-lookup"><span data-stu-id="7674a-120">System.String</span></span>

## <span data-ttu-id="7674a-121">출력</span><span class="sxs-lookup"><span data-stu-id="7674a-121">OUTPUTS</span></span>

### <span data-ttu-id="7674a-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span><span class="sxs-lookup"><span data-stu-id="7674a-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="7674a-123">참고 사항</span><span class="sxs-lookup"><span data-stu-id="7674a-123">NOTES</span></span>

## <span data-ttu-id="7674a-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="7674a-124">RELATED LINKS</span></span>

[<span data-ttu-id="7674a-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="7674a-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="7674a-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="7674a-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
