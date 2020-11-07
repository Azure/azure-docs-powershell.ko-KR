---
external help file: Microsoft.Azure.Commands.DataLakeAnalytics.dll-Help.xml
Module Name: AzureRM.DataLakeAnalytics
ms.assetid: E0E2617F-F6F1-434E-AD7C-27D309C2C3DA
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataLakeAnalytics/Commands.DataLakeAnalytics/help/Remove-AzureRmDataLakeAnalyticsDataSource.md
ms.openlocfilehash: 9b0e4b5da6ecd2877bab5860179cbaed80f43911
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93703772"
---
# <span data-ttu-id="948f1-101">Remove-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="948f1-101">Remove-AzureRmDataLakeAnalyticsDataSource</span></span>

## <span data-ttu-id="948f1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="948f1-102">SYNOPSIS</span></span>
<span data-ttu-id="948f1-103">Data Lake Analytics 계정에서 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-103">Removes a data source from a Data Lake Analytics account.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="948f1-104">구문과</span><span class="sxs-lookup"><span data-stu-id="948f1-104">SYNTAX</span></span>

### <span data-ttu-id="948f1-105">Data Lake storage 계정 제거</span><span class="sxs-lookup"><span data-stu-id="948f1-105">Remove a Data Lake storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-DataLakeStore] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="948f1-106">Blob 저장소 계정 제거</span><span class="sxs-lookup"><span data-stu-id="948f1-106">Remove a Blob storage account</span></span>
```
Remove-AzureRmDataLakeAnalyticsDataSource [-Account] <String> [-Blob] <String> [-Force] [-PassThru]
 [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="948f1-107">설명은</span><span class="sxs-lookup"><span data-stu-id="948f1-107">DESCRIPTION</span></span>
<span data-ttu-id="948f1-108">**AzureRmDataLakeAnalyticsDataSource** Cmdlet은 Azure Data Lake Analytics 계정에서 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-108">The **Remove-AzureRmDataLakeAnalyticsDataSource** cmdlet removes a data source from an Azure Data Lake Analytics account.</span></span>

## <span data-ttu-id="948f1-109">예제의</span><span class="sxs-lookup"><span data-stu-id="948f1-109">EXAMPLES</span></span>

### <span data-ttu-id="948f1-110">예제 1: 데이터 원본 제거</span><span class="sxs-lookup"><span data-stu-id="948f1-110">Example 1: Remove a data source</span></span>
```
PS C:\>Remove-AzureRmDataLakeAnalyticsDataSource -Account "ContosoAdlAccount" -Blob "AzureStorage01"
```

<span data-ttu-id="948f1-111">이 명령은 ContosoAdlAccount 이라는 계정에서 AzureStorage01 이라는 데이터 원본을 제거 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-111">This command removes the data source named AzureStorage01 from the account named ContosoAdlAccount.</span></span>

## <span data-ttu-id="948f1-112">변수</span><span class="sxs-lookup"><span data-stu-id="948f1-112">PARAMETERS</span></span>

### <span data-ttu-id="948f1-113">-계정</span><span class="sxs-lookup"><span data-stu-id="948f1-113">-Account</span></span>
<span data-ttu-id="948f1-114">Data Lake Analytics 계정 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-114">Specifies the Data Lake Analytics account name.</span></span>

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

### <span data-ttu-id="948f1-115">-Blob</span><span class="sxs-lookup"><span data-stu-id="948f1-115">-Blob</span></span>
<span data-ttu-id="948f1-116">제거할 AzureBlob 저장소 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-116">Specifies the name of the AzureBlob Storage account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Blob storage account
Aliases: AzureBlob

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f1-117">-DataLakeStore</span><span class="sxs-lookup"><span data-stu-id="948f1-117">-DataLakeStore</span></span>
<span data-ttu-id="948f1-118">제거할 AzureData Lake Store 계정의 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-118">Specifies the name of the AzureData Lake Store account to remove.</span></span>

```yaml
Type: System.String
Parameter Sets: Remove a Data Lake storage account
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="948f1-119">-Force</span><span class="sxs-lookup"><span data-stu-id="948f1-119">-Force</span></span>
<span data-ttu-id="948f1-120">사용자 확인을 요청 하지 않고 명령을 강제로 실행 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-120">Forces the command to run without asking for user confirmation.</span></span>

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

### <span data-ttu-id="948f1-121">-PassThru</span><span class="sxs-lookup"><span data-stu-id="948f1-121">-PassThru</span></span>
<span data-ttu-id="948f1-122">작업 중인 항목을 나타내는 개체를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-122">Returns an object representing the item with which you are working.</span></span>
<span data-ttu-id="948f1-123">기본적으로이 cmdlet은 출력을 생성 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-123">By default, this cmdlet does not generate any output.</span></span>

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

### <span data-ttu-id="948f1-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="948f1-124">-ResourceGroupName</span></span>
<span data-ttu-id="948f1-125">Data Lake Analytics 계정의 리소스 그룹 이름을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-125">Specifies the resource group name of the Data Lake Analytics account.</span></span>

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

### <span data-ttu-id="948f1-126">-확인</span><span class="sxs-lookup"><span data-stu-id="948f1-126">-Confirm</span></span>
<span data-ttu-id="948f1-127">Cmdlet을 실행 하기 전에 확인 메시지를 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="948f1-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="948f1-128">-WhatIf</span></span>
<span data-ttu-id="948f1-129">Cmdlet이 실행 되는 경우의 동작을 보여 줍니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="948f1-130">Cmdlet이 실행 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="948f1-131">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="948f1-131">-DefaultProfile</span></span>
<span data-ttu-id="948f1-132">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-132">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="948f1-133">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="948f1-133">CommonParameters</span></span>
<span data-ttu-id="948f1-134">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-134">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="948f1-135">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="948f1-135">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="948f1-136">입력</span><span class="sxs-lookup"><span data-stu-id="948f1-136">INPUTS</span></span>

## <span data-ttu-id="948f1-137">출력</span><span class="sxs-lookup"><span data-stu-id="948f1-137">OUTPUTS</span></span>

### <span data-ttu-id="948f1-138">부울</span><span class="sxs-lookup"><span data-stu-id="948f1-138">bool</span></span>
<span data-ttu-id="948f1-139">PassThru가 지정 된 경우 작업이 완료 되 면 true를 반환 합니다.</span><span class="sxs-lookup"><span data-stu-id="948f1-139">If PassThru is specified, returns true upon completion of the operation.</span></span>

## <span data-ttu-id="948f1-140">상속자</span><span class="sxs-lookup"><span data-stu-id="948f1-140">NOTES</span></span>

## <span data-ttu-id="948f1-141">관련 링크</span><span class="sxs-lookup"><span data-stu-id="948f1-141">RELATED LINKS</span></span>

[<span data-ttu-id="948f1-142">추가-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="948f1-142">Add-AzureRmDataLakeAnalyticsDataSource</span></span>](./Add-AzureRmDataLakeAnalyticsDataSource.md)

[<span data-ttu-id="948f1-143">Set-AzureRmDataLakeAnalyticsDataSource</span><span class="sxs-lookup"><span data-stu-id="948f1-143">Set-AzureRmDataLakeAnalyticsDataSource</span></span>](./Set-AzureRmDataLakeAnalyticsDataSource.md)


