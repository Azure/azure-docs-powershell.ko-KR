---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Set-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 258db8a7dc1d771b73ea4c4fa373b1861847b820
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703768"
---
# <span data-ttu-id="46fed-101">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="46fed-101">Set-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="46fed-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="46fed-102">SYNOPSIS</span></span>
<span data-ttu-id="46fed-103">Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="46fed-104">구문과</span><span class="sxs-lookup"><span data-stu-id="46fed-104">SYNTAX</span></span>

```
Set-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="46fed-105">설명은</span><span class="sxs-lookup"><span data-stu-id="46fed-105">DESCRIPTION</span></span>
<span data-ttu-id="46fed-106">**AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정의 데이터 원본에 대 한 세부 정보를 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-106">The **Set-AzureRmDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="46fed-107">예제의</span><span class="sxs-lookup"><span data-stu-id="46fed-107">EXAMPLES</span></span>

### <span data-ttu-id="46fed-108">예제 1: 데이터 원본에 대 한 선택 키 변경</span><span class="sxs-lookup"><span data-stu-id="46fed-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="46fed-109">이 명령은 Azure Blob 저장소 데이터 원본에 대해 저장 된 선택 키를 변경 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="46fed-110">변수</span><span class="sxs-lookup"><span data-stu-id="46fed-110">PARAMETERS</span></span>

### <span data-ttu-id="46fed-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="46fed-111">-AccessKey</span></span>
<span data-ttu-id="46fed-112">Azure Blob 저장소 데이터 원본의 새 선택 키를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="46fed-113">-계정</span><span class="sxs-lookup"><span data-stu-id="46fed-113">-Account</span></span>
<span data-ttu-id="46fed-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="46fed-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="46fed-115">-Blob</span></span>
<span data-ttu-id="46fed-116">Azure Blob 저장소 데이터 원본의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="46fed-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="46fed-117">-ResourceGroupName</span></span>
<span data-ttu-id="46fed-118">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-118">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="46fed-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="46fed-119">-DefaultProfile</span></span>
<span data-ttu-id="46fed-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-120">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="46fed-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="46fed-121">CommonParameters</span></span>
<span data-ttu-id="46fed-122">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="46fed-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="46fed-123">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="46fed-123">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="46fed-124">입력</span><span class="sxs-lookup"><span data-stu-id="46fed-124">INPUTS</span></span>

## <span data-ttu-id="46fed-125">출력</span><span class="sxs-lookup"><span data-stu-id="46fed-125">OUTPUTS</span></span>

### <span data-ttu-id="46fed-126">않아야</span><span class="sxs-lookup"><span data-stu-id="46fed-126">None</span></span>

## <span data-ttu-id="46fed-127">상속자</span><span class="sxs-lookup"><span data-stu-id="46fed-127">NOTES</span></span>

## <span data-ttu-id="46fed-128">관련 링크</span><span class="sxs-lookup"><span data-stu-id="46fed-128">RELATED LINKS</span></span>

[<span data-ttu-id="46fed-129">추가-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="46fed-129">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="46fed-130">제거-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="46fed-130">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>](./Remove-AzureRmDataLakeAnalyticsDataSource.md)


