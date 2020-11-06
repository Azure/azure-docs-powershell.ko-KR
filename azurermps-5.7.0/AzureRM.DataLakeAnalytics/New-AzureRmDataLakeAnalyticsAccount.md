---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0A7CD695-6D14-4BC9-B960-0CAFE502B88B
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/new-azurermdatalakeanalyticsaccount
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/New-AzureRmDataLakeAnalyticsAccount.md
ms.openlocfilehash: 36bf1bbfeb0c44189f5eeeaa0988d0314980e48d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93528993"
---
# <span data-ttu-id="60aa9-101">New-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-101">New-AzureRmDataLakeAnalyticsAccount</span></span>

## <span data-ttu-id="60aa9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="60aa9-102">SYNOPSIS</span></span>
<span data-ttu-id="60aa9-103">Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-103">Creates a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="60aa9-104">구문과</span><span class="sxs-lookup"><span data-stu-id="60aa9-104">SYNTAX</span></span>

```
New-AzureRmDataLakeAnalyticsAccount [-ResourceGroupName] <String> [-Name] <String> [-Location] <String>
 [-DefaultDataLakeStore] <String> [[-Tag] <Hashtable>] [-MaxAnalyticsUnits <Int32>] [-MaxJobCount <Int32>]
 [-QueryStoreRetention <Int32>] [-Tier <TierType>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="60aa9-105">설명은</span><span class="sxs-lookup"><span data-stu-id="60aa9-105">DESCRIPTION</span></span>
<span data-ttu-id="60aa9-106">**AzureRmDataLakeAnalyticsAccount** Cmdlet은 Azure Data Lake Analytics 계정을 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-106">The **New-AzureRmDataLakeAnalyticsAccount** cmdlet creates an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="60aa9-107">예제의</span><span class="sxs-lookup"><span data-stu-id="60aa9-107">EXAMPLES</span></span>

### <span data-ttu-id="60aa9-108">예제 1: Data Lake Analytics 계정 만들기</span><span class="sxs-lookup"><span data-stu-id="60aa9-108">Example 1: Create a Data Lake Analytics account</span></span>
```
PS C:\>New-AzureRmDataLakeAnalyticsAccount -Name "ContosoAdlAccount" -ResourceGroupName "ContosoOrg" -Location "East US 2" -DefaultDataLakeStore "ContosoAdlStore"
```

<span data-ttu-id="60aa9-109">이 명령은 ContosoAdlStore 데이터 저장소를 사용 하는 ContosoAdlAccount 이라는 데이터 호수 분석 계정을 ContosoOrg 이라는 리소스 그룹에 만듭니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-109">This command creates a Data Lake Analytics account named ContosoAdlAccount that uses the ContosoAdlStore Data Store, in the resource group named ContosoOrg.</span></span>

## <span data-ttu-id="60aa9-110">변수</span><span class="sxs-lookup"><span data-stu-id="60aa9-110">PARAMETERS</span></span>

### <span data-ttu-id="60aa9-111">-DefaultDataLakeStore</span><span class="sxs-lookup"><span data-stu-id="60aa9-111">-DefaultDataLakeStore</span></span>
<span data-ttu-id="60aa9-112">기본 데이터 원본으로 설정할 Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-112">Specifies the name of the Data Lake Store account to set as the default data source.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="60aa9-113">-DefaultProfile</span></span>
<span data-ttu-id="60aa9-114">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="60aa9-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-115">-위치</span><span class="sxs-lookup"><span data-stu-id="60aa9-115">-Location</span></span>
<span data-ttu-id="60aa9-116">Data Lake Analytics 계정을 만들 위치를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-116">Specifies the location at which to create the Data Lake Analytics account.</span></span>
<span data-ttu-id="60aa9-117">이번에는 미국 동부 2만 지원 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-117">Only East US 2 is supported at this time.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-118">-MaxAnalyticsUnits</span><span class="sxs-lookup"><span data-stu-id="60aa9-118">-MaxAnalyticsUnits</span></span>
<span data-ttu-id="60aa9-119">이 계정에 대해 지원 되는 최대 분석 단위 (선택 사항)입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-119">The optional maximum supported analytics units for this account.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: MaxDegreeOfParallelism

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-120">-MaxJobCount</span><span class="sxs-lookup"><span data-stu-id="60aa9-120">-MaxJobCount</span></span>
<span data-ttu-id="60aa9-121">계정에서 동시에 실행 되는 선택적으로 지원 되는 최대 작업 시간입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-121">The optional maximum supported jobs running under the account at the same time.</span></span> <span data-ttu-id="60aa9-122">아무것도 지정 하지 않으면 기본적으로 3이 됩니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-122">If none is specified, defaults to 3</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-123">-이름</span><span class="sxs-lookup"><span data-stu-id="60aa9-123">-Name</span></span>
<span data-ttu-id="60aa9-124">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-124">Specifies the Data Lake Analytics account name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-125">-QueryStoreRetention</span><span class="sxs-lookup"><span data-stu-id="60aa9-125">-QueryStoreRetention</span></span>
<span data-ttu-id="60aa9-126">작업 메타 데이터가 유지 되는 선택적 일 수입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-126">The optional number of days that job metadata is retained.</span></span> <span data-ttu-id="60aa9-127">지정 하지 않을 경우 기본값은 30 일입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-127">If none specified, the default is 30 days.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="60aa9-128">-ResourceGroupName</span></span>
<span data-ttu-id="60aa9-129">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-129">Specifies the resource group name of the Data Lake Analytics account.</span></span>
<span data-ttu-id="60aa9-130">리소스 그룹을 만들려면 New-AzureRmResourceGroup cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-130">To create a resource group, use the New-AzureRmResourceGroup cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-131">태그</span><span class="sxs-lookup"><span data-stu-id="60aa9-131">-Tag</span></span>
<span data-ttu-id="60aa9-132">이 계정과 연결 된 태그의 문자열 사전입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-132">A string,string dictionary of tags associated with this account</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-133">-티어</span><span class="sxs-lookup"><span data-stu-id="60aa9-133">-Tier</span></span>
<span data-ttu-id="60aa9-134">이 계정에서 사용할 적절 한 약정 계층입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-134">The desired commitment tier for this account to use.</span></span>

```yaml
Type: TierType
Parameter Sets: (All)
Aliases:
Accepted values: Consumption, Commitment100AUHours, Commitment500AUHours, Commitment1000AUHours, Commitment5000AUHours, Commitment10000AUHours, Commitment50000AUHours, Commitment100000AUHours, Commitment500000AUHours

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="60aa9-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="60aa9-135">CommonParameters</span></span>
<span data-ttu-id="60aa9-136">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="60aa9-137">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="60aa9-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="60aa9-138">입력</span><span class="sxs-lookup"><span data-stu-id="60aa9-138">INPUTS</span></span>

### <span data-ttu-id="60aa9-139">않아야</span><span class="sxs-lookup"><span data-stu-id="60aa9-139">None</span></span>
<span data-ttu-id="60aa9-140">이 cmdlet은 입력을 허용 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-140">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="60aa9-141">출력</span><span class="sxs-lookup"><span data-stu-id="60aa9-141">OUTPUTS</span></span>

### <span data-ttu-id="60aa9-142">PSDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-142">PSDataLakeAnalyticsAccount</span></span>
<span data-ttu-id="60aa9-143">새로 만든 계정에 대 한 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="60aa9-143">The details of the newly created account.</span></span>

## <span data-ttu-id="60aa9-144">상속자</span><span class="sxs-lookup"><span data-stu-id="60aa9-144">NOTES</span></span>

## <span data-ttu-id="60aa9-145">관련 링크</span><span class="sxs-lookup"><span data-stu-id="60aa9-145">RELATED LINKS</span></span>

[<span data-ttu-id="60aa9-146">Get-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-146">Get-AzureRmDataLakeAnalyticsAccount</span></span>](./Get-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="60aa9-147">제거-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-147">Remove-AzureRmDataLakeAnalyticsAccount</span></span>](./Remove-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="60aa9-148">Set-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-148">Set-AzureRmDataLakeAnalyticsAccount</span></span>](./Set-AzureRmDataLakeAnalyticsAccount.md)

[<span data-ttu-id="60aa9-149">테스트-AzureRmDataLakeAnalyticsAccount</span><span class="sxs-lookup"><span data-stu-id="60aa9-149">Test-AzureRmDataLakeAnalyticsAccount</span></span>](./Test-AzureRmDataLakeAnalyticsAccount.md)


