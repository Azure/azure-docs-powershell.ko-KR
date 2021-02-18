---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180916"
---
# <span data-ttu-id="fe4da-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe4da-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe4da-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fe4da-102">SYNOPSIS</span></span>
<span data-ttu-id="fe4da-103">특정 AAD 엔터티에 대한 Data Lake Analytics 계산 정책 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="fe4da-104">구문</span><span class="sxs-lookup"><span data-stu-id="fe4da-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fe4da-105">설명</span><span class="sxs-lookup"><span data-stu-id="fe4da-105">DESCRIPTION</span></span>
<span data-ttu-id="fe4da-106">**Update-AzDataLakeAnalyticsComputePolicy는** Azure Data Lake Analytics 계정의 특정 AAD 엔터티에 대해 지정된 계산 정책 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="fe4da-107">예제</span><span class="sxs-lookup"><span data-stu-id="fe4da-107">EXAMPLES</span></span>

### <span data-ttu-id="fe4da-108">예제 1: 계산 정책에서 하나의 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="fe4da-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="fe4da-109">이 명령은 사용자가 5개 이상의 분석 단위가 있는 작업을 제출할 수 있도록 "contosoadla" 계정에서 "myPolicy"라는 정책을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="fe4da-110">예제 2: 두 규칙 업데이트가 모두 있는 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="fe4da-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="fe4da-111">이 명령은 사용자가 5개 이상의 분석 단위 또는 우선 순위가 100보다 낮은 작업을 제출할 수 있도록 "contosoadla" 계정에 "myPolicy"라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="fe4da-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="fe4da-112">PARAMETERS</span></span>

### <span data-ttu-id="fe4da-113">-Account</span><span class="sxs-lookup"><span data-stu-id="fe4da-113">-Account</span></span>
<span data-ttu-id="fe4da-114">계산 정책을 업데이트할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="fe4da-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fe4da-115">-DefaultProfile</span></span>
<span data-ttu-id="fe4da-116">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="fe4da-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fe4da-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="fe4da-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="fe4da-118">이 정책에 대해 작업당 지원되는 최대 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="fe4da-119">이 매개 변수, MinPriorityPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelismPerJob

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4da-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="fe4da-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="fe4da-121">이 정책에 대해 작업당 지원되는 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="fe4da-122">MaxAnalyticsUnitsPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4da-123">-Name</span><span class="sxs-lookup"><span data-stu-id="fe4da-123">-Name</span></span>
<span data-ttu-id="fe4da-124">업데이트할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-124">Name of the compute policy to update.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ComputePolicyName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="fe4da-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fe4da-125">-ResourceGroupName</span></span>
<span data-ttu-id="fe4da-126">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="fe4da-127">선택 사항이며, 제공되지 않은 경우 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="fe4da-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="fe4da-128">-Confirm</span></span>
<span data-ttu-id="fe4da-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4da-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fe4da-130">-WhatIf</span></span>
<span data-ttu-id="fe4da-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="fe4da-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="fe4da-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="fe4da-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fe4da-133">CommonParameters</span></span>
<span data-ttu-id="fe4da-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="fe4da-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fe4da-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="fe4da-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fe4da-136">입력</span><span class="sxs-lookup"><span data-stu-id="fe4da-136">INPUTS</span></span>

### <span data-ttu-id="fe4da-137">System.String</span><span class="sxs-lookup"><span data-stu-id="fe4da-137">System.String</span></span>

### <span data-ttu-id="fe4da-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="fe4da-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="fe4da-139">출력</span><span class="sxs-lookup"><span data-stu-id="fe4da-139">OUTPUTS</span></span>

### <span data-ttu-id="fe4da-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="fe4da-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="fe4da-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="fe4da-141">NOTES</span></span>

## <span data-ttu-id="fe4da-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="fe4da-142">RELATED LINKS</span></span>
