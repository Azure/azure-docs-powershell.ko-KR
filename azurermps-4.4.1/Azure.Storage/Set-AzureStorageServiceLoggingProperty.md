---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: baba161c849918c95d5e1df91330dfd96a4c5629
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535571"
---
# <span data-ttu-id="2fa10-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2fa10-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="2fa10-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2fa10-102">SYNOPSIS</span></span>
<span data-ttu-id="2fa10-103">Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-103">Modifies logging for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2fa10-104">구문과</span><span class="sxs-lookup"><span data-stu-id="2fa10-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="2fa10-105">설명은</span><span class="sxs-lookup"><span data-stu-id="2fa10-105">DESCRIPTION</span></span>
<span data-ttu-id="2fa10-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="2fa10-107">예제의</span><span class="sxs-lookup"><span data-stu-id="2fa10-107">EXAMPLES</span></span>

### <span data-ttu-id="2fa10-108">예제 1: Blob 서비스에 대 한 로깅 속성 수정</span><span class="sxs-lookup"><span data-stu-id="2fa10-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="2fa10-109">이 명령은 blob 저장소에 대 한 버전 1.0 로깅을 수정 하 여 읽기 및 쓰기 작업을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="2fa10-110">Azure 저장소 서비스 로깅은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="2fa10-111">이 명령은 *PassThru* 매개 변수를 지정 하므로,이 명령은 수정 된 로깅 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="2fa10-112">변수</span><span class="sxs-lookup"><span data-stu-id="2fa10-112">PARAMETERS</span></span>

### <span data-ttu-id="2fa10-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="2fa10-113">-Context</span></span>
<span data-ttu-id="2fa10-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="2fa10-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

```yaml
Type: IStorageContext
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="2fa10-116">-LoggingOperations</span></span>
<span data-ttu-id="2fa10-117">Azure 저장소 서비스 작업의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="2fa10-118">Azure 저장소 서비스는이 매개 변수에서 지정 하는 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="2fa10-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fa10-120">않아야</span><span class="sxs-lookup"><span data-stu-id="2fa10-120">None</span></span>
- <span data-ttu-id="2fa10-121">자세한</span><span class="sxs-lookup"><span data-stu-id="2fa10-121">Read</span></span>
- <span data-ttu-id="2fa10-122">작성</span><span class="sxs-lookup"><span data-stu-id="2fa10-122">Write</span></span>
- <span data-ttu-id="2fa10-123">삭제</span><span class="sxs-lookup"><span data-stu-id="2fa10-123">Delete</span></span>
- <span data-ttu-id="2fa10-124">모든</span><span class="sxs-lookup"><span data-stu-id="2fa10-124">All</span></span>

```yaml
Type: LoggingOperations[]
Parameter Sets: (All)
Aliases: 
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="2fa10-125">-PassThru</span></span>
<span data-ttu-id="2fa10-126">이 cmdlet이 업데이트 된 로깅 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="2fa10-127">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-128">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="2fa10-128">-RetentionDays</span></span>
<span data-ttu-id="2fa10-129">Azure 저장소 서비스에서 기록 된 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: Int32
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="2fa10-130">-ServiceType</span></span>
<span data-ttu-id="2fa10-131">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-131">Specifies the storage service type.</span></span>
<span data-ttu-id="2fa10-132">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형에 대 한 로깅 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="2fa10-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="2fa10-134">블</span><span class="sxs-lookup"><span data-stu-id="2fa10-134">Blob</span></span> 
- <span data-ttu-id="2fa10-135">테이블로</span><span class="sxs-lookup"><span data-stu-id="2fa10-135">Table</span></span>
- <span data-ttu-id="2fa10-136">전담팀</span><span class="sxs-lookup"><span data-stu-id="2fa10-136">Queue</span></span>
- <span data-ttu-id="2fa10-137">파일</span><span class="sxs-lookup"><span data-stu-id="2fa10-137">File</span></span>

<span data-ttu-id="2fa10-138">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-138">The value of File is not currently supported.</span></span>

```yaml
Type: StorageServiceType
Parameter Sets: (All)
Aliases: 
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-139">-버전</span><span class="sxs-lookup"><span data-stu-id="2fa10-139">-Version</span></span>
<span data-ttu-id="2fa10-140">Azure 저장소 서비스 로깅 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="2fa10-141">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-141">The default value is 1.0.</span></span>

```yaml
Type: Double
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="2fa10-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2fa10-142">CommonParameters</span></span>
<span data-ttu-id="2fa10-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2fa10-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2fa10-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2fa10-145">입력</span><span class="sxs-lookup"><span data-stu-id="2fa10-145">INPUTS</span></span>

### <span data-ttu-id="2fa10-146">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fa10-146">IStorageContext</span></span>

<span data-ttu-id="2fa10-147">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-147">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="2fa10-148">출력</span><span class="sxs-lookup"><span data-stu-id="2fa10-148">OUTPUTS</span></span>

### <span data-ttu-id="2fa10-149">WindowsAzure. LoggingProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="2fa10-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="2fa10-150">상속자</span><span class="sxs-lookup"><span data-stu-id="2fa10-150">NOTES</span></span>

## <span data-ttu-id="2fa10-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="2fa10-151">RELATED LINKS</span></span>

[<span data-ttu-id="2fa10-152">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="2fa10-152">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="2fa10-153">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="2fa10-153">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


