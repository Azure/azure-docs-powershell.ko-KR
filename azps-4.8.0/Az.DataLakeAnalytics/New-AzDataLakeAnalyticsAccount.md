---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94212513"
---
# <span data-ttu-id="84f1b-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="84f1b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84f1b-102">SYNOPSIS</span></span>
<span data-ttu-id="84f1b-103">Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="84f1b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="84f1b-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="84f1b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="84f1b-105">DESCRIPTION</span></span>
<span data-ttu-id="84f1b-106">**AzDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="84f1b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="84f1b-107">EXAMPLES</span></span>

### <span data-ttu-id="84f1b-108">예제 1: Data Lake Analytics 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="84f1b-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="84f1b-109">이 명령은 ContosoAdlStore 데이터 저장소를 사용 하는 ContosoAdlAccount 이라는 데이터 호수 분석 계정을 ContosoOrg 이라는 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="84f1b-110">변수</span><span class="sxs-lookup"><span data-stu-id="84f1b-110">PARAMETERS</span></span>

### <span data-ttu-id="84f1b-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="84f1b-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="84f1b-112">기본 데이터 원본으로 설정할 Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="84f1b-113">-DefaultProfile</span></span>
<span data-ttu-id="84f1b-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="84f1b-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="84f1b-115">-위치</span><span class="sxs-lookup"><span data-stu-id="84f1b-115">-Location</span></span>
<span data-ttu-id="84f1b-116">Data Lake Analytics 계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="84f1b-117">이번에는 미국 동부 2만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="84f1b-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="84f1b-119">이 계정에 대해 지원 되는 최대 분석 단위 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="84f1b-120">-MaxJobCount</span></span>
<span data-ttu-id="84f1b-121">계정에서 동시에 실행 되는 선택적으로 지원 되는 최대 작업 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="84f1b-122">아무것도 지정 하지 않으면 기본적으로 3이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="84f1b-123">-이름</span><span class="sxs-lookup"><span data-stu-id="84f1b-123">-Name</span></span>
<span data-ttu-id="84f1b-124">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="84f1b-125">-QueryStoreRetention</span></span>
<span data-ttu-id="84f1b-126">작업 메타 데이터가 유지 되는 선택적 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="84f1b-127">지정 하지 않을 경우 기본값은 30 일입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="84f1b-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="84f1b-128">-ResourceGroupName</span></span>
<span data-ttu-id="84f1b-129">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="84f1b-130">리소스 그룹을 만들려면 New-AzResourceGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-131">태그</span><span class="sxs-lookup"><span data-stu-id="84f1b-131">-Tag</span></span>
<span data-ttu-id="84f1b-132">이 계정과 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-133">-티어</span><span class="sxs-lookup"><span data-stu-id="84f1b-133">-Tier</span></span>
<span data-ttu-id="84f1b-134">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType]
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="84f1b-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84f1b-135">CommonParameters</span></span>
<span data-ttu-id="84f1b-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="84f1b-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84f1b-137">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84f1b-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84f1b-138">입력</span><span class="sxs-lookup"><span data-stu-id="84f1b-138">INPUTS</span></span>

### <span data-ttu-id="84f1b-139">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="84f1b-139">System.String</span></span>

### <span data-ttu-id="84f1b-140">System.webserver. 컬렉션 테이블</span><span class="sxs-lookup"><span data-stu-id="84f1b-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="84f1b-141">시스템 Null 허용 ' 1 [[4.0.0.0, System.webserver, Version =, Culture = 중립, PublicKeyToken = 7cec85d7bea7798e])</span><span class="sxs-lookup"><span data-stu-id="84f1b-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="84f1b-142">시스템 Null 허용 ' 1 [[DataLake]. TierType, [Microsoft Azure. DataLake. 31bf3856ad364e35, Version = 3.0.0.0, Culture = 중립, PublicKeyToken =]]</span><span class="sxs-lookup"><span data-stu-id="84f1b-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="84f1b-143">출력</span><span class="sxs-lookup"><span data-stu-id="84f1b-143">OUTPUTS</span></span>

### <span data-ttu-id="84f1b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="84f1b-145">상속자</span><span class="sxs-lookup"><span data-stu-id="84f1b-145">NOTES</span></span>

## <span data-ttu-id="84f1b-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="84f1b-146">RELATED LINKS</span></span>

[<span data-ttu-id="84f1b-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="84f1b-148">제거-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="84f1b-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="84f1b-150">테스트-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="84f1b-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


