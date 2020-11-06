---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: ''
schema: 2.0.0
ms.openlocfilehash: dd1acb41a6f67fb281500ad8a0d37cb3c2e0a6dd
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524128"
---
# <span data-ttu-id="9e94c-101">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9e94c-101">Set-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="9e94c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9e94c-102">SYNOPSIS</span></span>
<span data-ttu-id="9e94c-103">Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="9e94c-104">구문과</span><span class="sxs-lookup"><span data-stu-id="9e94c-104">SYNTAX</span></span>

```
Set-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="9e94c-105">설명은</span><span class="sxs-lookup"><span data-stu-id="9e94c-105">DESCRIPTION</span></span>
<span data-ttu-id="9e94c-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-106">The **Set-AzureStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="9e94c-107">예제의</span><span class="sxs-lookup"><span data-stu-id="9e94c-107">EXAMPLES</span></span>

### <span data-ttu-id="9e94c-108">예제 1: Blob 서비스에 대 한 로깅 속성 수정</span><span class="sxs-lookup"><span data-stu-id="9e94c-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="9e94c-109">이 명령은 blob 저장소에 대 한 버전 1.0 로깅을 수정 하 여 읽기 및 쓰기 작업을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="9e94c-110">Azure 저장소 서비스 로깅은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="9e94c-111">이 명령은 *PassThru* 매개 변수를 지정 하므로,이 명령은 수정 된 로깅 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="9e94c-112">변수</span><span class="sxs-lookup"><span data-stu-id="9e94c-112">PARAMETERS</span></span>

### <span data-ttu-id="9e94c-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="9e94c-113">-Context</span></span>
<span data-ttu-id="9e94c-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="9e94c-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="9e94c-116">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="9e94c-116">-LoggingOperations</span></span>
<span data-ttu-id="9e94c-117">Azure 저장소 서비스 작업의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-117">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="9e94c-118">Azure 저장소 서비스는이 매개 변수에서 지정 하는 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-118">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="9e94c-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-119">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94c-120">않아야</span><span class="sxs-lookup"><span data-stu-id="9e94c-120">None</span></span>
- <span data-ttu-id="9e94c-121">자세한</span><span class="sxs-lookup"><span data-stu-id="9e94c-121">Read</span></span>
- <span data-ttu-id="9e94c-122">작성</span><span class="sxs-lookup"><span data-stu-id="9e94c-122">Write</span></span>
- <span data-ttu-id="9e94c-123">삭제</span><span class="sxs-lookup"><span data-stu-id="9e94c-123">Delete</span></span>
- <span data-ttu-id="9e94c-124">모든</span><span class="sxs-lookup"><span data-stu-id="9e94c-124">All</span></span>

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

### <span data-ttu-id="9e94c-125">-PassThru</span><span class="sxs-lookup"><span data-stu-id="9e94c-125">-PassThru</span></span>
<span data-ttu-id="9e94c-126">이 cmdlet이 업데이트 된 로깅 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-126">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="9e94c-127">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-127">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="9e94c-128">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="9e94c-128">-RetentionDays</span></span>
<span data-ttu-id="9e94c-129">Azure 저장소 서비스에서 기록 된 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-129">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="9e94c-130">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="9e94c-130">-ServiceType</span></span>
<span data-ttu-id="9e94c-131">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-131">Specifies the storage service type.</span></span>
<span data-ttu-id="9e94c-132">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형에 대 한 로깅 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-132">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="9e94c-133">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-133">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="9e94c-134">블</span><span class="sxs-lookup"><span data-stu-id="9e94c-134">Blob</span></span> 
- <span data-ttu-id="9e94c-135">테이블로</span><span class="sxs-lookup"><span data-stu-id="9e94c-135">Table</span></span>
- <span data-ttu-id="9e94c-136">전담팀</span><span class="sxs-lookup"><span data-stu-id="9e94c-136">Queue</span></span>
- <span data-ttu-id="9e94c-137">파일</span><span class="sxs-lookup"><span data-stu-id="9e94c-137">File</span></span>

<span data-ttu-id="9e94c-138">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-138">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="9e94c-139">-버전</span><span class="sxs-lookup"><span data-stu-id="9e94c-139">-Version</span></span>
<span data-ttu-id="9e94c-140">Azure 저장소 서비스 로깅 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-140">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="9e94c-141">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-141">The default value is 1.0.</span></span>

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

### <span data-ttu-id="9e94c-142">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9e94c-142">CommonParameters</span></span>
<span data-ttu-id="9e94c-143">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="9e94c-143">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9e94c-144">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9e94c-144">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9e94c-145">입력</span><span class="sxs-lookup"><span data-stu-id="9e94c-145">INPUTS</span></span>

## <span data-ttu-id="9e94c-146">출력</span><span class="sxs-lookup"><span data-stu-id="9e94c-146">OUTPUTS</span></span>

## <span data-ttu-id="9e94c-147">상속자</span><span class="sxs-lookup"><span data-stu-id="9e94c-147">NOTES</span></span>

## <span data-ttu-id="9e94c-148">관련 링크</span><span class="sxs-lookup"><span data-stu-id="9e94c-148">RELATED LINKS</span></span>

[<span data-ttu-id="9e94c-149">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="9e94c-149">Get-AzureStorageServiceLoggingProperty</span></span>](./Get-AzureStorageServiceLoggingProperty.md)

[<span data-ttu-id="9e94c-150">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="9e94c-150">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


