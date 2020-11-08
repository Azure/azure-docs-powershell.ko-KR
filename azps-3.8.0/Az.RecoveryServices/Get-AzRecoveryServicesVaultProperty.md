---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.Backup.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: C2A7F37B-5713-4430-B83F-C6745692396D
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/get-azrecoveryservicesvaultproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Get-AzRecoveryServicesVaultProperty.md
ms.openlocfilehash: 6602f1005877d4e38546338fd44d8fc51991a7b6
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94044715"
---
# <span data-ttu-id="6b19f-101">Get-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6b19f-101">Get-AzRecoveryServicesVaultProperty</span></span>

## <span data-ttu-id="6b19f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6b19f-102">SYNOPSIS</span></span>
<span data-ttu-id="6b19f-103">복구 서비스 자격 증명 모음의 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-103">Returns the properties of a Recovery Services Vault.</span></span>

## <span data-ttu-id="6b19f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="6b19f-104">SYNTAX</span></span>

```
Get-AzRecoveryServicesVaultProperty [-VaultId <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="6b19f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="6b19f-105">DESCRIPTION</span></span>
<span data-ttu-id="6b19f-106">**AzRecoveryServicesVaultProperty** Cmdlet은 Recovery services 자격 증명 모음의 속성을 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-106">The **Get-AzRecoveryServicesVaultProperty** cmdlet returns the properties of a Recovery services vault.</span></span>

## <span data-ttu-id="6b19f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="6b19f-107">EXAMPLES</span></span>

### <span data-ttu-id="6b19f-108">예제 1: 자격 증명 모음의 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="6b19f-108">Example 1: Get Properties of a vault</span></span>
```
PS C:\> $vault = Get-AzRecoveryServicesVault -Name "MyVaultName"
PS C:\> $props = Get-AzRecoveryServicesVaultProperty -VaultId $vault.Id
```

<span data-ttu-id="6b19f-109">첫 번째 명령은 자격 증명 모음 개체를 가져온 다음 $vault 변수에 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-109">The first command gets a Vault object and then stores it in the $vault variable.</span></span>
<span data-ttu-id="6b19f-110">두 번째 명령은 자격 증명 정보를 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-110">The second command Gets the Vault Properties.</span></span>

## <span data-ttu-id="6b19f-111">변수</span><span class="sxs-lookup"><span data-stu-id="6b19f-111">PARAMETERS</span></span>

### <span data-ttu-id="6b19f-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6b19f-112">-DefaultProfile</span></span>
<span data-ttu-id="6b19f-113">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6b19f-114">-VaultId</span><span class="sxs-lookup"><span data-stu-id="6b19f-114">-VaultId</span></span>
<span data-ttu-id="6b19f-115">복구 서비스 자격 증명 모음의 팔 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-115">ARM ID of the Recovery Services Vault.</span></span>

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

### <span data-ttu-id="6b19f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6b19f-116">CommonParameters</span></span>
<span data-ttu-id="6b19f-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="6b19f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6b19f-118">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="6b19f-118">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6b19f-119">입력</span><span class="sxs-lookup"><span data-stu-id="6b19f-119">INPUTS</span></span>

### <span data-ttu-id="6b19f-120">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="6b19f-120">System.String</span></span>

## <span data-ttu-id="6b19f-121">출력</span><span class="sxs-lookup"><span data-stu-id="6b19f-121">OUTPUTS</span></span>

### <span data-ttu-id="6b19f-122">BackupResourceVaultConfigResource/. m m/.</span><span class="sxs-lookup"><span data-stu-id="6b19f-122">Microsoft.Azure.Management.RecoveryServices.Backup.Models.BackupResourceVaultConfigResource</span></span>

## <span data-ttu-id="6b19f-123">상속자</span><span class="sxs-lookup"><span data-stu-id="6b19f-123">NOTES</span></span>

## <span data-ttu-id="6b19f-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6b19f-124">RELATED LINKS</span></span>

[<span data-ttu-id="6b19f-125">Get-AzRecoveryServicesVault</span><span class="sxs-lookup"><span data-stu-id="6b19f-125">Get-AzRecoveryServicesVault</span></span>](./Get-AzRecoveryServicesVault.md)

[<span data-ttu-id="6b19f-126">Set-AzRecoveryServicesVaultProperty</span><span class="sxs-lookup"><span data-stu-id="6b19f-126">Set-AzRecoveryServicesVaultProperty</span></span>](./Set-AzRecoveryServicesVaultProperty.md)
