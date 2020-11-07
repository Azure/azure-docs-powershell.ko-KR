---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
ms.openlocfilehash: f43386ff1eca223e8ff0e1e8ea7a07d1d8e25d0d
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93880805"
---
# <span data-ttu-id="1e43d-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1e43d-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="1e43d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="1e43d-102">SYNOPSIS</span></span>
<span data-ttu-id="1e43d-103">Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="1e43d-104">구문과</span><span class="sxs-lookup"><span data-stu-id="1e43d-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="1e43d-105">설명은</span><span class="sxs-lookup"><span data-stu-id="1e43d-105">DESCRIPTION</span></span>
<span data-ttu-id="1e43d-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="1e43d-107">예제의</span><span class="sxs-lookup"><span data-stu-id="1e43d-107">EXAMPLES</span></span>

### <span data-ttu-id="1e43d-108">예제 1: Blob 서비스에 대 한 로깅 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="1e43d-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="1e43d-109">이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="1e43d-110">변수</span><span class="sxs-lookup"><span data-stu-id="1e43d-110">PARAMETERS</span></span>

### <span data-ttu-id="1e43d-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="1e43d-111">-Context</span></span>
<span data-ttu-id="1e43d-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="1e43d-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="1e43d-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="1e43d-114">-DefaultProfile</span></span>
<span data-ttu-id="1e43d-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="1e43d-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="1e43d-116">-ServiceType</span></span>
<span data-ttu-id="1e43d-117">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-117">Specifies the storage service type.</span></span>
<span data-ttu-id="1e43d-118">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="1e43d-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="1e43d-120">블</span><span class="sxs-lookup"><span data-stu-id="1e43d-120">Blob</span></span> 
- <span data-ttu-id="1e43d-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="1e43d-121">Table</span></span>
- <span data-ttu-id="1e43d-122">전담팀</span><span class="sxs-lookup"><span data-stu-id="1e43d-122">Queue</span></span>
- <span data-ttu-id="1e43d-123">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="1e43d-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="1e43d-124">CommonParameters</span></span>
<span data-ttu-id="1e43d-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="1e43d-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="1e43d-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="1e43d-127">입력</span><span class="sxs-lookup"><span data-stu-id="1e43d-127">INPUTS</span></span>

### <span data-ttu-id="1e43d-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e43d-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="1e43d-129">출력</span><span class="sxs-lookup"><span data-stu-id="1e43d-129">OUTPUTS</span></span>

### <span data-ttu-id="1e43d-130">WindowsAzure. LoggingProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="1e43d-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="1e43d-131">상속자</span><span class="sxs-lookup"><span data-stu-id="1e43d-131">NOTES</span></span>

## <span data-ttu-id="1e43d-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="1e43d-132">RELATED LINKS</span></span>

[<span data-ttu-id="1e43d-133">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="1e43d-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="1e43d-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="1e43d-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


