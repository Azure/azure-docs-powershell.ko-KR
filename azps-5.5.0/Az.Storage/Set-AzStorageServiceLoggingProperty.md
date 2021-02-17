---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5422429E-C609-4C1F-A021-E2A085B5F74E
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceLoggingProperty.md
ms.openlocfilehash: 21c182dff12f8dd373000a295f964bd59484e337
ms.sourcegitcommit: c05d3d669b5631e526841f47b22513d78495350b
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 02/09/2021
ms.locfileid: "100207725"
---
# <span data-ttu-id="1b733-101">Set-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1b733-101">Set-AzStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="1b733-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1b733-102">SYNOPSIS</span></span>
<span data-ttu-id="1b733-103">Azure Storage 서비스에 대한 로깅을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-103">Modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1b733-104">구문</span><span class="sxs-lookup"><span data-stu-id="1b733-104">SYNTAX</span></span>

```
Set-AzStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Version <Double>]
 [-RetentionDays <Int32>] [-LoggingOperations <LoggingOperations[]>] [-PassThru] [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1b733-105">설명</span><span class="sxs-lookup"><span data-stu-id="1b733-105">DESCRIPTION</span></span>
<span data-ttu-id="1b733-106">**Set-AzStorageServiceLoggingProperty** cmdlet은 Azure Storage 서비스에 대한 로깅을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-106">The **Set-AzStorageServiceLoggingProperty** cmdlet modifies logging for Azure Storage services.</span></span>

## <span data-ttu-id="1b733-107">예제</span><span class="sxs-lookup"><span data-stu-id="1b733-107">EXAMPLES</span></span>

### <span data-ttu-id="1b733-108">예제 1: Blob service에 대한 로깅 속성 수정</span><span class="sxs-lookup"><span data-stu-id="1b733-108">Example 1: Modify logging properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceLoggingProperty -ServiceType Blob -LoggingOperations Read,Write -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="1b733-109">이 명령은 읽기 및 쓰기 작업을 포함하기 위해 Blob Storage에 대한 버전 1.0 로깅을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-109">This command modifies version 1.0 logging for blob storage to include read and write operations.</span></span>
<span data-ttu-id="1b733-110">Azure Storage 서비스 로깅은 10일 동안 항목을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-110">Azure Storage service logging retains entries for 10 days.</span></span>
<span data-ttu-id="1b733-111">이 명령은 *PassThru* 매개 변수를 지정하기 때문에 명령에 수정된 로깅 속성이 표시됩니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-111">Because this command specifies the *PassThru* parameter, the command displays the modified logging properties.</span></span>

## <span data-ttu-id="1b733-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="1b733-112">PARAMETERS</span></span>

### <span data-ttu-id="1b733-113">-Context</span><span class="sxs-lookup"><span data-stu-id="1b733-113">-Context</span></span>
<span data-ttu-id="1b733-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1b733-115">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1b733-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1b733-116">-DefaultProfile</span></span>
<span data-ttu-id="1b733-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1b733-118">-LoggingOperations</span><span class="sxs-lookup"><span data-stu-id="1b733-118">-LoggingOperations</span></span>
<span data-ttu-id="1b733-119">Azure Storage 서비스 작업의 배열을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-119">Specifies an array of Azure Storage service operations.</span></span>
<span data-ttu-id="1b733-120">Azure Storage 서비스는 이 매개 변수가 지정하는 작업을 기록합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-120">Azure Storage services logs the operations that this parameter specifies.</span></span>
<span data-ttu-id="1b733-121">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1b733-121">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b733-122">없음</span><span class="sxs-lookup"><span data-stu-id="1b733-122">None</span></span>
- <span data-ttu-id="1b733-123">읽기</span><span class="sxs-lookup"><span data-stu-id="1b733-123">Read</span></span>
- <span data-ttu-id="1b733-124">쓰기</span><span class="sxs-lookup"><span data-stu-id="1b733-124">Write</span></span>
- <span data-ttu-id="1b733-125">삭제</span><span class="sxs-lookup"><span data-stu-id="1b733-125">Delete</span></span>
- <span data-ttu-id="1b733-126">모두</span><span class="sxs-lookup"><span data-stu-id="1b733-126">All</span></span>

```yaml
Type: Microsoft.Azure.Storage.Shared.Protocol.LoggingOperations[]
Parameter Sets: (All)
Aliases:
Accepted values: None, Read, Write, Delete, All

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="1b733-127">-PassThru</span><span class="sxs-lookup"><span data-stu-id="1b733-127">-PassThru</span></span>
<span data-ttu-id="1b733-128">이 cmdlet이 업데이트된 로깅 속성을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-128">Indicates that this cmdlet returns the updated logging properties.</span></span>
<span data-ttu-id="1b733-129">이 매개 변수를 지정하지 않으면 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-129">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="1b733-130">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="1b733-130">-RetentionDays</span></span>
<span data-ttu-id="1b733-131">Azure Storage 서비스가 기록된 정보를 유지하는 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-131">Specifies the number of days that the Azure Storage service retains logged information.</span></span>

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

### <span data-ttu-id="1b733-132">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1b733-132">-ServiceType</span></span>
<span data-ttu-id="1b733-133">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-133">Specifies the storage service type.</span></span>
<span data-ttu-id="1b733-134">이 cmdlet은 이 매개 변수가 지정하는 서비스 형식에 대한 로깅 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-134">This cmdlet modifies the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1b733-135">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="1b733-135">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1b733-136">Blob</span><span class="sxs-lookup"><span data-stu-id="1b733-136">Blob</span></span> 
- <span data-ttu-id="1b733-137">표</span><span class="sxs-lookup"><span data-stu-id="1b733-137">Table</span></span>
- <span data-ttu-id="1b733-138">큐</span><span class="sxs-lookup"><span data-stu-id="1b733-138">Queue</span></span>
- <span data-ttu-id="1b733-139">파일 값은 현재 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-139">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="1b733-140">-Version</span><span class="sxs-lookup"><span data-stu-id="1b733-140">-Version</span></span>
<span data-ttu-id="1b733-141">Azure Storage 서비스 로깅의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-141">Specifies the version of the Azure Storage service logging.</span></span>
<span data-ttu-id="1b733-142">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="1b733-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1b733-143">CommonParameters</span></span>
<span data-ttu-id="1b733-144">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="1b733-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1b733-145">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="1b733-145">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1b733-146">입력</span><span class="sxs-lookup"><span data-stu-id="1b733-146">INPUTS</span></span>

### <span data-ttu-id="1b733-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b733-147">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1b733-148">출력</span><span class="sxs-lookup"><span data-stu-id="1b733-148">OUTPUTS</span></span>

### <span data-ttu-id="1b733-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span><span class="sxs-lookup"><span data-stu-id="1b733-149">Microsoft.Azure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="1b733-150">참고 사항</span><span class="sxs-lookup"><span data-stu-id="1b733-150">NOTES</span></span>

## <span data-ttu-id="1b733-151">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1b733-151">RELATED LINKS</span></span>

[<span data-ttu-id="1b733-152">Get-AzStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1b733-152">Get-AzStorageServiceLoggingProperty</span></span>](./Get-AzStorageServiceLoggingProperty.md)

[<span data-ttu-id="1b733-153">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="1b733-153">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


