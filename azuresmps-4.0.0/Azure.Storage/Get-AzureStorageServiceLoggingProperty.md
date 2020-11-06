---
external help file: Microsoft.WindowsAzure.Commands.Storage.dll-Help.xml
ms.assetid: 494291A1-D854-4E97-B5EE-27BB5653D97C
online version: ''
schema: 2.0.0
ms.openlocfilehash: d615c0a807c12640f20a72b97a2c11c2efcd5b28
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: ko-KR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93524015"
---
# <span data-ttu-id="bc675-101">Get-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bc675-101">Get-AzureStorageServiceLoggingProperty</span></span>

## <span data-ttu-id="bc675-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bc675-102">SYNOPSIS</span></span>
<span data-ttu-id="bc675-103">Azure Storage 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-103">Gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="bc675-104">구문과</span><span class="sxs-lookup"><span data-stu-id="bc675-104">SYNTAX</span></span>

```
Get-AzureStorageServiceLoggingProperty [-ServiceType] <StorageServiceType> [-Context <IStorageContext>]
 [<CommonParameters>]
```

## <span data-ttu-id="bc675-105">설명은</span><span class="sxs-lookup"><span data-stu-id="bc675-105">DESCRIPTION</span></span>
<span data-ttu-id="bc675-106">**AzureStorageServiceLoggingProperty** Cmdlet은 Azure 저장소 서비스에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-106">The **Get-AzureStorageServiceLoggingProperty** cmdlet gets logging properties for Azure Storage services.</span></span>

## <span data-ttu-id="bc675-107">예제의</span><span class="sxs-lookup"><span data-stu-id="bc675-107">EXAMPLES</span></span>

### <span data-ttu-id="bc675-108">예제 1: Blob 서비스에 대 한 로깅 속성 가져오기</span><span class="sxs-lookup"><span data-stu-id="bc675-108">Example 1: Get logging properties for the Blob service</span></span>
```
C:\PS>Get-AzureStorageServiceLoggingProperty -ServiceType Blob
```

<span data-ttu-id="bc675-109">이 명령은 blob 저장소에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-109">This command gets logging properties for blob storage.</span></span>

## <span data-ttu-id="bc675-110">변수</span><span class="sxs-lookup"><span data-stu-id="bc675-110">PARAMETERS</span></span>

### <span data-ttu-id="bc675-111">-컨텍스트</span><span class="sxs-lookup"><span data-stu-id="bc675-111">-Context</span></span>
<span data-ttu-id="bc675-112">Azure 저장소 컨텍스트를 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-112">Specifies an Azure storage context.</span></span>
<span data-ttu-id="bc675-113">저장소 컨텍스트를 얻으려면 New-AzureStorageContext cmdlet을 사용 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-113">To obtain a storage context, use the New-AzureStorageContext cmdlet.</span></span>

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

### <span data-ttu-id="bc675-114">-ServiceType</span><span class="sxs-lookup"><span data-stu-id="bc675-114">-ServiceType</span></span>
<span data-ttu-id="bc675-115">저장소 서비스 유형을 지정 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-115">Specifies the storage service type.</span></span>
<span data-ttu-id="bc675-116">이 cmdlet은이 매개 변수에서 지정 하는 서비스 형식에 대 한 로깅 속성을 가져옵니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-116">This cmdlet gets the logging properties for the service type that this parameter specifies.</span></span>
<span data-ttu-id="bc675-117">이 매개 변수에 허용 되는 값은 다음과 같습니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="bc675-118">블</span><span class="sxs-lookup"><span data-stu-id="bc675-118">Blob</span></span> 
- <span data-ttu-id="bc675-119">테이블로</span><span class="sxs-lookup"><span data-stu-id="bc675-119">Table</span></span>
- <span data-ttu-id="bc675-120">전담팀</span><span class="sxs-lookup"><span data-stu-id="bc675-120">Queue</span></span>
- <span data-ttu-id="bc675-121">파일</span><span class="sxs-lookup"><span data-stu-id="bc675-121">File</span></span>

<span data-ttu-id="bc675-122">현재 파일의 값이 지원 되지 않습니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-122">The value of File is not currently supported.</span></span>

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

### <span data-ttu-id="bc675-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bc675-123">CommonParameters</span></span>
<span data-ttu-id="bc675-124">이 cmdlet은-Debug,-ErrorAction,-Erroraction,-InformationAction,-Informationaction,-OutVariable,-OutBuffer,-PipelineVariable,-Verbose,-WarningAction,-WarningVariable 등의 공통 매개 변수를 지원 합니다.</span><span class="sxs-lookup"><span data-stu-id="bc675-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bc675-125">자세한 내용은 about_CommonParameters (을 참조 하세요 https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bc675-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bc675-126">입력</span><span class="sxs-lookup"><span data-stu-id="bc675-126">INPUTS</span></span>

## <span data-ttu-id="bc675-127">출력</span><span class="sxs-lookup"><span data-stu-id="bc675-127">OUTPUTS</span></span>

## <span data-ttu-id="bc675-128">상속자</span><span class="sxs-lookup"><span data-stu-id="bc675-128">NOTES</span></span>

## <span data-ttu-id="bc675-129">관련 링크</span><span class="sxs-lookup"><span data-stu-id="bc675-129">RELATED LINKS</span></span>

[<span data-ttu-id="bc675-130">새로운 AzureStorageContext</span><span class="sxs-lookup"><span data-stu-id="bc675-130">New-AzureStorageContext</span></span>](./New-AzureStorageContext.md)

[<span data-ttu-id="bc675-131">Set-AzureStorageServiceLoggingProperty</span><span class="sxs-lookup"><span data-stu-id="bc675-131">Set-AzureStorageServiceLoggingProperty</span></span>](./Set-AzureStorageServiceLoggingProperty.md)


