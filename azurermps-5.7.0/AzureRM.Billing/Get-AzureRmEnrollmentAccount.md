---
external help file: Microsoft.Azure.Commands.Billing.dll-Help.xml
Module Name: AzureRM.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.billing/get-azurermenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Billing/Commands.Billing/help/Get-AzureRmEnrollmentAccount.md
ms.openlocfilehash: d0efe107f15cf3e2bcb0d25c283fee306eeb404b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527048"
---
# <span data-ttu-id="fb4b7-101">Get-AzureRmEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="fb4b7-101">Get-AzureRmEnrollmentAccount</span></span>

## <span data-ttu-id="fb4b7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fb4b7-102">SYNOPSIS</span></span>
<span data-ttu-id="fb4b7-103">등록 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="fb4b7-103">Get enrollment accounts.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fb4b7-104">구문과</span><span class="sxs-lookup"><span data-stu-id="fb4b7-104">SYNTAX</span></span>

### <span data-ttu-id="fb4b7-105">목록 (기본값)</span><span class="sxs-lookup"><span data-stu-id="fb4b7-105">List (Default)</span></span>
```
Get-AzureRmEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="fb4b7-106">단일</span><span class="sxs-lookup"><span data-stu-id="fb4b7-106">Single</span></span>
```
Get-AzureRmEnrollmentAccount -ObjectId <System.String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fb4b7-107">설명은</span><span class="sxs-lookup"><span data-stu-id="fb4b7-107">DESCRIPTION</span></span>
<span data-ttu-id="fb4b7-108">**Get-AzureRmEnrollmentAccount** cmdlet은 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-108">The **Get-AzureRmEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="fb4b7-109">예제의</span><span class="sxs-lookup"><span data-stu-id="fb4b7-109">EXAMPLES</span></span>

### <span data-ttu-id="fb4b7-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="fb4b7-110">Example 1</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="fb4b7-111">사용 가능한 모든 등록 계정을 확보 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="fb4b7-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="fb4b7-112">Example 2</span></span>
```
PS C:\> Get-AzureRmEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="fb4b7-113">지정 된 개체 id를 사용 하 여 등록 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="fb4b7-114">변수</span><span class="sxs-lookup"><span data-stu-id="fb4b7-114">PARAMETERS</span></span>

### <span data-ttu-id="fb4b7-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fb4b7-115">-DefaultProfile</span></span>
<span data-ttu-id="fb4b7-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fb4b7-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fb4b7-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="fb4b7-117">-ObjectId</span></span>
<span data-ttu-id="fb4b7-118">가져올 특정 등록 계정의 ObjectId.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-118">ObjectId of a specific enrollment account to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Single
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fb4b7-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fb4b7-119">CommonParameters</span></span>
<span data-ttu-id="fb4b7-120">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fb4b7-121">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fb4b7-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fb4b7-122">입력</span><span class="sxs-lookup"><span data-stu-id="fb4b7-122">INPUTS</span></span>

### <span data-ttu-id="fb4b7-123">않아야</span><span class="sxs-lookup"><span data-stu-id="fb4b7-123">None</span></span>

## <span data-ttu-id="fb4b7-124">출력</span><span class="sxs-lookup"><span data-stu-id="fb4b7-124">OUTPUTS</span></span>

### <span data-ttu-id="fb4b7-125">System.webserver. List ' 1 [[Microsoft PSEnrollmentAccount, Microsoft Azure. 0.14.0.0, Version =, Culture = 중립, PublicKeyToken = null]])</span><span class="sxs-lookup"><span data-stu-id="fb4b7-125">System.Collections.Generic.List\`1[[Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount, Microsoft.Azure.Commands.Billing, Version=0.14.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>
<span data-ttu-id="fb4b7-126">PSEnrollmentAccount를 통해 서.</span><span class="sxs-lookup"><span data-stu-id="fb4b7-126">Microsoft.Azure.Commands.Billing.Models.PSEnrollmentAccount</span></span>

## <span data-ttu-id="fb4b7-127">상속자</span><span class="sxs-lookup"><span data-stu-id="fb4b7-127">NOTES</span></span>

## <span data-ttu-id="fb4b7-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fb4b7-128">RELATED LINKS</span></span>

