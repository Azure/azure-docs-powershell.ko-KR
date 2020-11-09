---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/update-azdatalakeanalyticscomputepolicy
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Update-AzDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 5dd36c9dbd263dc2e5c72cc6d57f95e29c456c41
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305714"
---
# <span data-ttu-id="f9187-101">Update-AzDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f9187-101">Update-AzDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f9187-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9187-102">SYNOPSIS</span></span>
<span data-ttu-id="f9187-103">특정 AAD 엔터티에 대 한 데이터 호수 분석 계산 정책 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-103">Updates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

## <span data-ttu-id="f9187-104">구문과</span><span class="sxs-lookup"><span data-stu-id="f9187-104">SYNTAX</span></span>

```
Update-AzDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-MaxAnalyticsUnitsPerJob <Int32>] [-MinPriorityPerJob <Int32>] [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f9187-105">설명은</span><span class="sxs-lookup"><span data-stu-id="f9187-105">DESCRIPTION</span></span>
<span data-ttu-id="f9187-106">**업데이트 AzDataLakeAnalyticsComputePolicy** 는 Azure Data Lake Analytics 계정에서 특정 AAD 엔터티에 대해 지정 된 계산 정책 규칙을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-106">The **Update-AzDataLakeAnalyticsComputePolicy** updates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="f9187-107">예제의</span><span class="sxs-lookup"><span data-stu-id="f9187-107">EXAMPLES</span></span>

### <span data-ttu-id="f9187-108">예제 1: 계산 정책에서 하나의 규칙 업데이트</span><span class="sxs-lookup"><span data-stu-id="f9187-108">Example 1: update one rule in a compute policy</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5
```

<span data-ttu-id="f9187-109">이 명령은 사용자가 5 개 이상의 분석 단위를 사용 하 여 작업을 제출할 수 없도록 "contosoadla" 계정의 "myPolicy" 라는 정책을 업데이트 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-109">This command updates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units.</span></span>

### <span data-ttu-id="f9187-110">예제 2: 두 규칙 업데이트를 모두 사용 하 여 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="f9187-110">Example 2: Create a compute policy with both rules update</span></span>
```
PS C:\>Update-AzDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -MaxAnalyticsUnitsPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="f9187-111">이 명령은 사용자가 5 개 이상의 분석 단위를 사용 하거나 우선 순위가 100 보다 낮은 작업을 제출할 수 없도록 "contosoadla" 계정에 "myPolicy" 이라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-111">This command creates a policy called "myPolicy" in account "contosoadla" to ensure the user cannot submit any job with more than 5 analytics units or with a priority lower than 100</span></span>

## <span data-ttu-id="f9187-112">변수</span><span class="sxs-lookup"><span data-stu-id="f9187-112">PARAMETERS</span></span>

### <span data-ttu-id="f9187-113">-계정</span><span class="sxs-lookup"><span data-stu-id="f9187-113">-Account</span></span>
<span data-ttu-id="f9187-114">계산 정책을 업데이트할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-114">Name of the account to update the compute policy in.</span></span>

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

### <span data-ttu-id="f9187-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9187-115">-DefaultProfile</span></span>
<span data-ttu-id="f9187-116">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="f9187-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f9187-117">-MaxAnalyticsUnitsPerJob</span><span class="sxs-lookup"><span data-stu-id="f9187-117">-MaxAnalyticsUnitsPerJob</span></span>
<span data-ttu-id="f9187-118">이 정책에 대해 지원 되는 작업당 최대 분석 단위 수입니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-118">The maximum supported analytics units per job for this policy.</span></span> <span data-ttu-id="f9187-119">This, MinPriorityPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-119">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f9187-120">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="f9187-120">-MinPriorityPerJob</span></span>
<span data-ttu-id="f9187-121">이 정책에 대해 지원 되는 작업당 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-121">The minimum supported priority per job for this policy.</span></span> <span data-ttu-id="f9187-122">This, MaxAnalyticsUnitsPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-122">Either this, MaxAnalyticsUnitsPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="f9187-123">-이름</span><span class="sxs-lookup"><span data-stu-id="f9187-123">-Name</span></span>
<span data-ttu-id="f9187-124">업데이트할 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-124">Name of the compute policy to update.</span></span>

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

### <span data-ttu-id="f9187-125">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9187-125">-ResourceGroupName</span></span>
<span data-ttu-id="f9187-126">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-126">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="f9187-127">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-127">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="f9187-128">-확인</span><span class="sxs-lookup"><span data-stu-id="f9187-128">-Confirm</span></span>
<span data-ttu-id="f9187-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f9187-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f9187-130">-WhatIf</span></span>
<span data-ttu-id="f9187-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-131">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f9187-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f9187-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9187-133">CommonParameters</span></span>
<span data-ttu-id="f9187-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9187-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9187-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9187-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9187-136">입력</span><span class="sxs-lookup"><span data-stu-id="f9187-136">INPUTS</span></span>

### <span data-ttu-id="f9187-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="f9187-137">System.String</span></span>

### <span data-ttu-id="f9187-138">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="f9187-138">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

## <span data-ttu-id="f9187-139">출력</span><span class="sxs-lookup"><span data-stu-id="f9187-139">OUTPUTS</span></span>

### <span data-ttu-id="f9187-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="f9187-140">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="f9187-141">상속자</span><span class="sxs-lookup"><span data-stu-id="f9187-141">NOTES</span></span>

## <span data-ttu-id="f9187-142">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9187-142">RELATED LINKS</span></span>
