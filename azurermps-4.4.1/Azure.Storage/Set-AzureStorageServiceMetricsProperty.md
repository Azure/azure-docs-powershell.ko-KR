---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Set-AzureStorageServiceMetricsProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: 3f295d42075054d676852c42028dc2e9fd8b82b1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93535563"
---
# <span data-ttu-id="71ba5-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71ba5-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="71ba5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71ba5-102">SYNOPSIS</span></span>
<span data-ttu-id="71ba5-103">Azure 저장소 서비스의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-103">Modifies metrics properties for the Azure Storage service.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="71ba5-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71ba5-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="71ba5-105">설명은</span><span class="sxs-lookup"><span data-stu-id="71ba5-105">DESCRIPTION</span></span>
<span data-ttu-id="71ba5-106">**AzureStorageServiceMetricsProperty** Cmdlet은 Azure 저장소 서비스에 대 한 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="71ba5-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71ba5-107">EXAMPLES</span></span>

### <span data-ttu-id="71ba5-108">예제 1: Blob 서비스에 대 한 메트릭 속성 수정</span><span class="sxs-lookup"><span data-stu-id="71ba5-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="71ba5-109">이 명령은 blob 저장소에 대 한 버전 1.0 메트릭을 서비스 수준으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="71ba5-110">Azure 저장소 서비스 메트릭은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="71ba5-111">이 명령은 *PassThru* 매개 변수를 지정 하므로 명령에 수정 된 메트릭 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="71ba5-112">변수</span><span class="sxs-lookup"><span data-stu-id="71ba5-112">PARAMETERS</span></span>

### <span data-ttu-id="71ba5-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="71ba5-113">-Context</span></span>
<span data-ttu-id="71ba5-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="71ba5-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="71ba5-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="71ba5-116">-MetricsLevel</span></span>
<span data-ttu-id="71ba5-117">Azure Storage가 서비스에 사용 하는 메트릭 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="71ba5-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71ba5-119">않아야</span><span class="sxs-lookup"><span data-stu-id="71ba5-119">None</span></span>
- <span data-ttu-id="71ba5-120">Services</span><span class="sxs-lookup"><span data-stu-id="71ba5-120">Service</span></span>
- <span data-ttu-id="71ba5-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="71ba5-121">ServiceAndApi</span></span>

```yaml
Type: MetricsLevel
Parameter Sets: (All)
Aliases: 
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ba5-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="71ba5-122">-MetricsType</span></span>
<span data-ttu-id="71ba5-123">메트릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-123">Specifies a metrics type.</span></span>
<span data-ttu-id="71ba5-124">이 cmldet는 Azure 저장소 서비스 메트릭 유형을이 매개 변수에서 지정 하는 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="71ba5-125">이 매개 변수에 허용 되는 값은 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: ServiceMetricsType
Parameter Sets: (All)
Aliases: 
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="71ba5-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71ba5-126">-PassThru</span></span>
<span data-ttu-id="71ba5-127">이 cmdlet이 업데이트 된 메트릭 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="71ba5-128">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="71ba5-129">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="71ba5-129">-RetentionDays</span></span>
<span data-ttu-id="71ba5-130">Azure 저장소 서비스에서 메트릭 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="71ba5-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="71ba5-131">-ServiceType</span></span>
<span data-ttu-id="71ba5-132">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-132">Specifies the storage service type.</span></span>
<span data-ttu-id="71ba5-133">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="71ba5-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71ba5-135">블</span><span class="sxs-lookup"><span data-stu-id="71ba5-135">Blob</span></span> 
- <span data-ttu-id="71ba5-136">테이블로</span><span class="sxs-lookup"><span data-stu-id="71ba5-136">Table</span></span>
- <span data-ttu-id="71ba5-137">전담팀</span><span class="sxs-lookup"><span data-stu-id="71ba5-137">Queue</span></span>
- <span data-ttu-id="71ba5-138">파일</span><span class="sxs-lookup"><span data-stu-id="71ba5-138">File</span></span>

<span data-ttu-id="71ba5-139">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="71ba5-140">-버전</span><span class="sxs-lookup"><span data-stu-id="71ba5-140">-Version</span></span>
<span data-ttu-id="71ba5-141">Azure 저장소 메트릭의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="71ba5-142">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="71ba5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71ba5-143">CommonParameters</span></span>
<span data-ttu-id="71ba5-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71ba5-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71ba5-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71ba5-146">입력</span><span class="sxs-lookup"><span data-stu-id="71ba5-146">INPUTS</span></span>

### <span data-ttu-id="71ba5-147">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="71ba5-147">IStorageContext</span></span>

<span data-ttu-id="71ba5-148">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-148">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="71ba5-149">출력</span><span class="sxs-lookup"><span data-stu-id="71ba5-149">OUTPUTS</span></span>

### <span data-ttu-id="71ba5-150">WindowsAzure. MetricsProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="71ba5-150">Microsoft.WindowsAzure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="71ba5-151">상속자</span><span class="sxs-lookup"><span data-stu-id="71ba5-151">NOTES</span></span>

## <span data-ttu-id="71ba5-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71ba5-152">RELATED LINKS</span></span>

[<span data-ttu-id="71ba5-153">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71ba5-153">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="71ba5-154">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="71ba5-154">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


