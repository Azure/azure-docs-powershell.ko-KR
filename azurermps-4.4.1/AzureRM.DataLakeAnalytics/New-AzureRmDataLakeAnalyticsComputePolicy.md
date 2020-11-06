---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsComputePolicy.md
ms.openlocfilehash: 1dfd9c4d55c9898ce9f4b656f53d7606ced11359
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93527632"
---
# <span data-ttu-id="38d6b-101">New-AzureRmDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="38d6b-101">New-AzureRmDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="38d6b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="38d6b-102">SYNOPSIS</span></span>
<span data-ttu-id="38d6b-103">특정 AAD 엔터티에 대 한 데이터 호수 분석 계산 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-103">Creates a Data Lake Analytics compute policy rule for a specific AAD entity.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="38d6b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="38d6b-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsComputePolicy [-ResourceGroupName <String>] [-Account] <String> [-Name] <String>
 [-ObjectId] <Guid> [-ObjectType] <String> [-MaxDegreeOfParallelismPerJob <Int32>] [-MinPriorityPerJob <Int32>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="38d6b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="38d6b-105">DESCRIPTION</span></span>
<span data-ttu-id="38d6b-106">**AzureRmDataLakeAnalyticsComputePolicy** 는 Azure Data Lake Analytics 계정에서 특정 AAD 엔터티에 대해 지정 된 계산 정책 규칙을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-106">The **New-AzureRmDataLakeAnalyticsComputePolicy** creates the specified compute policy rule for a specific AAD entity in an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="38d6b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="38d6b-107">EXAMPLES</span></span>

### <span data-ttu-id="38d6b-108">예제 1: 하나의 규칙만 사용 하 여 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="38d6b-108">Example 1: Create a compute policy with only one rule</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5
```

<span data-ttu-id="38d6b-109">이 명령은 5 개 이상의 병렬 처리를 사용 하 여 작업을 제출할 수 없도록 하는 id "83cb7ad2-3523-4b82-b909-d478b0d8aea3"의 사용자에 대해 "contosoadla" 계정에 "myPolicy" 라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-109">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism.</span></span>

### <span data-ttu-id="38d6b-110">예제 2: 두 규칙 집합을 모두 사용 하 여 계산 정책 만들기</span><span class="sxs-lookup"><span data-stu-id="38d6b-110">Example 2: Create a compute policy with both rules set</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsComputePolicy -Account "contosoadla" -Name "myPolicy" -ObjectId 83cb7ad2-3523-4b82-b909-d478b0d8aea3 -ObjectType User -MaxDegreeOfParallelismPerJob 5 -MinPriorityPerJob 100
```

<span data-ttu-id="38d6b-111">이 명령은 5 개 이상의 병렬 처리를 사용 하거나 우선 순위가 100 보다 낮은 작업을 제출할 수 없도록 하는 id "83cb7ad2-3523-4b82-b909-d478b0d8aea3"의 사용자에 대해 "contosoadla" 계정에 "myPolicy" 라는 정책을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-111">This command creates a policy called "myPolicy" in account "contosoadla" for the user with id "83cb7ad2-3523-4b82-b909-d478b0d8aea3" that ensures they cannot submit any job with more than 5 parallelism or with a priority lower than 100</span></span>

## <span data-ttu-id="38d6b-112">변수</span><span class="sxs-lookup"><span data-stu-id="38d6b-112">PARAMETERS</span></span>

### <span data-ttu-id="38d6b-113">-계정</span><span class="sxs-lookup"><span data-stu-id="38d6b-113">-Account</span></span>
<span data-ttu-id="38d6b-114">계산 정책을 추가할 계정의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-114">Name of the account to add the compute policy to.</span></span>

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

### <span data-ttu-id="38d6b-115">-MaxDegreeOfParallelismPerJob</span><span class="sxs-lookup"><span data-stu-id="38d6b-115">-MaxDegreeOfParallelismPerJob</span></span>
<span data-ttu-id="38d6b-116">이 정책에 대해 지원 되는 작업당 병렬 처리의 최대 수준입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-116">The maximum supported degree of parallelism per job for this policy.</span></span>
<span data-ttu-id="38d6b-117">This, MinPriorityPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-117">Either this, MinPriorityPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="38d6b-118">-MinPriorityPerJob</span><span class="sxs-lookup"><span data-stu-id="38d6b-118">-MinPriorityPerJob</span></span>
<span data-ttu-id="38d6b-119">이 정책에 대해 지원 되는 작업당 최소 우선 순위입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-119">The minimum supported priority per job for this policy.</span></span>
<span data-ttu-id="38d6b-120">This, MaxDegreeOfParallelismPerJob 또는 both 매개 변수 중 하나를 지정 해야 합니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-120">Either this, MaxDegreeOfParallelismPerJob, or both parameters must be specified.</span></span>

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

### <span data-ttu-id="38d6b-121">-이름</span><span class="sxs-lookup"><span data-stu-id="38d6b-121">-Name</span></span>
<span data-ttu-id="38d6b-122">만들 계산 정책의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-122">Name of the compute policy to create.</span></span>

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

### <span data-ttu-id="38d6b-123">-ObjectId</span><span class="sxs-lookup"><span data-stu-id="38d6b-123">-ObjectId</span></span>
<span data-ttu-id="38d6b-124">정책을 적용할 사용자 또는 그룹의 Azure Active Directory 개체 id입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-124">The Azure Active Directory object id for the user or group to apply the policy to.</span></span>

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

### <span data-ttu-id="38d6b-125">-ObjectType</span><span class="sxs-lookup"><span data-stu-id="38d6b-125">-ObjectType</span></span>
<span data-ttu-id="38d6b-126">전달 된 개체 ID의 Azure Active Directory 개체 형식입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-126">The Azure Active Directory object type for the object ID passed in.</span></span>

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

### <span data-ttu-id="38d6b-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="38d6b-127">-ResourceGroupName</span></span>
<span data-ttu-id="38d6b-128">계정이 있는 리소스 그룹의 이름입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-128">Name of resource group under which you the account exists.</span></span>
<span data-ttu-id="38d6b-129">선택 사항이 며 제공 되지 않은 경우 검색을 시도 합니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-129">Optional and will attempt to discover if not provided.</span></span>

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

### <span data-ttu-id="38d6b-130">-확인</span><span class="sxs-lookup"><span data-stu-id="38d6b-130">-Confirm</span></span>
<span data-ttu-id="38d6b-131">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="38d6b-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="38d6b-132">-WhatIf</span></span>
<span data-ttu-id="38d6b-133">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-133">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="38d6b-134">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="38d6b-135">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="38d6b-135">-DefaultProfile</span></span>
<span data-ttu-id="38d6b-136">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-136">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="38d6b-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="38d6b-137">CommonParameters</span></span>
<span data-ttu-id="38d6b-138">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="38d6b-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="38d6b-139">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="38d6b-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="38d6b-140">입력</span><span class="sxs-lookup"><span data-stu-id="38d6b-140">INPUTS</span></span>

### <span data-ttu-id="38d6b-141">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="38d6b-141">System.String</span></span>
<span data-ttu-id="38d6b-142">시스템. i a i.</span><span class="sxs-lookup"><span data-stu-id="38d6b-142">System.Guid System.Int32</span></span>

## <span data-ttu-id="38d6b-143">출력</span><span class="sxs-lookup"><span data-stu-id="38d6b-143">OUTPUTS</span></span>

### <span data-ttu-id="38d6b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span><span class="sxs-lookup"><span data-stu-id="38d6b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsComputePolicy</span></span>

## <span data-ttu-id="38d6b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="38d6b-145">NOTES</span></span>

## <span data-ttu-id="38d6b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="38d6b-146">RELATED LINKS</span></span>

