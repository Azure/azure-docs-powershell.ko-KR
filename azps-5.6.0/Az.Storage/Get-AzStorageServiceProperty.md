---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: eff94aac5ac9a1a71a12f31be81a1eb4c89bf73b
ms.sourcegitcommit: 4dfb0cc533b83f77afdcfbe2618c1e6c8d221330
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 03/04/2021
ms.locfileid: "101981387"
---
# <span data-ttu-id="f9f51-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="f9f51-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="f9f51-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9f51-102">SYNOPSIS</span></span>
<span data-ttu-id="f9f51-103">Azure Storage 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="f9f51-104">구문</span><span class="sxs-lookup"><span data-stu-id="f9f51-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9f51-105">설명</span><span class="sxs-lookup"><span data-stu-id="f9f51-105">DESCRIPTION</span></span>
<span data-ttu-id="f9f51-106">**Get-AzStorageServiceProperty** cmdlet은 Azure Storage 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="f9f51-107">예제</span><span class="sxs-lookup"><span data-stu-id="f9f51-107">EXAMPLES</span></span>

### <span data-ttu-id="f9f51-108">예제 1: Blob 서비스의 Azure Storage 서비스 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="f9f51-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzStorageServiceProperty -ServiceType Blob

Logging.Version                     : 1.0
Logging.LoggingOperations           : None
Logging.RetentionDays               : 
HourMetrics.Version                 : 1.0
HourMetrics.MetricsLevel            : ServiceAndApi
HourMetrics.RetentionDays           : 7
MinuteMetrics.Version               : 1.0
MinuteMetrics.MetricsLevel          : None
MinuteMetrics.RetentionDays         : 
DeleteRetentionPolicy.Enabled       : True
DeleteRetentionPolicy.RetentionDays : 70
Cors                                : 
DefaultServiceVersion               : 2017-07-29
```

<span data-ttu-id="f9f51-109">이 명령은 Blob 서비스의 DefaultServiceVersion 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="f9f51-110">매개 변수</span><span class="sxs-lookup"><span data-stu-id="f9f51-110">PARAMETERS</span></span>

### <span data-ttu-id="f9f51-111">-Context</span><span class="sxs-lookup"><span data-stu-id="f9f51-111">-Context</span></span>
<span data-ttu-id="f9f51-112">Azure Storage 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="f9f51-113">저장소 컨텍스트를 구하기 위해 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="f9f51-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9f51-114">-DefaultProfile</span></span>
<span data-ttu-id="f9f51-115">Azure와 통신하는 데 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f9f51-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="f9f51-116">-ServiceType</span></span>
<span data-ttu-id="f9f51-117">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-117">Specifies the storage service type.</span></span>
<span data-ttu-id="f9f51-118">이 cmdlet은 이 매개 변수가 지정하는 서비스 형식에 대한 로깅 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="f9f51-119">이 매개 변수에 대해 허용되는 값은 다음입니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="f9f51-120">Blob</span><span class="sxs-lookup"><span data-stu-id="f9f51-120">Blob</span></span> 
- <span data-ttu-id="f9f51-121">표</span><span class="sxs-lookup"><span data-stu-id="f9f51-121">Table</span></span>
- <span data-ttu-id="f9f51-122">큐</span><span class="sxs-lookup"><span data-stu-id="f9f51-122">Queue</span></span>
- <span data-ttu-id="f9f51-123">파일</span><span class="sxs-lookup"><span data-stu-id="f9f51-123">File</span></span>

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

### <span data-ttu-id="f9f51-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9f51-124">CommonParameters</span></span>
<span data-ttu-id="f9f51-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="f9f51-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9f51-126">자세한 내용은 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 를 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="f9f51-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9f51-127">입력</span><span class="sxs-lookup"><span data-stu-id="f9f51-127">INPUTS</span></span>

### <span data-ttu-id="f9f51-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="f9f51-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="f9f51-129">출력</span><span class="sxs-lookup"><span data-stu-id="f9f51-129">OUTPUTS</span></span>

### <span data-ttu-id="f9f51-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="f9f51-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="f9f51-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="f9f51-131">NOTES</span></span>

## <span data-ttu-id="f9f51-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="f9f51-132">RELATED LINKS</span></span>
