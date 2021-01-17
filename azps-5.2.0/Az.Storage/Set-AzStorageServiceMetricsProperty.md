---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 5878FAD4-A4BB-4DBF-A1F2-221FD34F0308
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/set-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Set-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: d3f32e44e5653d0d6a9c9b5a9a1eee27b66d43cf
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98348189"
---
# <span data-ttu-id="4f581-101">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4f581-101">Set-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="4f581-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4f581-102">SYNOPSIS</span></span>
<span data-ttu-id="4f581-103">Azure Storage 서비스에 대한 메트릭 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-103">Modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4f581-104">구문</span><span class="sxs-lookup"><span data-stu-id="4f581-104">SYNTAX</span></span>

```
Set-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Version <Double>] [-RetentionDays <Int32>] [-MetricsLevel <MetricsLevel>] [-PassThru]
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4f581-105">설명</span><span class="sxs-lookup"><span data-stu-id="4f581-105">DESCRIPTION</span></span>
<span data-ttu-id="4f581-106">**Set-AzStorageServiceMetricsProperty** cmdlet은 Azure Storage 서비스에 대한 메트릭 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-106">The **Set-AzStorageServiceMetricsProperty** cmdlet modifies metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="4f581-107">예제</span><span class="sxs-lookup"><span data-stu-id="4f581-107">EXAMPLES</span></span>

### <span data-ttu-id="4f581-108">예제 1: Blob service에 대한 메트릭 속성 수정</span><span class="sxs-lookup"><span data-stu-id="4f581-108">Example 1: Modify metrics properties for the Blob service</span></span>
```
C:\PS>Set-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour -MetricsLevel Service -PassThru -RetentionDays 10 -Version 1.0
```

<span data-ttu-id="4f581-109">이 명령은 Blob Storage에 대한 버전 1.0 메트릭을 서비스 수준으로 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-109">This command modifies version 1.0 metrics for blob storage to a level of Service.</span></span>
<span data-ttu-id="4f581-110">Azure Storage 서비스 메트릭은 10일 동안 항목을 보존합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-110">Azure Storage service metrics retains entries for 10 days.</span></span>
<span data-ttu-id="4f581-111">이 명령은 *PassThru* 매개 변수를 지정하기 때문에 명령은 수정된 메트릭 속성을 표시합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-111">Because this command specifies the *PassThru* parameter, the command displays the modified metrics properties.</span></span>

## <span data-ttu-id="4f581-112">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="4f581-112">PARAMETERS</span></span>

### <span data-ttu-id="4f581-113">-Context</span><span class="sxs-lookup"><span data-stu-id="4f581-113">-Context</span></span>
<span data-ttu-id="4f581-114">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-114">Specifies an Azure storage context.</span></span>
<span data-ttu-id="4f581-115">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-115">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="4f581-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4f581-116">-DefaultProfile</span></span>
<span data-ttu-id="4f581-117">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="4f581-118">-MetricsLevel</span><span class="sxs-lookup"><span data-stu-id="4f581-118">-MetricsLevel</span></span>
<span data-ttu-id="4f581-119">Azure Storage가 서비스에 사용하는 메트릭 수준을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-119">Specifies the metrics level that Azure Storage uses for the service.</span></span>
<span data-ttu-id="4f581-120">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="4f581-120">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f581-121">없음</span><span class="sxs-lookup"><span data-stu-id="4f581-121">None</span></span>
- <span data-ttu-id="4f581-122">서비스</span><span class="sxs-lookup"><span data-stu-id="4f581-122">Service</span></span>
- <span data-ttu-id="4f581-123">ServiceAndApi</span><span class="sxs-lookup"><span data-stu-id="4f581-123">ServiceAndApi</span></span>

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

### <span data-ttu-id="4f581-124">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="4f581-124">-MetricsType</span></span>
<span data-ttu-id="4f581-125">메트릭 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-125">Specifies a metrics type.</span></span>
<span data-ttu-id="4f581-126">이 cmdlet은 Azure Storage 서비스 메트릭 형식을 이 매개 변수가 지정하는 값으로 설정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-126">This cmdlet sets the Azure Storage service metrics type to the value that this parameter specifies.</span></span>
<span data-ttu-id="4f581-127">이 매개 변수에 허용되는 값은 Hour 및 Minute입니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-127">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="4f581-128">-PassThru</span><span class="sxs-lookup"><span data-stu-id="4f581-128">-PassThru</span></span>
<span data-ttu-id="4f581-129">이 cmdlet이 업데이트된 메트릭 속성을 반환하는지 나타냅니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-129">Indicates that this cmdlets returns the updated metrics properties.</span></span>
<span data-ttu-id="4f581-130">이 매개 변수를 지정하지 않으면 이 cmdlet은 값을 반환하지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-130">If you do not specify this parameter, this cmdlet does not return a value.</span></span>

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

### <span data-ttu-id="4f581-131">-RetentionDays</span><span class="sxs-lookup"><span data-stu-id="4f581-131">-RetentionDays</span></span>
<span data-ttu-id="4f581-132">Azure Storage 서비스가 메트릭 정보를 유지하는 일 수를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-132">Specifies the number of days that the Azure Storage service retains metrics information.</span></span>

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

### <span data-ttu-id="4f581-133">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="4f581-133">-ServiceType</span></span>
<span data-ttu-id="4f581-134">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-134">Specifies the storage service type.</span></span>
<span data-ttu-id="4f581-135">이 cmdlet은 이 매개 변수가 지정하는 서비스 형식에 대한 메트릭 속성을 수정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-135">This cmdlet modifies the metrics properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="4f581-136">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="4f581-136">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="4f581-137">Blob</span><span class="sxs-lookup"><span data-stu-id="4f581-137">Blob</span></span> 
- <span data-ttu-id="4f581-138">표</span><span class="sxs-lookup"><span data-stu-id="4f581-138">Table</span></span>
- <span data-ttu-id="4f581-139">큐</span><span class="sxs-lookup"><span data-stu-id="4f581-139">Queue</span></span>
- <span data-ttu-id="4f581-140">파일 값은 현재 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-140">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="4f581-141">-Version</span><span class="sxs-lookup"><span data-stu-id="4f581-141">-Version</span></span>
<span data-ttu-id="4f581-142">Azure Storage 메트릭의 버전을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-142">Specifies the version of the Azure Storage metrics.</span></span>
<span data-ttu-id="4f581-143">기본값은 1.0입니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-143">The default value is 1.0.</span></span>

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

### <span data-ttu-id="4f581-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4f581-144">CommonParameters</span></span>
<span data-ttu-id="4f581-145">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="4f581-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4f581-146">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="4f581-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4f581-147">입력</span><span class="sxs-lookup"><span data-stu-id="4f581-147">INPUTS</span></span>

### <span data-ttu-id="4f581-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f581-148">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="4f581-149">출력</span><span class="sxs-lookup"><span data-stu-id="4f581-149">OUTPUTS</span></span>

### <span data-ttu-id="4f581-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="4f581-150">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="4f581-151">참고 사항</span><span class="sxs-lookup"><span data-stu-id="4f581-151">NOTES</span></span>

## <span data-ttu-id="4f581-152">관련 링크</span><span class="sxs-lookup"><span data-stu-id="4f581-152">RELATED LINKS</span></span>

[<span data-ttu-id="4f581-153">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="4f581-153">Get-AzStorageServiceMetricsProperty</span></span>](./Get-AzStorageServiceMetricsProperty.md)

[<span data-ttu-id="4f581-154">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="4f581-154">New-AzStorageContext</span></span>](./New-AzStorageContext.md)


