---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 4d671e99ed8b5c26b98b8e224728785e034e450b
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93698530"
---
# <span data-ttu-id="296db-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="296db-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="296db-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="296db-102">SYNOPSIS</span></span>
<span data-ttu-id="296db-103">Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="296db-104">구문과</span><span class="sxs-lookup"><span data-stu-id="296db-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="296db-105">설명은</span><span class="sxs-lookup"><span data-stu-id="296db-105">DESCRIPTION</span></span>
<span data-ttu-id="296db-106">**AzStorageServiceLoggingProperty** Cmdlet은 Azure Storage 서비스에 대 한 로깅을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="296db-107">예제의</span><span class="sxs-lookup"><span data-stu-id="296db-107">EXAMPLES</span></span>

### <span data-ttu-id="296db-108">예제 1: Blob 서비스에 대 한 로깅 속성 수정</span><span class="sxs-lookup"><span data-stu-id="296db-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="296db-109">이 명령은 blob 저장소에 대 한 버전 1.0 로깅을 수정 하 여 읽기 및 쓰기 작업을 포함 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="296db-110">Azure 저장소 서비스 로깅은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="296db-111">이 명령은 *PassThru* 매개 변수를 지정 하므로,이 명령은 수정 된 로깅 속성을 표시 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="296db-112">변수</span><span class="sxs-lookup"><span data-stu-id="296db-112">PARAMETERS</span></span>

### <span data-ttu-id="296db-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="296db-113">-Context</span></span>
<span data-ttu-id="296db-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="296db-115">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="296db-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="296db-116">-DefaultProfile</span></span>
<span data-ttu-id="296db-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="296db-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="296db-118">-LoggingOperations</span></span>
<span data-ttu-id="296db-119">Azure 저장소 서비스 작업의 배열을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="296db-120">Azure 저장소 서비스는이 매개 변수에서 지정 하는 작업을 기록 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="296db-121">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="296db-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="296db-122">않아야</span><span class="sxs-lookup"><span data-stu-id="296db-122">None</span></span>
- <span data-ttu-id="296db-123">자세한</span><span class="sxs-lookup"><span data-stu-id="296db-123">Read</span></span>
- <span data-ttu-id="296db-124">작성</span><span class="sxs-lookup"><span data-stu-id="296db-124">Write</span></span>
- <span data-ttu-id="296db-125">삭제</span><span class="sxs-lookup"><span data-stu-id="296db-125">Delete</span></span>
- <span data-ttu-id="296db-126">모든</span><span class="sxs-lookup"><span data-stu-id="296db-126">All</span></span>

```yaml
Type: Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="296db-127">-PassThru</span></span>
<span data-ttu-id="296db-128">이 cmdlet이 업데이트 된 로깅 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="296db-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="296db-129">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="296db-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-130">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="296db-130">-RetentionDays</span></span>
<span data-ttu-id="296db-131">Azure 저장소 서비스에서 기록 된 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

```yaml
Type: System.Nullable`1[System.Int32]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="296db-132">-ServiceType</span></span>
<span data-ttu-id="296db-133">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-133">Specifies the storage service type.</span></span>
<span data-ttu-id="296db-134">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형에 대 한 로깅 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="296db-135">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="296db-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="296db-136">블</span><span class="sxs-lookup"><span data-stu-id="296db-136">Blob</span></span> 
- <span data-ttu-id="296db-137">테이블로</span><span class="sxs-lookup"><span data-stu-id="296db-137">Table</span></span>
- <span data-ttu-id="296db-138">전담팀</span><span class="sxs-lookup"><span data-stu-id="296db-138">Queue</span></span>
- <span data-ttu-id="296db-139">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="296db-139">File The value of File is not currently supported.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.StorageServiceType
Parameter Sets: (All)
Aliases:
Accepted values: Blob, Table, Queue, File

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-140">-버전</span><span class="sxs-lookup"><span data-stu-id="296db-140">-Version</span></span>
<span data-ttu-id="296db-141">Azure 저장소 서비스 로깅 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="296db-142">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="296db-142">The default value is 1.0.</span></span>

```yaml
Type: System.Nullable`1[System.Double]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="296db-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="296db-143">CommonParameters</span></span>
<span data-ttu-id="296db-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="296db-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="296db-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="296db-146">입력</span><span class="sxs-lookup"><span data-stu-id="296db-146">INPUTS</span></span>

### <span data-ttu-id="296db-147">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="296db-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="296db-148">출력</span><span class="sxs-lookup"><span data-stu-id="296db-148">OUTPUTS</span></span>

### <span data-ttu-id="296db-149">WindowsAzure. LoggingProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="296db-149">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="296db-150">상속자</span><span class="sxs-lookup"><span data-stu-id="296db-150">NOTES</span></span>

## <span data-ttu-id="296db-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="296db-151">RELATED LINKS</span></span>

[<span data-ttu-id="296db-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="296db-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="296db-153">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="296db-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


