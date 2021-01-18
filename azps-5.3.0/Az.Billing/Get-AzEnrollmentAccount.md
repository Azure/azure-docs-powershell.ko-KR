---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/en-us/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: 19d69847742086b7969dd3dacf45538d24869ee3
ms.sourcegitcommit: 68451baa389791703e666d95469602c5652609ee
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/05/2021
ms.locfileid: "98496247"
---
# <span data-ttu-id="26190-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="26190-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="26190-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="26190-102">SYNOPSIS</span></span>
<span data-ttu-id="26190-103">등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26190-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="26190-104">구문</span><span class="sxs-lookup"><span data-stu-id="26190-104">SYNTAX</span></span>

### <span data-ttu-id="26190-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="26190-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="26190-106">Single</span><span class="sxs-lookup"><span data-stu-id="26190-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="26190-107">설명</span><span class="sxs-lookup"><span data-stu-id="26190-107">DESCRIPTION</span></span>
<span data-ttu-id="26190-108">**Get-AzEnrollmentAccount** cmdlet은 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26190-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="26190-109">예제</span><span class="sxs-lookup"><span data-stu-id="26190-109">EXAMPLES</span></span>

### <span data-ttu-id="26190-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="26190-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="26190-111">사용 가능한 모든 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26190-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="26190-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="26190-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="26190-113">지정된 개체 ID로 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="26190-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="26190-114">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="26190-114">PARAMETERS</span></span>

### <span data-ttu-id="26190-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="26190-115">-DefaultProfile</span></span>
<span data-ttu-id="26190-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="26190-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="26190-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="26190-117">-ObjectId</span></span>
<span data-ttu-id="26190-118">얻을 특정 등록 계정의 ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="26190-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="26190-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="26190-119">CommonParameters</span></span>
<span data-ttu-id="26190-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="26190-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="26190-121">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="26190-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="26190-122">입력</span><span class="sxs-lookup"><span data-stu-id="26190-122">INPUTS</span></span>

### <span data-ttu-id="26190-123">없음</span><span class="sxs-lookup"><span data-stu-id="26190-123">None</span></span>

## <span data-ttu-id="26190-124">출력</span><span class="sxs-lookup"><span data-stu-id="26190-124">OUTPUTS</span></span>

### <span data-ttu-id="26190-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="26190-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="26190-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="26190-126">NOTES</span></span>

## <span data-ttu-id="26190-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="26190-127">RELATED LINKS</span></span>
