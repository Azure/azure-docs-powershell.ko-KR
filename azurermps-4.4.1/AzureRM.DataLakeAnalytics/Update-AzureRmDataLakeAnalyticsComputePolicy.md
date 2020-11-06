---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Update-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 67cffe7f0cdaebc655eb98321166bb7805844a5a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93534980"
---
# <span data-ttu-id="d3eeb-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d3eeb-101">Update-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d3eeb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d3eeb-102">SYNOPSIS</span></span>
<span data-ttu-id="d3eeb-103">특정 AAD 엔터티에 대 한 데이터 호수 분석 계산 정책 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d3eeb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="d3eeb-104">SYNTAX</span></span>

```
Update-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="d3eeb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="d3eeb-105">DESCRIPTION</span></span>
<span data-ttu-id="d3eeb-106">**업데이트 AzureRmDataLakeAnalyticsComputePolicy** 는 Azure Data Lake Analytics 계정에서 특정 AAD 엔터티에 대해 지정 된 계산 정책 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-106">The **Update-AzureRmDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="d3eeb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="d3eeb-107">EXAMPLES</span></span>

### <span data-ttu-id="d3eeb-108">예제 1: 계산 정책에서 하나의 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="d3eeb-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="d3eeb-109">이 명령은 사용자가 5 개 이상의 병렬 처리를 사용 하 여 작업을 제출할 수 없도록 "contosoadla" 계정의 "myPolicy" 라는 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="d3eeb-110">예제 2: 두 규칙 업데이트를 모두 사용 하 여 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="d3eeb-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="d3eeb-111">이 명령은 사용자가 5 개 이상의 병렬 처리를 사용 하거나 우선 순위가 100 보다 낮은 작업을 제출할 수 없도록 "contosoadla" 계정에 "myPolicy" 이라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="d3eeb-112">변수</span><span class="sxs-lookup"><span data-stu-id="d3eeb-112">PARAMETERS</span></span>

### <span data-ttu-id="d3eeb-113">-계정</span><span class="sxs-lookup"><span data-stu-id="d3eeb-113">-Account</span></span>
<span data-ttu-id="d3eeb-114">계산 정책을 업데이트할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="d3eeb-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="d3eeb-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="d3eeb-116">이 정책에 대해 지원 되는 작업당 병렬 처리의 최대 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-116">The maximum supported degree of parallelism per job for this policy.</span></span> <span data-ttu-id="d3eeb-117">This, MinPriorityPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d3eeb-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="d3eeb-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="d3eeb-119">이 정책에 대해 지원 되는 작업당 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-119">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="d3eeb-120">This, MaxDegreeOfParallelismPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="d3eeb-121">-이름</span><span class="sxs-lookup"><span data-stu-id="d3eeb-121">-Name</span></span>
<span data-ttu-id="d3eeb-122">업데이트할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-122">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="d3eeb-123">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d3eeb-123">-ResourceGroupName</span></span>
<span data-ttu-id="d3eeb-124">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-124">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="d3eeb-125">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-125">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="d3eeb-126">-확인</span><span class="sxs-lookup"><span data-stu-id="d3eeb-126">-Confirm</span></span>
<span data-ttu-id="d3eeb-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d3eeb-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d3eeb-128">-WhatIf</span></span>
<span data-ttu-id="d3eeb-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-129">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="d3eeb-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d3eeb-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d3eeb-131">-DefaultProfile</span></span>
<span data-ttu-id="d3eeb-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="d3eeb-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d3eeb-133">CommonParameters</span></span>
<span data-ttu-id="d3eeb-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d3eeb-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d3eeb-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d3eeb-136">입력</span><span class="sxs-lookup"><span data-stu-id="d3eeb-136">INPUTS</span></span>

### <span data-ttu-id="d3eeb-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="d3eeb-137">System.String</span></span>
<span data-ttu-id="d3eeb-138">시스템. i i.</span><span class="sxs-lookup"><span data-stu-id="d3eeb-138">System.Int32</span></span>

## <span data-ttu-id="d3eeb-139">출력</span><span class="sxs-lookup"><span data-stu-id="d3eeb-139">OUTPUTS</span></span>

### <span data-ttu-id="d3eeb-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="d3eeb-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="d3eeb-141">상속자</span><span class="sxs-lookup"><span data-stu-id="d3eeb-141">NOTES</span></span>

## <span data-ttu-id="d3eeb-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="d3eeb-142">RELATED LINKS</span></span>

