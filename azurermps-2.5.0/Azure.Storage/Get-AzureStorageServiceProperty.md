---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceproperty
schema: 2.0.0
ms.openlocfilehash: adb671b81dd26c1fa66ea98f98dddf8fffbb5356
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880798"
---
# <span data-ttu-id="0db37-101">Get-AzureStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0db37-101">Get-AzureStorageServiceProperty</span></span>

## <span data-ttu-id="0db37-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0db37-102">SYNOPSIS</span></span>
<span data-ttu-id="0db37-103">Azure 저장소 서비스에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-103">Gets properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0db37-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0db37-104">SYNTAX</span></span>

```
Get-AzureStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0db37-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0db37-105">DESCRIPTION</span></span>
<span data-ttu-id="0db37-106">**AzureStorageServiceProperty** Cmdlet은 Azure 저장소 서비스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-106">The **Get-AzureStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="0db37-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0db37-107">EXAMPLES</span></span>

### <span data-ttu-id="0db37-108">예제 1: Blob 서비스의 Azure Storage services 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0db37-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceProperty -ServiceType Blob

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

<span data-ttu-id="0db37-109">이 명령은 Blob 서비스의 DefaultServiceVersion 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="0db37-110">변수</span><span class="sxs-lookup"><span data-stu-id="0db37-110">PARAMETERS</span></span>

### <span data-ttu-id="0db37-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0db37-111">-Context</span></span>
<span data-ttu-id="0db37-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0db37-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0db37-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0db37-114">-DefaultProfile</span></span>
<span data-ttu-id="0db37-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0db37-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0db37-116">-ServiceType</span></span>
<span data-ttu-id="0db37-117">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-117">Specifies the storage service type.</span></span>
<span data-ttu-id="0db37-118">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="0db37-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0db37-120">블</span><span class="sxs-lookup"><span data-stu-id="0db37-120">Blob</span></span> 
- <span data-ttu-id="0db37-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="0db37-121">Table</span></span>
- <span data-ttu-id="0db37-122">전담팀</span><span class="sxs-lookup"><span data-stu-id="0db37-122">Queue</span></span>
- <span data-ttu-id="0db37-123">파일</span><span class="sxs-lookup"><span data-stu-id="0db37-123">File</span></span>

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

### <span data-ttu-id="0db37-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0db37-124">CommonParameters</span></span>
<span data-ttu-id="0db37-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0db37-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0db37-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0db37-127">입력</span><span class="sxs-lookup"><span data-stu-id="0db37-127">INPUTS</span></span>

### <span data-ttu-id="0db37-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0db37-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0db37-129">출력</span><span class="sxs-lookup"><span data-stu-id="0db37-129">OUTPUTS</span></span>

### <span data-ttu-id="0db37-130">WindowsAzure. ResourceModel를 PSSeriviceProperties로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0db37-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="0db37-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0db37-131">NOTES</span></span>

## <span data-ttu-id="0db37-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0db37-132">RELATED LINKS</span></span>