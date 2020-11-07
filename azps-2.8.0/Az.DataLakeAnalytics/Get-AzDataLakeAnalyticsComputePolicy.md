---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 776249a7a474e3918ed29003f631c984111ca25c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93696923"
---
# <span data-ttu-id="878e3-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="878e3-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="878e3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="878e3-102">SYNOPSIS</span></span>
<span data-ttu-id="878e3-103">데이터 호수 분석 계산 정책 또는 계산 정책 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="878e3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="878e3-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="878e3-105">설명은</span><span class="sxs-lookup"><span data-stu-id="878e3-105">DESCRIPTION</span></span>
<span data-ttu-id="878e3-106">**AzDataLakeAnalyticsComputePolicy** 에서 지정 된 Azure Data Lake 분석 계산 정책 또는 정책 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="878e3-107">예제의</span><span class="sxs-lookup"><span data-stu-id="878e3-107">EXAMPLES</span></span>

### <span data-ttu-id="878e3-108">예제 1: 지정 된 계산 정책 가져오기</span><span class="sxs-lookup"><span data-stu-id="878e3-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="878e3-109">이 명령은 ' contosoadla ' 계정에서 이름이 ' myPolicy ' 인 지정 된 계산 정책을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="878e3-110">예제 2: 계정에 있는 모든 계산 정책의 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="878e3-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="878e3-111">이 명령은 "contosoadla" 계정의 모든 계산 정책 목록을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="878e3-112">변수</span><span class="sxs-lookup"><span data-stu-id="878e3-112">PARAMETERS</span></span>

### <span data-ttu-id="878e3-113">-계정</span><span class="sxs-lookup"><span data-stu-id="878e3-113">-Account</span></span>
<span data-ttu-id="878e3-114">계산 정책이 나 정책을 가져올 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-114">Name of the account to get the compute policy or policies from.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AccountName

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878e3-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="878e3-115">-DefaultProfile</span></span>
<span data-ttu-id="878e3-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="878e3-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="878e3-117">-이름</span><span class="sxs-lookup"><span data-stu-id="878e3-117">-Name</span></span>
<span data-ttu-id="878e3-118">가져올 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-118">Name of the compute policy to get.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878e3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="878e3-119">-ResourceGroupName</span></span>
<span data-ttu-id="878e3-120">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="878e3-121">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-121">Optional and will attempt to discover if not provided.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="878e3-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="878e3-122">CommonParameters</span></span>
<span data-ttu-id="878e3-123">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="878e3-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="878e3-124">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="878e3-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="878e3-125">입력</span><span class="sxs-lookup"><span data-stu-id="878e3-125">INPUTS</span></span>

### <span data-ttu-id="878e3-126">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="878e3-126">System.String</span></span>

## <span data-ttu-id="878e3-127">출력</span><span class="sxs-lookup"><span data-stu-id="878e3-127">OUTPUTS</span></span>

### <span data-ttu-id="878e3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="878e3-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="878e3-129">상속자</span><span class="sxs-lookup"><span data-stu-id="878e3-129">NOTES</span></span>

## <span data-ttu-id="878e3-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="878e3-130">RELATED LINKS</span></span>
