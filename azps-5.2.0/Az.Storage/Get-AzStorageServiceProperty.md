---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: aff976a684f5a002e2b55f1282dd60756f21f2f2
ms.sourcegitcommit: 04221336bc9eed46c05ed1e828a6811534d4b4ab
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 12/08/2020
ms.locfileid: "98324932"
---
# <span data-ttu-id="601b8-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="601b8-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="601b8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="601b8-102">SYNOPSIS</span></span>
<span data-ttu-id="601b8-103">Azure Storage 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="601b8-104">구문</span><span class="sxs-lookup"><span data-stu-id="601b8-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="601b8-105">설명</span><span class="sxs-lookup"><span data-stu-id="601b8-105">DESCRIPTION</span></span>
<span data-ttu-id="601b8-106">**Get-AzStorageServiceProperty** cmdlet은 Azure Storage 서비스에 대한 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="601b8-107">예제</span><span class="sxs-lookup"><span data-stu-id="601b8-107">EXAMPLES</span></span>

### <span data-ttu-id="601b8-108">예제 1: Blob service의 Azure Storage 서비스 속성 얻기</span><span class="sxs-lookup"><span data-stu-id="601b8-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="601b8-109">이 명령은 Blob service의 DefaultServiceVersion 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="601b8-110">PARAMETERS</span><span class="sxs-lookup"><span data-stu-id="601b8-110">PARAMETERS</span></span>

### <span data-ttu-id="601b8-111">-Context</span><span class="sxs-lookup"><span data-stu-id="601b8-111">-Context</span></span>
<span data-ttu-id="601b8-112">Azure 저장소 컨텍스트를 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="601b8-113">저장소 컨텍스트를 얻습니다. New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="601b8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="601b8-114">-DefaultProfile</span></span>
<span data-ttu-id="601b8-115">Azure와의 통신에 사용되는 자격 증명, 계정, 테넌트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="601b8-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="601b8-116">-ServiceType</span></span>
<span data-ttu-id="601b8-117">저장소 서비스 유형을 지정합니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-117">Specifies the storage service type.</span></span>
<span data-ttu-id="601b8-118">이 cmdlet은 이 매개 변수가 지정하는 서비스 형식에 대한 로깅 속성을 얻습니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="601b8-119">이 매개 변수에 허용되는 값은</span><span class="sxs-lookup"><span data-stu-id="601b8-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="601b8-120">Blob</span><span class="sxs-lookup"><span data-stu-id="601b8-120">Blob</span></span> 
- <span data-ttu-id="601b8-121">표</span><span class="sxs-lookup"><span data-stu-id="601b8-121">Table</span></span>
- <span data-ttu-id="601b8-122">큐</span><span class="sxs-lookup"><span data-stu-id="601b8-122">Queue</span></span>
- <span data-ttu-id="601b8-123">파일</span><span class="sxs-lookup"><span data-stu-id="601b8-123">File</span></span>

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

### <span data-ttu-id="601b8-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="601b8-124">CommonParameters</span></span>
<span data-ttu-id="601b8-125">이 cmdlet은 -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction 및 -WarningVariable의 일반적인 매개 변수를 지원합니다.</span><span class="sxs-lookup"><span data-stu-id="601b8-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="601b8-126">자세한 내용은 다음 about_CommonParameters http://go.microsoft.com/fwlink/?LinkID=113216) 참조하세요.</span><span class="sxs-lookup"><span data-stu-id="601b8-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="601b8-127">입력</span><span class="sxs-lookup"><span data-stu-id="601b8-127">INPUTS</span></span>

### <span data-ttu-id="601b8-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span><span class="sxs-lookup"><span data-stu-id="601b8-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="601b8-129">출력</span><span class="sxs-lookup"><span data-stu-id="601b8-129">OUTPUTS</span></span>

### <span data-ttu-id="601b8-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span><span class="sxs-lookup"><span data-stu-id="601b8-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="601b8-131">참고 사항</span><span class="sxs-lookup"><span data-stu-id="601b8-131">NOTES</span></span>

## <span data-ttu-id="601b8-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="601b8-132">RELATED LINKS</span></span>
