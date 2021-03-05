---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: 2F28118E-6A34-4261-85BD-8CFDDC8A2707
online version: https://docs.microsoft.com/powershell/module/az.datalakeanalytics/set-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Set-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: cb51b1c703d527a2888bd0e80d8cc7a50d044e36
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101962368"
---
# <span data-ttu-id="1a4ae-101">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1a4ae-101">Set-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="1a4ae-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1a4ae-102">SYNOPSIS</span></span>
<span data-ttu-id="1a4ae-103">Data Lake Analytics 계정의 데이터 원본의 세부 정보를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-103">Modifies the details of a data source of a Data Lake Analytics account.</span></span>

## <span data-ttu-id="1a4ae-104">구문</span><span class="sxs-lookup"><span data-stu-id="1a4ae-104">SYNTAX</span></span>

```
Set-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-AccessKey] <String>
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1a4ae-105">설명</span><span class="sxs-lookup"><span data-stu-id="1a4ae-105">DESCRIPTION</span></span>
<span data-ttu-id="1a4ae-106">**Set-AzDataLakeAnalyticsDataSource** cmdlet은 Azure Data Lake Analytics 계정의 데이터 원본의 세부 정보를 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-106">The **Set-AzDataLakeAnalyticsDataSource** cmdlet modifies the details of a data source of an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="1a4ae-107">예제</span><span class="sxs-lookup"><span data-stu-id="1a4ae-107">EXAMPLES</span></span>

### <span data-ttu-id="1a4ae-108">예제 1: 데이터 원본에 대한 액세스 키 변경</span><span class="sxs-lookup"><span data-stu-id="1a4ae-108">Example 1: Change the access key for a data source</span></span>
```
PS C:\>Set-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "contosowasb" -AccessKey "...newaccesskey..."
```

<span data-ttu-id="1a4ae-109">이 명령은 Azure Blob Storage 데이터 원본에 저장된 액세스 키를 변경합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-109">This command changes the access key stored for an Azure Blob Storage data source.</span></span>

## <span data-ttu-id="1a4ae-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="1a4ae-110">PARAMETERS</span></span>

### <span data-ttu-id="1a4ae-111">-AccessKey</span><span class="sxs-lookup"><span data-stu-id="1a4ae-111">-AccessKey</span></span>
<span data-ttu-id="1a4ae-112">Azure Blob Storage 데이터 원본의 새 액세스 키를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-112">Specifies the new access key of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="1a4ae-113">-Account</span><span class="sxs-lookup"><span data-stu-id="1a4ae-113">-Account</span></span>
<span data-ttu-id="1a4ae-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="1a4ae-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="1a4ae-115">-Blob</span></span>
<span data-ttu-id="1a4ae-116">Azure Blob Storage 데이터 원본의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-116">Specifies the name of the Azure Blob Storage data source.</span></span>

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

### <span data-ttu-id="1a4ae-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1a4ae-117">-DefaultProfile</span></span>
<span data-ttu-id="1a4ae-118">azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="1a4ae-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="1a4ae-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="1a4ae-119">-ResourceGroupName</span></span>
<span data-ttu-id="1a4ae-120">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-120">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="1a4ae-121">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1a4ae-121">CommonParameters</span></span>
<span data-ttu-id="1a4ae-122">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-122">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1a4ae-123">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1a4ae-123">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1a4ae-124">입력</span><span class="sxs-lookup"><span data-stu-id="1a4ae-124">INPUTS</span></span>

### <span data-ttu-id="1a4ae-125">System.String</span><span class="sxs-lookup"><span data-stu-id="1a4ae-125">System.String</span></span>

## <span data-ttu-id="1a4ae-126">출력</span><span class="sxs-lookup"><span data-stu-id="1a4ae-126">OUTPUTS</span></span>

### <span data-ttu-id="1a4ae-127">System.Void</span><span class="sxs-lookup"><span data-stu-id="1a4ae-127">System.Void</span></span>

## <span data-ttu-id="1a4ae-128">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1a4ae-128">NOTES</span></span>

## <span data-ttu-id="1a4ae-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1a4ae-129">RELATED LINKS</span></span>

[<span data-ttu-id="1a4ae-130">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1a4ae-130">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="1a4ae-131">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="1a4ae-131">Remove-AzDataLakeAnalyticsDataSource</span></span>](./Remove-AzDataLakeAnalyticsDataSource.md)


