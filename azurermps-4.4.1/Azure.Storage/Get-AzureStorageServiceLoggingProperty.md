---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
gitcommit: https://github.com/Azure/azure-powershell/blob/1fa63f743120d7a7cd6cbb28ee43cd0f4c654af9
ms.openlocfilehash: a3981ba2b0759afec06bb4cf34bc1e086658765a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702084"
---
# <span data-ttu-id="b048a-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b048a-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="b048a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b048a-102">SYNOPSIS</span></span>
<span data-ttu-id="b048a-103">Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b048a-104">구문과</span><span class="sxs-lookup"><span data-stu-id="b048a-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="b048a-105">설명은</span><span class="sxs-lookup"><span data-stu-id="b048a-105">DESCRIPTION</span></span>
<span data-ttu-id="b048a-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="b048a-107">예제의</span><span class="sxs-lookup"><span data-stu-id="b048a-107">EXAMPLES</span></span>

### <span data-ttu-id="b048a-108">예제 1: Blob 서비스에 대 한 로깅 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="b048a-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="b048a-109">이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="b048a-110">변수</span><span class="sxs-lookup"><span data-stu-id="b048a-110">PARAMETERS</span></span>

### <span data-ttu-id="b048a-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="b048a-111">-Context</span></span>
<span data-ttu-id="b048a-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="b048a-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="b048a-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="b048a-114">-ServiceType</span></span>
<span data-ttu-id="b048a-115">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-115">Specifies the storage service type.</span></span>
<span data-ttu-id="b048a-116">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="b048a-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b048a-118">블</span><span class="sxs-lookup"><span data-stu-id="b048a-118">Blob</span></span> 
- <span data-ttu-id="b048a-119">테이블로</span><span class="sxs-lookup"><span data-stu-id="b048a-119">Table</span></span>
- <span data-ttu-id="b048a-120">전담팀</span><span class="sxs-lookup"><span data-stu-id="b048a-120">Queue</span></span>
- <span data-ttu-id="b048a-121">파일</span><span class="sxs-lookup"><span data-stu-id="b048a-121">File</span></span>

<span data-ttu-id="b048a-122">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="b048a-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b048a-123">CommonParameters</span></span>
<span data-ttu-id="b048a-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b048a-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b048a-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b048a-126">입력</span><span class="sxs-lookup"><span data-stu-id="b048a-126">INPUTS</span></span>

### <span data-ttu-id="b048a-127">IStorageContext</span><span class="sxs-lookup"><span data-stu-id="b048a-127">IStorageContext</span></span>

<span data-ttu-id="b048a-128">' Context ' 매개 변수는 파이프라인에서 ' IStorageContext ' 형식의 값을 허용 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-128">Parameter 'Context' accepts value of type 'IStorageContext' from the pipeline</span></span>

## <span data-ttu-id="b048a-129">출력</span><span class="sxs-lookup"><span data-stu-id="b048a-129">OUTPUTS</span></span>

### <span data-ttu-id="b048a-130">WindowsAzure. LoggingProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="b048a-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="b048a-131">상속자</span><span class="sxs-lookup"><span data-stu-id="b048a-131">NOTES</span></span>

## <span data-ttu-id="b048a-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="b048a-132">RELATED LINKS</span></span>

[<span data-ttu-id="b048a-133">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="b048a-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="b048a-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="b048a-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


