---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
ms.assetid: 3B5B828A-6B3E-49BD-8BA9-916F8B69B8E9
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageservicemetricsproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceMetricsProperty.md
ms.openlocfilehash: 7bca28da7b4729a414fafc5268bc4e0e02ee3c72
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876291"
---
# <span data-ttu-id="482ba-101">Get-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="482ba-101">Get-AzStorageServiceMetricsProperty</span></span>

## <span data-ttu-id="482ba-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="482ba-102">SYNOPSIS</span></span>
<span data-ttu-id="482ba-103">Azure 저장소 서비스에 대 한 메트릭 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-103">Gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="482ba-104">구문과</span><span class="sxs-lookup"><span data-stu-id="482ba-104">SYNTAX</span></span>

```
Get-AzStorageServiceMetricsProperty [-ServiceType] <StorageServiceType> [-MetricsType] <ServiceMetricsType>
 [-Context <IStorageContext>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="482ba-105">설명은</span><span class="sxs-lookup"><span data-stu-id="482ba-105">DESCRIPTION</span></span>
<span data-ttu-id="482ba-106">**AzStorageServiceMetricsProperty** Cmdlet은 Azure 저장소 서비스에 대 한 메트릭 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-106">The **Get-AzStorageServiceMetricsProperty** cmdlet gets metrics properties for the Azure Storage service.</span></span>

## <span data-ttu-id="482ba-107">예제의</span><span class="sxs-lookup"><span data-stu-id="482ba-107">EXAMPLES</span></span>

### <span data-ttu-id="482ba-108">예제 1: Blob 서비스에 대 한 메트릭 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="482ba-108">Example 1: Get metrics properties for the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceMetricsProperty -ServiceType Blob -MetricsType Hour
```

<span data-ttu-id="482ba-109">이 명령은 시간 메트릭 유형의 blob 저장소에 대 한 메트릭 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-109">This command gets metrics properties for blob storage for the Hour metrics type.</span></span>

## <span data-ttu-id="482ba-110">변수</span><span class="sxs-lookup"><span data-stu-id="482ba-110">PARAMETERS</span></span>

### <span data-ttu-id="482ba-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="482ba-111">-Context</span></span>
<span data-ttu-id="482ba-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="482ba-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="482ba-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="482ba-114">-DefaultProfile</span></span>
<span data-ttu-id="482ba-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="482ba-116">-MetricsType</span><span class="sxs-lookup"><span data-stu-id="482ba-116">-MetricsType</span></span>
<span data-ttu-id="482ba-117">메트릭 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-117">Specifies a metrics type.</span></span>
<span data-ttu-id="482ba-118">이 cmdlet은이 매개 변수에서 지정 하는 메트릭 유형에 대 한 Azure 저장소 서비스 메트릭 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-118">This cmdlet gets the Azure Storage service metrics properties for the metrics type that this parameter specifies.</span></span>
<span data-ttu-id="482ba-119">이 매개 변수에 허용 되는 값은 시간 및 분입니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-119">The acceptable values for this parameter are: Hour and Minute.</span></span>

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

### <span data-ttu-id="482ba-120">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="482ba-120">-ServiceType</span></span>
<span data-ttu-id="482ba-121">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-121">Specifies the storage service type.</span></span>
<span data-ttu-id="482ba-122">이 cmdlet은이 매개 변수에서 지정 하는 형식에 대 한 메트릭 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-122">This cmdlet gets the metrics properties for the type that this parameter specifies.</span></span>
<span data-ttu-id="482ba-123">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-123">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="482ba-124">블</span><span class="sxs-lookup"><span data-stu-id="482ba-124">Blob</span></span> 
- <span data-ttu-id="482ba-125">테이블로</span><span class="sxs-lookup"><span data-stu-id="482ba-125">Table</span></span>
- <span data-ttu-id="482ba-126">전담팀</span><span class="sxs-lookup"><span data-stu-id="482ba-126">Queue</span></span>
- <span data-ttu-id="482ba-127">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-127">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="482ba-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="482ba-128">CommonParameters</span></span>
<span data-ttu-id="482ba-129">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="482ba-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="482ba-130">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="482ba-130">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="482ba-131">입력</span><span class="sxs-lookup"><span data-stu-id="482ba-131">INPUTS</span></span>

### <span data-ttu-id="482ba-132">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="482ba-132">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="482ba-133">출력</span><span class="sxs-lookup"><span data-stu-id="482ba-133">OUTPUTS</span></span>

### <span data-ttu-id="482ba-134">MetricsProperties/. m a w.</span><span class="sxs-lookup"><span data-stu-id="482ba-134">Microsoft.WindowsAz.Storage.Shared.Protocol.MetricsProperties</span></span>

## <span data-ttu-id="482ba-135">상속자</span><span class="sxs-lookup"><span data-stu-id="482ba-135">NOTES</span></span>

## <span data-ttu-id="482ba-136">관련 링크</span><span class="sxs-lookup"><span data-stu-id="482ba-136">RELATED LINKS</span></span>

[<span data-ttu-id="482ba-137">새로운 AzStorageContext</span><span class="sxs-lookup"><span data-stu-id="482ba-137">New-AzStorageContext</span></span>](./New-AzStorageContext.md)

[<span data-ttu-id="482ba-138">Set-AzStorageServiceMetricsProperty</span><span class="sxs-lookup"><span data-stu-id="482ba-138">Set-AzStorageServiceMetricsProperty</span></span>](./Set-AzStorageServiceMetricsProperty.md)


