---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: c27319e368223b00ba17caf9d408e6a1010c766d
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101994457"
---
# <span data-ttu-id="55898-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="55898-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="55898-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="55898-102">SYNOPSIS</span></span>
<span data-ttu-id="55898-103">특정 AAD 엔터티에 대한 Data Lake Analytics 계산 정책 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="55898-104">구문</span><span class="sxs-lookup"><span data-stu-id="55898-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="55898-105">설명</span><span class="sxs-lookup"><span data-stu-id="55898-105">DESCRIPTION</span></span>
<span data-ttu-id="55898-106">**Update-AzDataLakeAnalyticsComputePolicy는** Azure Data Lake Analytics 계정의 특정 AAD 엔터티에 대해 지정된 계산 정책 규칙을 업데이트합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="55898-107">예제</span><span class="sxs-lookup"><span data-stu-id="55898-107">EXAMPLES</span></span>

### <span data-ttu-id="55898-108">예제 1: 계산 정책에서 하나의 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="55898-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="55898-109">이 명령은 "contosoadla" 계정에서 "myPolicy"라는 정책을 업데이트하여 사용자가 5개 이상의 분석 단위를 사용하여 작업을 제출할 수 없습니다.</span><span class="sxs-lookup"><span data-stu-id="55898-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="55898-110">예제 2: 두 규칙 업데이트가 모두 있는 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="55898-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="55898-111">이 명령은 사용자가 5개 이상의 분석 단위 또는 우선 순위가 100보다 낮은 작업을 제출할 수 있도록 "contosoadla"에 "myPolicy"라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="55898-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="55898-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="55898-112">PARAMETERS</span></span>

### <span data-ttu-id="55898-113">-Account</span><span class="sxs-lookup"><span data-stu-id="55898-113">-Account</span></span>
<span data-ttu-id="55898-114">계산 정책을 업데이트할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55898-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="55898-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="55898-115">-DefaultProfile</span></span>
<span data-ttu-id="55898-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="55898-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="55898-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="55898-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="55898-118">이 정책에 대해 작업당 지원되는 최대 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="55898-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="55898-119">이 경우 MinPriorityPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="55898-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="55898-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="55898-121">이 정책에 대해 작업당 지원되는 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="55898-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="55898-122">이 경우 MaxAnalyticsUnitsPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="55898-123">-Name</span><span class="sxs-lookup"><span data-stu-id="55898-123">-Name</span></span>
<span data-ttu-id="55898-124">업데이트할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55898-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="55898-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="55898-125">-ResourceGroupName</span></span>
<span data-ttu-id="55898-126">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="55898-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="55898-127">선택 사항이며 제공되지 않은 경우 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="55898-128">-확인</span><span class="sxs-lookup"><span data-stu-id="55898-128">-Confirm</span></span>
<span data-ttu-id="55898-129">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="55898-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="55898-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="55898-130">-WhatIf</span></span>
<span data-ttu-id="55898-131">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="55898-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="55898-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="55898-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="55898-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="55898-133">CommonParameters</span></span>
<span data-ttu-id="55898-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="55898-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="55898-135">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="55898-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="55898-136">입력</span><span class="sxs-lookup"><span data-stu-id="55898-136">INPUTS</span></span>

### <span data-ttu-id="55898-137">System.String</span><span class="sxs-lookup"><span data-stu-id="55898-137">System.String</span></span>

### <span data-ttu-id="55898-138">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="55898-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="55898-139">출력</span><span class="sxs-lookup"><span data-stu-id="55898-139">OUTPUTS</span></span>

### <span data-ttu-id="55898-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="55898-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="55898-141">참고 사항</span><span class="sxs-lookup"><span data-stu-id="55898-141">NOTES</span></span>

## <span data-ttu-id="55898-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="55898-142">RELATED LINKS</span></span>
