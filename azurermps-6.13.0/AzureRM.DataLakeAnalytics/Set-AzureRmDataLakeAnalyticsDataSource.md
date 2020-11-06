---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datalakeanalytics/set-azurermdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 8aae62ccbf79f2b3c59f6009aa5233daf00853fd
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93532040"
---
# <span data-ttu-id="01385-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01385-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="01385-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="01385-102">SYNOPSIS</span></span>
<span data-ttu-id="01385-103">Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="01385-104">구문과</span><span class="sxs-lookup"><span data-stu-id="01385-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="01385-105">설명은</span><span class="sxs-lookup"><span data-stu-id="01385-105">DESCRIPTION</span></span>
<span data-ttu-id="01385-106">**AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="01385-107">예제의</span><span class="sxs-lookup"><span data-stu-id="01385-107">EXAMPLES</span></span>

### <span data-ttu-id="01385-108">예제 1: 데이터 원본에 대 한 선택 키 변경</span><span class="sxs-lookup"><span data-stu-id="01385-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="01385-109">이 명령은 Azure Blob 저장소 데이터 원본에 대해 저장 된 선택 키를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="01385-110">변수</span><span class="sxs-lookup"><span data-stu-id="01385-110">PARAMETERS</span></span>

### <span data-ttu-id="01385-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="01385-111">-AccessKey</span></span>
<span data-ttu-id="01385-112">Azure Blob 저장소 데이터 원본의 새 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="01385-113">-계정</span><span class="sxs-lookup"><span data-stu-id="01385-113">-Account</span></span>
<span data-ttu-id="01385-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="01385-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="01385-115">-Blob</span></span>
<span data-ttu-id="01385-116">Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-116">Specifies the name of the Azure Blob Storage data source.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01385-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="01385-117">-DefaultProfile</span></span>
<span data-ttu-id="01385-118">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="01385-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="01385-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="01385-119">-ResourceGroupName</span></span>
<span data-ttu-id="01385-120">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="01385-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="01385-121">CommonParameters</span></span>
<span data-ttu-id="01385-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="01385-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="01385-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="01385-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="01385-124">입력</span><span class="sxs-lookup"><span data-stu-id="01385-124">INPUTS</span></span>

### <span data-ttu-id="01385-125">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="01385-125">System.String</span></span>

## <span data-ttu-id="01385-126">출력</span><span class="sxs-lookup"><span data-stu-id="01385-126">OUTPUTS</span></span>

### <span data-ttu-id="01385-127">시스템. i a o</span><span class="sxs-lookup"><span data-stu-id="01385-127">System.Void</span></span>

## <span data-ttu-id="01385-128">상속자</span><span class="sxs-lookup"><span data-stu-id="01385-128">NOTES</span></span>

## <span data-ttu-id="01385-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="01385-129">RELATED LINKS</span></span>

[<span data-ttu-id="01385-130">추가-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01385-130">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="01385-131">제거-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="01385-131">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


