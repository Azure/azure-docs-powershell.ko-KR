---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Billing.dll-Help.xml
Module Name: Az.Billing
online version: https://docs.microsoft.com/powershell/module/az.billing/get-azenrollmentaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Billing/Billing/help/Get-AzEnrollmentAccount.md
ms.openlocfilehash: d05499ded326787b9930574872dd0681f773d1c5
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101992931"
---
# <span data-ttu-id="15d72-101">Get-AzEnrollmentAccount</span><span class="sxs-lookup"><span data-stu-id="15d72-101">Get-AzEnrollmentAccount</span></span>

## <span data-ttu-id="15d72-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15d72-102">SYNOPSIS</span></span>
<span data-ttu-id="15d72-103">등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-103">Get enrollment accounts.</span></span>

## <span data-ttu-id="15d72-104">구문</span><span class="sxs-lookup"><span data-stu-id="15d72-104">SYNTAX</span></span>

### <span data-ttu-id="15d72-105">목록(기본값)</span><span class="sxs-lookup"><span data-stu-id="15d72-105">List (Default)</span></span>
```
Get-AzEnrollmentAccount [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="15d72-106">Single</span><span class="sxs-lookup"><span data-stu-id="15d72-106">Single</span></span>
```
Get-AzEnrollmentAccount [-ObjectId] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15d72-107">설명</span><span class="sxs-lookup"><span data-stu-id="15d72-107">DESCRIPTION</span></span>
<span data-ttu-id="15d72-108">**Get-AzEnrollmentAccount** cmdlet은 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-108">The **Get-AzEnrollmentAccount** cmdlet gets enrollment accounts.</span></span>

## <span data-ttu-id="15d72-109">예제</span><span class="sxs-lookup"><span data-stu-id="15d72-109">EXAMPLES</span></span>

### <span data-ttu-id="15d72-110">예제 1</span><span class="sxs-lookup"><span data-stu-id="15d72-110">Example 1</span></span>
```
PS C:\> Get-AzEnrollmentAccount

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
7ff524ac-a0de-4402-876f-934ccee3b601 carol@contoso.onmicrosoft.com
```

<span data-ttu-id="15d72-111">사용 가능한 모든 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-111">Get all available enrollment accounts.</span></span>

### <span data-ttu-id="15d72-112">예제 2</span><span class="sxs-lookup"><span data-stu-id="15d72-112">Example 2</span></span>
```
PS C:\> Get-AzEnrollmentAccount -ObjectId dbd8453d-071f-4fb4-8e01-c99f5b067649

ObjectId                             PrincipalName
--------                             -------------
dbd8453d-071f-4fb4-8e01-c99f5b067649 jason@contoso.onmicrosoft.com
```

<span data-ttu-id="15d72-113">지정된 개체 ID를 통해 등록 계정을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-113">Get the enrollment account with the specified object id.</span></span>

## <span data-ttu-id="15d72-114">매개 변수</span><span class="sxs-lookup"><span data-stu-id="15d72-114">PARAMETERS</span></span>

### <span data-ttu-id="15d72-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15d72-115">-DefaultProfile</span></span>
<span data-ttu-id="15d72-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="15d72-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="15d72-117">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="15d72-117">-ObjectId</span></span>
<span data-ttu-id="15d72-118">얻을 특정 등록 계정의 ObjectId입니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-118">ObjectId of a specific enrollment account to get.</span></span>

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

### <span data-ttu-id="15d72-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15d72-119">CommonParameters</span></span>
<span data-ttu-id="15d72-120">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="15d72-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15d72-121">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="15d72-121">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15d72-122">입력</span><span class="sxs-lookup"><span data-stu-id="15d72-122">INPUTS</span></span>

### <span data-ttu-id="15d72-123">없음</span><span class="sxs-lookup"><span data-stu-id="15d72-123">None</span></span>

## <span data-ttu-id="15d72-124">출력</span><span class="sxs-lookup"><span data-stu-id="15d72-124">OUTPUTS</span></span>

### <span data-ttu-id="15d72-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span><span class="sxs-lookup"><span data-stu-id="15d72-125">Microsoft.Azure.Commands.Billing.Models.PSBillingPeriod</span></span>

## <span data-ttu-id="15d72-126">참고 사항</span><span class="sxs-lookup"><span data-stu-id="15d72-126">NOTES</span></span>

## <span data-ttu-id="15d72-127">관련 링크</span><span class="sxs-lookup"><span data-stu-id="15d72-127">RELATED LINKS</span></span>
