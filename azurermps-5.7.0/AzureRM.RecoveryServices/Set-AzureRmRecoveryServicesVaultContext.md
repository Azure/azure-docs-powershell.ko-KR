---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 9329f35377731eeb3e59e01a673129b5505abf49
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703244"
---
# <span data-ttu-id="20fc2-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="20fc2-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="20fc2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20fc2-102">SYNOPSIS</span></span>
<span data-ttu-id="20fc2-103">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20fc2-104">구문과</span><span class="sxs-lookup"><span data-stu-id="20fc2-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="20fc2-105">설명은</span><span class="sxs-lookup"><span data-stu-id="20fc2-105">DESCRIPTION</span></span>
<span data-ttu-id="20fc2-106">**AzureRmRecoveryServicesVaultContext** Cmdlet은 Azure Site Recovery 서비스에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="20fc2-107">예제의</span><span class="sxs-lookup"><span data-stu-id="20fc2-107">EXAMPLES</span></span>

### <span data-ttu-id="20fc2-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="20fc2-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="20fc2-109">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-109">Sets vault context.</span></span>

## <span data-ttu-id="20fc2-110">변수</span><span class="sxs-lookup"><span data-stu-id="20fc2-110">PARAMETERS</span></span>

### <span data-ttu-id="20fc2-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="20fc2-111">-Vault</span></span>
<span data-ttu-id="20fc2-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="20fc2-113">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="20fc2-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="20fc2-114">-DefaultProfile</span></span>
<span data-ttu-id="20fc2-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="20fc2-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20fc2-116">CommonParameters</span></span>
<span data-ttu-id="20fc2-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20fc2-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20fc2-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20fc2-119">입력</span><span class="sxs-lookup"><span data-stu-id="20fc2-119">INPUTS</span></span>

### <span data-ttu-id="20fc2-120">ARSVault</span><span class="sxs-lookup"><span data-stu-id="20fc2-120">ARSVault</span></span>
<span data-ttu-id="20fc2-121">' Vault ' 매개 변수는 파이프라인에서 ' ARSVault ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="20fc2-121">Parameter 'Vault' accepts value of type 'ARSVault' from the pipeline</span></span>

## <span data-ttu-id="20fc2-122">출력</span><span class="sxs-lookup"><span data-stu-id="20fc2-122">OUTPUTS</span></span>

## <span data-ttu-id="20fc2-123">상속자</span><span class="sxs-lookup"><span data-stu-id="20fc2-123">NOTES</span></span>

## <span data-ttu-id="20fc2-124">관련 링크</span><span class="sxs-lookup"><span data-stu-id="20fc2-124">RELATED LINKS</span></span>

