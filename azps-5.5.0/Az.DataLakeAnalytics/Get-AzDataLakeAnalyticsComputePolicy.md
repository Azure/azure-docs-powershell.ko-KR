---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/get-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Get-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 56b1a9378914a7fa2220e948b64c357b06f6f4dc
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100208664"
---
# <span data-ttu-id="8da58-101">Get-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8da58-101">Get-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8da58-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8da58-102">SYNOPSIS</span></span>
<span data-ttu-id="8da58-103">Data Lake Analytics 계산 정책 또는 계산 정책 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-103">Gets a Data Lake Analytics compute policy or list of compute policies.</span></span>

## <span data-ttu-id="8da58-104">구문</span><span class="sxs-lookup"><span data-stu-id="8da58-104">SYNTAX</span></span>

```
Get-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8da58-105">설명</span><span class="sxs-lookup"><span data-stu-id="8da58-105">DESCRIPTION</span></span>
<span data-ttu-id="8da58-106">**Get-AzDataLakeAnalyticsComputePolicy는** 지정된 Azure Data Lake Analytics 계산 정책 또는 정책 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-106">The **Get-AzDataLakeAnalyticsComputePolicy** gets a specified Azure Data Lake Analytics compute policy or a list of policies.</span></span>

## <span data-ttu-id="8da58-107">예제</span><span class="sxs-lookup"><span data-stu-id="8da58-107">EXAMPLES</span></span>

### <span data-ttu-id="8da58-108">예제 1: 지정된 계산 정책 얻기</span><span class="sxs-lookup"><span data-stu-id="8da58-108">Example 1: Get a specified compute policy</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name myPolicy
```

<span data-ttu-id="8da58-109">이 명령은 계정 'contosoadla'에서 이름이 'myPolicy'인 지정된 계산 정책을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-109">This command gets the specified compute policy with name 'myPolicy' in account 'contosoadla'.</span></span>

### <span data-ttu-id="8da58-110">예제 2: 계정의 모든 계산 정책 목록</span><span class="sxs-lookup"><span data-stu-id="8da58-110">Example 2: Get a list of all compute policies in the account</span></span>
```
PS C:\>Get-AzDataLakeAnalyticsComputePolicy -AccountName "contosoadla"
```

<span data-ttu-id="8da58-111">이 명령은 "contosoadla" 계정의 모든 계산 정책 목록을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-111">This command gets a list of all compute policies in the account "contosoadla"</span></span>

## <span data-ttu-id="8da58-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="8da58-112">PARAMETERS</span></span>

### <span data-ttu-id="8da58-113">-Account</span><span class="sxs-lookup"><span data-stu-id="8da58-113">-Account</span></span>
<span data-ttu-id="8da58-114">계산 정책 또는 정책을 얻을 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-114">Name of the account to get the compute policy or policies from.</span></span>

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

### <span data-ttu-id="8da58-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8da58-115">-DefaultProfile</span></span>
<span data-ttu-id="8da58-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="8da58-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8da58-117">-Name</span><span class="sxs-lookup"><span data-stu-id="8da58-117">-Name</span></span>
<span data-ttu-id="8da58-118">얻을 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-118">Name of the compute policy to get.</span></span>

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

### <span data-ttu-id="8da58-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="8da58-119">-ResourceGroupName</span></span>
<span data-ttu-id="8da58-120">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-120">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="8da58-121">선택 사항이며, 제공되지 않은 경우 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-121">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="8da58-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8da58-122">CommonParameters</span></span>
<span data-ttu-id="8da58-123">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="8da58-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8da58-124">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="8da58-124">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8da58-125">입력</span><span class="sxs-lookup"><span data-stu-id="8da58-125">INPUTS</span></span>

### <span data-ttu-id="8da58-126">System.String</span><span class="sxs-lookup"><span data-stu-id="8da58-126">System.String</span></span>

## <span data-ttu-id="8da58-127">출력</span><span class="sxs-lookup"><span data-stu-id="8da58-127">OUTPUTS</span></span>

### <span data-ttu-id="8da58-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="8da58-128">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="8da58-129">참고 사항</span><span class="sxs-lookup"><span data-stu-id="8da58-129">NOTES</span></span>

## <span data-ttu-id="8da58-130">관련 링크</span><span class="sxs-lookup"><span data-stu-id="8da58-130">RELATED LINKS</span></span>
