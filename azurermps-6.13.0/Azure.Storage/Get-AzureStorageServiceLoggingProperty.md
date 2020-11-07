---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
Module Name: Azure.Storage
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: https://docs.microsoft.com/en-us/powershell/module/azure.storage/get-azurestorageserviceloggingproperty
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/Storage/Commands.Storage/help/Get-AzureStorageServiceLoggingProperty.md
ms.openlocfilehash: b622f117549a77c54a24964240cd6d17a084993d
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93702823"
---
# <span data-ttu-id="597bb-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="597bb-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="597bb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="597bb-102">SYNOPSIS</span></span>
<span data-ttu-id="597bb-103">Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-103">Gets logging properties for Azure Storage services.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="597bb-104">구문과</span><span class="sxs-lookup"><span data-stu-id="597bb-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="597bb-105">설명은</span><span class="sxs-lookup"><span data-stu-id="597bb-105">DESCRIPTION</span></span>
<span data-ttu-id="597bb-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="597bb-107">예제의</span><span class="sxs-lookup"><span data-stu-id="597bb-107">EXAMPLES</span></span>

### <span data-ttu-id="597bb-108">예제 1: Blob 서비스에 대 한 로깅 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="597bb-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="597bb-109">이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="597bb-110">변수</span><span class="sxs-lookup"><span data-stu-id="597bb-110">PARAMETERS</span></span>

### <span data-ttu-id="597bb-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="597bb-111">-Context</span></span>
<span data-ttu-id="597bb-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="597bb-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="597bb-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="597bb-114">-DefaultProfile</span></span>
<span data-ttu-id="597bb-115">Azure와 통신 하는 데 사용 되는 자격 증명, 계정, 테 넌 트 및 구독입니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-115">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="597bb-116">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="597bb-116">-ServiceType</span></span>
<span data-ttu-id="597bb-117">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-117">Specifies the storage service type.</span></span>
<span data-ttu-id="597bb-118">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-118">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="597bb-119">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-119">The acceptable values for this parameter are:</span></span>
- <span data-ttu-id="597bb-120">블</span><span class="sxs-lookup"><span data-stu-id="597bb-120">Blob</span></span> 
- <span data-ttu-id="597bb-121">테이블로</span><span class="sxs-lookup"><span data-stu-id="597bb-121">Table</span></span>
- <span data-ttu-id="597bb-122">전담팀</span><span class="sxs-lookup"><span data-stu-id="597bb-122">Queue</span></span>
- <span data-ttu-id="597bb-123">파일 값이 현재 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-123">File The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="597bb-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="597bb-124">CommonParameters</span></span>
<span data-ttu-id="597bb-125">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="597bb-126">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="597bb-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="597bb-127">입력</span><span class="sxs-lookup"><span data-stu-id="597bb-127">INPUTS</span></span>

### <span data-ttu-id="597bb-128">Microsoft. Azure. 일반. IStorageContext</span><span class="sxs-lookup"><span data-stu-id="597bb-128">Microsoft.Azure.Commands.Common.Authentication.Abstractions.IStorageContext</span></span>

## <span data-ttu-id="597bb-129">출력</span><span class="sxs-lookup"><span data-stu-id="597bb-129">OUTPUTS</span></span>

### <span data-ttu-id="597bb-130">WindowsAzure. LoggingProperties를 저장 합니다.</span><span class="sxs-lookup"><span data-stu-id="597bb-130">Microsoft.WindowsAzure.Storage.Shared.Protocol.LoggingProperties</span></span>

## <span data-ttu-id="597bb-131">상속자</span><span class="sxs-lookup"><span data-stu-id="597bb-131">NOTES</span></span>

## <span data-ttu-id="597bb-132">관련 링크</span><span class="sxs-lookup"><span data-stu-id="597bb-132">RELATED LINKS</span></span>

[<span data-ttu-id="597bb-133">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="597bb-133">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="597bb-134">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="597bb-134">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


