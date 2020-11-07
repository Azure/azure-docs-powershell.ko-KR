---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d5d43a0aebcc553a230655d52399081548aae209
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703909"
---
# <span data-ttu-id="f247e-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="f247e-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="f247e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f247e-102">SYNOPSIS</span></span>
<span data-ttu-id="f247e-103">등록 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="f247e-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f247e-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f247e-104">SYNTAX</span></span>

### <span data-ttu-id="f247e-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="f247e-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f247e-106">단일</span><span class="sxs-lookup"><span data-stu-id="f247e-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f247e-107">설명은</span><span class="sxs-lookup"><span data-stu-id="f247e-107">DESCRIPTION</span></span>
<span data-ttu-id="f247e-108">**Get-AzureRmEnrollmentAccount** cmdlet은 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f247e-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="f247e-109">예제의</span><span class="sxs-lookup"><span data-stu-id="f247e-109">EXAMPLES</span></span>

### <span data-ttu-id="f247e-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="f247e-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="f247e-111">사용 가능한 모든 등록 계정을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="f247e-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="f247e-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="f247e-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="f247e-113">지정 된 개체 id를 사용 하 여 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="f247e-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="f247e-114">변수</span><span class="sxs-lookup"><span data-stu-id="f247e-114">PARAMETERS</span></span>

### <span data-ttu-id="f247e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f247e-115">-DefaultProfile</span></span>
<span data-ttu-id="f247e-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f247e-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f247e-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="f247e-117">-ObjectId</span></span>
<span data-ttu-id="f247e-118">가져올 특정 등록 계정의 ObjectId.</span><span class="sxs-lookup"><span data-stu-id="f247e-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f247e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f247e-119">CommonParameters</span></span>
<span data-ttu-id="f247e-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f247e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f247e-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f247e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f247e-122">입력</span><span class="sxs-lookup"><span data-stu-id="f247e-122">INPUTS</span></span>

### <span data-ttu-id="f247e-123">않아야</span><span class="sxs-lookup"><span data-stu-id="f247e-123">None</span></span>

## <span data-ttu-id="f247e-124">출력</span><span class="sxs-lookup"><span data-stu-id="f247e-124">OUTPUTS</span></span>

### <span data-ttu-id="f247e-125">PSBillingPeriod를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="f247e-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="f247e-126">상속자</span><span class="sxs-lookup"><span data-stu-id="f247e-126">NOTES</span></span>

## <span data-ttu-id="f247e-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f247e-127">RELATED LINKS</span></span>
