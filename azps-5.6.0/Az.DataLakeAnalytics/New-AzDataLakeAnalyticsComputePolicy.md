---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 7cd9231134b7b78d51a9a86777c54dd99e1ffa90
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101988260"
---
# <span data-ttu-id="ec440-101">New-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ec440-101">New-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ec440-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ec440-102">SYNOPSIS</span></span>
<span data-ttu-id="ec440-103">특정 AAD 엔터티에 대한 Data Lake Analytics 계산 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="ec440-104">구문</span><span class="sxs-lookup"><span data-stu-id="ec440-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ec440-105">설명</span><span class="sxs-lookup"><span data-stu-id="ec440-105">DESCRIPTION</span></span>
<span data-ttu-id="ec440-106">**New-AzDataLakeAnalyticsComputePolicy는** Azure Data Lake Analytics 계정에서 특정 AAD 엔터티에 대해 지정된 계산 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-106">The **New-AzDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="ec440-107">예제</span><span class="sxs-lookup"><span data-stu-id="ec440-107">EXAMPLES</span></span>

### <span data-ttu-id="ec440-108">예제 1: 하나의 규칙으로 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ec440-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="ec440-109">이 명령은 "83cb7ad2-3523-4b82-b909-d478b0d8aea3"을 사용하여 사용자에 대한 계정 "contosoadla"에 "myPolicy"라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="ec440-110">예제 2: 두 규칙 집합을 모두 사용하여 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="ec440-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="ec440-111">이 명령은 5개 이상의 분석 단위 또는 우선 순위가 100보다 낮은 작업을 제출할 수 없는 "83cb7ad2-3523-4b82-b909-d478b0d8aea3"을 사용하여 사용자에 대한 계정 "contosoadla"에 "myPolicy"라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="ec440-112">매개 변수</span><span class="sxs-lookup"><span data-stu-id="ec440-112">PARAMETERS</span></span>

### <span data-ttu-id="ec440-113">-Account</span><span class="sxs-lookup"><span data-stu-id="ec440-113">-Account</span></span>
<span data-ttu-id="ec440-114">계산 정책을 추가할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="ec440-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ec440-115">-DefaultProfile</span></span>
<span data-ttu-id="ec440-116">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="ec440-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="ec440-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="ec440-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="ec440-118">이 정책에 대해 작업당 지원되는 최대 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-118">The maximum supported analytics units per job for this policy.</span></span>
<span data-ttu-id="ec440-119">이 경우 MinPriorityPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="ec440-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="ec440-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="ec440-121">이 정책에 대해 작업당 지원되는 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-121">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="ec440-122">이 경우 MaxAnalyticsUnitsPerJob 또는 두 매개 변수를 모두 지정해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="ec440-123">-Name</span><span class="sxs-lookup"><span data-stu-id="ec440-123">-Name</span></span>
<span data-ttu-id="ec440-124">만들 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-124">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="ec440-125">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="ec440-125">-ObjectId</span></span>
<span data-ttu-id="ec440-126">정책을 적용할 사용자 또는 그룹에 대한 Azure Active Directory 개체 ID입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-126">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

```yaml
Type: System.Guid
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec440-127">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="ec440-127">-ObjectType</span></span>
<span data-ttu-id="ec440-128">전달된 개체 ID에 대한 Azure Active Directory 개체 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-128">The Azure Active Directory object type for the object ID passed in.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: User, Group, ServicePrincipal

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ec440-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ec440-129">-ResourceGroupName</span></span>
<span data-ttu-id="ec440-130">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-130">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="ec440-131">선택 사항이며 제공되지 않은 경우 검색을 시도합니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-131">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="ec440-132">-확인</span><span class="sxs-lookup"><span data-stu-id="ec440-132">-Confirm</span></span>
<span data-ttu-id="ec440-133">cmdlet을 실행하기 전에 확인을 묻는 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-133">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="ec440-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ec440-134">-WhatIf</span></span>
<span data-ttu-id="ec440-135">cmdlet이 실행되는 경우 어떻게 될지 보여줍니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-135">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="ec440-136">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-136">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="ec440-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ec440-137">CommonParameters</span></span>
<span data-ttu-id="ec440-138">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="ec440-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ec440-139">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="ec440-139">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ec440-140">입력</span><span class="sxs-lookup"><span data-stu-id="ec440-140">INPUTS</span></span>

### <span data-ttu-id="ec440-141">System.String</span><span class="sxs-lookup"><span data-stu-id="ec440-141">System.String</span></span>

### <span data-ttu-id="ec440-142">System.Guid</span><span class="sxs-lookup"><span data-stu-id="ec440-142">System.Guid</span></span>

### <span data-ttu-id="ec440-143">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="ec440-143">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="ec440-144">출력</span><span class="sxs-lookup"><span data-stu-id="ec440-144">OUTPUTS</span></span>

### <span data-ttu-id="ec440-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="ec440-145">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="ec440-146">참고 사항</span><span class="sxs-lookup"><span data-stu-id="ec440-146">NOTES</span></span>

## <span data-ttu-id="ec440-147">관련 링크</span><span class="sxs-lookup"><span data-stu-id="ec440-147">RELATED LINKS</span></span>
