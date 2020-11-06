---
external help file: Microsoft.Azure.Commands.RecoveryServices.ARM.dll-Help.xml
Module Name: AzureRM.RecoveryServices
ms.assetid: 368DD95E-EA25-4FC4-8171-CB7348FE480C
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.recoveryservices/set-azurermrecoveryservicesvaultcontext
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/RecoveryServices/Commands.RecoveryServices/help/Set-AzureRmRecoveryServicesVaultContext.md
ms.openlocfilehash: 0989bdcc14a9f7e3cbd65af11aea843cdd0ec6e2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93526099"
---
# <span data-ttu-id="9b41f-101">Set-AzureRmRecoveryServicesVaultContext</span><span class="sxs-lookup"><span data-stu-id="9b41f-101">Set-AzureRmRecoveryServicesVaultContext</span></span>

## <span data-ttu-id="9b41f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9b41f-102">SYNOPSIS</span></span>
<span data-ttu-id="9b41f-103">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-103">Sets vault context.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9b41f-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9b41f-104">SYNTAX</span></span>

```
Set-AzureRmRecoveryServicesVaultContext -Vault <ARSVault> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9b41f-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9b41f-105">DESCRIPTION</span></span>
<span data-ttu-id="9b41f-106">**AzureRmRecoveryServicesVaultContext** Cmdlet은 Azure Site Recovery 서비스에 대 한 자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-106">The **Set-AzureRmRecoveryServicesVaultContext** cmdlet sets the vault context for Azure Site Recovery services.</span></span>

## <span data-ttu-id="9b41f-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9b41f-107">EXAMPLES</span></span>

### <span data-ttu-id="9b41f-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="9b41f-108">Example 1</span></span>
```
PS C:\> Set-AzureRmRecoveryServicesVaultContext -Vault $vault
```

<span data-ttu-id="9b41f-109">자격 증명 모음 컨텍스트를 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-109">Sets vault context.</span></span>

## <span data-ttu-id="9b41f-110">변수</span><span class="sxs-lookup"><span data-stu-id="9b41f-110">PARAMETERS</span></span>

### <span data-ttu-id="9b41f-111">-저장실</span><span class="sxs-lookup"><span data-stu-id="9b41f-111">-Vault</span></span>
<span data-ttu-id="9b41f-112">자격 증명 모음의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-112">Specifies the name of the vault.</span></span>
<span data-ttu-id="9b41f-113">자격 증명 모음이 **AzureRmRecoveryServicesVault** 개체 여야 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-113">The vault must be an **AzureRmRecoveryServicesVault** object.</span></span>

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

### <span data-ttu-id="9b41f-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9b41f-114">-DefaultProfile</span></span>
<span data-ttu-id="9b41f-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9b41f-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9b41f-116">CommonParameters</span></span>
<span data-ttu-id="9b41f-117">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9b41f-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9b41f-118">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9b41f-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9b41f-119">입력</span><span class="sxs-lookup"><span data-stu-id="9b41f-119">INPUTS</span></span>

### <span data-ttu-id="9b41f-120">ARSVault를 통한 명령</span><span class="sxs-lookup"><span data-stu-id="9b41f-120">Microsoft.Azure.Commands.RecoveryServices.ARSVault</span></span>
<span data-ttu-id="9b41f-121">매개 변수: 자격 증명 모음 (ByValue)</span><span class="sxs-lookup"><span data-stu-id="9b41f-121">Parameters: Vault (ByValue)</span></span>

## <span data-ttu-id="9b41f-122">출력</span><span class="sxs-lookup"><span data-stu-id="9b41f-122">OUTPUTS</span></span>

### <span data-ttu-id="9b41f-123">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="9b41f-123">System.Void</span></span>

## <span data-ttu-id="9b41f-124">상속자</span><span class="sxs-lookup"><span data-stu-id="9b41f-124">NOTES</span></span>

## <span data-ttu-id="9b41f-125">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9b41f-125">RELATED LINKS</span></span>
