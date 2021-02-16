---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/new-azdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/New-AzDataLakeAnalyticsAccount.md
ms.openlocfilehash: c79665a6ed21309a7a702d9fd5bc5e876aa2ff21
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100204400"
---
# <span data-ttu-id="a2be5-101">New-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-101">New-AzDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a2be5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a2be5-102">SYNOPSIS</span></span>
<span data-ttu-id="a2be5-103">Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-103">Creates a Data Lake Analytics account.</span></span>

## <span data-ttu-id="a2be5-104">구문</span><span class="sxs-lookup"><span data-stu-id="a2be5-104">SYNTAX</span></span>

```
New-AzDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="a2be5-105">설명</span><span class="sxs-lookup"><span data-stu-id="a2be5-105">DESCRIPTION</span></span>
<span data-ttu-id="a2be5-106">**New-AzDataLakeAnalyticsAccount** cmdlet은 Azure Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-106">The **New-AzDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="a2be5-107">예제</span><span class="sxs-lookup"><span data-stu-id="a2be5-107">EXAMPLES</span></span>

### <span data-ttu-id="a2be5-108">예제 1: Data Lake Analytics 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="a2be5-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="a2be5-109">이 명령은 ContosoOrg라는 리소스 그룹에 ContosoAdlStore 데이터 저장소를 사용하는 ContosoAdlAccount라는 Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="a2be5-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="a2be5-110">PARAMETERS</span></span>

### <span data-ttu-id="a2be5-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="a2be5-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="a2be5-112">기본 데이터 원본으로 설정할 Data Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

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

### <span data-ttu-id="a2be5-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a2be5-113">-DefaultProfile</span></span>
<span data-ttu-id="a2be5-114">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="a2be5-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a2be5-115">-Location</span><span class="sxs-lookup"><span data-stu-id="a2be5-115">-Location</span></span>
<span data-ttu-id="a2be5-116">Data Lake Analytics 계정을 만들 위치를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="a2be5-117">현재 미국 동부 2만 지원됩니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-117">Only East US 2 is supported at this time.</span></span>

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

### <span data-ttu-id="a2be5-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="a2be5-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="a2be5-119">이 계정에 대해 지원되는 선택적 최대 분석 단위입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-119">The optional maximum supported analytics units for this account.</span></span>

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

### <span data-ttu-id="a2be5-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="a2be5-120">-MaxJobCount</span></span>
<span data-ttu-id="a2be5-121">동시에 계정에서 실행되는 선택적 최대 지원 작업입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="a2be5-122">지정하지 않으면 기본값은 3입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-122">If none is specified, defaults to 3</span></span>

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

### <span data-ttu-id="a2be5-123">-Name</span><span class="sxs-lookup"><span data-stu-id="a2be5-123">-Name</span></span>
<span data-ttu-id="a2be5-124">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-124">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="a2be5-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="a2be5-125">-QueryStoreRetention</span></span>
<span data-ttu-id="a2be5-126">작업 메타데이터가 보존되는 선택적 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="a2be5-127">지정하지 않으면 기본값은 30일입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-127">If none specified, the default is 30 days.</span></span>

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

### <span data-ttu-id="a2be5-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a2be5-128">-ResourceGroupName</span></span>
<span data-ttu-id="a2be5-129">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="a2be5-130">리소스 그룹을 만들 경우 New-AzResourceGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-130">To create a resource group, use the New-AzResourceGroup cmdlet.</span></span>

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

### <span data-ttu-id="a2be5-131">-Tag</span><span class="sxs-lookup"><span data-stu-id="a2be5-131">-Tag</span></span>
<span data-ttu-id="a2be5-132">문자열, 이 계정과 연결된 태그의 문자열 사전</span><span class="sxs-lookup"><span data-stu-id="a2be5-132">A string,string dictionary of tags associated with this account</span></span>

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

### <span data-ttu-id="a2be5-133">-Tier</span><span class="sxs-lookup"><span data-stu-id="a2be5-133">-Tier</span></span>
<span data-ttu-id="a2be5-134">이 계정에 사용할 원하는 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-134">The desired commitment tier for this account to use.</span></span>

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

### <span data-ttu-id="a2be5-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a2be5-135">CommonParameters</span></span>
<span data-ttu-id="a2be5-136">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="a2be5-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a2be5-137">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="a2be5-137">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a2be5-138">입력</span><span class="sxs-lookup"><span data-stu-id="a2be5-138">INPUTS</span></span>

### <span data-ttu-id="a2be5-139">System.String</span><span class="sxs-lookup"><span data-stu-id="a2be5-139">System.String</span></span>

### <span data-ttu-id="a2be5-140">System.Collections.Hashtable</span><span class="sxs-lookup"><span data-stu-id="a2be5-140">System.Collections.Hashtable</span></span>

### <span data-ttu-id="a2be5-141">System.Nullable'1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span><span class="sxs-lookup"><span data-stu-id="a2be5-141">System.Nullable\`1[[System.Int32, System.Private.CoreLib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=7cec85d7bea7798e]]</span></span>

### <span data-ttu-id="a2be5-142">System.Nullable'1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span><span class="sxs-lookup"><span data-stu-id="a2be5-142">System.Nullable\`1[[Microsoft.Azure.Management.DataLake.Analytics.Models.TierType, Microsoft.Azure.Management.DataLake.Analytics, Version=3.0.0.0, Culture=neutral, PublicKeyToken=31bf3856ad364e35]]</span></span>

## <span data-ttu-id="a2be5-143">출력</span><span class="sxs-lookup"><span data-stu-id="a2be5-143">OUTPUTS</span></span>

### <span data-ttu-id="a2be5-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-144">Microsoft.Azure.Commands.DataLakeAnalytics.Models.PSDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="a2be5-145">참고 사항</span><span class="sxs-lookup"><span data-stu-id="a2be5-145">NOTES</span></span>

## <span data-ttu-id="a2be5-146">관련 링크</span><span class="sxs-lookup"><span data-stu-id="a2be5-146">RELATED LINKS</span></span>

[<span data-ttu-id="a2be5-147">Get-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-147">Get-AzDataLakeAnalyticsAccount</span></span>](./Get-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a2be5-148">Remove-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-148">Remove-AzDataLakeAnalyticsAccount</span></span>](./Remove-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a2be5-149">Set-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-149">Set-AzDataLakeAnalyticsAccount</span></span>](./Set-AzDataLakeAnalyticsAccount.md)

[<span data-ttu-id="a2be5-150">Test-AzDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="a2be5-150">Test-AzDataLakeAnalyticsAccount</span></span>](./Test-AzDataLakeAnalyticsAccount.md)


