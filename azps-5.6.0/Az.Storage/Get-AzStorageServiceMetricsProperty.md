---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 36b2251fa0fb2324a58368df75e43c9aa1480546
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981403"
---
# <span data-ttu-id="6e599-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6e599-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="6e599-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6e599-102">SYNOPSIS</span></span>
<span data-ttu-id="6e599-103">Azure Storage 서비스에 대한 메트릭 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6e599-104">구문</span><span class="sxs-lookup"><span data-stu-id="6e599-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6e599-105">설명</span><span class="sxs-lookup"><span data-stu-id="6e599-105">DESCRIPTION</span></span>
<span data-ttu-id="6e599-106">**Get-AzStorageServiceMetricsProperty** cmdlet은 Azure Storage 서비스에 대한 메트릭 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="6e599-107">예제</span><span class="sxs-lookup"><span data-stu-id="6e599-107">EXAMPLES</span></span>

### <span data-ttu-id="6e599-108">예제 1: Blob 서비스에 대한 메트릭 속성 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="6e599-109">이 명령은 Hour 메트릭 형식에 대한 Blob Storage에 대한 메트릭 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="6e599-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="6e599-110">PARAMETERS</span></span>

### <span data-ttu-id="6e599-111">-Context</span><span class="sxs-lookup"><span data-stu-id="6e599-111">-Context</span></span>
<span data-ttu-id="6e599-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="6e599-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="6e599-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6e599-114">-DefaultProfile</span></span>
<span data-ttu-id="6e599-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6e599-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="6e599-116">-MetricsType</span></span>
<span data-ttu-id="6e599-117">메트릭 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-117">Specifies a metrics type.</span></span>
<span data-ttu-id="6e599-118">이 cmdlet은 이 매개 변수가 지정하는 메트릭 유형에 대한 Azure Storage 서비스 메트릭 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="6e599-119">이 매개 변수에 대해 허용되는 값은 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="6e599-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="6e599-120">-ServiceType</span></span>
<span data-ttu-id="6e599-121">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-121">Specifies the storage service type.</span></span>
<span data-ttu-id="6e599-122">이 cmdlet은 이 매개 변수가 지정하는 형식에 대한 메트릭 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="6e599-123">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="6e599-124">Blob</span><span class="sxs-lookup"><span data-stu-id="6e599-124">Blob</span></span> 
- <span data-ttu-id="6e599-125">표</span><span class="sxs-lookup"><span data-stu-id="6e599-125">Table</span></span>
- <span data-ttu-id="6e599-126">큐</span><span class="sxs-lookup"><span data-stu-id="6e599-126">Queue</span></span>
- <span data-ttu-id="6e599-127">파일 값은 현재 지원되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="6e599-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6e599-128">CommonParameters</span></span>
<span data-ttu-id="6e599-129">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="6e599-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6e599-130">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="6e599-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6e599-131">입력</span><span class="sxs-lookup"><span data-stu-id="6e599-131">INPUTS</span></span>

### <span data-ttu-id="6e599-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e599-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="6e599-133">출력</span><span class="sxs-lookup"><span data-stu-id="6e599-133">OUTPUTS</span></span>

### <span data-ttu-id="6e599-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span><span class="sxs-lookup"><span data-stu-id="6e599-134">Microsoft.Azure.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="6e599-135">참고 사항</span><span class="sxs-lookup"><span data-stu-id="6e599-135">NOTES</span></span>

## <span data-ttu-id="6e599-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="6e599-136">RELATED LINKS</span></span>

[<span data-ttu-id="6e599-137">New-AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="6e599-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="6e599-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="6e599-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


