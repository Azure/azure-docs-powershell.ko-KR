---
external help file: ''
Module Name: Azs.Subscriptions
online version: https://docs.microsoft.com/powershell/module/azs.subscriptions/get-azsoffer
schema: 2.0.0
ms.openlocfilehash: 7b2fcb224486915e78bdd90a84941ac0207a45c3
ms.sourcegitcommit: 09eb4dbfcad6fce303b793dafe9bebdef589db03
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/08/2020
ms.locfileid: "94047028"
---
# <span data-ttu-id="79d9a-101">Get-AzsOffer</span><span class="sxs-lookup"><span data-stu-id="79d9a-101">Get-AzsOffer</span></span>

## <span data-ttu-id="79d9a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79d9a-102">SYNOPSIS</span></span>
<span data-ttu-id="79d9a-103">루트 공급자에 대 한 공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-103">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="79d9a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="79d9a-104">SYNTAX</span></span>

```
Get-AzsOffer [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="79d9a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="79d9a-105">DESCRIPTION</span></span>
<span data-ttu-id="79d9a-106">루트 공급자에 대 한 공개 서비스 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-106">Get the list of public offers for the root provider.</span></span>

## <span data-ttu-id="79d9a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="79d9a-107">EXAMPLES</span></span>

### <span data-ttu-id="79d9a-108">예제 1</span><span class="sxs-lookup"><span data-stu-id="79d9a-108">Example 1</span></span>
```powershell
PS C:\> Get-AzsOffer | fl *

Description : 
DisplayName : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Id          : /delegatedProviders/default/offers/TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6
Name        : TestOffer-fef68214-ba47-469c-89a7-07faf7947ad6

Description : 
DisplayName : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Id          : /delegatedProviders/default/offers/TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
Name        : TestOffer-8322dc27-47a0-4446-89a0-eb5a0ec3b12b
```

<span data-ttu-id="79d9a-109">공개 행사 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="79d9a-109">Get the list of public offers</span></span>

## <span data-ttu-id="79d9a-110">변수</span><span class="sxs-lookup"><span data-stu-id="79d9a-110">PARAMETERS</span></span>

### <span data-ttu-id="79d9a-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79d9a-111">-DefaultProfile</span></span>
<span data-ttu-id="79d9a-112">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False

```

### <span data-ttu-id="79d9a-113">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79d9a-113">CommonParameters</span></span>
<span data-ttu-id="79d9a-114">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="79d9a-114">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79d9a-115">자세한 내용은 [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)을 참조 하세요.</span><span class="sxs-lookup"><span data-stu-id="79d9a-115">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79d9a-116">입력</span><span class="sxs-lookup"><span data-stu-id="79d9a-116">INPUTS</span></span>

## <span data-ttu-id="79d9a-117">출력</span><span class="sxs-lookup"><span data-stu-id="79d9a-117">OUTPUTS</span></span>

### <span data-ttu-id="79d9a-118">Api20151101를 통해 제공 되는 PowerShell.</span><span class="sxs-lookup"><span data-stu-id="79d9a-118">Microsoft.Azure.PowerShell.Cmdlets.Subscription.Models.Api20151101.IOffer</span></span>



## <span data-ttu-id="79d9a-119">상속자</span><span class="sxs-lookup"><span data-stu-id="79d9a-119">NOTES</span></span>

## <span data-ttu-id="79d9a-120">관련 링크</span><span class="sxs-lookup"><span data-stu-id="79d9a-120">RELATED LINKS</span></span>

