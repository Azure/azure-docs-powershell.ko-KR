---
external help file: Microsoft.Azure.PowerShell.Cmdlets.RecoveryServices.dll-Help.xml
Module Name: Az.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/az.recoveryservices/set-azrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/RecoveryServices/RecoveryServices/help/Set-AzRecoveryServicesVaultContext.md
ms.openlocfilehash: 4d8839d36bf337e3a710fe31384bb022582a371d
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93699604"
---
# <span data-ttu-id="1241c-101">Set-AzRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="1241c-101">Set-AzRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="1241c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1241c-102">SYNOPSIS</span></span>
<span data-ttu-id="1241c-103">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-103">Sets vault context.</span></span>

## <span data-ttu-id="1241c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1241c-104">SYNTAX</span></span>

```
Set-AzRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="1241c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1241c-105">DESCRIPTION</span></span>
<span data-ttu-id="1241c-106">**AzRecoveryServicesVaultContext** Cmdlet은 Azure Site Recovery 서비스에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-106">The **Set-AzRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="1241c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1241c-107">EXAMPLES</span></span>

### <span data-ttu-id="1241c-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="1241c-108">Example 1</span></span>
```
PS C:\> Set-AzRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="1241c-109">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-109">Sets vault context.</span></span>

## <span data-ttu-id="1241c-110">변수</span><span class="sxs-lookup"><span data-stu-id="1241c-110">PARAMETERS</span></span>

### <span data-ttu-id="1241c-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1241c-111">-DefaultProfile</span></span>
<span data-ttu-id="1241c-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="1241c-113">-저장실</span><span class="sxs-lookup"><span data-stu-id="1241c-113">-Vault</span></span>
<span data-ttu-id="1241c-114">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-114">Specifies the name of the vault.</span></span>
<span data-ttu-id="1241c-115">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-115">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="1241c-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1241c-116">CommonParameters</span></span>
<span data-ttu-id="1241c-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1241c-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1241c-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1241c-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1241c-119">입력</span><span class="sxs-lookup"><span data-stu-id="1241c-119">INPUTS</span></span>

### <span data-ttu-id="1241c-120">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="1241c-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>

## <span data-ttu-id="1241c-121">출력</span><span class="sxs-lookup"><span data-stu-id="1241c-121">OUTPUTS</span></span>

### <span data-ttu-id="1241c-122">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="1241c-122">System.Void</span></span>

## <span data-ttu-id="1241c-123">상속자</span><span class="sxs-lookup"><span data-stu-id="1241c-123">NOTES</span></span>

## <span data-ttu-id="1241c-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1241c-124">RELATED LINKS</span></span>