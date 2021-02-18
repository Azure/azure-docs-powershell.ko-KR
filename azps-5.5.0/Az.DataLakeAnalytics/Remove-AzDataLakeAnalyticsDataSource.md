---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100180924"
---
# <span data-ttu-id="5d64b-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5d64b-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="5d64b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5d64b-102">SYNOPSIS</span></span>
<span data-ttu-id="5d64b-103">Data Lake Analytics 계정에서 데이터 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d64b-104">구문</span><span class="sxs-lookup"><span data-stu-id="5d64b-104">SYNTAX</span></span>

### <span data-ttu-id="5d64b-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d64b-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="5d64b-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="5d64b-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="5d64b-107">설명</span><span class="sxs-lookup"><span data-stu-id="5d64b-107">DESCRIPTION</span></span>
<span data-ttu-id="5d64b-108">**Remove-AzDataLakeAnalyticsDataSource** cmdlet은 Azure Data Lake Analytics 계정에서 데이터 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="5d64b-109">예제</span><span class="sxs-lookup"><span data-stu-id="5d64b-109">EXAMPLES</span></span>

### <span data-ttu-id="5d64b-110">예제 1: 데이터 원본 제거</span><span class="sxs-lookup"><span data-stu-id="5d64b-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="5d64b-111">이 명령은 ContosoAdlAccount라는 계정에서 AzureStorage01이라는 데이터 원본을 제거합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="5d64b-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="5d64b-112">PARAMETERS</span></span>

### <span data-ttu-id="5d64b-113">-Account</span><span class="sxs-lookup"><span data-stu-id="5d64b-113">-Account</span></span>
<span data-ttu-id="5d64b-114">Data Lake Analytics 계정 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="5d64b-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="5d64b-115">-Blob</span></span>
<span data-ttu-id="5d64b-116">제거할 AzureBlob Storage 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveBlobStorageAccount
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="5d64b-117">-DataLakeStore</span></span>
<span data-ttu-id="5d64b-118">제거할 AzureData Lake Store 계정의 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: RemoveDataLakeStorageAccount
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5d64b-119">-DefaultProfile</span></span>
<span data-ttu-id="5d64b-120">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독</span><span class="sxs-lookup"><span data-stu-id="5d64b-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="5d64b-121">-Force</span><span class="sxs-lookup"><span data-stu-id="5d64b-121">-Force</span></span>
<span data-ttu-id="5d64b-122">사용자 확인을 요청하지 않고 명령을 강제로 실행합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-122">Forces the command to run without asking for user confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="5d64b-123">-PassThru</span></span>
<span data-ttu-id="5d64b-124">작업하는 항목을 나타내는 개체를 반환합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="5d64b-125">기본적으로 이 cmdlet은 출력을 생성하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-125">By default, this cmdlet does not generate any output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="5d64b-126">-ResourceGroupName</span></span>
<span data-ttu-id="5d64b-127">Data Lake Analytics 계정의 리소스 그룹 이름을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-128">-Confirm</span><span class="sxs-lookup"><span data-stu-id="5d64b-128">-Confirm</span></span>
<span data-ttu-id="5d64b-129">cmdlet을 실행하기 전에 확인 메시지가 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-129">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="5d64b-130">-WhatIf</span></span>
<span data-ttu-id="5d64b-131">cmdlet이 실행되는 경우의 결과 표시</span><span class="sxs-lookup"><span data-stu-id="5d64b-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="5d64b-132">cmdlet이 실행되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-132">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5d64b-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5d64b-133">CommonParameters</span></span>
<span data-ttu-id="5d64b-134">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="5d64b-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5d64b-135">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="5d64b-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5d64b-136">입력</span><span class="sxs-lookup"><span data-stu-id="5d64b-136">INPUTS</span></span>

### <span data-ttu-id="5d64b-137">System.String</span><span class="sxs-lookup"><span data-stu-id="5d64b-137">System.String</span></span>

## <span data-ttu-id="5d64b-138">출력</span><span class="sxs-lookup"><span data-stu-id="5d64b-138">OUTPUTS</span></span>

### <span data-ttu-id="5d64b-139">System.Boolean</span><span class="sxs-lookup"><span data-stu-id="5d64b-139">System.Boolean</span></span>

## <span data-ttu-id="5d64b-140">참고 사항</span><span class="sxs-lookup"><span data-stu-id="5d64b-140">NOTES</span></span>

## <span data-ttu-id="5d64b-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="5d64b-141">RELATED LINKS</span></span>

[<span data-ttu-id="5d64b-142">Add-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5d64b-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="5d64b-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="5d64b-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


