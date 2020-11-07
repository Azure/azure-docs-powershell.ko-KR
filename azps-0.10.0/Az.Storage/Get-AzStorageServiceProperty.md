---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Storage.dll-Help.xml
Module Name: Az.Storage
online version: https://docs.microsoft.com/en-us/powershell/module/az.storage/get-azstorageserviceproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Storage/Storage.Management/help/Get-AzStorageServiceProperty.md
ms.openlocfilehash: 6b7944f96eb3ccc67322593d9056b39e83ee9010
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93876290"
---
# <span data-ttu-id="0a21b-101">Get-AzStorageServiceProperty</span><span class="sxs-lookup"><span data-stu-id="0a21b-101">Get-AzStorageServiceProperty</span></span>

## <span data-ttu-id="0a21b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a21b-102">SYNOPSIS</span></span>
<span data-ttu-id="0a21b-103">Azure 저장소 서비스에 대 한 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-103">Gets properties for Azure Storage services.</span></span>

## <span data-ttu-id="0a21b-104">구문과</span><span class="sxs-lookup"><span data-stu-id="0a21b-104">SYNTAX</span></span>

```
Get-AzStorageServiceProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="0a21b-105">설명은</span><span class="sxs-lookup"><span data-stu-id="0a21b-105">DESCRIPTION</span></span>
<span data-ttu-id="0a21b-106">**AzStorageServiceProperty** Cmdlet은 Azure 저장소 서비스의 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-106">The **Get-AzStorageServiceProperty** cmdlet gets the properties for Azure Storage services.</span></span>

## <span data-ttu-id="0a21b-107">예제의</span><span class="sxs-lookup"><span data-stu-id="0a21b-107">EXAMPLES</span></span>

### <span data-ttu-id="0a21b-108">예제 1: Blob 서비스의 Azure Storage services 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="0a21b-108">Example 1: Get  Azure Storage services property of the Blob service</span></span>
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

<span data-ttu-id="0a21b-109">이 명령은 Blob 서비스의 DefaultServiceVersion 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-109">This command gets DefaultServiceVersion property of the Blob service.</span></span>

## <span data-ttu-id="0a21b-110">변수</span><span class="sxs-lookup"><span data-stu-id="0a21b-110">PARAMETERS</span></span>

### <span data-ttu-id="0a21b-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="0a21b-111">-Context</span></span>
<span data-ttu-id="0a21b-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="0a21b-113">저장소 컨텍스트를 얻으려면 New-AzStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-113">To obtain a storage context, use the New-AzStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="0a21b-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a21b-114">-DefaultProfile</span></span>
<span data-ttu-id="0a21b-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="0a21b-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="0a21b-116">-ServiceType</span></span>
<span data-ttu-id="0a21b-117">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-117">Specifies the storage service type.</span></span>
<span data-ttu-id="0a21b-118">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="0a21b-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="0a21b-120">블</span><span class="sxs-lookup"><span data-stu-id="0a21b-120">Blob</span></span> 
- <span data-ttu-id="0a21b-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="0a21b-121">Table</span></span>
- <span data-ttu-id="0a21b-122">전담팀</span><span class="sxs-lookup"><span data-stu-id="0a21b-122">Queue</span></span>
- <span data-ttu-id="0a21b-123">파일</span><span class="sxs-lookup"><span data-stu-id="0a21b-123">File</span></span>

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

### <span data-ttu-id="0a21b-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a21b-124">CommonParameters</span></span>
<span data-ttu-id="0a21b-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a21b-126">자세한 내용은 about_CommonParameters (을 참조 하세요 http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0a21b-126">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a21b-127">입력</span><span class="sxs-lookup"><span data-stu-id="0a21b-127">INPUTS</span></span>

### <span data-ttu-id="0a21b-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="0a21b-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="0a21b-129">출력</span><span class="sxs-lookup"><span data-stu-id="0a21b-129">OUTPUTS</span></span>

### <span data-ttu-id="0a21b-130">WindowsAzure. ResourceModel를 PSSeriviceProperties로 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="0a21b-130">Microsoft.WindowsAzure.Commands.Storage.Model.ResourceModel.PSSeriviceProperties</span></span>

## <span data-ttu-id="0a21b-131">상속자</span><span class="sxs-lookup"><span data-stu-id="0a21b-131">NOTES</span></span>

## <span data-ttu-id="0a21b-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="0a21b-132">RELATED LINKS</span></span>
