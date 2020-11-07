---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 0377C4E9-C1DC-49BA-BBC4-5598C83234F8
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Get-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: b7f2c6f2077d0b7e9c7510f6984ada15a65d6ef2
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93711584"
---
# <span data-ttu-id="65cb3-101">Get-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="65cb3-101">Get-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="65cb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="65cb3-102">SYNOPSIS</span></span>
<span data-ttu-id="65cb3-103">Data Lake Analytics 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-103">Gets a Data Lake Analytics data source.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="65cb3-104">구문과</span><span class="sxs-lookup"><span data-stu-id="65cb3-104">SYNTAX</span></span>

### <span data-ttu-id="65cb3-105">모든 데이터 원본 나열 (기본값)</span><span class="sxs-lookup"><span data-stu-id="65cb3-105">List all data sources (Default)</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cb3-106">Data Lake Store 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="65cb3-106">Get a Data Lake Store account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="65cb3-107">Blob 저장소 계정 가져오기</span><span class="sxs-lookup"><span data-stu-id="65cb3-107">Get a Blob storage account</span></span>
```
Get-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [[-ResourceGroupName] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="65cb3-108">설명은</span><span class="sxs-lookup"><span data-stu-id="65cb3-108">DESCRIPTION</span></span>
<span data-ttu-id="65cb3-109">**AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-109">The **Get-AzureRmDataLakeAnalyticsDataSource** cmdlet gets an Azure Data Lake Analytics data source.</span></span>

## <span data-ttu-id="65cb3-110">예제의</span><span class="sxs-lookup"><span data-stu-id="65cb3-110">EXAMPLES</span></span>

### <span data-ttu-id="65cb3-111">예제 1: 계정에서 데이터 원본 가져오기</span><span class="sxs-lookup"><span data-stu-id="65cb3-111">Example 1: Get a data source from an account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataLakeStore "ContosoAdls"
```

<span data-ttu-id="65cb3-112">이 명령은 Data Lake Analytics 계정에서 ContosoAdls 이라는 Data Lake Store 데이터 원본을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-112">This command gets a Data Lake Store data source named ContosoAdls from a Data Lake Analytics account.</span></span>

### <span data-ttu-id="65cb3-113">예제 2: Data Lake Analytics 계정에서 Data Lake Store 계정 목록 가져오기</span><span class="sxs-lookup"><span data-stu-id="65cb3-113">Example 2: Get the list of Data Lake Store accounts in a Data Lake Analytics account</span></span>
```
PS C:\>Get-AzureRmDataLakeAnalyticsDataSource -AccountName "ContosoAdlA" -DataSource "DataLakeStore"
```

<span data-ttu-id="65cb3-114">이 명령은 Data Lake Analytics 계정에서 모든 Data Lake Store 계정을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-114">This command gets all Data Lake Store accounts from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="65cb3-115">변수</span><span class="sxs-lookup"><span data-stu-id="65cb3-115">PARAMETERS</span></span>

### <span data-ttu-id="65cb3-116">-계정</span><span class="sxs-lookup"><span data-stu-id="65cb3-116">-Account</span></span>
<span data-ttu-id="65cb3-117">이 cmdlet이 데이터 원본을 가져오는 데이터 호수 분석 계정을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-117">Specifies the Data Lake Analytics account that this cmdlet gets data sources.</span></span>

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

### <span data-ttu-id="65cb3-118">-Blob</span><span class="sxs-lookup"><span data-stu-id="65cb3-118">-Blob</span></span>
<span data-ttu-id="65cb3-119">Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-119">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65cb3-120">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="65cb3-120">-DataLakeStore</span></span>
<span data-ttu-id="65cb3-121">Data Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-121">Specifies the name of the Data Lake Store account.</span></span>

```yaml
Type: System.String
Parameter Sets: Get a Data Lake Store account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65cb3-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="65cb3-122">-ResourceGroupName</span></span>
<span data-ttu-id="65cb3-123">데이터 원본을 포함 하는 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-123">Specifies the resource group name that contains the data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="65cb3-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="65cb3-124">-DefaultProfile</span></span>
<span data-ttu-id="65cb3-125">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="65cb3-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="65cb3-126">CommonParameters</span></span>
<span data-ttu-id="65cb3-127">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="65cb3-128">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="65cb3-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="65cb3-129">입력</span><span class="sxs-lookup"><span data-stu-id="65cb3-129">INPUTS</span></span>

## <span data-ttu-id="65cb3-130">출력</span><span class="sxs-lookup"><span data-stu-id="65cb3-130">OUTPUTS</span></span>

### <span data-ttu-id="65cb3-131">PSStorageAccountInfo</span><span class="sxs-lookup"><span data-stu-id="65cb3-131">PSStorageAccountInfo</span></span>
<span data-ttu-id="65cb3-132">지정 된 Azure Storage 계정 세부 정보입니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-132">The specified Azure Storage account details.</span></span>

### <span data-ttu-id="65cb3-133">PSDataLakeStoreAccountInfo</span><span class="sxs-lookup"><span data-stu-id="65cb3-133">PSDataLakeStoreAccountInfo</span></span>
<span data-ttu-id="65cb3-134">지정 된 Data Lake Store 계정 세부 정보</span><span class="sxs-lookup"><span data-stu-id="65cb3-134">The specified Data Lake Store account details</span></span>

### <span data-ttu-id="65cb3-135">목록<AdlDataSource></span><span class="sxs-lookup"><span data-stu-id="65cb3-135">List<AdlDataSource></span></span>
<span data-ttu-id="65cb3-136">지정 된 Data Lake Analytics 계정의 Azure 저장소 계정 및 Data Lake Store 계정 목록입니다.</span><span class="sxs-lookup"><span data-stu-id="65cb3-136">The list of both Azure Storage accounts and Data Lake Store accounts in the specified Data Lake Analytics account.</span></span>

## <span data-ttu-id="65cb3-137">상속자</span><span class="sxs-lookup"><span data-stu-id="65cb3-137">NOTES</span></span>

## <span data-ttu-id="65cb3-138">관련 링크</span><span class="sxs-lookup"><span data-stu-id="65cb3-138">RELATED LINKS</span></span>

[<span data-ttu-id="65cb3-139">추가-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="65cb3-139">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="65cb3-140">제거-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="65cb3-140">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="65cb3-141">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="65cb3-141">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


