---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataLakeAnalytics.dll-Help.xml
Module Name: Az.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: https://docs.microsoft.com/en-us/powershell/module/az.datalakeanalytics/remove-azdatalakeanalyticsdatasource
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataLakeAnalytics/DataLakeAnalytics/help/Remove-AzDataLakeAnalyticsDataSource.md
ms.openlocfilehash: dfdd338fd5b49813d17e089755b419605761af3a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94305786"
---
# <span data-ttu-id="28cdd-101">Remove-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28cdd-101">Remove-AzDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="28cdd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="28cdd-102">SYNOPSIS</span></span>
<span data-ttu-id="28cdd-103">Data Lake Analytics 계정에서 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-103">Removes a data source from a Data Lake Analytics account.</span></span>

## <span data-ttu-id="28cdd-104">구문과</span><span class="sxs-lookup"><span data-stu-id="28cdd-104">SYNTAX</span></span>

### <span data-ttu-id="28cdd-105">RemoveDataLakeStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28cdd-105">RemoveDataLakeStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="28cdd-106">RemoveBlobStorageAccount</span><span class="sxs-lookup"><span data-stu-id="28cdd-106">RemoveBlobStorageAccount</span></span>
```
Remove-AzDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="28cdd-107">설명은</span><span class="sxs-lookup"><span data-stu-id="28cdd-107">DESCRIPTION</span></span>
<span data-ttu-id="28cdd-108">**AzDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정에서 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-108">The **Remove-AzDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="28cdd-109">예제의</span><span class="sxs-lookup"><span data-stu-id="28cdd-109">EXAMPLES</span></span>

### <span data-ttu-id="28cdd-110">예제 1: 데이터 원본 제거</span><span class="sxs-lookup"><span data-stu-id="28cdd-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="28cdd-111">이 명령은 ContosoAdlAccount 이라는 계정에서 AzureStorage01 이라는 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="28cdd-112">변수</span><span class="sxs-lookup"><span data-stu-id="28cdd-112">PARAMETERS</span></span>

### <span data-ttu-id="28cdd-113">-계정</span><span class="sxs-lookup"><span data-stu-id="28cdd-113">-Account</span></span>
<span data-ttu-id="28cdd-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="28cdd-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="28cdd-115">-Blob</span></span>
<span data-ttu-id="28cdd-116">제거할 AzureBlob 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

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

### <span data-ttu-id="28cdd-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="28cdd-117">-DataLakeStore</span></span>
<span data-ttu-id="28cdd-118">제거할 AzureData Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

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

### <span data-ttu-id="28cdd-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="28cdd-119">-DefaultProfile</span></span>
<span data-ttu-id="28cdd-120">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독</span><span class="sxs-lookup"><span data-stu-id="28cdd-120">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="28cdd-121">-Force</span><span class="sxs-lookup"><span data-stu-id="28cdd-121">-Force</span></span>
<span data-ttu-id="28cdd-122">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-122">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="28cdd-123">-PassThru</span><span class="sxs-lookup"><span data-stu-id="28cdd-123">-PassThru</span></span>
<span data-ttu-id="28cdd-124">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-124">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="28cdd-125">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-125">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="28cdd-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="28cdd-126">-ResourceGroupName</span></span>
<span data-ttu-id="28cdd-127">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-127">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="28cdd-128">-확인</span><span class="sxs-lookup"><span data-stu-id="28cdd-128">-Confirm</span></span>
<span data-ttu-id="28cdd-129">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="28cdd-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="28cdd-130">-WhatIf</span></span>
<span data-ttu-id="28cdd-131">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="28cdd-132">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="28cdd-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="28cdd-133">CommonParameters</span></span>
<span data-ttu-id="28cdd-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="28cdd-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="28cdd-135">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="28cdd-135">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="28cdd-136">입력</span><span class="sxs-lookup"><span data-stu-id="28cdd-136">INPUTS</span></span>

### <span data-ttu-id="28cdd-137">System. 문자열</span><span class="sxs-lookup"><span data-stu-id="28cdd-137">System.String</span></span>

## <span data-ttu-id="28cdd-138">출력</span><span class="sxs-lookup"><span data-stu-id="28cdd-138">OUTPUTS</span></span>

### <span data-ttu-id="28cdd-139">시스템 부울</span><span class="sxs-lookup"><span data-stu-id="28cdd-139">System.Boolean</span></span>

## <span data-ttu-id="28cdd-140">상속자</span><span class="sxs-lookup"><span data-stu-id="28cdd-140">NOTES</span></span>

## <span data-ttu-id="28cdd-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="28cdd-141">RELATED LINKS</span></span>

[<span data-ttu-id="28cdd-142">추가-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28cdd-142">Add-AzDataLakeAnalyticsDataSource</span></span>](./Add-AzDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="28cdd-143">Set-AzDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="28cdd-143">Set-AzDataLakeAnalyticsDataSource</span></span>](./Set-AzDataLakeAnalyticsDataSource.md)


