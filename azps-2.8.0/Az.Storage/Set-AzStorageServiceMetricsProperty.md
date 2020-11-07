---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 21bac0db2ca35a94edc80fd8f17ad85361883007
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93689299"
---
# <span data-ttu-id="59082-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="59082-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="59082-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="59082-102">SYNOPSIS</span></span>
<span data-ttu-id="59082-103">Azure 저장소 서비스의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="59082-104">구문과</span><span class="sxs-lookup"><span data-stu-id="59082-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="59082-105">설명은</span><span class="sxs-lookup"><span data-stu-id="59082-105">DESCRIPTION</span></span>
<span data-ttu-id="59082-106">**AzStorageServiceMetricsProperty** Cmdlet은 Azure 저장소 서비스에 대 한 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="59082-107">예제의</span><span class="sxs-lookup"><span data-stu-id="59082-107">EXAMPLES</span></span>

### <span data-ttu-id="59082-108">예제 1: Blob 서비스에 대 한 메트릭 속성 수정</span><span class="sxs-lookup"><span data-stu-id="59082-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="59082-109">이 명령은 blob 저장소에 대 한 버전 1.0 메트릭을 서비스 수준으로 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="59082-110">Azure 저장소 서비스 메트릭은 10 일 동안 항목을 유지 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="59082-111">이 명령은 *PassThru* 매개 변수를 지정 하므로 명령에 수정 된 메트릭 속성이 표시 됩니다.</span><span class="sxs-lookup"><span data-stu-id="59082-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="59082-112">변수</span><span class="sxs-lookup"><span data-stu-id="59082-112">PARAMETERS</span></span>

### <span data-ttu-id="59082-113">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="59082-113">-Context</span></span>
<span data-ttu-id="59082-114">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="59082-115">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="59082-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="59082-116">-DefaultProfile</span></span>
<span data-ttu-id="59082-117">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="59082-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="59082-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="59082-118">-MetricsLevel</span></span>
<span data-ttu-id="59082-119">Azure Storage가 서비스에 사용 하는 메트릭 수준을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="59082-120">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="59082-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59082-121">않아야</span><span class="sxs-lookup"><span data-stu-id="59082-121">None</span></span>
- <span data-ttu-id="59082-122">Services</span><span class="sxs-lookup"><span data-stu-id="59082-122">Service</span></span>
- <span data-ttu-id="59082-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="59082-123">ServiceAndApi</span></span>

```yaml
Type: System.Nullable`1[Microsoft.Azure.Storage.Shared.Protocol.MetricsLevel]
Parameter Sets: (All)
Aliases:
Accepted values: None, Service, ServiceAndApi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59082-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="59082-124">-MetricsType</span></span>
<span data-ttu-id="59082-125">메트릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-125">Specifies a metrics type.</span></span>
<span data-ttu-id="59082-126">이 cmdlet은 Azure 저장소 서비스 메트릭 유형을이 매개 변수에서 지정 하는 값으로 설정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="59082-127">이 매개 변수에 허용 되는 값은 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="59082-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

```yaml
Type: Microsoft.WindowsAzure.Commands.Storage.Common.ServiceMetricsType
Parameter Sets: (All)
Aliases:
Accepted values: Hour, Minute

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="59082-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="59082-128">-PassThru</span></span>
<span data-ttu-id="59082-129">이 cmdlet이 업데이트 된 메트릭 속성을 반환 함을 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="59082-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="59082-130">이 매개 변수를 지정 하지 않으면이 cmdlet은 값을 반환 하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59082-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="59082-131">-보존 기간</span><span class="sxs-lookup"><span data-stu-id="59082-131">-RetentionDays</span></span>
<span data-ttu-id="59082-132">Azure 저장소 서비스에서 메트릭 정보를 유지 하는 일 수를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="59082-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="59082-133">-ServiceType</span></span>
<span data-ttu-id="59082-134">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-134">Specifies the storage service type.</span></span>
<span data-ttu-id="59082-135">이 cmdlet은이 매개 변수에서 지정 하는 서비스 유형의 메트릭 속성을 수정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="59082-136">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="59082-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="59082-137">블</span><span class="sxs-lookup"><span data-stu-id="59082-137">Blob</span></span> 
- <span data-ttu-id="59082-138">테이블로</span><span class="sxs-lookup"><span data-stu-id="59082-138">Table</span></span>
- <span data-ttu-id="59082-139">전담팀</span><span class="sxs-lookup"><span data-stu-id="59082-139">Queue</span></span>
- <span data-ttu-id="59082-140">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="59082-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="59082-141">-버전</span><span class="sxs-lookup"><span data-stu-id="59082-141">-Version</span></span>
<span data-ttu-id="59082-142">Azure 저장소 메트릭의 버전을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="59082-143">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="59082-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="59082-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="59082-144">CommonParameters</span></span>
<span data-ttu-id="59082-145">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="59082-146">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="59082-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="59082-147">입력</span><span class="sxs-lookup"><span data-stu-id="59082-147">INPUTS</span></span>

### <span data-ttu-id="59082-148">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="59082-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="59082-149">출력</span><span class="sxs-lookup"><span data-stu-id="59082-149">OUTPUTS</span></span>

### <span data-ttu-id="59082-150">MetricsProperties을 (를) 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="59082-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="59082-151">상속자</span><span class="sxs-lookup"><span data-stu-id="59082-151">NOTES</span></span>

## <span data-ttu-id="59082-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="59082-152">RELATED LINKS</span></span>

[<span data-ttu-id="59082-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="59082-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="59082-154">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="59082-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


