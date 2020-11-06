---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: ''
schema: 2.0.0
ms.openlocfilehash: 51921a7d67cd8a297f5cd61716362f13cef6cdc9
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524124"
---
# <span data-ttu-id="71c3d-101">Set-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71c3d-101">Set-AzureStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="71c3d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="71c3d-102">SYNOPSIS</span></span>
<span data-ttu-id="71c3d-103">Azure 저장소 서비스의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="71c3d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="71c3d-104">SYNTAX</span></span>

```
Set-AzureStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [<CommonParameters>]
```

## <span data-ttu-id="71c3d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="71c3d-105">DESCRIPTION</span></span>
<span data-ttu-id="71c3d-106">**AzureStorageServiceMetricsProperty** Cmdlet은 Azure 저장소 서비스에 대 한 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-106">The **Set-AzureStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="71c3d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="71c3d-107">EXAMPLES</span></span>

### <span data-ttu-id="71c3d-108">예제 1: Blob 서비스에 대 한 메트릭 속성 수정</span><span class="sxs-lookup"><span data-stu-id="71c3d-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzureStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="71c3d-109">이 명령은 blob 저장소에 대 한 버전 1.0 메트릭을 서비스 수준으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="71c3d-110">Azure 저장소 서비스 메트릭은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="71c3d-111">이 명령은 *PassThru* 매개 변수를 지정 하므로 명령에 수정 된 메트릭 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="71c3d-112">변수</span><span class="sxs-lookup"><span data-stu-id="71c3d-112">PARAMETERS</span></span>

### <span data-ttu-id="71c3d-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="71c3d-113">-Context</span></span>
<span data-ttu-id="71c3d-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="71c3d-115">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-115">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="71c3d-116">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="71c3d-116">-MetricsLevel</span></span>
<span data-ttu-id="71c3d-117">Azure Storage가 서비스에 사용 하는 메트릭 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-117">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="71c3d-118">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-118">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71c3d-119">않아야</span><span class="sxs-lookup"><span data-stu-id="71c3d-119">None</span></span>
- <span data-ttu-id="71c3d-120">Services</span><span class="sxs-lookup"><span data-stu-id="71c3d-120">Service</span></span>
- <span data-ttu-id="71c3d-121">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="71c3d-121">ServiceAndApi</span></span>

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

### <span data-ttu-id="71c3d-122">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="71c3d-122">-MetricsType</span></span>
<span data-ttu-id="71c3d-123">메트릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-123">Specifies a metrics type.</span></span>
<span data-ttu-id="71c3d-124">이 cmldet는 Azure 저장소 서비스 메트릭 유형을이 매개 변수에서 지정 하는 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-124">This cmldet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="71c3d-125">이 매개 변수에 허용 되는 값은 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-125">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="71c3d-126">-PassThru</span><span class="sxs-lookup"><span data-stu-id="71c3d-126">-PassThru</span></span>
<span data-ttu-id="71c3d-127">이 cmdlet이 업데이트 된 메트릭 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-127">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="71c3d-128">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-128">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="71c3d-129">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="71c3d-129">-RetentionDays</span></span>
<span data-ttu-id="71c3d-130">Azure 저장소 서비스에서 메트릭 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-130">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="71c3d-131">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="71c3d-131">-ServiceType</span></span>
<span data-ttu-id="71c3d-132">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-132">Specifies the storage service type.</span></span>
<span data-ttu-id="71c3d-133">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-133">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="71c3d-134">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-134">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="71c3d-135">블</span><span class="sxs-lookup"><span data-stu-id="71c3d-135">Blob</span></span> 
- <span data-ttu-id="71c3d-136">테이블로</span><span class="sxs-lookup"><span data-stu-id="71c3d-136">Table</span></span>
- <span data-ttu-id="71c3d-137">전담팀</span><span class="sxs-lookup"><span data-stu-id="71c3d-137">Queue</span></span>
- <span data-ttu-id="71c3d-138">파일</span><span class="sxs-lookup"><span data-stu-id="71c3d-138">File</span></span>

<span data-ttu-id="71c3d-139">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-139">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="71c3d-140">-버전</span><span class="sxs-lookup"><span data-stu-id="71c3d-140">-Version</span></span>
<span data-ttu-id="71c3d-141">Azure 저장소 메트릭의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-141">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="71c3d-142">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-142">The default value is 1.0.</span></span>

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

### <span data-ttu-id="71c3d-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="71c3d-143">CommonParameters</span></span>
<span data-ttu-id="71c3d-144">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="71c3d-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="71c3d-145">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="71c3d-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="71c3d-146">입력</span><span class="sxs-lookup"><span data-stu-id="71c3d-146">INPUTS</span></span>

## <span data-ttu-id="71c3d-147">출력</span><span class="sxs-lookup"><span data-stu-id="71c3d-147">OUTPUTS</span></span>

## <span data-ttu-id="71c3d-148">상속자</span><span class="sxs-lookup"><span data-stu-id="71c3d-148">NOTES</span></span>

## <span data-ttu-id="71c3d-149">관련 링크</span><span class="sxs-lookup"><span data-stu-id="71c3d-149">RELATED LINKS</span></span>

[<span data-ttu-id="71c3d-150">Get-AzureStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="71c3d-150">Get-AzureStorageServiceMetricsProperty</span></span>](./Get-AzureStorageServiceMetricsProperty.md)

[<span data-ttu-id="71c3d-151">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="71c3d-151">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)


